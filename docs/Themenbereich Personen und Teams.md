# Personen und Teams

Personen und Teams bilden die Grundlage für viele Funktionen in yonesty.

Sie verbinden Menschen mit Rollen, Zielen, Prozessen, Fähigkeiten, Feedbacks und Aktivitäten. Deshalb empfiehlt es sich, die Stammdaten möglichst früh vollständig zu pflegen.

## Empfehlung: Microsoft Entra ID / Azure Synchronisation

Der einfachste Weg ist die automatische Synchronisation der Personen aus Microsoft Entra ID (ehemals Azure Active Directory).

Dabei werden vorhandene Benutzerkonten aus Microsoft 365 automatisch nach yonesty übernommen.

Vorteile:

- Keine doppelte Pflege von Benutzerkonten
- Automatische Übernahme von Namen und E-Mail-Adressen
- Aktualisierung bei Änderungen im Microsoft-Tenant
- Grundlage für Single Sign-On (SSO)
- Unterstützung der Microsoft Authentifizierung inklusive MFA

Nach der Synchronisation können die Personen direkt in Rollen, Teams, Zielen, Prozessen und Feedbackgesprächen verwendet werden.

## Personen manuell anlegen

Alternativ können Personen auch manuell angelegt werden.

Dazu navigieren Sie zu:

```text
Administration
→ Stammdaten
→ Personen
```

Anschließend wählen Sie:

```text
+ Person anlegen
```

### Mögliche Stammdaten einer Person

- Vorname
- Nachname
- E-Mail-Adresse
- Status (aktiv / inaktiv)
- Zugeordnete Rollen
- Zugeordnete Teams
- Fähigkeiten
- Ziele
- Feedbackgespräche

## Personen und Rollen

Eine Person kann mehrere Rollen besitzen.

Beispiele:

- Mitarbeiter
- Teamleiter
- Product Owner
- Prozessverantwortlicher
- Geschäftsführer

Die Zuordnung von Rollen kann zeitlich begrenzt werden.

Dadurch lassen sich auch zukünftige oder historische Verantwortlichkeiten nachvollziehen.

## Teams

Teams gruppieren Personen innerhalb einer Organisation.

Ein Team kann beispielsweise sein:

- Vertrieb
- Marketing
- Entwicklung
- HR
- Produktion
- Service

Teams schaffen Transparenz über Zuständigkeiten und erleichtern die Zuordnung von Zielen, Rollen und Prozessen.

## Team anlegen

Navigieren Sie zu:

```text
Administration
→ Stammdaten
→ Teams
```

Anschließend wählen Sie:

```text
+ Team anlegen
```

### Stammdaten eines Teams

- Teamname
- Beschreibung
- Teambesitzer
- Teamleiter
- Zugeordnete Personen
- Zugeordnete Rollen

## Teambesitzer und Teamleiter

Optional kann für jedes Team ein Teambesitzer und ein Teamleiter definiert werden.

Diese Personen dienen als Ansprechpartner für das Team und können beispielsweise Verantwortlichkeiten innerhalb von Prozessen oder Zielen übernehmen.

## Personen im Team verwalten

Nach dem Anlegen eines Teams können Personen hinzugefügt werden.

Eine Person kann Mitglied mehrerer Teams sein.

Dadurch lassen sich auch Matrixorganisationen oder Projektstrukturen einfach abbilden.

## Verwendung in yonesty

Personen und Teams werden in vielen Bereichen von yonesty verwendet:

- Rollen
- Ziele
- Prozesse
- RACI-Matrizen
- Fähigkeiten
- Feedbackgespräche
- Aktivitäten
- Organisationseinheiten

Je vollständiger die Stammdaten gepflegt sind, desto aussagekräftiger werden Auswertungen, Matrizen und die Unterstützung durch Yona.

## Unterstützung durch Yona

Yona nutzt die hinterlegten Personen-, Rollen- und Teaminformationen, um Fragen im organisatorischen Kontext beantworten zu können.

Beispiele:

- Welche Ziele verfolgt mein Team?
- Wer ist für diesen Prozess verantwortlich?
- Welche Fähigkeiten fehlen im Team?
- Welche offenen Aktivitäten betreffen mein Team?
- Welche Rollen sind aktuell unbesetzt?

Dabei berücksichtigt Yona immer die verfügbaren Berechtigungen und zeigt ausschließlich Informationen an, auf die die jeweilige Person zugreifen darf.
