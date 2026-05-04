# iOS Fitness App — Getting Started Plan
## Process, Costs & Requirements

---

## 1. Hardware Requirements

### A Mac is mandatory
Apple requires Xcode to build and submit iOS apps, and Xcode only runs on macOS.

| Option | Cost | Notes |
|---|---|---|
| MacBook Air M2/M3 | £1,099–£1,299 | Best value, plenty of power for development |
| MacBook Pro M3 | £1,699+ | Only needed for heavy workloads |
| Mac Mini M2 | £599 | Cheapest option — needs separate monitor/keyboard |
| Second-hand Mac (M1+) | £500–£800 | M1 or later recommended |

> If you already own a Mac running macOS Ventura (13) or later, you're good to go.

### iPhone for testing
- Any modern iPhone works
- You can use the iOS Simulator built into Xcode for basic testing
- A physical device is recommended before submitting to the App Store

---

## 2. Software Requirements

All free unless noted.

| Software | Cost | Purpose |
|---|---|---|
| **Xcode** | Free | Apple's IDE — download from Mac App Store |
| **Node.js** | Free | Required for React Native |
| **Watchman** | Free | File watcher used by React Native |
| **CocoaPods** | Free | iOS dependency manager |
| **VS Code** | Free | Code editor (optional but recommended) |
| **Apple Developer Account** | £79/year | Required to submit to App Store |

### Installation order
1. Install Xcode from the Mac App Store (large download, ~10GB)
2. Install Node.js from [nodejs.org](https://nodejs.org)
3. Install Watchman: `brew install watchman`
4. Install CocoaPods: `sudo gem install cocoapods`
5. Scaffold the app: `npx react-native init DnbFitness`

---

## 3. Apple Developer Account

- Enrol at [developer.apple.com/programs/enroll](https://developer.apple.com/programs/enroll)
- Cost: **£79/year**
- Required for:
  - Testing on a physical device
  - Submitting to the App Store
  - Access to App Store Connect
- Approval typically takes **1–2 business days**
- Pay by credit/debit card; must match your Apple ID name

> You do not need the developer account during early development — the Simulator works without it.

---

## 4. Recommended Technology Stack

**React Native** is the best starting point for a solo developer:

- Write in **JavaScript/TypeScript** (familiar if you've done web work)
- One codebase that runs on both **iOS and Android** when you're ready to expand
- Large ecosystem of ready-made components (calendars, charts, animations)
- Meta-maintained, widely used in production apps

**Key libraries you'll likely use:**
| Library | Purpose |
|---|---|
| `@react-navigation/native` | Screen navigation |
| `react-native-paper` | UI components (buttons, cards, inputs) |
| `@tanstack/react-query` | Data fetching & caching |
| `react-native-reanimated` | Smooth animations |
| `expo-av` | Video/audio for guided workouts (if needed) |
| `@supabase/supabase-js` | Database for user data / plans |

---

## 5. App Store Submission Process

### Step 1 — Build & archive in Xcode
- Connect your Apple Developer account to Xcode
- Select **Any iOS Device** as the build target
- **Product → Archive**
- Xcode creates a release build

### Step 2 — Upload via Xcode Organiser
- Open the Organiser window after archiving
- Click **Distribute App → App Store Connect → Upload**
- Xcode handles signing automatically with your developer account

### Step 3 — Configure in App Store Connect
Go to [appstoreconnect.apple.com](https://appstoreconnect.apple.com) and fill in:
- App name, subtitle, description
- Keywords (used for search)
- Category (Health & Fitness)
- Screenshots — required sizes:
  - iPhone 6.7" (iPhone 15 Pro Max)
  - iPhone 6.5" (iPhone 14 Plus)
  - iPad 12.9" (if supporting iPad)
- App icon: 1024×1024px PNG, no transparency, no rounded corners
- Support URL and Privacy Policy URL (both required)
- Pricing: Free or paid

### Step 4 — Submit for review
- Select the uploaded build
- Answer the export compliance questions (usually "No" for a fitness app)
- Click **Submit for Review**
- Apple reviews within **1–3 business days**

### Common rejection reasons to avoid
- Missing or broken privacy policy link
- App crashes on launch
- Placeholder or lorem ipsum content
- Misleading screenshots
- Missing purpose strings (e.g. why the app needs camera/health access)

---

## 6. Privacy Policy (Required)

Apple requires a privacy policy for all apps. For a fitness app it needs to cover:

- What personal data is collected (e.g. name, workout history, health data)
- How it is stored and used
- Whether it is shared with third parties
- How users can request deletion

**Free options:**
- [privacypolicygenerator.info](https://www.privacypolicygenerator.info) — generates a policy in minutes
- Host it on GitHub Pages (free) or any simple webpage

---

## 7. Costs Summary

| Item | Cost |
|---|---|
| Apple Developer Account | £79 / year |
| Mac (if needed) | £599–£1,299 (one-off) |
| React Native & tooling | Free |
| Supabase (database/auth) | Free tier available |
| Privacy policy hosting | Free |
| App Store listing | Free (included in developer account) |
| **Minimum (own a Mac)** | **£79/year** |
| **Minimum (need a Mac)** | **£678+ first year** |

---

## 8. Timeline (Part-Time Development)

| Phase | Time |
|---|---|
| Mac setup, Xcode, React Native install | 1–2 days |
| Apple Developer account activation | 1–2 days |
| Build V1 of the app | 4–8 weeks |
| Screenshots, icon, App Store metadata | 2–3 days |
| Apple review | 1–3 business days |
| **Total to first App Store release** | **~6–10 weeks** |

---

## 9. Recommended First Steps

1. **Enrol in the Apple Developer Program** — do this now as it takes a couple of days
2. **Install Xcode** on your Mac
3. **Run the React Native environment setup** guide at [reactnative.dev/docs/environment-setup](https://reactnative.dev/docs/environment-setup) (select macOS + iOS)
4. **Create a "Hello World" app** and run it in the Simulator — confirms everything is working
5. **Write a basic privacy policy** and host it before submitting

---

*Plan prepared: May 2026*
