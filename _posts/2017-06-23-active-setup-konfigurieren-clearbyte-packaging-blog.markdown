---
layout: post 
title:  "Active Setup konfigurieren | clearByte Packaging Blog" 
date:   2017-06-23T19:49:30.990Z 
categories: deployment msi activesetup
link: http://blog.clearbyte.ch/active-setup/ 
tags:
  - links
ogtype: article 
---

## ACTIVE SETUP KONFIGURIEREN
August 2016 | Eliane Megert

Active Setup ist ein Mechanismus, welcher das einmalige Ausführen von Befehlen pro Benutzer ermöglicht. Active Setup läuft früh während dem Login des Users ab, d.h. bevor die Shell geladen ist und der Desktop erscheint. Der Mechanismus wird in der Regel durch Applikationen bzw. von Installationen gebraucht, um die initiale Konfiguration für den Benutzer aufzusetzen. Es kann jedoch weitläufig eingesetzt werden, wie beispielswiese für das Gestalten einer individuellen Benutzerumgebung im Unternehmen oder auch einfach für das Ausführen von einzelnen Befehlen im Benutzerkontext.
Registry Entries in Bezug auf Active Setup

Wenn ein Benutzer sich am System anmeldet werden die folgenden Registry-Einträge verglichen:

HKLMSoftwareMicrosoftActive SetupInstalled Components< UID >
HKCUSoftwareMicrosoftActive SetupInstalled Components< UID >
Wird der Key im HKCU nicht gefunden so wird der Befehl, welcher unter HKLM eingetragen ist ausgeführt. Der Key wird nun in HKCU dupliziert und beim nächsten Login nicht mehr ausgeführt. Der <UID>-Key muss ein Unikat sein, es ist empfehlenswert hier eine GUID zu benützen.

Werte

Default Value

Type: REG_SZ
Optionaler Name der Komponente. Ist ein Namen hier eingetragen wir dieser im Active Setup Dialog angezeigt wenn der Befehl ausgeführt wird.
IsInstalled

Type: REG_DWORD
Mögliche Werte:
Der Befehl wird derzeit nicht ausgeführt.
Der Befehl wird ausgeführt. Das ist der Standartwert, auch wenn der IsInstalled Wert nicht existiert.
Locale

Type: REG_SZ
Ein beliebiger String, welcher die Sprache der Active Setup Komponente definiert. Sofern der String im Benutzerteil des Active Setups nicht gefunden wird, oder sich vom Key unter HKLM unterscheidet, wird der Befehl ausgeführt.
Anmerkung: Active Setup kennt hier keine Einschränkungen oder Regeln bezüglich des Wertes. Man kann „abc“ oder auch „de“ oder „en“ eintragen. Sobald der Befehl ausgeführt wird, wird der Wert in den Benutzerteil kopiert.
StubPath

Type: REG_SZ oder REG_EXPAND_SZ
Format: Ein beliebiger, ausführbarer Befehl wie z.B. „cscript.exe „c:Program Files (x86)AdobecopyUserFiles.vbs““
Das ist der Befehl, welcher durch das Active Setup ausgeführt wird.
Version

Type: REG_SZ
Format: 4 Zahlen, separiert durch Kommas wie z.B.: 1,2,3,4
Ist eine Version gegeben, wird der Befehl nur ausgeführt wenn die zugehörige Nummer in HKCU tiefer oder gar nicht vorhanden ist. Möchte man, dass der Befehl erneut abläuft, muss die Version in HKLM erhöht werden. Dieser Mechanismus wird auch von Windows Updates gebraucht. Z.B. wenn IE 8 aktualisiert wird auf einer Maschine, auf der IE 7 Installiert ist. Mit dem Erhöhen der Versionsnummer in HKLM wird das Ausführen der initialen Benutzerkonfiguration erneut erzwungen.
RunOnce vs Active Setup

RunOnce: Läuft einmal pro Benutzer und löscht den ausgeführten Registrykey, welcher den Befehl enthält, aus dem System.
RunOnce: Läuft nachdem die Shell geladen wurde.
Active Setup: Der auszuführende Key bleibt in der Registry erhalten.
Active Setup: Läuft bevor die Shell geladen wurde.
Wichtiges zu Active Setup

Active Setup beinhaltet weder ein Timeout noch ein anderer Mechanismus für das Error Handling. D.h ohne Fehlerkontrolle kann sich eine Maschine hier aufhängen.
Auf einem 64-Bit System kann sowohl 64-Bit wie auch 32-Bit Active Setup benützt werden. Die 32-Bit Active Setup Einträge werden in den Wow6432Node migriert. Die 32-Bit Einträge werden zuerst ausgeführt.
Um eine Reihenfolge innerhalb der ActiveSetup Komponenten zu generieren können die „>“ und „<“ Zeichen benützt werden:

„>“ VOR dem Schlüsselnamen – Active Setup läuft am Schluss
„<“ VOR dem Sschlüsselnamen – Active Setup läuft zuerst
B. >{22d6f312-b0f6-11d0-94ab-0080c74c7e95}
