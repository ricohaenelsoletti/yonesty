# yonesty & Yona meets MCP

**Yona in Claude – Einrichtung Version 1 (API-Token)**

> Stand: November 2026 · yonesty powered by soletti
> Version 1: Anmeldung per API-Token im Request-Header, Yona arbeitet lesend.
> Version 2 (geplant): Benutzeranmeldung mit Authentifizierung und MFA.

---

## Warum MCP mit Claude?

yonesty ist das Navigationssystem für Organisationen: Rollen, Prozesse, Ziele, Fähigkeiten, Teams und Aktivitäten sind dort zu einem lebendigen Modell verbunden. Mit Yona lassen sich diese Zusammenhänge per Frage sichtbar machen.

Über das **Model Context Protocol (MCP)** kommt Yona jetzt dorthin, wo viele ohnehin schon arbeiten: direkt in **Claude**. MCP ist ein offener Standard, über den KI-Assistenten sicher auf Daten und Werkzeuge anderer Systeme zugreifen können. yonesty stellt dafür einen eigenen MCP-Server bereit.

Das bringt dir:

- **Ein Ort für alles:** Du fragst Claude, Claude holt sich die Antworten aus yonesty. Kein Umschalten zwischen Anwendungen.
- **Kontext statt Suche:** „Was steht diesen Monat noch für mich an?“ – Claude verbindet Ziele, Key Results und Aktivitäten zu einer klaren Antwort.
- **Kombinierbar:** In Claude lässt sich yonesty mit anderen Konnektoren und Dokumenten zusammenbringen, etwa für Vorbereitungen von Feedbackgesprächen, Statusberichte oder Workshop-Unterlagen.
- **Deine Rechte gelten auch hier:** Yona sieht in Claude nur die Daten, die du auch als Nutzerin oder Nutzer in yonesty siehst.
- **Transparent und steuerbar:** Der Zugriff läuft über einen persönlichen Token mit Ablaufdatum. In Claude legst du fest, welche Werkzeuge der Konnektor nutzen darf.

**Yona wächst Schritt für Schritt mit:** Zum Start arbeitet Yona lesend. Nach und nach wird Yona zu mehr aktiver Mitarbeit befähigt, zum Beispiel Fortschritte aktualisieren oder Feedbacks hinterlegen.

Yona trifft keine Entscheidungen, sondern hilft Menschen, bessere Entscheidungen zu treffen. **Your next step with honesty.**

---

## Voraussetzungen

- Ein Zugang zu yonesty mit **Admin-Berechtigung** in der Organisation (für Schritt 1 und 2)
- Ein Claude-Konto, in dem benutzerdefinierte Konnektoren hinzugefügt werden können (im Team- oder Enterprise-Plan: Owner, siehe Abschnitt unten)
- Die MCP-URL deiner yonesty-Instanz, z. B. `https://demo.yonesty.cloud/mcp`

---

## Schritt 1: MCP am Nutzer aktivieren (als Admin in yonesty)

1. In yonesty anmelden und den **Admin-Bereich** öffnen.
2. Zu **Personen** wechseln und die gewünschte Person öffnen (Personendetails).
3. Den Reiter **Berechtigungen** wählen.
4. Im Abschnitt **MCP Berechtigung** das Häkchen bei **MCP API aktivieren** setzen.
5. **Speichern**.

<figure>
    <img src="/screenshots/yonesty-MCP-API-aktivieren.png">
    <figcaption>MCP API aktivieren und Token erstellen</figcaption>
</figure>

---

## Schritt 2: API-Token für die Authentifizierung generieren

1. Im selben Abschnitt auf **API Token erstellen oder erneuern** klicken.
2. yonesty zeigt anschließend:
   - die **URL** des MCP-Servers (z. B. `https://demo.yonesty.cloud/mcp`)
   - den **Token**
   - das **Ablaufdatum** des Tokens
3. Mit **API URL in Zwischenablage kopieren** und **API Token in Zwischenablage kopieren** beide Werte übernehmen.

Der Token wird in der KI-Chatanwendung als HTTP-Header **`x-api-token`** angegeben.

> **Wichtig: Der Token ist persönlich.**
> Der Token gehört zu genau einer Person in yonesty. Über diesen Token sieht Yona in Claude **nur die Daten, die diese Person auch als Nutzer in yonesty sieht**. Rollen, Teams und Berechtigungen aus yonesty gelten damit unverändert auch in Claude.
>
> - Behandle den Token wie ein Passwort: nicht in Chats, E-Mails oder Dokumenten weitergeben.
> - Ablaufdatum notieren. Vor Ablauf mit **API Token erstellen oder erneuern** einen neuen Token erzeugen und in Claude aktualisieren.

---

## Schritt 3: „Yona“ als Konnektor in Claude einrichten

1. In Claude die Konnektor-Einstellungen öffnen und **Benutzerdefinierten Konnektor hinzufügen** wählen (im Team- oder Enterprise-Plan über die Organisationseinstellungen, siehe unten).
2. **Name:** z. B. `Yona - Hammer und Nagel`
3. **URL:** die MCP-URL aus Schritt 2, z. B. `https://demo.yonesty.cloud/mcp`
4. **Authentifizierung:** **Keine Anmeldung** wählen (für Server mit API-Schlüssel statt OAuth).
5. **Request-Header:** auf **Header hinzufügen** klicken
   - Name: `x-api-token`
   - Wert: der Token aus Schritt 2
   - **Required** anhaken
6. Konnektor speichern.

<figure>
    <img src="/screenshots/yonesty-MCP-Claude-Konnektor.png">
    <figcaption>Claude Einrichtung mit Web-Konnektor</figcaption>
</figure>

---

## Schritt 4: Berechtigungen für den Konnektor einrichten

Nach dem Hinzufügen zeigt Claude die Werkzeuge (Tools), die der yonesty-MCP-Server bereitstellt. In Version 1 sind das **lesende Werkzeuge**, z. B. für Ziele, Aktivitäten, Rollen, Prozesse, Teams, Fähigkeiten, RACI und News.

In den Konnektor-Einstellungen von Claude legst du je Werkzeug fest, ob Claude es ohne Rückfrage nutzen darf, vorher fragen soll oder es gar nicht nutzen darf.

> **Was Yona sieht, entscheidet yonesty.** Unabhängig von diesen Einstellungen in Claude liefert yonesty nur die Daten, die die Person hinter dem Token auch als Nutzer in yonesty sieht.

---

## Schritt 5: Die Arbeit mit Yona als Assistent kann beginnen

Im Chat den Konnektor aktivieren und einfach losfragen:

- „Guten Morgen Yona, was steht in diesem Monat noch für mich im HR an?“
- „Welche Ziele meines Teams sind aktuell gefährdet?“
- „Welche Prozesse haben keine verantwortliche Rolle?“
- „Welche Fähigkeiten fehlen mir noch für die Rolle Teamleitung?“

<figure>
    <img src="/screenshots/yonesty-MCP-Yona-in-Claude.png">
    <figcaption>Yona in Claude ist ready</figcaption>
</figure>

**Yona in Claude ist ready. Let's get started!**

---

## Für Admins: Bereitstellung im Claude Team- oder Enterprise-Plan

In Claude Team und Enterprise fügt ein **Owner** benutzerdefinierte Konnektoren für die gesamte Organisation hinzu. Mitglieder ohne diese Rolle können selbst keinen benutzerdefinierten Konnektor anlegen.

**Als Owner:**

1. **Organisationseinstellungen → Konnektoren** öffnen.
2. **Hinzufügen** wählen, dann **Benutzerdefiniert** und **Web**.
3. URL, Authentifizierung und Request-Header wie in Schritt 3 eintragen.
4. Mit **Hinzufügen** abschließen.

**Als Mitglied:**

1. **Anpassen → Konnektoren** öffnen.
2. Den Konnektor mit dem Label **Custom** suchen.
3. **Verbinden** klicken und den Konnektor im Chat aktivieren.

> ⚠️ **Wichtig für Version 1 im Team-Plan**
> Die Werte im Request-Header legt der Owner einmalig für den Konnektor fest. **Alle Mitglieder, die diesen Konnektor nutzen, greifen mit demselben Token auf yonesty zu** und sehen damit die Daten der Person, zu der dieser Token gehört.
>
> Für Version 1 heißt das:
> - Für persönliche Nutzung mit eigenen Daten eignet sich Version 1 vor allem für Einzelkonten oder für Pilot- und Demo-Szenarien.
> - Wird ein Konnektor für die ganze Organisation bereitgestellt, sollte der Token zu einem Nutzer gehören, dessen Sicht in yonesty für alle Mitglieder passt.
>
> **Version 2** löst das: Mit der Benutzeranmeldung meldet sich jede Person selbst an, und Yona sieht für jede Person genau ihre eigenen yonesty-Daten.

---

## Ausblick

**Version 2:**
- Anmeldung pro Person über den Login von yonesty (Authentifizierung statt API-Token)
- Absicherung mit Multi-Faktor-Authentifizierung (MFA)

**Yona wird aktiver:**
- Schrittweise mehr Mitarbeit über reines Lesen hinaus, z. B. Fortschritte aktualisieren oder Feedbacks hinterlegen

---

## Weitere Informationen

- yonesty Dokumentation: [docs.yonesty.cloud](https://docs.yonesty.cloud)
- yonesty Website: [yonesty.cloud](https://yonesty.cloud)
- Claude: [Custom Connectors mit Remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)
- Ansprechpartner: Rico Hänel, soletti
