# Administration

## Microsoft Authentication
yonesty mit erhöhtem Sicherheitslevel geht mit einer Authentication. yonesty mag Microsoft.

### Grundkonfiguration in yonesty

1. Standardfunktion für Azure Sync konfigurieren
    * Gehe zu Admin - Stammdaten - Funktionen und wähle eine Rolle als Standardfunktion für den Azure Sync.
  
2. Berechtigungen für neue Benutzer festlegen:
    *  Stelle sicher, dass das Berechtigungssystem für neue Benutzer, die durch den Azure Sync hinzugefügt werden, korrekt konfiguriert ist.
    *  Eine Berechtigungsrolle benötigt ebenfalls den Standard für Azure Sync.

<figure>
    <img src="/screenshots/yonesty-Administration-Funktion-SetAsStandard.png">
    <figcaption>Notwendiges Setup an der Funktion</figcaption>
</figure>

<figure>
    <img src="/screenshots/yonesty-Administration-Berechtigungen.png">
    <figcaption>Notwendiges Setup an der Berechtigung</figcaption>
</figure>


### Einrichtung im Microsoft Admin Center

Rufe die notwendigen Daten unter admin.microsoft.com ab und übertrage diese in die entsprechenden Felder.
1. Microsoft Entra Admin Center: Öffne Microsoft Entra und wähle Unternehmensanwendungen.
2. Neue App-Registrierung: Gib einen Namen für die neue Registrierung an und wähle „Nur Konten in diesem Organisationsverzeichnis“.

<figure>
    <img src="/screenshots/Microsoft-Graph-Einrichtung-Azure-yonesty-App-Rechte.png">
    <figcaption>Notwendige Berechtigungen</figcaption>
</figure>

3. App-Registrierungen: Wähle App-Registrierungen und hinterlege die Umleitungs-URI (Typ = Web) mit der URL: https://[tenant name].yonesty.cloud/oauth/azure/redirect
4. Zertifikate und geheime Clientschlüssel: Erstelle einen neuen geheimen Clientschlüssel, füge eine Beschreibung hinzu und wähle die Gültigkeit aus.
5. Kopiere den Schlüsselwert für die Azure Client ID in yonesty.
6. API-Berechtigungen: Erteile die Administratorzustimmung für deine Domäne.
7. Authentifizierung Web: URL einfügen

### Verknüpfung yonesty x Microsoft

Navigiere im Admin-Bereich zu Organisationen - Azure Einstellungen und hinterlege die notwendigen Informationen.

1. Azure Client ID: Anwendungs-ID (Client)
2. Azure Cloud Instanz: URL der autoritativen Stelle https://login.microsoftonline.com
3. Azure Tenant ID: Verzeichnis-ID (Mandant)
4. Azure Graph-API-Endpunkt: Microsoft Graph-API Endpunkt https://graph.microsoft.com/v1.0/
5. Azure Client ID Secret: Zertifikate Schlüsselwert
6. Aktiviere die Authentifizierung in den Azure Einstellungen.

