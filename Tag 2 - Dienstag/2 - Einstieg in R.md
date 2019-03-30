2 - Einstieg in R
========================================================
author: Benedict Witzenberger
date: 16.04.2019
autosize: true

Was ist R?
========================================================

> "R is a system for statistical computation and graphics. It consists of a language plus a run-time environment with graphics, a debugger, access to certain system functions, and the ability to run programs stored in script files."

> (Quelle: [R FAQ](https://cran.r-project.org/doc/FAQ/R-FAQ.html))

Was ist R?
========================================================

* Entstanden 1996 an der University of Auckland
* Entwickelt von Robert Gentleman und Ross Ihaka
* Basiert auf den Sprachen `S` und `Scheme`
* inzwischen gibt es eine breite Entwicklercommunity, die die Sprache voranbringt

R vs Python
========================================================
**R**

* Entwickelt von Statistikern
* viele statistische Tools
* einfache M�glichkeiten zur Datenvisualisierung
* gutes User-Interface durch RStudio
* vielf�ltigere L�sungen f�r dasselbe Problem
* verbreitet im Journalismus und der Wirtschaft
* relative steile Lernkurve, aber nach den Basics geht es schnell
* Bibliotheken: CRAN (Comprehensive R Archive Network)

***

**Python**

* Entwickelt in der Informatik
* multi-funktionelle Sprache
* schneller
* einfachere Syntax
* weniger L�sungen f�r dasselbe Problem
* relativ flache Lernkurve
* Bibliotheken: PyPi

R vs Python
========================================================

Es gibt Bibliotheken, die Programmcode der einen Sprache in der anderen Sprache ausf�hren k�nnen.

* R in Python: RPy2
* Python in R: rPython

R vs Python
========================================================

Fazit: 

Beide Sprachen haben vor und Nachteile.

Wir lernen hier R, weil es im Journalismus weiter verbreitet ist. Seine Konzepte stammen eher aus der Statistik stammen - und f�hren daher f�r unsere Zwecke schneller zu Ergebnissen.


Heute Vormittag
========================================================

Die Kommandozeile

Editoren

Github

Die Kommandozeile
========================================================

**Warum?**

Jeder nutzt heute haupts�chlich grafische Benutzerinterfaces - aber: �ber die Kommandozeile geben wir Befehle direkt an den Computer.

Microsofts `cmd.exe` nutzt teilweise andere Befehle.


Bash vs DOS
========================================================

Change Directory: `cd` in Bash, `cd` oder `chdir` in DOS

List Contents of Directory:  `ls` in Bash, `dir` in DOS

Move or Rename a File: `mv` in Bash, `move` und `rename` in DOS

Copy a File: `cp` in Bash, `copy` in DOS

Delete a File: `rm` in Bash, `del` oder `erase` in DOS

Create a Directory:  `mkdir` in Bash, `mkdir` in DOS

Use a Text Editor: `vi` or `nano` in Bash,  `edit` in DOS


Eine Kommandozeileneingabe
========================================================

![](anatomy.png)

Quelle: https://www.learnenough.com/command-line-tutorial/basics


Echo
========================================================

`echo xyz` gibt *xyz* zur�ck. In der Konsole ist das vielleicht erstmal egal, aber wir k�nnen das auch in Dateien schreiben

Auf **UNIX**

`echo "Hello World"`

`echo Hello World`

`echo "Hello World`

 

**L�sung, wenn die Konsole h�ngt: Strg + C / Ctrl + C**

Echo in eine Datei
========================================================

`echo "Ich bin ein Test-Text" > test.txt`

`>` leitet den Inhalt von echo in eine Datei

Wie k�nnen wir das �berpr�fen?

**UNIX**

`cat`

**Windows**

`type`

Noch eine Zeile hinzuf�gen:

`echo "Ich bin ein weiterer Test-Text" >> test.txt`

`>>` ist der Append-Operator


Verzeichnis wechseln / Dateien anzeigen
========================================================

**UNIX**

`cd [Ordnername]` oder `cd ..` f�r eine Ebene hoch

`ls`

**Windows**

`cd [Ordnername]` oder `cd ..` f�r eine Ebene hoch

`dir`

Suchen:

`ls *.txt` oder

`dir *.txt`

Hilfe bekommen
========================================================

**UNIX**

`man [Kommando]` oder `help [Kommando]`

**WINDOWS**

`help [Kommando]`


Neue (leere) Datei erstellen
========================================================

**UNIX**

`touch test.txt`

**WINDOWS**

`echo. > test.txt` oder `type nul > test.txt`

Datei umbenennen
========================================================

**UNIX**

`mv test_alt.txt test_neu.txt`

**WINDOWS**

`rename test_alt.txt test_neu.txt`

Geht auch f�r alle Dateien mit einer Auswahl:

`mv *.htm *.html`

`rename *.htm *.html`

**TIPP**

Verwende bei Dateinamen die TAB-Taste f�r Autovervollst�ndigung.


Datei kopieren
========================================================

**UNIX**

`cp test.txt test_kopie.txt`

**WINDOWS**

`copy test.txt test_kopie.txt`


Datei l�schen
========================================================

**UNIX**

`rm test_kopie.txt` (`-f` ohne Nachfragen und `-r` f�r Unterverzeichnisse)

**WINDOWS**

`del test_kopie.txt` (`/F` ohne Nachfragen und `/S` f�r Unterverzeichnisse)

Sehr m�chtiges Werkzeug, sollte mit Bedacht eingesetzt werden.

NICHT BENUTZEN: `rm -rf /` im Root-Verzeichnis

***

![](rm_rf.png)


�bung Kommandozeile
========================================================

1. Schreibe "Hallo Welt" in die Konsole.

2. Erstelle ein Verzeichnis h�her eine leere Datei mit dem Namen `kommandozeile.txt`.

3. Schreibe "Ich kann Kommandozeile" in die Datei mit dem Namen `kommandozeile.txt`

4. Erstelle eine Kopie von dieser Datei.

5. �berpr�fe, ob die Kopie erstellt wurde.

6. L�sche die Kopie �ber die Kommandozeile.


Weitere n�tzliche Tools
========================================================

`ip a` (UNIX) oder `ipconfig` (Windows): Gibt Infos �ber die aktuellen Netzwerkverbindungen

`curl` kann Dateien herunterladen

`tar` kann Dateien ver- und entpacken


Editoren
========================================================

In der Kommandozeile k�nnen wir verschiedene Editoren aufrufen.