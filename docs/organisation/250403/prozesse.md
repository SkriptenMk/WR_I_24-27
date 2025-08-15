# Darstellung von Prozessen als Flussidagramm mit Hilfe von TikZ

Das folgende Listing zeigt ein schematisches Beispiel für die Darstellung eines
Flussdiagramms mit Hilfe von TikZ.

```latex
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Flussdiagramm-Beispiel für Informatik-Unterricht
% Zweck: Demonstration der grundlegenden Flussdiagramm-Elemente und deren
% Implementierung in LaTeX/TikZ
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

% --- Dokumentklasse und Pakete ---
\documentclass{standalone}  % Erzeugt ein Dokument ohne Seitenränder - ideal für einzelne Diagramme

% Laden der benötigten TikZ-Bibliotheken
\usepackage{tikz}  % Hauptpaket für das Erstellen von Vektorgrafiken
\usetikzlibrary{
    arrows,      % Ermöglicht verschiedene Pfeilstile
    positioning, % Vereinfacht die relative Positionierung von Elementen
    calc,        % Erlaubt mathematische Berechnungen von Positionen
    shapes       % Stellt zusätzliche Formen wie Trapeze und Rauten zur Verfügung
}

\begin{document}

% --- Beginn des Flussdiagramms ---
% Die eckigen Klammern enthalten globale Stiloptionen für das gesamte Diagramm
\begin{tikzpicture}[
    % Definition der verschiedenen Knotentypen (Shapes) für das Flussdiagramm
    % Jeder Typ entspricht einem Standard-Symbol in Flussdiagrammen
    % Start/Ende-Knoten: Abgerundetes Rechteck
    end/.style={
        draw,                    % Zeichnet den Rahmen
        rectangle,               % Grundform ist ein Rechteck
        rounded corners=2mm,     % Rundet die Ecken ab
        minimum width=2cm,       % Legt Mindestbreite fest
        align=center             % Zentriert den Text im Knoten
    },
    % Eingabe/Ausgabe-Knoten: Trapez
    io/.style={
        draw,
        trapezium,                 % Trapezform für Ein-/Ausgabe
        trapezium left angle=70,   % Linker Winkel des Trapez
        trapezium right angle=110, % Rechter Winkel des Trapez
        minimum width=2cm,
        align=center
    },
    % Prozess-Knoten: Rechteck
    process/.style={
        draw,
        rectangle,              % Standardrechteck für Prozessschritte
        minimum width=2cm,
        align=center
    },
    % Entscheidungs-Knoten: Raute
    decision/.style={
        draw,
        diamond,                % Rautenform für Entscheidungen
        minimum width=2cm,
        align=center
    }
]

    % --- Definition der Knoten ---
    % Jeder Knoten wird mit \node erstellt und erhält einen Namen für spätere Referenzen
    
    % Startknoten
    \node[end] (start) {Start};  % (start) ist der Name zur Referenzierung
    
    % Eingabe-Knoten, positioniert unter dem Start
    \node[io, below = of start] (input) {Eingabe};
    
    % Verarbeitungs-Knoten
    \node[process, below = of input] (process) {Verarbeitung};
    
    % Entscheidungs-Knoten
    \node[decision, below = of process] (decision) {Bedingung?};
    
    % End-Knoten
    \node[end, below = of decision] (end) {Ende};

    % --- Definition der Verbindungspfeile ---
    % Pfeile verbinden die Knoten und zeigen den Programmfluss
    
    % Hauptpfade von oben nach unten
    \path[->, draw] (start) -- (input);      % Start → Eingabe
    \path[->, draw] (input) -- (process);    % Eingabe → Verarbeitung
    \path[->, draw] (process) -- (decision); % Verarbeitung → Entscheidung
    \path[->, draw] (decision) -- (end);     % Entscheidung → Ende
    
    % Schleifenpfad: Geht von der Entscheidung zurück zur Verarbeitung
    % Verwendet -| und |- für rechtwinklige Verbindungen
    \path[->, draw] (decision.east) -| ++(1,0) |- (process.east);
    % .east bezieht sich auf den östlichen (rechten) Ankerpunkt des Knotens
    % ++(1,0) verschiebt den Pfad 1 Einheit nach rechts
    % |- erzeugt eine vertikale-horizontale Verbindung zurück zum Prozess

\end{tikzpicture}
\end{document}
```

Die Datei mit dem obigen Listing wird mit dem Befehl `pdflatex dateiname.tex`
kompiliert. Das Resultat ist eine PDF-Datei. Wenn als Resultat eine SVG-Datei
erzeugt werden soll, geschieht das mit den beiden Befehlen:
```bash
latex dateiname.tex
dvisvgm --no-fonts dateiname.dvi
```

Das Diagramm aus obigem Listing sieht wie folgt aus:

![Flussdiagramm](bsp.svg)