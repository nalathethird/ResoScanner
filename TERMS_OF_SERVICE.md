# Terms of Service - Resonite Log Scanner Bot

**Last Updated:** October 27, 2025

## 1. Acceptance of Terms

By using the Resonite Log Scanner Bot ("the Bot"/"ResoScanner"), you agree to these Terms of Service. If you do not agree, do not use the Bot.

## 2. Description of Service

The Bot provides automated analysis of Resonite game log files to help users identify mod-related issues. The service includes:

- Analyzing uploaded `.log` files
- Detecting loaded mods and mod loaders
- Identifying outdated or problematic mods
- Providing recommendations for mod management
- Cross-referencing with public mod manifests

## 3. User Responsibilities

### 3.1 Appropriate Use
You agree to:
- Only upload your own log files or files you have permission to share
- Use the Bot for legitimate Resonite mod troubleshooting purposes
- Not attempt to abuse, exploit, or overload the Bot's resources
- Not upload malicious files or attempt to compromise the Bot

### 3.2 Rate Limiting
The Bot implements rate limiting to ensure fair access:
- Maximum 3 monitored channels per Discord server, or scan in every channel if not setup
- Reasonable usage of log scanning features
- DM scanning available for all users

### 3.3 Administrator Commands
Server administrators using slash commands acknowledge:
- Channel configuration affects all server members
- Properly configuring monitored channels is their responsibility
- They have authority to manage Bot settings for their server

## 4. Data Processing and Privacy

### 4.1 No Data Storage
**IMPORTANT:** The Bot does NOT store or persist your log files:
- Log files are processed entirely in memory (RAM)
- No logs are saved to disk or external database (Discord is the only exception)
- Log content is immediately discarded after analysis
- Only analysis results (metadata) are stored in Discord messages

### 4.2 Temporary Processing
During analysis, log files are:
- Downloaded from Discord's servers into memory
- Parsed and analyzed in real-time
- Cleared from memory immediately after processing
- Subject to garbage collection to free resources

### 4.3 What We Access
The Bot only accesses:
- Log file contents (temporarily, in memory)
- Discord user IDs and usernames (for message context)
- Discord server/channel IDs (for routing responses)
- Public mod manifest data (from GitHub repositories)

### 4.4 Third-Party Services
The Bot interacts with:
- **Discord API:** For bot functionality
- **GitHub API:** To fetch public mod manifests
- No other external services receive your data

## 5. Intellectual Property

### 5.1 User Content
You retain all rights to log files you upload. By using the Bot, you grant us a temporary, non-exclusive license to process your logs solely for providing the analysis service.

### 5.2 Bot Content
The Bot's code, analysis algorithms, and output formatting are provided as-is. Analysis results and recommendations are suggestions only.

## 6. Disclaimers and Limitations

### 6.1 No Warranty
The Bot is provided "AS IS" without warranty of any kind:
- Analysis results may not be 100% accurate
- MonkeyLoader scanning is curently in the experimental phase and might not work properly
- Mod detection depends on log format
- Recommendations are suggestions, not guarantees

### 6.2 Limitation of Liability
The Bot operator is not liable for:
- Incorrect analysis results
- Mod compatibility issues
- Data loss or corruption
- Service interruptions or downtime
- Decisions made based on Bot recommendations

### 6.3 Third-Party Content
The Bot references third-party mod manifests and repositories. We are not responsible for:
- Accuracy of manifest data
- Availability of linked resources
- Security of third-party mods
- Compatibility of recommended updates

## 7. Experimental Features

### 7.1 MonkeyLoader Support
MonkeyLoader scanning is marked as EXPERIMENTAL because:
- Log format is not formatted for verified mods and/or manifests
- Version information may be incomplete
- Results may not be fully accurate
- The feature is under active development

Users acknowledge these limitations when using MonkeyLoader logs with out service.

## 8. Service Modifications

We reserve the right to:
- Modify or discontinue the Bot at any time
- Update these Terms of Service
- Change feature availability
- Implement additional rate limiting
- Block abusive users or servers

## 9. Privacy and GDPR Compliance

### 9.1 Minimal Data Collection
We collect minimal data necessary for operation:
- Discord IDs (users, channels, servers) - Public information
- Usage statistics (logs analyzed, errors encountered)
- Configuration data (monitored channels per server)

### 9.2 No Personal Information
We do NOT collect:
- Real names or email addresses
- IP addresses
- Location data
- Resonite account information
- Personal data from log files

### 9.3 Data Retention
- **Log files:** NOT stored (zero retention)
- **Configuration:** Stored locally, can be deleted on request
- **Usage statistics:** Aggregate only, no personal data
- **Discord messages:** Subject to Discord's retention policy

### 9.4 User Rights
You have the right to:
- Request deletion of your server's configuration data
- Stop using the Bot at any time
- Report privacy concerns to the Bot operator (please open an [Issue](https://github.com/nalathethird/ResoScanner/issues/new/choose))

## 10. Geographic Restrictions

The Bot operates on a single server for now, but is subject to:
- Discord's Terms of Service
- GitHub's Terms of Service
- Applicable laws in your jurisdiction

## 11. Contact and Support

For questions, concerns, or to report issues:
- Open an [Issue](https://github.com/nalathethird/ResoScanner/issues/new/choose) on the Bot's GitHub repository
- Contact the Bot operator through Discord - (nalathethird)
- Report Terms of Service violations to Discord

## 12. Termination

We may terminate or suspend access to the Bot for:
- Violation of these Terms
- Abusive behavior or spam
- Technical limitations
- Legal requirements

You may stop using the Bot at any time by:
- Removing the Bot from your server
- Stopping DM interactions
- Requesting data deletion via Email - [projectzeia454@gmail.com]

## 13. Changes to Terms

We may update these Terms at any time. Continued use of the Bot after changes constitutes acceptance of new terms.

## 14. Severability

If any provision of these Terms is found invalid, the remaining provisions continue in effect.

## 15. Entire Agreement

These Terms constitute the entire agreement between you and the Bot operator regarding use of the service.

---

**By using the Resonite Log Scanner Bot, you acknowledge that you have read, understood, and agree to these Terms of Service.**
