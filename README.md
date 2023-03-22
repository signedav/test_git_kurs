# Github Rezept

## Einige Infos
### Was ist Git?
Das subversion tool. Das Programm. Die Technologie. Git ist nicht dasselbe wie Github.
### Was ist Github?
Der Host. Die Cloud. Alternativ gibt es auch Gitlab.
### Was ist ein Repository?
Ein Repository ist ein abgekapseltes Projekt - wie ein einzelner Server auf einem Github Account (wie zBs. opengisch, signedav oder qgis)
### Wofür ist Git und Github etc. im Gegensatz zu einer Cloud?
- Bei Github trackt man alle Änderungen (mit manueller Beschreibung).
- Bei Github pusht man aktiv (manuell) Änderungen.
- Github ermöglicht aktive (kontrolliert vom User) Konfliktlösung.
### Arbeite ich online?
Auch wenn es möglich ist über den Browser Dateien in Github zu ändern, zieht man sich üblicherweise das Repository lokal in einen Ordner. Arbeitet dort, speichert dort, commitet dort (trackt einzelne Änderungen) und pusht schliesslich wieder auf das Online Repository.
### Was ist ein Github Account 
- Ein Account pro User
- User können selbst Repositories führen oder man kann Organisationen gründen
- Organisationen (zBs. opengisch) kann auch Repositories führen
### Konsole 
Es ist am einfachsten, diese Github Kommandos lokal auf einem Terminal/Konsole auszuführen. Das ist eine textbasierte Steuerung des Betriebssystems. Hier einige Commandos:

```bash
# Auflisten des Inhalts in meinem Documents Verzeichnis mit: ls -l
dave@windows ~/Documents
$ ls -l
total 2
drwxrwxr-x  3 dave dave 4096 Jan 17 14:13 flyingtapir
drwxrwxr-x  4 dave dave 4096 Mär 22 11:47 arbeiten

# In ein Verzeichnis gehen mit: cd <verzeichnis>
dave@windows ~/Documents
$ cd arbeiten
dave@windows ~/Documents/arbeiten

# Zurück gehen mit: cd ..
dave@windows ~/Documents/arbeiten
$ cd ..
dave@windows ~/Documents

# Neues Verzeichnis erstellen mit: mkdir <verzeichnis>
dave@windows ~/Documents
$ mkdir github_repos
```

## 1. Repository "klonen": Wie ich das Repository auf meinen Computer bringe

Das Repository von Github musst du nun bei dir lokal haben. Dafür musst du es "klonen". Die zu "klonende" URL findest du auf Github:
![image](https://user-images.githubusercontent.com/28384354/226886694-632c1fb5-c307-4bd6-a2e0-c729f93cb413.png)


Und dann "klonst" du mit dem Git-Kommando `git clone` in deiner Konsole:

```bash
# Repository klonen
dave@windows ~/Documents/github_repos
$ git clone git@github.com:signedav/github-cookbook.git
```

Wenn es ein neues Repository war, dann kommt noch die Warnung, dass es ein leeres Repository ist - das ist okay.

Anschliessend hast du einen neuen Ordner erstellt mit dem Namen des Repositories:
```bash
dave@windows ~/Documents/github_repos
$ ls -l
total 8
drwxrwxr-x 2 dave dave 4096 Mär 22 11:47 erster_ordner
-rw-rw-r-- 1 dave dave 2737 Mär 22 12:10 README.md
```

Du hast dort auch einen unsichtbaren Ordner `.git` - der ist aber (noch) nicht relevant hier.

### Benutze SSH und nicht HTTPS wenn du lesen möchtest

> Für lesenden Zugriff reicht eine HTTPS-URL, jedoch wird ein SSH-Key zum Schreiben auf GitHub-Repositories benötigt. Denn die Authentifizierung von Nutzerinnen und Nutzern per Username/Password wird auf GitHub seit August 2021 nicht mehr unterstützt.

#### Einrichten deiner SSH Verbindung

## 2. Ändern ein Files

Die Files abändern, Ordner hinzufügen und löschen etc. kannst du alles über den Explorer und mit den Tools deiner Wahl machen. Da musst du dich nicht mehr mit der Konsole herumschlagen.

### 3. Änderungen "stagen" und "commiten"

### 4. Änderungen auf das online Repository "pushen"