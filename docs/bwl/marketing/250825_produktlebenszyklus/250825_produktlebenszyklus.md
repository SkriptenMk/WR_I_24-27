# Produktlebenszyklus

Der Produktlebenszyklus beschreibt die verschiedenen Phasen, die ein
Produkt von der Markteinführung bis zur Marktentfernung durchläuft.
Dieses Modell hilft Unternehmen, strategische Entscheidungen über
Marketing, Preisgestaltung und Produktentwicklung zu treffen. Die
klassischen Phasen sind: 

* Einführungsphase
* Wachstumsphase
* Reifephase
* Sättigungsphase
* Degenerationsphase

Zusätzlich kann durch einen Relaunch der Zyklus verlängert werden.

## Umsatz- und Gewinnentwicklung

Der Verlauf von Umsatz und Gewinn ist charakteristisch für die einzelnen
Phasen des Produktlebenszyklus. 

* **Einführungsphase**: Der Umsatz ist niedrig, während die hohen Kosten
  für Forschung, Entwicklung und Marketing zu einem negativen Gewinn
  führen. 

* **Wachstumsphase**: Der Umsatz steigt stark an. Der Gewinn wird positiv
  und erreicht gegen Ende der Phase seinen Höhepunkt, da die
  Produktionskosten durch Skaleneffekte sinken.

* **Reife- & Sättigungsphase**: Der Umsatz erreicht seinen Höhepunkt und
  beginnt dann langsam zu sinken. Der Wettbewerbsdruck steigt, was zu
  höheren Marketingausgaben und sinkenden Preisen führen kann. Der Gewinn
  geht daher zurück.

* **Degenerationsphase**: Umsatz und Gewinn sinken deutlich. Das
  Unternehmen muss entscheiden, ob das Produkt vom Markt genommen oder
  durch einen Relaunch neu positioniert wird.

Die folgende Grafik veranschaulicht den typischen Verlauf von Umsatz und Gewinn über den Produktlebenszyklus.

\begin{tikzpicture}
    \draw[->] (0,0) -- (12,0) node[right] {Zeit};
    \draw[->] (0,0) -- (0,6) node[above] {Umsatz/Gewinn};

    % Phasen
    \draw[dashed] (2.5,0) -- (2.5,5.5);
    \node[above] at (1.25,5.5) {Einführung};
    \draw[dashed] (5,0) -- (5,5.5);
    \node[above] at (3.75,5.5) {Wachstum};
    \draw[dashed] (8,0) -- (8,5.5);
    \node[above] at (6.5,5.5) {Reife};
    \draw[dashed] (10,0) -- (10,5.5);
    \node[above] at (9,5.5) {Sättigung};
    \node[above] at (11,5.5) {Degeneration};

    % Umsatzkurve (blau)
    \draw[blue, thick, label=Umsatz] (0,0.5) .. controls (1.5,1) and (3,4) .. (5,5) .. controls (7,6) and (8,5) .. (10,4.5) .. controls (11,3) .. (11.5, 2);
    \node[blue, right] at (11.5, 2) {Umsatz};

    % Gewinnkurve (rot)
    \draw[red, thick, label=Gewinn] (0,0) .. controls (1.5,-1) and (2.5,0) .. (4,3) .. controls (6,4) and (8,2) .. (10,1) .. controls (11,-0.5) .. (11.5, -1);
    \node[red, right] at (11.5, -1) {Gewinn};
    
    % Relaunch (grün)
    \draw[green, thick, dashed, label=Relaunch] (9,1.5) .. controls (10,2.5) and (11,3.5) .. (12,4);
    \node[green, above] at (11,4.2) {Relaunch};
\end{tikzpicture}

## Die einzelnen Phasen im Detail

1. Einführungsphase
    In der Einführungsphase wird das Produkt neu auf dem Markt
    eingeführt. Wichtige Aspekte dieser Phase sind: 

    * Marktforschung: Identifikation der Zielgruppe und ihrer Bedürfnisse.

    * Marketingstrategie: Entwicklung einer Strategie zur Bekanntmachung
      des Produkts (hohe Werbeausgaben). 

    * Vertriebskanäle: Auswahl und Aufbau geeigneter Vertriebskanäle.

2. Wachstumsphase
   In der Wachstumsphase gewinnt das Produkt an Marktanteil und
   Bekanntheit. Wichtige Aspekte dieser Phase sind: 

   * Skalierung der Produktion: Anpassung der Produktionskapazitäten an
     die steigende Nachfrage. 

   * Marketingmaßnahmen: Intensivierung der Marketingaktivitäten zur
     weiteren Steigerung des Bekanntheitsgrads. 

   * Kundenfeedback: Sammlung von Kundenfeedback zur kontinuierlichen
     Verbesserung des Produkts.

3. Reifephase & Sättigungsphase
   In der Reifephase hat das Produkt seinen Umsatzhöhepunkt erreicht,
   der Markt ist in der Sättigungsphase zunehmend gesättigt. 

   * Marktsättigung: Das Wachstum verlangsamt sich und kommt zum Stillstand.

   * Wettbewerbsanalyse: Der Wettbewerb ist am intensivsten. Preiskämpfe sind üblich.

   * Produktvariationen: Einführung von Produktvariationen zur Ansprache neuer Zielgruppen oder zur Differenzierung.

4. Degenerationsphase
   In der Degenerationsphase nimmt die Nachfrage nach dem Produkt ab.
   Wichtige Aspekte dieser Phase sind: 

   * Kostenmanagement: Reduzierung der Kosten zur Erhaltung der Rentabilität.

   * Produktabkündigung: Gegebenenfalls Einstellung des Produkts und Kommunikation an die Kunden.

   * Neuproduktentwicklung: Fokussierung auf die Entwicklung neuer Produkte zur Sicherstellung des Unternehmenserfolgs.

5. Relaunch
   Ein Relaunch ist eine strategische Maßnahme, um ein Produkt, das sich
   in der Reife- oder Degenerationsphase befindet, neu zu beleben. Ziele
   sind die Verlängerung des Lebenszyklus und die erneute Steigerung von
   Umsatz und Gewinn. Maßnahmen für einen Relaunch können sein: 

   * Produktmodifikation: Verbesserung von Qualität, Funktionen oder Design.

   * Marketing-Neuausrichtung: Ansprache neuer Zielgruppen oder Änderung der Werbebotschaft.

   * Erschließung neuer Märkte: Expansion in neue geografische Regionen.

   Ein erfolgreicher Relaunch kann den Degenerationsprozess aufhalten
   und eine neue Wachstumsphase einleiten. 

## Fazit 

Der Produktlebenszyklus ist ein wichtiges Konzept im Marketing. Die
Analyse von Umsatz und Gewinn in den einzelnen Phasen hilft Unternehmen,
ihre Produkte strategisch zu positionieren und erfolgreich zu
vermarkten. Durch ein tiefes Verständnis der verschiedenen Phasen und
der Möglichkeit eines Relaunches können Unternehmen proaktiv auf
Veränderungen im Markt reagieren und ihre Produkte kontinuierlich
anpassen. 