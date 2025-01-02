# discordMusicBot

Dies ist ein Discord Music Bot, der Musik auf einem Discord-Server abspielen kann. Der Bot reagiert auf Befehle in einem bestimmten Channel und ermöglicht die Steuerung der Musik sowie die Anzeige von Song-Informationen.

## Voraussetzungen

- Node.js (mindestens Version 16.x)
- Ein Discord-Bot-Token
- Ein Discord-Server (Guild), auf dem der Bot betrieben wird
- Ein Voice-Channel für die Musikwiedergabe
- Ein Text-Channel für die Steuerung des Bots und die Anzeige von Song-Informationen

## Installation

1. **Klonen des Repositories:**

   Klone dieses Repository auf deinen lokalen Rechner:

   ```
   git clone https://github.com/DEIN_USERNAME/discord-music-bot.git
   cd discord-music-bot
   ```

2. **Abhängigkeiten installieren:**

   Stelle sicher, dass du [Node.js](https://nodejs.org/) installiert hast, und führe dann den folgenden Befehl aus, um alle Abhängigkeiten zu installieren:

   ```
   npm install
   ```

3. **Konfiguration:**

   Erstelle eine `config.json`-Datei im Hauptverzeichnis und füge deine spezifischen Einstellungen ein. Weitere Informationen zur Konfiguration findest du weiter unten.

4. **Bot starten:**

   Nachdem du die `config.json` korrekt eingerichtet hast, kannst du den Bot mit folgendem Befehl starten:

   ```
   npm start
   ```

## Konfigurationsdatei (`config.json`)

Die `config.json`-Datei enthält wichtige Einstellungen für deinen Discord Music Bot. Hier werden die Discord-Bot-Token, die Channel-IDs und andere Optionen definiert.

### Beispiel einer `config.json`:

```
{
"clientId": "DEIN_BOT_ID",
"guildId": "DEIN_SERVER_ID",
"voiceChannelId": "DEIN_VOICE_CHANNEL_ID",
"messageChannelId": "DEIN_COMMAND_CHANNEL_ID",
"commandsChannelId": "DEIN_MESSAGE_CHANNEL_ID",
"prefix": "!",
"token": "DEIN_BOT_TOKEN"
}
```

### Erklärung der einzelnen Werte:

- **`clientId`**:
  - **Beschreibung**: Dies ist die Client-ID deines Bots, die beim Erstellen des Bots im [Discord Developer Portal](https://discord.com/developers/applications) zu finden ist.
  - **Beispiel**: `"clientId": "123456789012345678"`
- **`guildId`**:

  - **Beschreibung**: Die ID des Discord-Servers (Guild), auf dem der Bot aktiv sein soll.
  - **Beispiel**: `"guildId": "987654321098765432"`

- **`voiceChannelId`**:

  - **Beschreibung**: Die ID des Voice-Channels, dem der Bot automatisch beitreten soll, wenn er startet.
  - **Beispiel**: `"voiceChannelId": "112233445566778899"`

- **`messageChannelId`**:

  - **Beschreibung**: Die ID des Text-Channels, in dem der Bot auf Befehle reagiert. In diesem Channel empfängt der Bot Befehle wie `!play`, `!skip`, etc.
  - **Beispiel**: `"messageChannelId": "223344556677889900"`

- **`commandsChannelId`**:

  - **Beschreibung**: Die ID des Text-Channels, in dem der Bot Informationen zum aktuellen Song anzeigt, wenn man ihn dort pingt.
  - **Beispiel**: `"commandsChannelId": "334455667788990011"`

- **`prefix`**:

  - **Beschreibung**: Das Präfix, das vor einem Befehl im Text-Channel verwendet wird. Standardmäßig ist es `!`, aber du kannst es auf ein anderes Zeichen oder Wort ändern, je nachdem, wie du den Bot nutzen möchtest.
  - **Beispiel**: `"prefix": "!"`

- **`token`**:
  - **Beschreibung**: Dein Bot-Token, das du im [Discord Developer Portal](https://discord.com/developers/applications) generieren kannst. Dieses Token wird für die Authentifizierung des Bots bei Discord benötigt.
  - **Beispiel**: `"token": "DEIN_BOT_TOKEN"`

> **Wichtig:** Stelle sicher, dass du die tatsächlichen IDs und dein Bot-Token korrekt einfügst, um sicherzustellen, dass der Bot korrekt funktioniert.

## Bot-Befehle

Der Bot reagiert auf die folgenden Befehle:

- **`!play <name_der_.mp3/playlist_ordnername> [-shuffle] [-loop]`**: Spielt einen Song oder eine Playlist ab.
- **`!skip/!next`**: Überspringt den aktuellen Song.
- **`!stop`**: Stoppt die Musikwiedergabe und entfernt den Bot aus dem Voice-Channel.
- **`!addnext/!addlast <name_der_.mp3>`**: Fügt den angegebenen Song der Warteschlange an nächster oder letzter Stelle hinzu.
- **`!current`**: Zeigt den aktuell laufenden Song an.

## Wichtige Hinweise

- Achte darauf, dass der Bot über die richtigen Berechtigungen verfügt, um Nachrichten zu senden, auf Channels zuzugreifen und Musik in Voice-Channels zu spielen.
- Du kannst den Bot anpassen, indem du weitere Funktionen hinzufügst oder Änderungen an der `config.json` vornimmst.
