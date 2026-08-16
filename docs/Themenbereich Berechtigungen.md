# Berechtigungen

Berechtigungen steuern, welche Informationen Personen in yonesty sehen, bearbeiten oder verwalten dürfen.

Eine durchdachte Berechtigungsstruktur sorgt dafür, dass Mitarbeitende genau die Informationen erhalten, die sie für ihre Arbeit benötigen, ohne von unnötigen Daten abgelenkt zu werden.

Gleichzeitig stellen Berechtigungen sicher, dass sensible Informationen geschützt bleiben.

## Grundprinzip

In yonesty sollten Berechtigungen möglichst einfach und nachvollziehbar sein.

Als Orientierung gilt:

> So wenig Berechtigungen wie möglich, so viele wie nötig.

Die meisten Organisationen kommen mit wenigen Berechtigungsrollen aus.

## Arten von Berechtigungen

### Administrator

Administratoren verwalten die gesamte Organisation.

Typische Aufgaben:

- Organisation einrichten
- Personen verwalten
- Teams verwalten
- Rollen verwalten
- Prozesse verwalten
- Ziele verwalten
- Berechtigungen vergeben
- Azure Synchronisation konfigurieren

Administratoren können grundsätzlich alle Informationen der Organisation sehen und bearbeiten.

### Teamleiter

Teamleiter verantworten ein oder mehrere Teams.

Typische Aufgaben:

- Teammitglieder betreuen
- Teamziele verfolgen
- Feedbackgespräche durchführen
- Aktivitäten koordinieren
- Fähigkeiten entwickeln

Teamleiter benötigen meistens Zugriff auf:

- das eigene Team
- die Teamziele
- die Teamprozesse
- Feedbacks ihres Teams

### Mitarbeitende

Mitarbeitende besitzen in der Regel die geringsten Berechtigungen.

Typische Aufgaben:

- eigene Ziele verfolgen
- eigene Rollen verstehen
- Feedback geben
- Aktivitäten bearbeiten

Mitarbeitende benötigen normalerweise Zugriff auf:

- ihre eigenen Ziele
- ihre eigenen Rollen
- ihre eigenen Fähigkeiten
- ihre eigenen Aktivitäten
- freigegebene Prozesse

### Fachverantwortliche

Fachverantwortliche besitzen zusätzliche Rechte für bestimmte Themenbereiche.

Beispiele:

- Prozessmanager
- Qualitätsmanager
- HR-Verantwortliche
- Compliance Manager

Diese Personen benötigen Zugriff auf die von ihnen verantworteten Objekte.

<figure>
    <img src="screenshots/yonesty - Berechtigungen.png">
    <figcaption>yonesty Berechtigungen und Möglichkeiten für Rechte und Datenschutz</figcaption>
</figure>

## Yona - unser KI Assistent

Yona berücksichtigt immer die vorhandenen Berechtigungen.

Das bedeutet:

Zwei Personen können dieselbe Frage stellen und unterschiedliche Antworten erhalten.

Beispiel:

### Frage

> Welche Ziele sind aktuell gefährdet?

* Der CEO sieht alle relevanten Unternehmensziele.
* Der Teamleiter sieht die Ziele seines Teams.
* Der Mitarbeiter sieht nur die für ihn freigegebenen Ziele.

Yona zeigt niemals Informationen an, auf die eine Person keinen Zugriff besitzt.
