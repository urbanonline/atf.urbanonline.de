# Quelldateien für die Webseite atf.urbanonline.de

Die Firma Urban GmbH veranstaltet am 09. Oktober 2025 einen Praxisworkshop mit dem Titel `Erfolgreicher Einsatz von Tränkeautomaten
und UV-C Hygienisierung in der Kälberaufzucht`. Zur Bewerbung dieser Veranstaltung wurde die Seite [`https://atf.urbanonline.de`](https://atf.urbanonline.de) erstellt, dieses Repository enthält die entsprechenden Quelltexte und dient dem Deployment der Webseite.

## Technologie

Zur Erstellung der Seite wird der Site-Generator [Hugo](https://gohugo.io/) genutzt. Grundlage der Seite ist das Theme [hugo-conference](https://github.com/jweslley/hugo-conference) von [Jonhnny Weslley](https://github.com/jweslley). Das Theme wurde sehr stark modifiziert und angepasst, lediglich die Grundstruktur des Themes blieb erhalten.

## Installation SSG Hugo

Installieren sie den Site-Generator Hugo gemäß den [Anweisungen](https://gohugo.io/installation/) der offiziellen Dokumentation.

## Lokaler Preview der Webseite

1. Erzeugen Sie eine lokale Kopie des Repositories auf ihrem Rechner:

    ```
    git clone --depth 1 https://github.com/urbanonline/atf.urbanonline.de.git
    ```

1. Starten Sie eine lokale Vorschau der Webseite, indem Sie folgenden Befehl aufrufen:

    ```
    hugo server
    ```

1. Öffnen Sie Ihren Webbrowser und geben Sie [`http://localhost:1313`](http://localhost:1313) in die Navigationsleiste ein. Dadurch wird eine lokale Instanz der Homepage `atf.urbanonline.de` gestartet. Sie können nun Änderungen am Quellcode vornehmen, nach dem Speichern werden die getätigten Änderungen sofort in Ihrem Browser angezeigt (hot reload).

## Deployment der Webseite

- Die Webseite wird auf [GitHub Pages](https://pages.github.com/) gehostet.

- Das Deployment der Seite erfolgt mittels einer sog. [GitHub Action](https://github.com/features/actions).

- Das entsprechende [action file](/.github/workflows/deploy.yml) wird bei jedem Push eines Commits auf den Branch `main` automatisch ausgeführt, die Webseite wird also nach jeder Einspielung einer Änderung automatisch neu erzeugt.

- Falls nötig, kann das Deployment der Seite auch [manuell](https://github.com/urbanonline/atf.urbanonline.de/actions/workflows/deploy.yml) gestartet werden.