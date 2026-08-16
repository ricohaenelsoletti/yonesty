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

## Berechtigungen und Yona

Yona berücksichtigt immer die vorhandenen Berechtigungen.

Das bedeutet:

Zwei Personen können dieselbe Frage stellen und unterschiedliche Antworten erhalten.

Beispiel:

### Frage

> Welche Ziele sind aktuell gefährdet?

### CEO

Der CEO sieht alle relevanten Unternehmensziele.

### Teamleiter

Der Teamleiter sieht die Ziele seines Teams.

### Mitarbeiter

Der Mitarbeiter sieht nur die für ihn freigegebenen Ziele.

Yona zeigt niemals Informationen an, auf die eine Person keinen Zugriff besitzt.

## Empfohlene Einrichtung

### Beispiel 1: Kleine Organisation

Bis ca. 50 Mitarbeitende

| Rolle | Berechtigung |
|---------|---------|
| Geschäftsführung | Administrator |
| Teamleiter | Teamleiter |
| Mitarbeitende | Standardbenutzer |

Diese Struktur reicht häufig bereits aus.

---

### Beispiel 2: Mittelständisches Unternehmen

100 bis 500 Mitarbeitende

| Funktion | Berechtigung |
|---------|---------|
| CEO | Administrator |
| COO | Administrator |
| Leiter HR | Fachverantwortlicher |
| Prozessmanager | Fachverantwortlicher |
| Teamleiter | Teamleiter |
| Mitarbeitende | Standardbenutzer |

Dadurch können Fachbereiche ihre Daten selbst pflegen, ohne vollständige Administrationsrechte zu erhalten.

---

### Beispiel 3: Organisation mit hoher Compliance

Für Unternehmen mit erhöhten Anforderungen an Datenschutz oder Governance.

| Funktion | Berechtigung |
|---------|---------|
| Systemadministrator | Administrator |
| Head of Risk & Compliance | Fachverantwortlicher |
| Legal Counsel | Fachverantwortlicher |
| Teamleiter | Teamleiter |
| Mitarbeitende | Standardbenutzer |

Hier bleiben sensible Informationen bei den jeweils verantwortlichen Fachbereichen.

## Empfehlungen aus der Praxis

### Wenige Administratoren

Administratoren sollten sparsam vergeben werden.

Empfehlung:

- CEO
- COO
- Systemadministrator

Mehr Administratoren erhöhen die Komplexität und das Risiko unbeabsichtigter Änderungen.

### Verantwortung an Fachbereiche delegieren

Beispiele:

- HR pflegt Personen und Feedbacks
- Prozessmanagement pflegt Prozesse
- Qualitätsmanagement pflegt Standards
- Teamleiter pflegen Teamziele

Dadurch bleiben die Informationen aktuell und fachlich korrekt.

### Teams konsequent nutzen

Berechtigungen sollten möglichst über Teams organisiert werden.

Beispiel:

```text
Team Vertrieb
→ Vertriebsziele
→ Vertriebsprozesse
→ Vertriebsaktivitäten

Team Marketing
→ Marketingziele
→ Marketingprozesse
→ Marketingaktivitäten
```

Das erleichtert die Pflege deutlich.

## Typische Fehler

### Zu viele Administratoren

Häufig erhalten zu viele Personen Vollzugriff.

Folgen:

- fehlende Transparenz
- inkonsistente Stammdaten
- ungewollte Änderungen

### Zu komplexe Berechtigungsstrukturen

Zu viele Sonderfälle erschweren die Administration.

Besser:

- wenige Rollen
- klare Verantwortlichkeiten
- eindeutige Teamstrukturen

### Keine Teamverantwortlichen

Wenn Teams keine Besitzer und Teamleiter besitzen, bleiben Ziele, Prozesse und Aktivitäten häufig ungepflegt.

## Empfehlung für den Start

Für die meisten Organisationen ist folgende Struktur optimal:

```text
Administrator
│
├── Fachverantwortliche
│   ├── HR
│   ├── Prozesse
│   ├── Compliance
│   └── Qualität
│
├── Teamleiter
│
└── Mitarbeitende
```

Diese Struktur ist einfach, nachvollziehbar und unterstützt gleichzeitig die meisten Anwendungsfälle in yonesty.
