# Privacy Policy - Resonite Log Scanner Bot

**Last Updated:** October 27, 2025

## Overview

This Privacy Policy explains how the Resonite Log Scanner Bot ("we", "us", "ResoScanner", "the Bot") handles your data. **We are committed to protecting your privacy and do not store your log files.**

## What Data We Process

### 1. Log Files (NOT STORED)
**IMPORTANT: Your log files are NEVER stored or saved.**

When you upload a log file:
- The file is downloaded into the Bot's RAM (memory)
- Analysis is performed in real-time
- The log content is immediately discarded after analysis
- No trace of the log file remains on our systems

**Technical Details:**
- Logs exist only in volatile memory (RAM)
- Memory is cleared immediately after processing
- Garbage collection ensures complete removal
- No disk writes, no database storage, no backups

### 2. Analysis Results (Temporary)
The Bot sends analysis results as Discord messages, which include:
- Detected mod names and versions
- Mod loader type (RML, MonkeyLoader, etc.)
- Resonite version
- Error summaries and recommendations

**Storage:** These messages are stored by Discord according to their privacy policy, not by us.

### 3. Discord Identifiers (Minimal Collection)
We temporarily access:
- **User IDs:** To know who uploaded the log
- **Channel IDs:** To respond in the correct channel
- **Server IDs:** To apply per-server configuration

**Purpose:** Required for basic Bot functionality  
**Storage:** Server configurations stored locally (see below)  
**Retention:** Can be deleted on request

### 4. Server Configuration (Persistent)
Server administrators using `/addlogchannel` create configuration data:
- Server ID (Discord's public identifier)
- List of monitored channel IDs (up to 3 per server)

**Storage:** Stored in `guild_channels.json` on the Bot's host machine  
**Retention:** Until server removes channels or leaves the Bot  
**Deletion:** Automatically deleted when Bot leaves server, or on request

## What Data We DO NOT Collect

We explicitly DO NOT collect, store, or process:
- ❌ Real names or email addresses
- ❌ IP addresses or location data
- ❌ Resonite account credentials
- ❌ Session tokens or authentication data
- ❌ Personal information from log files
- ❌ Chat messages or Discord conversations
- ❌ User behavior or analytics beyond basic usage statistics

## How We Use Data

### Log File Processing
1. User uploads `.log` file to Discord
2. Bot downloads file into RAM
3. Bot analyzes mod data, errors, versions
4. Bot generates analysis results
5. Bot posts results to Discord
6. **Log content is cleared from memory**
7. Garbage collection removes all traces

**Timeline:** Entire process takes 2-5 seconds  
**Storage Duration:** 0 seconds on disk (only in RAM during processing)

### Configuration Management
Server configurations are used to:
- Determine which channels to monitor
- Respect server administrators' preferences
- Limit monitoring to 3 channels per server (rate limiting)

### Public Manifest Access
The Bot accesses public mod manifests from:
- **GitHub:** `resonite-mod-manifest` repository
- **Purpose:** Cross-reference mod versions and updates
- **Data Sent:** None (public read-only access)

## Data Sharing and Third Parties

### Who We Share With
- **Discord:** Required for Bot functionality (Discord Privacy Policy applies)
- **GitHub:** Public API calls to fetch mod manifests (read-only)
- **No one else:** We do not sell, rent, or share data with third parties

### What Gets Shared
- **With Discord:** Analysis results (as message responses)
- **With GitHub:** None (public API, no data sent)
- **With Others:** Nothing

## Data Security

### Technical Safeguards
- **In-Memory Processing:** Logs never touch disk
- **Immediate Disposal:** Content cleared after analysis
- **Secure Connections:** HTTPS for Discord and GitHub APIs
- **Limited Access:** Bot token secured, not exposed
- **No Database:** No persistent storage of sensitive data

### Limitations
While we implement security best practices:
- We rely on Discord's infrastructure security
- GitHub's availability affects manifest access
- Bot host machine must be secured (operator's responsibility)

## Your Rights

### Right to Access
You can request:
- Confirmation of what data we hold (likely none)
- Copy of server configuration data
- Explanation of how your data is processed

### Right to Deletion
You can request:
- Deletion of server configuration data
- Removal of Bot from your server
- Confirmation of data disposal

**How to Request:** Contact Bot operator via Discord or GitHub issues

### Right to Object
You can:
- Stop using the Bot at any time
- Remove Bot from your server
- Decline to upload logs

## Children's Privacy

The Bot does not knowingly collect data from children under 13 (or applicable age in your jurisdiction). Discord's Terms of Service require users to be 13+.

## GDPR Compliance (EU Users)

### Legal Basis for Processing
- **Consent:** By using the Bot, you consent to this processing
- **Legitimate Interest:** Providing log analysis service
- **Minimal Data:** We collect only what's necessary

### Data Controller
The Bot operator is the data controller. Contact information provided in README.md.

### Data Protection Officer
For small-scale operations, a DPO is not required. Contact the Bot operator for privacy concerns.

### Cross-Border Transfers
The Bot may process data across borders:
- Discord's servers (global infrastructure)
- GitHub's servers (global CDN)
- Bot host location (check with operator)

## CCPA Compliance (California Users)

### Categories of Data Collected
- **Identifiers:** Discord user/server/channel IDs (public)
- **Internet Activity:** Log file uploads (not stored)
- **No Sale:** We do not sell personal information

### Your Rights Under CCPA
- Right to know what data is collected
- Right to delete data
- Right to opt-out of sales (N/A - we don't sell data)

## Data Retention

| Data Type | Retention Period |
|-----------|------------------|
| Log File Content | 0 seconds (RAM only) |
| Analysis Results | Per Discord's retention policy |
| Server Configuration | Until removal or Bot departure |
| Usage Statistics | Aggregate only, indefinite |

## Cookies and Tracking

The Bot does NOT use:
- Cookies
- Analytics services
- Advertising networks

## Changes to This Policy

We may update this Privacy Policy to reflect:
- Changes in Bot functionality
- Legal or regulatory requirements
- Best practice improvements

**Notification:** Major changes will be announced in Bot status or documentation.

## International Users

The Bot operates on one server. Your data may be processed:
- Where Discord's servers are located - when you upload an attachment
- Where the Bot's host machine is located

You consent to this processing by using the Bot.

## Contact Us

For privacy questions, concerns, or requests:
- Open an issue on the Bot's GitHub repository
- Contact the Bot operator through Discord
- Email: [projectzeia454@gmail.com]

**Response Time:** We aim to respond within 7 days.

## Legal Compliance

We comply with:
- GDPR (General Data Protection Regulation) - EU
- CCPA (California Consumer Privacy Act) - California
- Discord's Terms of Service and Privacy Policy
- GitHub's Terms of Service and Privacy Policy

## Data Breach Notification

In the unlikely event of a data breach:
- We will notify affected users within 72 hours (GDPR requirement)
- We will describe the nature of the breach
- We will explain steps taken to mitigate harm

**Likelihood:** Very low, as we don't store sensitive data.

## Third-Party Links

Analysis results may include links to:
- GitHub repositories (mod sources)
- Public mod manifests
- Discord channels

**Disclaimer:** We are not responsible for privacy practices of linked sites.

## Your Consent

By using the Resonite Log Scanner Bot, you consent to:
- Processing of log files in memory (not stored)
- Temporary storage of server configuration data
- Access to public Discord identifiers
- This Privacy Policy

## Withdrawal of Consent

You may withdraw consent at any time by:
- Stopping use of the Bot
- Removing Bot from your server
- Requesting data deletion
- Contacting the Bot operator

---

**Summary: We don't store your logs. Period. Your privacy is protected by design.**

**Questions? Contact the Bot operator.**
