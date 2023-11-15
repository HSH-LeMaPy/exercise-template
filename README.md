# HSH Aufgabenblatt Template

Dieses Repository enthält eine Vorlage zum Erstellen von Aufgabenblättern für Kurse an der Hochschule Hannover. Die Aufgaben werden in Quarto geschrieben und können in PDF-Dateien konvertiert werden.

## Quick start

### Voraussetzungen

Folgende Voraussetzungen müssen erfüllt sein:

1. Quarto in einer Version >= 1.4: https://github.com/quarto-dev/quarto-cli/releases
2. TinyTex als LaTeX Distribution: `quarto install tinytex`
3. Python und folgende Pakete: `pip install jupyter matplotlib sympy sympy_plot_backends pandas`
4. Eine Entwicklungsumgebung z.B. VSCode mit dem Quarto Plugin: https://code.visualstudio.com/ und https://marketplace.visualstudio.com/items?itemName=quarto.quarto

### Erstellen eines neuen Projektes

Sobald die Voraussetzungen erfüllt sind, kann der folgende Befehl genutzt werden, um ein neues Projekt anzulegen: `quarto use template hsh-lemapy/exercise-template`.

### Ordnerstruktur

| Ordner           | Beschreibung                                                                                                                        |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| _output          | Das Zielverzeichnis, in dem die generierten Aufgabenblätter abgelegt werden                                                         |
| Anhang           | Dateien, die direkt in das Zielverzeichnis kopiert werden                                                                           |
| Aufgabenblaetter | Definieren den Rahmen für das Aufgabenblatt und referenzieren Einzelaufgaben                                                        |
| Einzelaufgaben   | Einzelne Aufgaben inkl. Lösungen. Die Aufgaben werden in Kapitel unterteilt und die Lösungen sind per Profil "solved" einblendbar |
| Ressourcen       | Inhalte wie Bilder, die in den Aufgabenblättern eingebunden werden, aber nicht in das Zielverzeichnis kopiert werden                |

### Befehle

- `quarto render`: Baut alle Aufgabenblätter und kopiert diese in das Zielverzeichnis
- `quarto render --profile solved`: Baut alle Aufgabenblätter inkl. Lösungen und kopiert diese in das Zielverzeichnis

### Aktualisieren des Templates

Sollte das Template selbst aktualisiert werden, kann der folgende Befehl genutzt werden, um das Projekt auf das neue Template zu aktualisieren: `quarto update extension hsh-lemapy/exercise-template`

## Nützliche Links:
- https://quarto.org/docs/authoring/markdown-basics.html
- https://github.com/quarto-ext/include-code-files
