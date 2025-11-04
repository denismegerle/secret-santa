# Secret Santa — Minimal Web App (Firebase + GitHub Pages)

---

## ✨ Features

- 🔒 **Private reveals** — each participant can reveal their match once.
- 🚫 **Exclusion rules** — disallow specific giver→receiver pairs.
- 🔁 **No mutual pairs** — prevent A↔B two‑cycles.
- 🔢 **Optional PINs** — avoid accidental reveals.
- ⏰ **Reveal windows** — enforce when reveals are allowed.
- 💬 **Custom message** — organizer can leave a note (budget/date/theme).
- 🌓 **Light & dark mode** — minimalist responsive UI.

---

## 🚀 Quick Start

1. **Clone this repo & enable GitHub Pages**
   ```bash
   git clone https://github.com/denismegerle/secret-santa.git
   cd secret-santa
   ```

2. **Create a Firebase project**
   - Enable **Anonymous Authentication**.
   - Enable **Cloud Firestore** in test mode (or use the included rules).
   - Copy your Firebase config (apiKey, projectId, etc.) into the `<script>` block inside the HTML file.

3. **Add Firestore Rules**  
   Copy the rules from the bottom of `index.html` into Firebase → Firestore → Rules → *Publish*.

4. **Deploy and Share**  
   Go to your Pages URL, create a session, and share the generated link with your friends.

---

## 🧪 Check Deployment Status

Visit:  
👉 **https://denismegerle.github.io/secret-santa/**

---

## 🧰 Tech Stack

| Layer | Technology |
|:------|:------------|
| Frontend | HTML, CSS, Vanilla JS |
| Backend | Firebase (Firestore + Anonymous Auth) |
| Hosting | GitHub Pages |

---

## 🔐 Firestore Rules Summary

- Anyone can read sessions and player states.
- Only the session creator can create/update documents.
- Participants can flip their `revealed` field **exactly once**, enforced by rules.

---

## 🧩 License
MIT © [Denis Megerle]

Fork, remix, and have fun gifting 🎅
