# WR_I_24-27

## Anleitung für die Publikation

Hier ist eine klare Schritt-für-Schritt-Anleitung, wie du deine **lokal** auf dem Computer erstellten JupyterBook-Dateien (`_build/html`) auf GitHub Pages veröffentlichst.

Die einfachste und sauberste Methode für lokal gerenderte Dateien ist die Verwendung des Python-Tools `ghp-import`. Es nimmt deinen HTML-Ordner und pusht ihn in einen speziellen Branch (meist `gh-pages`), ohne dass du manuell Git-Merges durchführen musst.

---

### Voraussetzungen

1. Du hast ein GitHub-Repository für dein Buch angelegt.
2. Du befindest dich im Terminal im Hauptverzeichnis deines Buches.
3. Du hast JupyterBook bereits installiert.

---

### Schritt 1: Das Buch lokal bauen

Stelle sicher, dass du die aktuellste Version deines Buches gebaut hast.

```bash
jupyter-book build .
# Oder, falls dein Buch in einem Unterordner liegt:
# jupyter-book build mein_buch_ordner

```

Überprüfe kurz, ob der Ordner `_build/html` existiert und die index.html enthält.

### Schritt 2: Das Deployment-Tool installieren

Wir nutzen `ghp-import`. Dieses kleine Tool kopiert einen Ordner in einen Git-Branch.

```bash
pip install ghp-import

```

### Schritt 3: Den HTML-Ordner zu GitHub pushen

Führe nun den folgenden Befehl aus. Er macht drei Dinge gleichzeitig: Er erstellt eine `.nojekyll`-Datei (wichtig!), kopiert den HTML-Ordner und pusht alles auf den `gh-pages` Branch in deinem Repository.

```bash
ghp-import -n -p -f _build/html

```

**Erklärung der Flags:**

* `-n`: Erstellt eine `.nojekyll` Datei. **Sehr wichtig**, da GitHub Pages sonst Ordner, die mit einem Unterstrich beginnen (wie `_static` in JupyterBook), ignoriert.
* `-p`: Pusht den Branch direkt zu GitHub.
* `-f`: Erzwingt den Push (überschreibt den alten Stand im `gh-pages` Branch komplett).
* `_build/html`: Der Pfad zu deinen gerenderten Dateien.

### Schritt 4: GitHub Pages in den Einstellungen aktivieren

Nun müssen wir GitHub mitteilen, dass der neu erstellte Branch als Website ausgeliefert werden soll.

1. Gehe auf GitHub in dein Repository.
2. Klicke oben auf den Reiter **Settings** (Einstellungen).
3. Wähle in der linken Seitenleiste **Pages**.
4. Unter **Build and deployment** > **Source**, wähle **Deploy from a branch**.
5. Unter **Branch**, wähle `gh-pages` und den Ordner `/(root)`.
6. Klicke auf **Save**.

> **Hinweis:** Es kann 1–2 Minuten dauern, bis die Seite live ist. Wenn du die Seite neu lädst, erscheint oben oft eine Leiste mit dem Link zu deiner Live-Seite.

---

### Wichtige Hinweise für den Workflow

#### 1. `.gitignore` pflegen

Achte darauf, dass dein `_build` Ordner in deiner `.gitignore` Datei steht. Du willst die generierten HTML-Dateien in der Regel **nicht** in deinen `main` Branch committen, sondern nur den Quellcode (die `.ipynb` und `.md` Dateien).

Deine `.gitignore` sollte mindestens das enthalten:

```text
_build/
.ipynb_checkpoints/

```

#### 2. Synchronisation

Da du lokal renderst, ist der Workflow ab jetzt immer:

1. Änderungen am Inhalt vornehmen.
2. `jupyter-book build .`
3. `ghp-import -n -p -f _build/html`

#### 3. Caching Probleme?

Wenn du Änderungen gemacht hast, diese aber nach dem Build nicht sichtbar sind, lösche den Build-Ordner vor dem Neubauen, um einen sauberen Stand zu haben:

```bash
jupyter-book clean .
jupyter-book build .

```