## Universelle Gruppen, globale Gruppen, lokale Domänengruppen
### AD Gruppentypen: universelle Gruppen, globale Gruppen, globale Gruppen, lokale Domänengruppen
#### Gruppen 
* Verteilergruppen - Wird für E-Mails verwendet. Nützlich für Programme wie MS Exchange.
* Sicherheitsgruppen - Wird zum Schutz von Dateien/Ordnern, Druckern usw. verwendet.
  * Lokal - Wird auf dem lokalen SAM (Local Computers) gespeichert.
  * Domänenlokal - Wird auf Domänencontrollern gespeichert.
  * Globale Gruppen - Bietet Ihnen einen größeren Gruppenumfang.
  * Universell - Bietet Ihnen einen noch breiteren Gruppenumfang.

#### Group Scopes
Der Gruppenrahmen beschreibt in der Regel die Art der Benutzer, die auf eine für ihre Verwaltung einfache Weise zusammengeschlossen werden sollen. Daher spielen Gruppen eine wichtige Rolle in der Domäne. Eine Gruppe kann Mitglied einer anderen Gruppe(n) sein, die als Gruppenverschachtelung bezeichnet wird. Eine oder mehrere Gruppen können Mitglieder einer beliebigen Gruppe in der gesamten Domain(s) innerhalb eines Waldes sein.

Domäne Lokale Gruppe: Verwenden Sie diesen Bereich, um Berechtigungen für Domänenressourcen zu erteilen, die sich in der gleichen Domäne befinden, in der die lokale Domänengruppe erstellt wurde. Lokale Domänen-Gruppen können auf allen gemischten, nativen und vorläufigen funktionalen Ebenen von Domänen und Wäldern existieren. Die Mitgliedschaft in lokalen Gruppen der Domäne ist nicht beschränkt, da Benutzer Mitglieder als Benutzerkonten und universelle und globale Gruppen aus jeder Domäne hinzufügen können. Die Verschachtelung kann nicht in einer lokalen Domänengruppe durchgeführt werden. Eine lokale Domänengruppe wird nicht Mitglied einer anderen lokalen Domäne oder einer anderen Gruppe in derselben Domäne sein.

Globale Gruppe: Benutzer mit ähnlichen Funktionen können unter dem globalen Bereich gruppiert werden und erhalten die Berechtigung, auf eine Ressource (wie einen Drucker oder einen freigegebenen Ordner und Dateien) zuzugreifen, die in der lokalen oder einer anderen Domäne im selben Wald verfügbar ist. Einfach ausgedrückt, können globale Gruppen verwendet werden, um Berechtigungen zu erteilen, um Zugriff auf Ressourcen zu erhalten, die sich in jeder Domäne, aber in einem einzigen Wald befinden, da ihre Mitgliedschaften begrenzt sind. Benutzerkonten und globale Gruppen können nur aus der Domäne hinzugefügt werden, in der die globale Gruppe erstellt wird. Die Verschachtelung ist in globalen Gruppen innerhalb anderer Gruppen möglich, da Benutzer aus jeder Domäne eine globale Gruppe zu einer anderen globalen Gruppe hinzufügen können. Sie können Mitglieder einer lokalen Domänengruppe sein, um die Berechtigung für domänenspezifische Ressourcen (wie Drucker und veröffentlichte Ordner) zu erteilen. Globale Gruppen gibt es auf allen gemischten, nativen und vorläufigen funktionalen Ebenen von Bereichen und Wäldern.

Universeller Gruppenumfang: Diese Gruppen werden genau für die E-Mail-Verteilung verwendet und können Zugriff auf Ressourcen in allen vertrauenswürdigen Domänen erhalten, da diese Gruppen nur als Sicherheitsprinzip (Sicherheitsgruppentyp) in einer nativen Windows 2000 oder Windows Server 2003 Domänenfunktionsebene verwendet werden können. Universelle Gruppenmitgliedschaften sind nicht begrenzt wie globale Gruppen. Alle Domänenbenutzerkonten und -gruppen können Mitglied einer Universalgruppe sein. Universelle Gruppen können unter einer globalen oder lokalen Gruppe in einer beliebigen Domäne verschachtelt werden. 

Universelle Gruppe: kann Benutzer und Gruppen (global und universell) aus jeder Domäne im Wald enthalten.  Universelle Gruppen kümmern sich nicht um Vertrauen.  Universelle Gruppen können Mitglied in lokalen Domänengruppen oder anderen universellen Gruppen sein, aber NICHT in globalen Gruppen.

Globale Gruppe: kann Benutzer, Computer und Gruppen aus derselben Domäne enthalten, aber KEINE universellen Gruppen.  Kann Mitglied in globalen Gruppen derselben Domäne, lokalen Domänengruppen oder universellen Gruppen einer beliebigen Domäne in der Forstwirtschaft oder vertrauenswürdigen Domänen sein.

Domäne Lokale Gruppe:  Kann Benutzer, Computer, globale Gruppen und universelle Gruppen aus jeder Domäne im Wald und jeder vertrauenswürdigen Domäne sowie lokale Domänengruppen aus derselben Domäne enthalten.  Kann Mitglied einer beliebigen lokalen Domänengruppe in derselben Domäne sein.

Die kurze Antwort ist, dass lokale Domänengruppen die einzigen Gruppen sind, die Mitglieder von außerhalb des Waldes haben können. Und verwenden Sie globale Gruppen, wenn Sie Vertrauen haben, universelle Gruppen, wenn Sie sich nicht um Vertrauen kümmern.

#### Wann müssen wir die lokale, globale und universelle Gruppenberechtigung verwenden?

Verwenden Sie globale Sicherheitsgruppen, um Benutzer- (oder Computer-) Konten mit ähnlichen Merkmalen zu gruppieren, z.B. Mitglieder der Vertriebsabteilung.

Verwenden Sie domänenlokale Sicherheitsgruppen, um den Zugriff auf Ressourcen (Freigabe, NTFS, Drucker) zu definieren,
zum Beispiel würden Sie die lokale Domänengruppe "DL ColorPrinter Print" erstellen und dieser Gruppe die Druckberechtigung zuweisen. Dann würden Sie die globale Sicherheitsgruppe Vertrieb in die Gruppe "DL ColorPrinter Print" einordnen, um den Druck für den Vertrieb zu ermöglichen. Wenn die Marketingabteilung den gleichen Drucker verwenden möchte, müssen Sie eine globale Gruppe Marketing anlegen und diese Gruppe in die Gruppe "DL ColorPrinter Print" aufnehmen. Diese Strategie wird als A-G-DL-P bezeichnet. Legen Sie Konten in globalen Gruppen, globale Gruppen in lokalen Domänengruppen an und weisen Sie Berechtigungen zu lokalen Domänengruppen zu, und Sie werden die Berechtigung nur einmal vergeben. Alles andere geschieht in Active Directory-Benutzern und -Computern, wenn Sie die Gruppenzugehörigkeit ändern.

Universelle Gruppen sollten nur in Gebieten mit mehreren Domänen verwendet werden. Universelle Gruppen werden verwendet, um globale Gruppen zu verschachteln. Die Konzernstrategie wird dann als A-G-U-DL-P bezeichnet.

* Globale Gruppen:
Verwenden Sie diese, um Benutzer mit ähnlichen Anforderungen innerhalb der Organisation, Vertriebsmitarbeiter, Finanzexperten, Manager usw. zu gruppieren.
* Domänenlokale Gruppen:
Verwenden Sie diese Option, um den Zugriff auf Ressourcen festzulegen, z.B. Datenbankbenutzer, Farbdruckerbenutzer.
* Universelle Gruppen
Nur in mehrfachen Domänen verwenden, um waldbreite Rechte zu vergeben.
