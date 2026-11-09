# Privacy Policy for Dockium Browser

**Effective Date:** November 8, 2026  
**Last Updated:** November 8, 2026  

At **Dockium**, protecting user privacy is foundational to our design. This Privacy Policy details how data is handled across Dockium's client-side features, including isolated sessions, local email storage, proxy routing, and memory management.

---

## 1. Local-First Architecture & No Cloud Sync

Dockium operates on a **local-first privacy model**:
* **No Account Sync:** Dockium does **not** collect, sync, or back up your browsing history, bookmarks, saved credentials, installed Chrome extensions, or settings to any external cloud infrastructure operated by Dockium.
* **Local Storage:** All preferences, session data, cookies, and local database stores remain exclusively on your Windows device filesystem.

## 2. Feature-Specific Data Handling

### A. Dock Apps & Isolated Sessions
* **Session Partitioning:** Dock Apps execute within isolated browser session containers. Cookies, site storage, and cache partitions for each Dock App instance are stored locally in separate directories on your device.
* **Zero Cross-Tracking:** Session data is never aggregated across isolated instances or uploaded to Dockium servers.

### B. System Tray & Background Notifications
* **Local Unread Badging:** To show unread message badges in the Dock App sidebar and Windows System Tray, Dockium parses notification counts directly from active client-side DOM elements/web APIs.
* **No Telemetry Transmission:** Unread notification counts and active application statuses are calculated strictly on your machine and are never sent to external telemetry servers.

### C. Integrated Email Client (Gmail & Outlook)
* **Local Credentials & Tokens:** OAuth tokens, login sessions, email metadata, and message contents are fetched directly between your device and your email provider's servers (Google / Microsoft).
* **Local Offline Storage:** Downloaded emails and drafts for offline usage are cached locally on your device's hard drive using local database encryption.
* **Zero Proxy/Relay:** Email traffic is never routed through Dockium servers. We cannot read, analyze, process, or sell your email contents.

### D. Rust Adblocker
* **On-Device Filtering:** Adblocking rules are compiled and executed locally using a high-performance Rust engine. Block decision logic occurs entirely on your device.
* **No URL Logging:** Dockium does not record, log, or transmit the URLs of web requests evaluated or blocked by the adblock engine.

### E. Tor Network & Custom Proxy Routing
* **Zero Destination Logs:** When routing web traffic through Tor or custom proxies (globally or per-site), requests are encrypted and dispatched through the selected relays/nodes. Dockium does not track your destination IP addresses, DNS queries, or browsing destinations.
* **Exit Country Preferences:** Your chosen exit country rules and per-site proxy configurations are saved locally in your browser preferences.

### F. PowerSleep (Tab Hibernation)
* **Local Process Termination:** When a tab reaches your configured inactivity timeout, its system process is suspended locally to reduce system RAM consumption. The lightweight "husk tab" stores the tab URL locally to facilitate reloading upon user interaction. No browser state is shared externally.

### G. Chrome Extensions
* **Third-Party Extensions:** Extensions installed from the Chrome Web Store run locally within your browser. Extensions may have their own data collection practices governed by their respective privacy policies.

## 3. Data Sharing and Disclosure

Because Dockium does not collect your browsing history, email contents, or network traffic logs, **we do not sell, rent, trade, or monetize your personal data.**

We only disclose data in the following rare scenarios:
* **Legal Requirements:** If required by a valid law enforcement order targeting our corporate entities, we can only provide data that is actually in our possession (which is limited to basic support emails sent to us directly). We cannot provide browsing histories, email stores, or proxy logs, as we do not possess them.

## 4. Security
Dockium leverages Chromium's sandbox model alongside Windows security primitives to protect isolated sessions and encrypted local storage. However, overall system security also relies on maintaining the security of your Windows operating system and device.

## 5. Your Data Control & Deletion
You retain complete control over your data directly within Dockium:
* **Clear Data:** You can clear cookies, isolated session storage, and cache per Dock App or globally at any time via Browser Settings.
* **Email Accounts:** Removing an email account from the sidebar client immediately purges associated local database caches and tokens from your drive.
* **App Removal:** Uninstalling Dockium removes stored local binaries and profile folders according to standard Windows uninstallation routines.

## 6. Policy Updates
We may update this Privacy Policy from time to time to reflect software updates or legal changes. Updates will be reflected by the "Last Updated" date at the top of this document.

## 7. Contact Us
For questions regarding this Privacy Policy or privacy practices within Dockium, please contact:  
**Email:** privacy@dockium.com
