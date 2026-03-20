# 🖨️ Printing Press — Order Management System

A lightweight, browser-based order management web app built for a local printing press business. No installation needed — just open the link and start managing orders.

> **Built as a freelance project for a real client (Shri Printers, Mubarakpur)**

---

## 🔗 Live Demo
🌐 [Click here to view live](#) *(replace with your GitHub Pages link)*

---

## 📸 Preview

> *(Add a screenshot here — drag and drop an image in GitHub)*

---

## ✨ Features

| Feature | Details |
|---|---|
| 📋 Order Management | Add, edit, delete orders with full details |
| 🔍 Search & Filter | Search by name, filter by type, status, payment |
| 💰 Payment Tracking | Unpaid / Partial / Paid — auto calculated |
| 🚚 Delivery Tracking | Pending → In Progress → Ready → Delivered |
| ⚡ Quick Actions | Update order status in one click from the list |
| 🖨️ Printable Bill | Clean receipt with business details per order |
| ☁️ Cloud Storage | Firebase Firestore — syncs across all devices |
| 📊 Dashboard Stats | Live count of pending, ready, and unpaid orders |
| ✅ Smart Validations | Phone, dates, amounts — all validated on input |

---

## 🛠️ Tech Stack

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=flat&logo=github&logoColor=white)

- **Frontend** — Pure HTML, CSS, JavaScript (no frameworks)
- **Database** — Firebase Firestore (real-time cloud sync)
- **Hosting** — GitHub Pages (free, auto-deploy on push)

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/printing-press-order-management.git
cd printing-press-order-management
```

### 2. Create a Firebase project
1. Go to [firebase.google.com](https://firebase.google.com) → **Add Project**
2. Enable **Firestore Database** → Start in test mode
3. Go to **Project Settings → Your Apps → Web** → Register app
4. Copy your Firebase config

### 3. Add your Firebase config
Open `index.html` and replace the placeholder values:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  databaseURL: "YOUR_DATABASE_URL",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

### 4. Set Firestore security rules
In Firebase Console → Firestore → **Rules** tab:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

### 5. Run
Just open `index.html` in any browser — no build step or server needed. ✅

---

## 📁 Project Structure

```
📦 printing-press-order-management
 ┣ 📄 index.html       → complete app (single file)
 ┗ 📄 README.md        → documentation
```

---

## 🧾 Order Types Supported

- 💍 Wedding Cards
- 🧾 Receipt Books
- 📚 Binding
- 🎓 Certificates
- 📊 Report Cards
- 📰 Magazines
- 📦 Other (custom)

---

## 💡 Key Design Decisions

- **Single file app** — entire frontend in one HTML file, easy to deploy anywhere
- **No backend server** — Firebase handles all data, zero server maintenance
- **Offline-friendly UI** — loads instantly, Firebase syncs in background
- **Print-ready bills** — uses browser's native print for clean receipts

---

## 👩‍💻 Author

**Mansi** — Freelance Web Developer

---

## 📄 License

This project is open source under the [MIT License](LICENSE).
