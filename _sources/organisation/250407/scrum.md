# Scrum

Traditionellerweise werden Projekte nach dem Wasserfall-Modell geplant und
umgesetzt. In diesem Modell wird das Projekt in die Phasen Problemanalyse,
Planung, Umsetzung und Evaluation unterteilt. Diese Phasen werden eine nach der
anderen durchlaufen. Diese Vorgehensweise hat den Nachteil, dass es schwierig
ist, auf Änderungen zu reagieren. Dies ist insbesondere in der
Softwareentwicklung ein Problem. Oft erkennen Kunden erst während der
Entwicklung, was für Anforderungen sie an das Produkt haben.

Diese Problematik hat im Software Engineering zu Agilen Methoden geführt. Die
Kernprinzipien Agiler Methoden wurden im Agilen Manifest festgehalten.

## Agiles Manifest

>Wir erschließen bessere Wege, Software zu entwickeln,
>indem wir es selbst tun und anderen dabei helfen.
>Durch diese Tätigkeit haben wir diese Werte zu schätzen gelernt:
>
>**Individuen und Interaktionen** mehr als Prozesse und Werkzeuge
>**Funktionierende Software** mehr als umfassende Dokumentation
>**Zusammenarbeit mit dem Kunden** mehr als Vertragsverhandlung
>**Reagieren auf Veränderung** mehr als das Befolgen eines Plans
>
>Das heißt, obwohl wir die Werte auf der rechten Seite wichtig finden,
>schätzen wir die Werte auf der linken Seite höher ein.[^1]

## Scrum

Scrum ist eine der beliebtesten agilen Techniken.  
Sie wurde erstmals von Hirotaka Takeuchi und Ikujiro Nonaka 1986 unter dem Titel
„The New New Product Development Game“ in der Harvard Business Review
vorgestellt.

### Grundsätzliche Vorgehensweise

Scrum verfolgt einen iterativen und inkrementellen Ansatz zur
Softwareentwicklung. Statt das gesamte Projekt von Anfang bis Ende
durchzuplanen, wird die Entwicklung in kurze Zeitabschnitte (Sprints)
unterteilt, in denen jeweils ein funktionierendes, wenn auch unvollständiges,
Produkt steht.

Im Zentrum des Scrum-Prozesses steht das **Product Backlog**. Es enthält alle
Anforderungen, Features und Verbesserungen, die für das Produkt umgesetzt werden
sollen. Diese werden als User Stories formuliert, die aus Kundensicht
beschreiben, welche Funktionalität gewünscht wird. Beispiel: "Als Benutzer
möchte ich mich anmelden können, um auf mein Konto zuzugreifen." 

Das Product Backlog wird vom Product Owner gepflegt und nach Prioritäten
geordnet. Der Product Owner ist der Vertreter des Kunden im Projekt. Die
wichtigsten Aspekte sind: 

- **Priorisierung**: Die wichtigsten Items stehen oben und werden zuerst
  bearbeitet 
- **Detaillierung**: Je höher die Priorität, desto ausführlicher ist die
  Beschreibung 
- **Flexibilität**: Das Backlog kann jederzeit angepasst werden, wenn sich
  Anforderungen ändern 
- **Transparenz**: Alle Teammitglieder haben Einblick in das Backlog

Zu Beginn jedes Sprints wählt das Team die Items mit der höchsten Priorität aus
dem Product Backlog aus und überführt sie in das Sprint Backlog. Das Sprint
Backlog enthält die konkreten Aufgaben, die während des Sprints umgesetzt werden
sollen. 

Die grundlegenden Prinzipien von Scrum sind:
- **Transparenz**: Alle wichtigen Aspekte des Prozesses sind sichtbar
- **Überprüfung**: Regelmässige Inspektion der Ergebnisse und des Prozesses
- **Anpassung**: Kontinuierliche Verbesserung basierend auf den Erkenntnissen


### Ablauf eines Sprints

Ein Sprint ist ein Zeitraum von 1
bis 4 Wochen, in dem ein Teil des Projektes umgesetzt wird. Am Ende eines
Sprints steht eine funktionsfähige Version des Produktes. Der Sprint kann in
vier Elemente unterteilt werden:

- **Sprint-Planung**: In der Sprint-Planung wird festgelegt, welche Aufgaben im
  Sprint umgesetzt werden sollen. Der Product Owner stellt die Aufgaben vor und
  das Team entscheidet, welche Aufgaben im Sprint umgesetzt werden.
- **Sprint**: In der Sprint-Phase wird das Produkt umgesetzt. Das Team arbeitet
  an den Aufgaben, die in der Sprint-Planung festgelegt wurden. Am Ende des
  Sprints steht eine funktionsfähige Version des Produktes.
- **Daily Scrum** (Daily Standup): Das Daily Scrum ist ein tägliches Meeting von
  maximal 15 Minuten, 
  bei dem jedes Teammitglied berichtet, was es seit dem letzten Meeting getan hat,
  was es als nächstes tun wird und welche Hindernisse es dabei gibt. Es dient der
  Koordination innerhalb des Teams.
- **Sprint Review und Retrospektive**: Nach Abschluss des Sprints wird das Ergebnis
  im Sprint Review dem Product Owner und ggf. weiteren Stakeholdern präsentiert.
  In der Retrospektive analysiert das Team den vergangenen Sprint und identifiziert
  Verbesserungspotenziale für zukünftige Sprints.

### Weitere Rollen im Scrum-Prozess

Neben dem **Product Owner** werden in Scrum die folgenden beiden Rollen
definiert:

- **Scrum Master**: Der Scrum Master fungiert als Servant Leader für das Team
  und die Organisation.  
  Seine Hauptaufgaben umfassen:
  - Moderation der Scrum-Events (Daily Scrum, Sprint Planning, Review, Retrospektive)
  - Beseitigung von Hindernissen, die das Team bei der Arbeit behindern
  - Coaching des Teams in Selbstorganisation und funktionsübergreifender
    Zusammenarbeit 
  - Schaffung eines produktiven Umfelds für hohe Wertschöpfung
  - Abschirmung des Teams vor externen Störungen und Ablenkungen
  - Förderung von Veränderungen, die die Produktivität des Teams erhöhen
- **Entwicklungsteam**: Das Entwicklungsteam hat folgende Eigenschaften:
  - Besteht typischerweise aus 3-9 Personen (optimale Größe für Zusammenarbeit)
  - Ist selbstorganisierend - das Team entscheidet selbst, wie es die Arbeit erledigt
  - Kennt keine Hierarchie oder spezielle Titel innerhalb des Teams
  - Trägt als Ganzes die Verantwortung für das Produktinkrement
  - Arbeitet gemeinsam an den Sprint-Aufgaben
  - Passt seine Arbeitsweise kontinuierlich an die Herausforderungen im Projekt an

### Hilfsmittel zur Steuerung

Zur Überwachung des Projektfortschritts können verschiedene Werkzeuge eingesetzt
werden:
- **Scrum Board**: Ein physisches oder digitales Board, auf dem die Aufgaben
  visualisiert werden. Es zeigt den aktuellen Status der Aufgaben (To Do, In
  Progress, Done).
- **Burndown Chart**: Ein Diagramm, das den verbleibenden Aufwand im Sprint
  darstellt. Es zeigt, wie viel Arbeit noch zu erledigen ist und ob das Team im
  Zeitplan liegt.
- **Velocity**: Eine Kennzahl, die angibt, wie viel Arbeit das Team in einem
  Sprint erledigt hat. Sie wird in Story Points gemessen und hilft, die
  Kapazität des Teams für zukünftige Sprints abzuschätzen.



[^1]: [Agiles Manifest](https://agilemanifesto.org/iso/de/manifesto.html),
    https://agilemanifesto.org/iso/de/manifesto.html, besucht am 4. April 2025