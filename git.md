# allgemeine git Befehle

Ein Projekt mit git klonen
```
git clone git@github.com:st4rga2er/python_for_beginners.git
```

Einen neuen Branch anlegen
```
git switch -c <name>
# zum Beispiel
git switch -c feature/mein_tolles_feature
```

Aktuellen Branch anzeigen lassen
```
# Der aktive Branch ist mit einem '*' gekennzeichnet
git branch
```

Einen Branch wechseln
```
git switch <name>
```

Änderungen anzeigen lassem
```
git status
```

Eine Datei zu einem Commit hinzufügen
```
git add <datei>
# oder alle Dateien (Tip, erst mit git status nachsehen)
git add -A
```

Änderungen an einer Datei ansehen
```
git diff <datei>
```

Einen Commit mit einer Nachricht vorbereiten
```
git commit -m "A commit message"
```

Einen Commit nach github schicken
```
git push
```

Den aktuellen Stand von github holen
```
git pull
```

# Arbeitsablauf für einen neuen Branch
```
# Branch erstellen
git switch -c feature/hello_world
# Änderungen machen, wie neue Dateien erstellen, vorhandene bearbeiten
...
# 1. Änderungen mit commit-Message vorbereiten
git status
# Änderungen evtl. ansehen
git diff <datei>
git add <Datei> # oder git add -A
git commit -m "Implementierung von Feature xyz"
# 1. Änderungen nach github schicken
git push
# Feierabend machen
...
# Am nächsten Tag aktuelle Änderungen von github holen
git pull
# weitere Änderungen machen
...
# Änderungen für den commit vorbereiten
git commit -a --amend --no-edit
# Änderungen nach github schicken
git push --force
# Feierabend machen
...
# Am nächsten Tag aktuelle Änderungen von github holen
git pull
...
# usw.
```