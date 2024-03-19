## Shell-Variablen
- setzen innerhalb einer Shell mit  `foo=’bar’` oder `set foo=’bar’`
- ausgeben mit `echo $foo`
- auf null setzen mit `unset foo`
- innerhalb der shell verfügbar, nicht für Subprozesse (=Prozesse, die aus dieser shell gestartet werden)!

## Umgebungsvariablen
### bekannte Umgebungsvariablen
Viele "eingebaute" umgebungsvariablen (nützlich für Skripte)
- `USER` (Username)
- `HOME` (Home-Verzeichnis)
- `PATH` (dafür muss ich etwas ausholen..)
- `SHELL` (Verwendete shell, z.B. `/bin/bash/` oder `/usr/bin/zsh`
- `PWD` (aktuelles Arbeitsverzeichnis, siehe Befehl `pwd` -> print working directory)
- `HOSTNAME` (Hostname der Maschine)
Diese Umgebungsvariablen können von jedem Programm gelesen werden!

### Umgebungsvariablen ausgeben
```
env
```

### eigene Umgebungsvariablen setzen
Umgebungsvariablen lassen sich selbst setzen.
Diese sind dann (im gegensatz zu shell-variablen) von Subprozessen lesbar!
- Für aktuelle Shell und alle Subprozesse: `export foo='bar'`
- Nur für einen Prozess `foo='bar' <befehl für programm>`
- Systemweit (nicht zu empfehlen): `/etc/environment` (auf Linux)
