# Privacy Policy for Chemistry Bonding Simulator

**Effective Date:** January 1, 2026  
**Last Updated:** December 1, 2025  
**Version:** 1.0  
**Extension Version:** 0.0.014

---

## Table of Contents

1. [Our Commitment to Your Privacy](#our-commitment-to-your-privacy)
2. [Introduction](#introduction)
3. [Information We Collect](#information-we-collect)
4. [How We Use Information](#how-we-use-information)
5. [Data Storage and Security](#data-storage-and-security)
6. [Data Sharing and Third Parties](#data-sharing-and-third-parties)
7. [Permissions Explained](#permissions-explained)
8. [Your Rights and Controls](#your-rights-and-controls)
9. [Children's Privacy](#childrens-privacy)
10. [Data Retention and Deletion](#data-retention-and-deletion)
11. [International Data Transfers](#international-data-transfers)
12. [Changes to This Policy](#changes-to-this-policy)
13. [Legal Compliance](#legal-compliance)
14. [Contact Information](#contact-information)

---

## Our Commitment to Your Privacy

**We do not sell, rent, trade, or monetize your data in any way. Period.**

Chemistry Bonding Simulator is an educational tool created to enhance learning, not to collect personal information or track users. Every design decision prioritizes your privacy and data security.

---

## Introduction

### What is Chemistry Bonding Simulator?

Chemistry Bonding Simulator ("the Extension", "we", "our") is a Google Chrome browser extension that provides interactive chemistry learning experiences while you watch educational videos on YouTube. The Extension creates overlays with molecular building challenges, quizzes, and visual demonstrations synchronized to specific video timestamps.

### Purpose of This Policy

This Privacy Policy explains:
- What data the Extension collects (minimal)
- How data is stored and used (locally only)
- Your rights regarding data control (complete)
- Our commitment to never selling or sharing your data

### Scope

This policy applies to:
- The Chrome Extension "Chemistry Bonding Simulator"
- All features and functionalities within the Extension
- All versions of the Extension available through the Chrome Web Store

---

## Information We Collect

### 1. Data We Actively Store Locally

The Extension stores the following data **exclusively on your local device** using Chrome's `chrome.storage.local` API:

#### A. Challenge Performance Data
**What We Store:**
- Challenge scores (numerical values, e.g., 50 points)
- Challenge completion status (completed: true/false)
- Time taken to complete challenges (in seconds)
- Challenge type (quiz, experiment, demonstration)
- Challenge activity subtype (bonding, multiple-choice, atom-visualization, etc.)
- Challenge identifier (e.g., "water_challenge", "quiz_name")
- YouTube video ID where challenge occurred (e.g., "RQRmNdQVucE")
- Timestamp when score was recorded (ISO 8601 format)
- Reason for failure if applicable (e.g., "Time's up!", "Challenge skipped")

**Example of Stored Data:**
```json
{
  "videoId": "RQRmNdQVucE",
  "challengeId": "water_challenge",
  "type": "experiment",
  "activityType": "experiment",
  "subtype": "bonding",
  "score": 85,
  "timeElapsed": 32,
  "completed": true,
  "autoDetected": true,
  "timestamp": "2026-01-15T14:32:01.234Z"
}
```

**Why We Store This:**
- To display your learning progress in the Extension popup
- To show your recent scores and achievements
- To help you track your improvement over time

**What We Do NOT Store:**
- Your name or personal identity
- Your email address or contact information
- Your Google account information
- Your browsing history beyond the specific video where you completed challenges
- Any demographic information (age, location, gender, etc.)

#### B. User Settings
**What We Store:**
- Auto-pause preference (boolean: true/false)
  - Controls whether the video automatically pauses when you fail a challenge

**Example of Stored Data:**
```json
{
  "settings": {
    "autoPauseOnFail": true
  }
}
```

**Why We Store This:**
- To remember your preferences across browser sessions
- To provide a personalized learning experience

### 2. Data We Process Temporarily (Not Stored)

The Extension temporarily processes the following data **in your browser's memory only** (this data is never written to disk or transmitted):

#### A. Video Context Information
- Current YouTube video ID (extracted from URL)
- Current video timestamp (seconds elapsed)
- Video element status (playing/paused)

**Why We Process This:**
- To determine when to trigger educational challenges
- To synchronize challenges with video content
- To pause/resume video playback during challenges

**Data Lifecycle:**
This data exists only while you're on a YouTube video page and is immediately cleared when you:
- Navigate to a different page
- Close the tab
- Refresh the page

#### B. Challenge State Information
- Current atoms displayed on screen (type, position, velocity)
- Chemical bonds formed between atoms
- Valence electrons being rendered
- Challenge timer countdowns
- Selected quiz answer indices
- Challenge activation flags

**Why We Process This:**
- To render interactive chemistry simulations
- To validate molecular structures you create
- To enforce challenge time limits
- To determine correct/incorrect answers

**Data Lifecycle:**
This data is cleared:
- When you complete or skip a challenge
- When you navigate away from the video
- When the Extension is disabled or reloaded

#### C. Configuration Data
- Challenge definitions from `videoMappings.json`
  - Video IDs, challenge types, timestamps, questions, answers, target molecules
  - This file is bundled with the Extension and contains no user data

**Why We Process This:**
- To know which challenges to present for each video
- To validate your answers and molecular structures
- To calculate scores based on predefined criteria

### 3. Data We Do NOT Collect

We explicitly **do not collect, store, or transmit**:

❌ Personal identification information (name, email, phone, address)  
❌ Google account information or YouTube user data  
❌ Complete browsing history or visited URLs  
❌ Search queries or video watch history  
❌ IP addresses or device identifiers  
❌ Location data (GPS, city, country)  
❌ Demographic information (age, gender, education level)  
❌ Financial information or payment details  
❌ Social media profiles or connections  
❌ Device information (hardware specs, OS version)  
❌ Cookies or tracking identifiers  
❌ User behavior analytics or telemetry  
❌ Keystroke logging or form data  
❌ Screenshots or screen recordings  
❌ Audio or video captured from your device  
❌ Files or documents from your computer  

---

## How We Use Information

### Local Processing Only

**All data processing occurs entirely on your device.** The Extension does not have any backend servers, databases, or cloud infrastructure. There are no network requests to external APIs (except loading the Extension files from Chrome's servers during installation).

### Specific Use Cases

#### 1. Displaying Your Progress
- **Data Used:** Challenge scores, completion status, timestamps
- **Purpose:** Show your recent performance in the Extension popup
- **Visibility:** Only visible to you in your browser
- **Example:** "Recent Scores" section showing your last 5 challenge attempts

#### 2. Personalizing Experience
- **Data Used:** User settings (auto-pause preference)
- **Purpose:** Remember your preferences across sessions
- **Example:** If you disabled auto-pause, video continues playing after failed challenges

#### 3. Challenge Synchronization
- **Data Used:** Video timestamp, video ID, challenge mappings
- **Purpose:** Trigger the right challenge at the right time
- **Example:** At 52 seconds in video "RQRmNdQVucE", spawn the water molecule challenge

#### 4. Validating Chemistry
- **Data Used:** Atom positions, bond connections, target molecule definitions
- **Purpose:** Determine if you've correctly built the target molecule
- **Example:** Check if you've bonded 2 hydrogens to 1 oxygen to form H₂O

#### 5. Calculating Scores
- **Data Used:** Time taken, challenge difficulty, scoring criteria
- **Purpose:** Award points based on speed and accuracy
- **Example:** Base score 100 + time bonus 15 = 115 points for quick completion

---

## Data Storage and Security

### Storage Location

**Chrome Local Storage:**
All persistent data is stored using Chrome's `chrome.storage.local` API, which:
- Stores data only on your device
- Is isolated per Chrome profile (other users on your computer cannot access it)
- Persists until you clear browser data or uninstall the Extension
- Has no storage quota limits for extensions (unlike `localStorage`)

**File System Path (Approximate):**
- **Windows:** `%LOCALAPPDATA%\Google\Chrome\User Data\Default\Local Extension Settings\[extension-id]`
- **macOS:** `~/Library/Application Support/Google/Chrome/Default/Local Extension Settings/[extension-id]`
- **Linux:** `~/.config/google-chrome/Default/Local Extension Settings/[extension-id]`

**Note:** You don't need to know these paths; Chrome manages this data automatically.

### Security Measures

#### 1. No Network Transmission
- The Extension makes **zero network requests** after installation
- No data leaves your device
- No external APIs or servers are contacted
- No third-party analytics services (Google Analytics, etc.)

#### 2. Manifest V3 Security
The Extension uses Chrome's latest Manifest V3 architecture, which provides:
- Stricter permission controls
- Service worker isolation
- Content Security Policy (CSP) enforcement
- No remote code execution

#### 3. Minimal Permissions
The Extension requests only essential permissions:
- `activeTab`: Interact with the current tab only
- `scripting`: Inject educational overlays
- `storage`: Save scores locally
- `host_permissions`: Work on YouTube.com

**No Dangerous Permissions:**
- ❌ No `webRequest` (cannot intercept network traffic)
- ❌ No `cookies` (cannot read authentication data)
- ❌ No `history` (cannot access browsing history)
- ❌ No `geolocation` (cannot track location)
- ❌ No `clipboardRead` (cannot read clipboard)

#### 4. Code Transparency
- All Extension code is included in the Chrome Web Store package
- No obfuscated or minified code (human-readable JavaScript)
- No external script loading
- Open for inspection by security researchers

### Data Encryption

**At Rest:**
- Chrome encrypts local storage data using your operating system's encryption mechanisms
- On Windows: Data Protection API (DPAPI)
- On macOS: Keychain integration
- On Linux: System keyring integration

**In Transit:**
- Not applicable (no data transmission)

---

## Data Sharing and Third Parties

### Zero Data Sharing

**We do not share, sell, rent, trade, or transfer your data to any third parties. Ever.**

This includes:
- No sharing with advertisers
- No sharing with analytics companies
- No sharing with educational institutions
- No sharing with research organizations
- No sharing with parent companies or subsidiaries (we have none)
- No sharing with government agencies (except under valid legal compulsion, see Legal Compliance)

### Third-Party Services

#### YouTube.com
**Relationship:**
The Extension operates on YouTube's website to provide educational overlays.

**Data Exchange:**
- **From YouTube to Extension:** The Extension reads the video ID from the URL and current timestamp from the video player (publicly available information)
- **From Extension to YouTube:** None. The Extension does not send any data to YouTube's servers

**YouTube's Privacy Policy:**
When you use YouTube, YouTube's own privacy policy applies to data YouTube collects. The Extension does not modify or interfere with YouTube's data collection. Please review YouTube's privacy policy at: https://www.youtube.com/privacy

#### Chrome Web Store
**Relationship:**
The Extension is distributed through Google's Chrome Web Store.

**Data Exchange:**
- **Installation:** When you install the Extension, Google knows you installed it (part of Chrome's normal operation)
- **Updates:** Chrome checks for Extension updates automatically
- **Reviews:** If you leave a review on the Web Store, Google collects that data per their policies

**Google's Privacy Policy:**
Google's privacy policy governs data collected through Chrome and the Web Store: https://policies.google.com/privacy

### No Embedded Third-Party Code

The Extension does **not** include:
- ❌ Third-party analytics SDKs (Google Analytics, Mixpanel, etc.)
- ❌ Advertising networks or trackers
- ❌ Social media widgets (Facebook, Twitter, etc.)
- ❌ Payment processors
- ❌ Customer support chat widgets
- ❌ Error reporting services (Sentry, Rollbar, etc.)
- ❌ A/B testing frameworks
- ❌ Content Delivery Networks (CDNs) for runtime code

All code is bundled with the Extension at installation time.

---

## Permissions Explained

The Extension requests the following Chrome permissions. Here's exactly what each permission allows and why it's necessary:

### 1. `activeTab`
**What it allows:**
- Read and modify the current tab when you click the Extension icon
- Inject content scripts into the active tab

**Why we need it:**
- To add hydrogen and oxygen atoms when you click "Add H" or "Add O" buttons in the popup
- To display the interactive chemistry simulator overlay on YouTube

**What we do NOT do:**
- Access tabs in the background
- Read data from tabs you're not actively using
- Track which tabs you have open

**Technical details:**
This is a "transient permission" that only grants access to the current tab, and only while you're interacting with the Extension popup.

### 2. `scripting`
**What it allows:**
- Inject JavaScript and CSS files into web pages
- Execute scripts programmatically

**Why we need it:**
- To load the chemistry simulator code (content.js, challenge modules, CSS styles)
- To render atoms, bonds, and challenges on YouTube pages
- To create the interactive overlays and animations

**What we do NOT do:**
- Inject scripts into non-YouTube pages
- Modify page content unrelated to educational challenges
- Inject tracking or advertising scripts

**Technical details:**
All injected scripts are included in the Extension package and reviewed by Chrome Web Store during approval.

### 3. `storage`
**What it allows:**
- Save data using `chrome.storage.local` API
- Read previously saved data

**Why we need it:**
- To save your challenge scores and performance history
- To remember your settings (auto-pause preference)
- To display your progress in the Extension popup

**What we do NOT do:**
- Access Chrome's cookie storage
- Read data from other extensions
- Sync data to Google's cloud servers (we don't use `chrome.storage.sync`)

**Technical details:**
Data is stored locally only. Maximum storage is unlimited for extensions (vs. 10MB for `localStorage`).

### 4. `host_permissions: <all_urls>`
**What it allows:**
- Run content scripts on all websites

**Why we need it:**
- To work on any YouTube video URL (youtube.com/watch?v=...)
- To potentially support other educational video platforms in the future

**Why the broad permission:**
YouTube video URLs are dynamic and unpredictable. We cannot specify individual URLs in advance.

**What we actually do:**
- The Extension only activates on `youtube.com/watch` pages
- Content scripts check `window.location.hostname === 'www.youtube.com'` before running
- No functionality is activated on other websites

**What we do NOT do:**
- Access your banking websites, email, or social media
- Read passwords or form data from other sites
- Inject ads or modify content on non-YouTube pages

**Future commitment:**
If we add support for other video platforms (e.g., Vimeo, educational sites), we will:
1. Update this Privacy Policy
2. Notify users via Chrome Web Store update notes
3. Restrict host permissions to only those specific domains if possible

---

## Your Rights and Controls

### Complete Data Ownership

You have **absolute control** over your data because it's stored only on your device.

### Your Rights

#### 1. Right to Access
**What it means:** You can view all data the Extension has stored.

**How to exercise:**
- Open Chrome DevTools (F12 or Right-click → Inspect)
- Go to Application tab → Storage → Local Storage → Extension ID
- Or use Chrome's storage viewer: `chrome://extensions/` → Chemistry Bonding Simulator → Inspect views → background page (if available)

**Programmatic access:**
```javascript
chrome.storage.local.get(null, (data) => {
  console.log('All stored data:', data);
});
```

#### 2. Right to Deletion
**What it means:** You can delete all data at any time.

**How to exercise:**
- **Method 1:** Clear via Chrome Settings
  - `chrome://settings/content/all` → Search for Extension → Clear data
- **Method 2:** Clear via DevTools
  - Application tab → Storage → Local Storage → Right-click → Clear
- **Method 3:** Uninstall Extension
  - Removes all data automatically

**Programmatic deletion:**
```javascript
chrome.storage.local.clear(() => {
  console.log('All data deleted');
});
```

#### 3. Right to Export
**What it means:** You can export your scores to keep a copy.

**How to exercise:**
- Use DevTools as described in "Right to Access"
- Copy the JSON data
- Save to a text file

**Future feature:**
We may add an "Export Scores" button to the Extension popup in future versions.

#### 4. Right to Disable
**What it means:** You can stop the Extension at any time without losing your Chrome installation or other extensions.

**How to exercise:**
- `chrome://extensions/` → Toggle off Chemistry Bonding Simulator
- Or uninstall: `chrome://extensions/` → Remove

**Effect:**
- Content scripts will no longer run on YouTube
- Stored data remains on device until explicitly cleared
- You can re-enable the Extension later without data loss

#### 5. Right to Object
**What it means:** You can object to specific functionality.

**How to exercise:**
- Disable the Extension (stops all functionality)
- Provide feedback via Chrome Web Store reviews
- Contact us via the contact information below

**Limitations:**
The Extension has minimal optional features. Most functionality is core to its purpose (displaying chemistry challenges). You cannot selectively disable data storage without disabling the Extension entirely.

### Data Portability

**Export Format:** JSON (industry-standard, human-readable)

**Compatibility:** Data exported from the Extension can be:
- Viewed in any text editor
- Parsed by any JSON-compatible software
- Imported into spreadsheets (Excel, Google Sheets)
- Used for personal record-keeping

**No lock-in:** Your data is not in a proprietary format. You're never dependent on the Extension to access your scores.

---

## Children's Privacy

### COPPA Compliance

The Extension complies with the Children's Online Privacy Protection Act (COPPA).

**Age requirement:** None. The Extension can be used by individuals of all ages, including children under 13.

**Why we can make this claim:**
- COPPA restricts **collection** of personal information from children under 13
- The Extension does not collect personal information (as defined by COPPA) from users of any age
- No name, address, email, phone number, social security number, or geolocation is collected
- No persistent identifiers used for tracking across websites

**Data collected from children:**
The Extension stores the same minimal data for all users regardless of age:
- Challenge scores (not personally identifiable)
- Settings preferences (not personally identifiable)

**Parental controls:**
- Parents can view all stored data using the methods described in "Your Rights and Controls"
- Parents can delete data or uninstall the Extension at any time
- No parental consent is required because no personal information is collected

**Educational context:**
The Extension is designed for educational use in:
- Schools and classrooms
- Homeschooling environments
- Independent learning by students

Teachers and parents can supervise usage by:
- Monitoring which YouTube videos students access
- Reviewing stored scores in the Extension popup
- Using Chrome's supervised user features

### FERPA Considerations

For educators in the United States:

The Extension does not create "education records" under the Family Educational Rights and Privacy Act (FERPA) because:
- Scores are stored locally on each student's device
- No centralized database of student performance exists
- Schools do not transmit student data to us (we receive nothing)
- Teachers cannot access student scores remotely

**Recommendation for schools:**
If you use the Extension in a classroom setting and want to track student progress:
- Students can manually share their scores with you
- Use separate assessment tools for official grading
- Treat Extension scores as informal practice, not official records

---

## Data Retention and Deletion

### How Long We Store Data

**Persistent storage:**
- Challenge scores and settings are stored **indefinitely** on your device
- Data persists until you manually delete it or uninstall the Extension

**Why indefinite storage:**
- To allow you to track long-term learning progress
- To preserve your settings across browser restarts
- You have complete control to delete data at any time (see "Your Rights and Controls")

**No automatic deletion:**
The Extension does not automatically delete old scores. If you want to remove old data:
- Use `chrome.storage.local.clear()` in DevTools
- Or uninstall and reinstall the Extension

### What Happens When You Uninstall

**Immediate effects:**
1. Extension code is removed from Chrome
2. Content scripts stop running on YouTube
3. Extension icon disappears from toolbar
4. All stored data (scores, settings) is deleted from `chrome.storage.local`

**What is NOT deleted:**
- YouTube watch history (managed by YouTube, not us)
- Chrome browsing history (managed by Chrome, not us)

**Reinstallation:**
If you reinstall the Extension:
- You start with a blank slate (no scores)
- Previous data cannot be recovered
- Settings reset to defaults

### Data Backup

**Our responsibility:**
We do not back up your data to any servers. It exists only on your device.

**Your responsibility:**
If you want to preserve your scores before uninstalling:
1. Export data via DevTools (see "Right to Export")
2. Save the JSON to a file
3. After reinstalling, you could theoretically re-import by pasting into `chrome.storage.local` (advanced users)

**No cloud sync:**
The Extension does not use `chrome.storage.sync`, so your scores are **not** synchronized across devices. Each device has its own independent score history.

---

## International Data Transfers

### No Cross-Border Data Transfers

**All data stays on your device.** There are no data transfers, period.

**Why this section exists:**
Regulations like GDPR require privacy policies to disclose international data transfers. For transparency:

**Transfers that DO occur:**
1. **Extension installation:** When you install from the Chrome Web Store, Google's servers (which may be in various countries) deliver the Extension code to your device.
   - This is governed by Google's privacy policy, not ours
   - Only Extension code is transferred, not your personal data

2. **YouTube usage:** When you watch YouTube videos, YouTube's servers (global CDN) deliver video content.
   - This is governed by YouTube's privacy policy, not ours
   - The Extension does not initiate or modify these transfers

**Transfers that DO NOT occur:**
- ❌ The Extension does not send your scores to servers in any country
- ❌ The Extension does not send data to us (we have no servers)
- ❌ The Extension does not use cloud storage services

### GDPR Compliance (EU Users)

**Legal basis for processing:**
- **Consent:** By installing the Extension, you consent to local storage of scores
- **Legitimate interest:** Processing challenge data is necessary to provide the educational service you requested

**Data controller:**
You are effectively the data controller of your own data because it's stored on your device and you have complete control.

**Data processor:**
We (the Extension developers) do not act as a data processor because we do not process your data on our systems.

**Your GDPR rights:**
All GDPR rights (access, rectification, erasure, restriction, portability, objection) are fulfilled by the controls described in "Your Rights and Controls."

**EU Representative:**
Not required because we do not process personal data of EU users outside their own devices.

### CCPA Compliance (California Users)

**Sale of personal information:**
We do **not** sell personal information. (We don't collect it in the first place.)

**Categories of personal information collected:**
- None (challenge scores are not "personal information" under CCPA because they cannot reasonably identify you)

**Right to know:**
See "Your Rights and Controls" → "Right to Access"

**Right to delete:**
See "Your Rights and Controls" → "Right to Deletion"

**Right to opt-out of sale:**
Not applicable (we don't sell data)

**Non-discrimination:**
Not applicable (we don't provide tiered services based on data collection)

---

## Changes to This Policy

### Notification of Changes

**How we notify you:**
1. **Version number update:** The version number at the top of this policy will increment
2. **Chrome Web Store updates:** Changes will be described in update notes when you update the Extension
3. **In-Extension notice:** Future versions may display a notification if privacy practices change materially

**What constitutes a "material change":**
- Collecting new types of data
- Sharing data with third parties (currently never happens)
- Using data for new purposes
- Changing data storage location (e.g., moving to cloud storage)

**What does NOT constitute a material change:**
- Clarifying existing language
- Adding more detail to existing disclosures
- Fixing typos or grammatical errors
- Updating contact information

### Version History

**Current version:** 1.0 (December 1, 2025)
- First comprehensive privacy policy
- Extensive detail on data handling
- Commitment to zero data sales through January 2026 and beyond

**Previous versions:**
- Version 0.0.1 (November 18, 2025) - Initial brief policy

### Your Continued Use

**Acceptance of changes:**
By continuing to use the Extension after a policy update, you accept the updated terms.

**Objection to changes:**
If you disagree with a policy change:
1. Discontinue use of the Extension
2. Uninstall the Extension
3. Your data will be deleted upon uninstallation

---

## Legal Compliance

### Law Enforcement Requests

**Current situation:**
Because we do not collect or store any user data on our servers, we have nothing to provide to law enforcement.

**Hypothetical scenario:**
If law enforcement requests data about your Extension usage:
- We cannot provide it (we don't have it)
- They would need to request data from you directly or obtain your device
- Local data on your device may be accessible via lawful search warrants executed on your device

**Transparency:**
If we ever receive law enforcement requests, we will:
- Review requests for legal validity
- Notify affected users if legally permitted
- Publish transparency reports if requests become common

**No NSL or FISA orders:**
We have never received a National Security Letter or Foreign Intelligence Surveillance Act order. (We wouldn't have data to provide anyway.)

### Terms of Service Compliance

**YouTube's Terms:**
The Extension respects YouTube's Terms of Service by:
- Not downloading videos
- Not blocking ads (we don't interact with ad elements)
- Not automating actions (user interaction required)
- Only overlaying educational content

**Chrome Web Store Policies:**
The Extension complies with Chrome Web Store Developer Program Policies by:
- Using permissions only for stated purposes
- Not including malicious code
- Maintaining a clear privacy policy (this document)
- Not engaging in keyword stuffing or misleading metadata

### Warranty Disclaimer

**AS-IS BASIS:**
The Extension is provided "as is" without warranties of any kind.

**No liability for data loss:**
While we strive to preserve your locally stored scores, we are not liable for data loss due to:
- Browser crashes
- Operating system updates
- Storage corruption
- User error (accidental deletion)
- Device theft or damage

**Backup recommendation:**
Export your scores periodically if they're important to you (see "Right to Export").

---

## Contact Information

### How to Reach Us

**For privacy questions:**
- Email: [To be added - please provide a contact email]
- Chrome Web Store Support: [Via Extension listing page]

**For bug reports or technical issues:**
- Chrome Web Store Reviews: Leave a detailed review
- [GitHub repository if public]

**For legal inquiries:**
- [To be added - legal contact if applicable]

**Response time:**
We aim to respond to privacy inquiries within 7 business days. Please note that this Extension is a small educational project, and we may not have dedicated support staff.

### Supervisory Authority (EU Users)

If you're in the European Union and believe your data protection rights have been violated, you have the right to lodge a complaint with your national data protection authority.

**Note:** Because we don't process your data on our servers, any complaint would likely pertain to Chrome's or YouTube's handling of data, not the Extension itself.

---

## Acknowledgments

This privacy policy was written with care to be:
- **Comprehensive:** Covering all aspects of data handling
- **Transparent:** Explaining exactly what happens to data
- **Accessible:** Using plain language, not legal jargon
- **Honest:** No hidden data collection or misleading claims

We believe users deserve to know exactly how extensions work. If anything in this policy is unclear, please contact us.

---

## Summary for Quick Reference

**What we collect:**
- Challenge scores (numbers)
- Settings (auto-pause yes/no)

**Where it's stored:**
- Your device only (Chrome local storage)

**Who can access it:**
- Only you

**What we do with it:**
- Display your progress in the Extension popup
- Nothing else

**What we DON'T do:**
- ❌ Sell data
- ❌ Share data with third parties
- ❌ Send data to our servers (we have no servers)
- ❌ Track you across websites
- ❌ Collect personal information

**Your control:**
- ✅ View all data anytime
- ✅ Delete all data anytime
- ✅ Export data anytime
- ✅ Uninstall anytime

**Our promise:**
We will never sell your data. This commitment is unconditional and permanent.

---

**End of Privacy Policy**

**Policy Valid Through:** January 31, 2026 (and beyond)  
**Next Review Date:** January 1, 2026 or upon material changes  
**Questions?** See Contact Information section above.

---

*This privacy policy was prepared with reference to best practices from GDPR, CCPA, COPPA, and Chrome Web Store requirements. It represents our good-faith commitment to user privacy and transparency.*
