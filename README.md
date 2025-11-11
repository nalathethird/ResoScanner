<p align="center">
  <a href="#">
    <img src="https://raw.githubusercontent.com/nalathethird/ResoScanner/main/ResoScannerIcon.png" height="120">
  </a>
</p>

# ResoScanner - A Resonite focused Modded Log Scanner

This README explains the bots intentions and purpose, for [Terms Of Service](https://github.com/nalathethird/ResoScanner/blob/main/TERMS_OF_SERVICE.md) and [Privacy Policy](https://yellowdogman.com/), see their respective .MD's.

### [INVITE ResoScanner!](https://discord.com/oauth2/authorize?client_id=1431852171972051068)

## Features

- **Instant Log Analysis**: Upload your Resonite `.log` file in a configured channel or DM the bot, and get results in seconds.
- **Mod Loader Support**: Detects mods from ResoniteModLoader (RML), MonkeyLoader, BepInEx, and MelonLoader.
- **Error & Warning Detection**: Finds failed mods, errors, and warnings, with severity color-coding in Discord embeds.
- **Outdated Mod Detection**: Checks for outdated mods using the official manifest and provides update links.
- **Version Awareness**: Parses Resonite version from logs, shows how old your build is, and compares to the latest Steam release.
- **Actionable Recommendations**: Provides clear suggestions for fixing detected issues.
- **Privacy-Friendly**: Logs are processed in memory only and never stored.
- **Admin Channel Configuration(Servers Only)**: Use `/addlogchannel`, `/removelogchannel`, and `/listlogchannels` to control where the bot scans for logs.
- **Automatic Status Updates**: Bot status updates when manifest/build info changes.

**(I have several things I would like to do with this bot before an official release or pre-release, including cluster setup, proper InteractionsEndpoints, etc. but Im in a rough spot IRL, and this is hard to do with a short attention span.)**

## Quick Start

1. **Invite the bot** to your Discord server or DM it directly.
2. **Upload your Resonite `.log` file**.
3. **Get instant feedback** on modding issues!

## Configuration

- **Channel Setup**: Use `/addlogchannel` to add a channel for log scanning (admin only). Up to 3 channels per server.
- **Send a `.log` anywhere!**: You can send a log file in any channel or DM, and the bot will respond in the same channel!

## Privacy & Security

- Logs are never stored or shared.
- No user tracking or analytics.
- Only public APIs (Steam, Git/ThunderStore manifests) are accessed.

## Supported Mod Loaders

- ResoniteModLoader (RML)
- MonkeyLoader
- BepInEx
- MelonLoader (rarely used in Resonite, but supported anyway)

#### [TERMS OF SERVICE](https://github.com/nalathethird/ResoScanner/blob/main/TERMS_OF_SERVICE.md)
- Service description
- User responsibilities
- Data processing transparency
- No warranty disclaimers
- GDPR/CCPA compliance
- Experimental features notice

#### [PRIVACY POLICY](https://github.com/nalathethird/ResoScanner/blob/main/PRIVACY_POLICY.md)
- **PRIMARY FOCUS: No log storage**
- Immediate data disposal
- Minimal data collection
- GDPR/CCPA compliance
- User rights explained

### 2. Memory Management & Privacy
**Logs are NEVER stored - direct example from my code:**

```csharp
// Download log into RAM only
string? logContent = await httpClient.GetStringAsync(logFile.Url);

// Analyze immediately
var analysis = await _logParser.AnalyzeLogAsync(logContent);

// Clear content reference
logContent = null;

// Explicit GC for large files
if (logFile.Size > 5MB)
{
    GC.Collect();
    GC.WaitForPendingFinalizers();
}
```

**Privacy guarantees:**
- ✅ No disk writes of log content
- ✅ No database storage
- ✅ No file caching
- ✅ Immediate memory disposal
- ✅ Explicit garbage collection
- ✅ Only analysis results sent to Discord Channel via Direct Message or Server Channel

## Slash Commands Usage - For ADMINS (will not work in DM's)

### Adding a Channel
```
1. Admin goes to desired channel
2. Types: /addlogchannel
3. Bot responds: "Channel added for log scanning!"
4. Logs uploaded here are now scanned and parsed back!
```

### Removing a Channel
```
1. Admin goes to monitored channel
2. Types: /removelogchannel
3. Bot responds: "Deleted dedicated log scanning channel"
4. Channel no longer monitored
```

### Listing Channels
```
1. Admin types: /listlogchannels (in any channel)
2. Bot responds with list of monitored channels
3. Shows count: ex. "2/3 channels"
```

## Credits
- [Resonite](https://resonite.com/) and related assets © [Yellow Dog Man Studios](https://yellowdogman.com/). Used under CC0 license.
- [BepisLoader](https://github.com/ResoniteModding)
- [MonkeyLoader](https://github.com/ResoniteModdingGroup)
- [ResoniteModLoader](https://github.com/resonite-modding-group/)
- Other assets have been modified from their original sources by Nalathethird.
