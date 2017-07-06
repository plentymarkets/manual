# Handbuch + AsciiDoc

## Doku Generator installieren

Der Doku Generator übersetzt AsciiDoc in .twig-Dateien für das Handbuch-Plugin.

1. Das Tool benötigt [Node.js ab Version 6.8.X](https://nodejs.org/en/):
   - *Welche Node.js-Version ist installiert?*
   Der Befehl `node -v` gibt die installierte Version von Node.js aus. Führt der Befehl zu einem Fehler ist Node.js überhaupt nicht installiert. [Node.js herunterladen](https://nodejs.org/en/)
   
2. Die Installation erfolgt über **npm** (wird zusammen mit Node.js installiert) [Installationsanleitung auf GitHub](https://github.com/plentymarkets/docgen)
   - Optional kann das Projekt auch geklont werden. In diesem Fall kann das Script über `node /path/to/project main.js` anstelle des globalen Befehls `docgen` ausgeführt werden.


## Editor / Entwicklungsumgebung

Es existieren gute AsciiDoc-Plugins für IntelliJ und für Atom.

**IntelliJ** 

1. Öffne Tab "Plugins" in den Einstellungen "IntelliJ IDEA > Preferences"
2. Klicke auf "Browse Repositories"
3. Suche nach "AsciiDoc" und installiere das Plugin.

**Atom**

1. Öffne Tab "Packages" in den Einstellungen "Atom > Preferences"
2. Installiere die Pakete:
	- asciidoc-preview
	- language-asciidoc
	- autocomplete-asciidoc (optional)

Alternativ gibt es diverse Seiten, um online AsciiDoc-Dokumente zu bearbeiten und live zu betrachen:

- [http://gist.asciidoctor.org/](http://gist.asciidoctor.org/)
- [https://asciidoclive.com](https://asciidoclive.com)


## AsciiDoc Hilfe

- [Writers Guide](http://asciidoctor.org/docs/asciidoc-writers-guide/)
- [Quick Reference](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)
- [User Manual](http://asciidoctor.org/docs/user-manual/)