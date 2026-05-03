### **Git**

###### Git Status erklären: 

Auf dem Branch b03 wurden Änderungen an CONTRIBUTION.md und homework/b03.md vorgenommen, die noch nicht committed wurden und noch mit git add hinzugefügt werden müssen.

Außerdem wurde eine neue Datei foo.java erstellt, die bisher nicht im Repository ist.

Aktuell gibt es keine Veränderungen, die committed wurden, im Vergleich zu der letzten Version.



Befehlssequenz für foo.java: 

git add foo.java

git commit



###### Git Spiel:

1\.

* Was passierte an tag 01? Markus beginnt sein Abenteuer, bekämpft eine Ratte, dann eine schlafende Ratte und wird hungrig. Es wird Text geändert und die Werte entsprechend angepasst.

Eingaben: 

git log --oneline

git show 4aa8019

git show e3233e4

git show fa49e74

git show 590fc86

git show d0e415c

git show 2a0717e

* Wann hat der Held zum ersten Mal 4 experience Punkte? An Tag 01.3

Eingaben:

git show 590fc86

* Wann hat der Held zum ersten Mal 10 hunger Punkte? Tag 02

Eingaben: 

git log -p stats.md

* Wie viele Heiltränke hat der Held insgesamt in seinem Rucksack gehabt? 2 Heiltränke

Eingaben:

git log -p rucksack.md

* Was hat der Held im Shop gekauft? Und wie viel Gold hat er dafür bezahlt? Einen Heiltrank und ein Brot für jeweils 5 Gold.

Eingaben:

git log -p rucksack.md

* Was passierte zwischen tag 03 und tag 04, d.h. was änderte sich zwischen diesen Commits? Es wurden 10 Gold abgezogen, health von 5 auf 10 geändert, hunger von 10 auf 0 reduziert und ein Text hinzugefügt. 

Eingaben:

git diff 2ffebcf 39568d5

* Hat der Held etwas gegessen? Falls ja, was und wann? Ja, ein Brot an Tag 03.17

Eingaben: 

git log -p rucksack.md



2\. in stats.md die 40 auf 42 geändert und die Datei gespeichert.

Eingaben:

git add stats.md

git commit



3\. Text in questlog.md hinzugefügt.

Eingaben:

git add questlog.md

git commit -m "tag 04.6"



4\. Text in questlog.md hinzugefügt und stats.md angepasst.

Eingaben:

git add questlog.md stats.md

git commit -m "tag 04.7"



5\. Neue Datei gear.md erstellt. Die Ausrüstungszeilen von stats.md entfernt und in gear.md kopiert.

Eingaben:

git add stats.md gear.md

git commit -m "tag 04.8"



###### Commit-Meldungen:

Das erste Beispiel ist recht kurz gefasst und für Nutzer unklar, es ist eher für die Mitentwickler sinnvoll.

Das zweite Beispiel zeigt deutlicher was geändert wurde und beschreibt es genauer.



### Gradle

* Welche Tasks? 

Eingabe in der Konsole: .\\gradlew tasks

* Java-Dateien anlegen? 

unter \\app\\src\\main\\java  

die Test-Dateien kommen in \\app\\src\\test\\java 

externe Dateien wie Bilder kommen in \\app\\src\\main\\resources

* Unterteilung Buildskript+Aufgaben:

Plugins (definiert verwendete Funktionen, zB java)

Repositories (definiert wo Bibliotheken gesucht werden)

Dependencies (definiert externe Bibliotheken und lokale Abhängigkeiten für verschiedene Build-Phasen)

* plugin application tasks:

erstellt einen ausführbare JVM Anwendung für einen einfachen Start der lokalen Anwendung.

wendet das java plugin an.

* Ansteuern in IDE:

rechts in der Leiste Gradle anklicken für die tasks.



##### Java-Projekt anlegen

hat alles funktioniert :D



