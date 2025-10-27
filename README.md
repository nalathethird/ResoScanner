<p align="center">
  <a href="#">
    <img src="https://raw.githubusercontent.com/nalathethird/ResoScanner/main/ResoScannerIcon.png" height="120">
  </a>
</p>

# ResoScanner
A privatly hosted Discord Bot to Scan Resonite Modded Client logs and parse back a readable format.

This README explains the bots intentions and purpose, for [Terms Of Service](https://github.com/nalathethird/ResoScanner/blob/main/TERMS_OF_SERVICE.md) and [Privacy Policy](https://yellowdogman.com/), see their respective .MD's.

Sadly, I would like to keep this bots code Private for now, until I can fully and cleanly make a well documented bot. 

I have several things I would like to do with this bot before an official release or pre-release, including cluster setup, proper InteractionsEndpoints, etc. but Im in a rough spot IRL, and this is hard to do with a short attention span.

If like to motivate me further, please consider Starting the Repo, or Donating to me on [Kofi](https://ko-fi.com/zeianala)☕

### [INVITE ResoScanner!](https://discord.com/oauth2/authorize?client_id=1431852171972051068)

## Complete Feature List

### Core Functionality
- ✅ Multi-loader support (RML, MonkeyLoader, BepInEx, MelonLoader)
- ✅ Mod Detection and SHA256 verification (via Verified Mod manifest for RML)
- ✅ Outdated mod detection
- ✅ Unverified mod identification
- ✅ Error analysis for Mods

### Channel Configuration
- ✅ Per-server slash commands
- ✅ Max 3 channels per server
- ✅ Admin-only management
- ✅ DM support (for people who dont want a public log shown)

### Privacy & Security
- ✅ RAM-only log processing
- ✅ Immediate data disposal
- ✅ Explicit garbage collection
- ✅ No persistent storage
- ✅ Comprehensive TOS and Detailed Privacy Policy, following GDPR compliance and CCPA compliance

### User Experience
- ✅ Embed shows a image of the Loader they are using
- ✅ Upgrade path for outdated mods via the Verified Mod Manifest on GitHub
- ✅ Actionable recommendations - not a guarenteed fix

### 1. Terms of Service & Privacy Policy

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
**Logs are NEVER stored - example from our code:**

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

**Users can:**
- Configure channels via slash commands
- Upload logs safely (never stored)
- Get instant mod analysis
- Trust privacy guarantees

## Credits
- [Resonite](https://resonite.com/) and related assets © [Yellow Dog Man Studios](https://yellowdogman.com/). Used under CC0 license.
- [BepisLoader](https://github.com/ResoniteModding)
- [MonkeyLoader](https://github.com/ResoniteModdingGroup)
- [ResoniteModLoader](https://github.com/resonite-modding-group/)
