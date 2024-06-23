# LaTeX Template
Dieses Template dient der Erstellung von Studienarbeiten. Es kann in der Datei [`main.pdf`](./main.pdf) eingesehen werden.

## Set-up

Dieses Template kann in einem LaTeX-Editor (z.B. Overleaf, MiKTeX, etc.) ohne weitere Konfigurationen verwendet werden.

### Visual Studio Code

Sollte eine Bearbeitung in Visual Studio Code gewünscht sein, sollten die empfohlenen Erweiterungen installiert werden. Diese können über das Command (`Ctrl+Shift+P`) `Extensions: Show Recommended Extensions` angezeigt und installiert werden.

Anschließend muss eine LaTeX-Distribution installiert werden, damit das Dokument generiert werden kann.

### Installation LaTeX-Distribution unter Windows

Unter Windows kann die MiKTeX-Distribution über `winget` installiert werden. Dafür muss folgender Befehl ausgeführt werden:

```PowerShell
winget install MiKTeX.MiKTeX
```


## Verwendung

### Individualisierung

1. Datei [`1_TitleAuthorKeywords.tex`](1_TitleAutorKeywords.tex) können folgende Metadaten angepasst werden:
- Titel der Arbeit
- Namen der Autoren
- Schlüsselwörter
- Datum

2. In der Datei [`2_Acronyms.tex`](2_Acronyms.tex) können Abkürzungen hinzugefügt werden. Diese werden automatisch im Dokument referenziert und im Abkürzungsverzeichnis aufgeführt.

3. In der Datei [`3_Glossary.tex`](3_Glossary.tex) können Glossareinträge hinzugefügt werden. Diese werden automatisch im Dokument referenziert und im Glossarverzeichnis aufgeführt.

4. In der Datei [`styling/header-footer.tex`](styling/header-footer.tex) müssen folgende Metadaten angepasst werden:

- Modulname
- Name der Oragnisation

5. In dem Verzeichnis [`content`](content) können die einzelnen Kapitel in separaten Dateien erstellt werden. Diese Dateien müssen in der [`content/index.tex`](content/index.tex) referenziert werden.

6. In der Datei [`sources.bib`](sources.bib) können Quellen hinzugefügt werden. Diese müssen im `biblatex`-Format vorliegen. Die Quellen werden automatisch im Literaturverzeichnis aufgeführt. Die Anpassung des Stils kann in der Datei [`main.tex`](main.tex) vorgenommen werden.

7. In der Datei [`content/0_Abstract.tex`](content/0_Abstract.tex) kann das Abstract der Arbeit verfasst werden.

In der Datei [`content/1_Kapitel1.tex`](content/1_Kapitel1.tex) sind Beispiele für die Verwendung von Abkürzungen, Glossareinträgen Quellenverweisen und die Einbindung von Graphiken enthalten.

### GitHub Actions
In der Datei [`.github/workflows/latex.yml`](.github/workflows/latex.yml) ist ein GitHub Action Workflow definiert, der bei jedem Push auf den `main`-Branch das Dokument generiert und als Artefakt bereitstellt. Dieses kann in den Actions heruntergeladen werden.

### Optionale Funktionen

In der `.bib`-Datei des Quellenverzeichnisses kann ein optionaler `annotation`-Key verwendet werden, um den Quellen ein Kommentar zu geben (z.B. Warum die Quelle verwendet wurde oder was sie enthält).

### Quellenverwaltung
Für die Verwaltung der Quellen wird das Tool Zotero empfohlen. Es kann über die Website [Zotero.org](https://www.zotero.org/) heruntergeladen werden. Die Quellen können in Zotero verwaltet und in das `.bib`-Format exportiert werden. Ein automatischer Export in eine lokale `.bib`-Datei ist ebenfalls möglich mit der Erweiterung [Better BibTeX for Zotero](https://retorque.re/zotero-better-bibtex/).

### VS Code Erweiterungen (Rechtschreibprüfung, LateX-Tools)
Für die Bearbeitung wird die Verwendung von Visual Studio Code empfohlen. Es können die empfohlenen Erweiterungen installiert werden, um die Bearbeitung zu erleichtern. Die Erweiterungen können über das Command (`Ctrl+Shift+P`) `Extensions: Show Recommended Extensions` angezeigt und installiert werden. So kann auch eine Rechtschreibüberprüfung mit der Erweiterung `CSpell` durchgeführt werden. Entsprechende Konfigurationen sind für die Sprachen `de` und `en` bereits in der Datei [`cspell.js`](cspell.json) und im Ordner `.cspell` vorhanden.
# Lizenz
Dieses Template steht unter der MIT-Lizenz. Weitere Informationen können der Datei `LICENSE` entnommen werden.
