## Verwendung der Gruppenverschachtelungsstrategie - AD Best Practices für die Gruppenstrategie

### Vorwort

Ich habe diesen Blogeintrag übersetzt und erstellt, um einen Einblick geben zu können, wie Active Directory-Gruppen für den Zugriff auf Ressourcen genutzt werden sollten, basierend darauf, wie die Microsoft-Ingenieure sie ursprünglich für die Nutzung konzipiert haben. 
Die hier vorgestellte Methode ist vergleichbar mit der, wie ich sie im Klassenzimmer unterrichten und beschreiben würde. Natürlich bin ich beim Unterrichten vor der Klasse etwas animierter mit einem ′ breiten Whiteboard, wo ich das große Format voll ausnutzen kann. Ich werde es in diesem Blog abschwächen, um Ihre Lesezeit zu verkürzen, einige Grafiken zur Verfügung zu stellen und gleich zur Sache zu kommen.
Einige der Grafiken in diesem Blog sind aktuelle Kursunterlagen, die aus dem Microsoft Official Curriculum MOC 6425C und MOC 6425B Kursunterlagen "Konfiguration und Fehlerbehebung von Windows Server 2008 Active Directory Domain Services" geändert wurden. Weitere Informationen zu diesem 5-Tage-Kurs mit Instructor-Led finden Sie unter folgendem Link:

MOC 6425C Konfiguration und Fehlerbehebung von Windows Server 2008 Active Directory Domain Services -
5 Tage, von einem Instructor geleitet, im Klassenzimmer oder online.
http://www.microsoft.com/learning/en/us/Course.aspx?ID=6425C&Locale=en-us

Es gibt auch 20 Stunden, eine selbstgesteuerte Online-Version dieses Kurses ist ebenfalls verfügbar. Informationen zu dieser Version finden Sie unter dem untenstehenden Link. Zum Zeitpunkt dieses Schreibens, 31.12.2011, betragen die Kosten USD $319,00:
https://www.microsoftelearning.com/eLearning/offerDetail.aspx?offerPriceId=222031

Der vom Instruktor geführte Kurs kostet viel mehr. Für die Preisgestaltung wenden Sie sich bitte an ein Microsoft CPLS-Center (Certified Partner for Learning Solutions).
Die in diesem Blog verwendete Terminologie beinhaltet die Terminologie IGDLA (Resource Access Design Practice), kurz für "Identities, Global Groups, Domain local groups, and Access".

Die bisherige Terminologie war jedoch AGDLP, kurz für "Add Accounts to Global Groups, then to Domain Local Groups, then apply Permissions to the Domain Local Group".
Bei jedem anderen Namen erhält der Benutzer am Ende des Tages die Berechtigungen, die für die lokale Domänengruppe auf der Ressource gelten. IGDLA bietet mehr einen allgemeinen Anwendungsbereich und definiert nicht nur spezifisch, wie AD-Gruppen funktionieren. Die IDGLA passt sich der aktuellen Terminologie der branchenüblichen Praxis an, was der Grund dafür war, sie zu ändern. 

### Was sind Gruppen und wofür werden sie verwendet

Bevor Sie Gruppen in Ihrer Umgebung implementieren, ist es von Vorteil zu verstehen, wie Gruppen verwendet werden und welche Arten von Gruppen es gibt. Es ist auch wichtig, den Gruppenumfang zu verstehen, um die richtige Gruppenart und Verwendung in verschiedenen Szenarien zu identifizieren. Darüber hinaus ist es wichtig, eine Gruppennamenskonvention zu definieren, um einfacher zu "sehen", was der Gruppentyp und die Absichten sind, wenn man sich nur den Namen der Gruppe ansieht, sowie die Funktion zum Verschachteln von Gruppen und die Vorteile dieses Ansatzes zu verstehen.

Die Verwendung von Gruppen macht es für das Betriebssystem effizienter, Berechtigungen für eine ACL aufzuzählen. Stellen Sie sich vor, Sie haben 300 Benutzerkonten auf einer ACL. Das System muss jedes einzelne Benutzerkonto bzw. die SID-Nummern des Benutzerkontos in der ACL auflisten. Dies wird als Leistungsrückstand erkannt. Es ist nicht nur ein Performance-Hit, es ist auch schwer, den Überblick zu behalten.

Wenn Sie Gruppen verwenden, fügen Sie der Ressource den Gruppennamen hinzu. Sie fügen das Benutzerkonto auch der Gruppe in Active Directory hinzu. Was also passiert, ist, wenn sich der Benutzer anmeldet, hat das Sitzungsticket, das zusammengestellt wird, die Benutzerkonten-SID und die Gruppen-SID. Wenn Sie auf die Ressource zugreifen, gleicht das System daher einfach die SID-Einträge des Sitzungstickets des Benutzers mit den SID-Einträgen auf der Ressourcen-ACL ab. Sehr einfach, einfach zu verwalten und äußerst effizient.
Beachten Sie, dass einige der Funktionen in Ihrer Active Directory-Infrastruktur vorhanden sein können oder nicht, je nachdem, welche Betriebssystemversion Ihre Domänencontroller sind, oder in einer gemischten NT4-Umgebung. Was der älteste Domänencontroller ist, der noch in der Domäne und/oder im Forest existiert, ist ebenfalls ein Faktor. Funktionen wie die Gruppenverschachtelung sind möglicherweise nicht vorhanden, wenn die AD-Domäne und/oder die Forstfunktionsebenen nicht auf den neuesten Stand gebracht wurden. Die Verwendung von Gruppen trägt auch dazu bei, den allgemeinen Verwaltungsaufwand für den Umgang mit dem Benutzerzugriff zu reduzieren, anstatt einfach ein Benutzerkonto zu einer Ressource hinzuzufügen. Was passiert, wenn dieser Benutzer das Unternehmen verlässt? 
Einige Institutionen behalten das Konto, deaktivieren es aber. Andere Institutionen werden das Konto löschen. Was passiert also, wenn Sie ein Benutzerkonto löschen, das noch in einer ACL angegeben ist? 
Das Benutzerkonto in der ACL einer Ressource bleibt erhalten, aber nur als SID-Nummer und nicht der Name des Benutzerkontos, da es gelöscht wurde. Dies kann verwirrend werden, um herauszufinden, wer das Konto war, aber an diesem Punkt spielt es keine Rolle, weil du weißt, dass es ein Konto war, das gelöscht wurde. In diesem Fall können Sie nur den SID-Eintrag in der ACL löschen. Es sei denn, Sie sollten das Konto reanimieren, ob Sie eine autorisierte Wiederherstellung durchführen, ADRestore.Net verwenden oder ein Konto aus dem AD-Papierkorb mit Windows 2008 R2 oder neuer wiederherstellen, aber das ist ein anderes Thema außerhalb des Umfangs dieses Blogs.

Und was passiert, wenn Sie nur Benutzerkonten anstelle von Gruppen verwenden? Man könnte sagen, dass ich nur 20 Benutzer habe, also werde ich es einfach per Benutzerkonto tun. Dann, nach einer Weile, wächst das Unternehmen, mehr Benutzer werden eingestellt, Sie fügen sie immer wieder Ressourcen hinzu, die auf ihren Benutzerkonten basieren, aber eines Tages schauen Sie es sich an und sagen: Wow, wir haben jetzt über 200 Benutzer, und wir haben Probleme, den Überblick zu behalten, wer Zugang zu was hat. 
Wenn ich nur anfangs Gruppen benutzt und einfach Benutzer zu den Gruppen hinzugefügt oder entfernt hätte, wenn sich ihre Rollen oder Positionen im Unternehmen geändert hätten, hätte ich einen besseren Umgang mit diesem Durcheinander gehabt, und es wäre eine Sache weniger auf meinem Teller, mit der ich mich jetzt befassen müsste.

### Rollengruppen

Wir können rollenbasierte Gruppen erstellen, um die tägliche Administration zu erleichtern. Rollengruppen, z.B. basierend auf ihren Funktionen:
* Umsatz
* Marketing
* Buchhalter
* Manager
* Leiter der Buchhaltung
* Vertriebsleiter
* etc

### Gruppenbenennungskonvention

Die Namenskonvention ist wichtig. Normalerweise möchte ich meine Gruppen nach Gruppentyp, Rolle und Zugriff benennen. Zum Beispiel werde ich eine Global Group (GG) für die Buchhalter erstellen, die nur Lesezugriff benötigen:
G_Buchhalter_Lesen

Und für die Buchhalter, die volle Kontrolle brauchen:
G_Buchhalter_FC

Natürlich möchten wir normalerweise nicht die volle Kontrolle übernehmen, denn neben der vollen Kontrolle, die es erlaubt, etwas zu ändern, erlaubt es auch die Möglichkeit, Berechtigungen zu ändern und das Eigentum an einer Ressource zu übernehmen. In vielen Fällen funktioniert die NTFS-Berechtigung "Ändern" gut, und die Benutzer werden den Unterschied nicht kennen, solange sie sehen, dass sie Elemente erstellen, ändern und löschen können.

Zusammenfassend lässt sich sagen, dass Sie rollenbasierte Gruppen erstellen und richtig benennen sollten, um sie leicht zu identifizieren und zu verwalten.

Gültigkeitsbereiche für Gruppen
Es gibt vier Gruppenbereiche:
* Lokal
* Global
* Domäne Lokal
* Universell

Die Merkmale, die die Gültigkeitsbereiche definieren, fallen in diese Kategorien:

* Replikation. Wo ist die Gruppe definiert und in welche Systeme wird die Gruppe repliziert?
Mitgliedschaft. Welche Arten von Sicherheitsprinzipien kann die Gruppe als Mitglieder enthalten? Kann die Gruppe Sicherheitsprinzipien aus vertrauenswürdigen Domänen aufnehmen?
* Verfügbarkeit. Wo kann die Gruppe eingesetzt werden? Ist die Gruppe verfügbar, um sie zu einer anderen Gruppe hinzuzufügen? Ist die Gruppe verfügbar, um sie zu einer ACL hinzuzufügen?
* Verfügbarkeits des Vertrauens. Ein Trust erlaubt es einer Domäne, zur Benutzerauthentifizierung auf eine andere Domäne zu verweisen, Sicherheitsprinzipien der anderen Domäne als Gruppenmitglieder aufzunehmen und Berechtigungen den Sicherheitsprinzipien der anderen Domäne zuzuweisen. 

Die verwendete Terminologie kann verwirrend sein. Wenn Domain A Domain B vertraut, ist Domain A die vertrauenswürdige Domain und Domain B die vertrauenswürdige Domain. Domäne A akzeptiert die Anmeldeinformationen von Benutzern in Domäne B. Sie leitet Anfragen von Domänen-B-Benutzern zur Authentifizierung an einen Domänencontroller in Domäne B weiter, weil sie dem Identitätsspeicher und Authentifizierungsdienst von Domäne B vertraut. Domäne A kann die Sicherheitsprinzipien von Domäne B zu Gruppen und ACLs in Domäne A hinzufügen.

![Gruppenverschachtelungsmöglichkeiten](ScopesSummarized.jpg)
