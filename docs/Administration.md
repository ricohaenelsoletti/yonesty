# Administration

## Microsoft Authentication
yonesty mit erhöhtem Sicherheitslevel geht mit einer Authentication. yonesty mag Microsoft.

### Grundkonfiguration in yonesty

1. Standardfunktion für Azure Sync konfigurierenGehe zu Admin - Stammdaten - Funktionen und wähle eine Rolle als Standardfunktion für den Azure Sync.
2. Berechtigungen für neue Benutzer festlegen: Stelle sicher, dass das Berechtigungssystem für neue Benutzer, die durch den Azure Sync hinzugefügt werden, korrekt konfiguriert ist.
Eine Berechtigungsrolle benötigt ebenfalls den Standard für Azure Sync.
3. Azure Einstellungen: Navigiere im Admin-Bereich zu Organisationen - Azure Einstellungen und hinterlege die notwendigen Informationen.
Aktiviere die Authentifizierung in den Azure Einstellungen.


### Einrichtung im Microsoft Admin Center

1. Rufe die notwendigen Daten unter admin.microsoft.com ab und übertrage diese in die entsprechenden Felder.
2. Microsoft Entra Admin Center: Öffne Microsoft Entra und wähle Unternehmensanwendungen.
3. Neue App-Registrierung
4. Gib einen Namen für die neue Registrierung an und wähle „Nur Konten in diesem Organisationsverzeichnis“.

<figure>
    <img src="/screenshots/Microsoft-Graph-Einrichtung-Azure-yonesty-App-Rechte.png">
    <figcaption>Notwendige Berechtigungen</figcaption>
</figure>
6. App-Registrierungen
7. Wähle App-Registrierungen und hinterlege die Umleitungs-URI (Typ = Web) mit der URL: https://[tenant name].yonesty.cloud/oauth/azure/redirect
8. Zertifikate und geheime Clientschlüssel: Erstelle einen neuen geheimen Clientschlüssel, füge eine Beschreibung hinzu und wähle die Gültigkeit aus.
9. Kopiere den Schlüsselwert für die Azure Client ID in yonesty.
10. API-Berechtigungen: Erteile die Administratorzustimmung für deine Domäne.
11. Authentifizierung Web: URL einfügen

### Verknüpfung yonesty x Microsoft
Werte aus Entra übertragen: Kopiere die Werte aus Entra in die entsprechenden Felder im Admin-Bereich der yonesty App:

1. Azure Client ID: Anwendungs-ID (Client)
2. Azure Cloud Instanz: URL der autoritativen Stelle https://login.microsoftonline.com
3. Azure Tenant ID: Verzeichnis-ID (Mandant)
4. Azure Graph-API-Endpunkt: Microsoft Graph-API Endpunkt https://graph.microsoft.com/v1.0/
5. Azure Client ID Secret: Zertifikate Schlüsselwert
