# 🚀 DevSync – Developer Productivity Suite with Portfolio Builder

> *DevSync* is a premium developer-first SaaS platform designed to help engineers track their growth, manage daily dev logs, and publish professional portfolios — all in one ecosystem.  
> Built with 💻 Java Spring Boot, 📱 Jetpack Compose, and 🌐 HTML/CSS, DevSync bridges productivity and portfolio into a single seamless tool.

---

## 🧠 Product Overview

*DevSync empowers developers to:*
- Log bugs, commits, goals, and daily work using clean interfaces
- Track skill growth in DSA, projects, frameworks, and languages
- Instantly generate and customize personal *developer portfolios* from templates
- Export weekly/monthly productivity reports
- Maintain visibility into career growth — and showcase it when needed

---

## 🛠 Tech Stack

| Layer         | Stack                                |
|---------------|---------------------------------------|
| Backend       | Java 17, Spring Boot, Spring Security |
| Android App   | Jetpack Compose, Room, Retrofit       |
| Web Panel     | HTML5, CSS3 (No JavaScript)           |
| Auth & Sync   | Firebase Auth + Firebase Realtime DB  |
| Portfolio CMS | HTML Templates with dynamic binding   |
| Reports       | iText / Apache PDFBox (PDF exports)   |
| Billing       | Stripe (Subscription-based Access)   |
| Hosting       | Render / Railway / Firebase Hosting   |

---

## 💡 Key Features (v1.0 – Live)

### 🧑‍💻 Productivity & Workflow
- 🐞 *Bug Tracker:* Add, resolve, and archive code bugs by severity
- ⏱ *Dev Journal:* Daily logbook with timestamped entries
- 📚 *Skill Tracker:* Track DSA, language mastery, and side projects
- 🔁 *Commit Log Parser:* Upload GitHub URLs to auto-parse history

### 🎨 Portfolio Templates (New!)
- Choose from pre-designed *developer portfolio layouts*
- Edit skills, projects, bio — and publish immediately
- Export as HTML, PDF, or host via Firebase

### 📄 Report Generator
- Export PDF summaries: Bugs fixed, goals achieved, commits made
- Ideal for *internship reports, **placement prep*, or GitHub README

---

## 🧭 Menus & UI Navigation

### 📱 Android App (Jetpack Compose)

| Menu       | Function                              |
|------------|----------------------------------------|
| 🧭 Dashboard | Snapshot of tasks, logs, portfolio status |
| 🐞 Bugs      | Bug log list & tracker module         |
| 📚 Learning  | Add/edit skill goals                  |
| 📓 Journal   | Write & edit daily logs               |
| 🔁 Commits   | GitHub repo parser                    |
| 🎨 Portfolio | Template selector & editor            |
| 🧾 Reports   | PDF summary generator                 |
| ⚙ Settings  | Theme, Auth, Subscription check       |
| 👤 Profile   | View account & payment info           |

### 💻 Web Panel (HTML/CSS Only)

- Dashboard  
- Bug Tracker  
- Daily Journal  
- Learning Goals  
- GitHub Parser  
- Portfolio Templates  
- PDF Reports  
- Settings / Billing  
- Logout  

---

## 🔒 Subscription Model & Access Control

### 🎯 Subscription Plan (via Stripe)

| Plan        | Price     | Access Level                         |
|-------------|-----------|--------------------------------------|
| Free        | ₹0        | Journal, bugs, learning tracker only |
| Pro Monthly | ₹199/mo   | + Portfolio templates, PDF reports   |
| Pro Yearly  | ₹1,999/yr | + All features, upcoming AI tools    |

> 💡 All billing managed securely via *Stripe Checkout* with webhook integration for license verification.

---

## 🔐 Security & Access Implementation

- *Firebase Auth:* All users must sign in via Google or email
- *Spring Boot Guarded APIs:* Use Firebase ID token in header
- *Stripe Webhook Sync:* When payment is successful, set proUser = true in Firebase or internal DB
- *Access Control:* UI and API routes verify if proUser === true before allowing:
  - Access to portfolio editor
  - GitHub parser
  - PDF report generator

> If subscription expires → show “Upgrade to Pro” banner and lock premium features.

---

## 🚧 Upcoming Features (Roadmap)

| Feature                  | Target Release | Description |
|--------------------------|----------------|-------------|
| 🌐 Custom Portfolio Domain | v1.1           | Use your own domain (e.g. aditya.dev) |
| 📈 AI Growth Reports      | v1.2           | Weekly summary via OpenAI API |
| 🛠 VS Code Extension     | v1.3           | Log bugs and journal right from editor |
| 🧩 Community Templates   | v1.4           | Upload and share your portfolio layouts |
| 📤 GitHub Sync + PR Logs | v1.5           | Auto-import commit + PR history |

---

## 🧱 Directory Structure (Internal Repo)

```bash
DevSync/
├── backend/           # Spring Boot APIs + Stripe + Auth
├── android-app/       # Jetpack Compose App
├── web/               # HTML/CSS dashboard and templates
├── templates/         # Portfolio layout files
├── stripe/            # Billing + Webhook handler
├── firebase/          # Firebase config + Firestore rules
├── docs/              # Business model, screenshots
└── README.md
