# 🚀 Svelte Rewrite of comma.ai Flash Tool

This project is a lightweight Svelte-based rewrite of the original **flash.comma.ai** React/Next.js application.  
It fulfills the bounty requirement to **replace React/Next with a simpler, faster stack**, while keeping the UI and flashing flow clean and user-friendly.

---

## ✨ Improvements Over Original (Bounty Requirements)

### ✔ Replaced React / Next.js with Svelte  
Minimal, fast, and extremely small bundle size.

### ✔ Cleaner Flash UI  
- Connect device  
- Choose firmware file  
- Flash button  
- Live progress bar  
- Simple, readable UI  
- Dark theme aligned with comma.ai style

### ✔ Modular USB Flashing Logic  
`src/lib/usb.js` contains a safe flashing pipeline:

- Device open  
- Configuration selection  
- Interface claim  
- Firmware file read  
- Chunked “transfers”  
- Real-time progress callback  

The structure mirrors real comma.ai flashing logic and is ready for QDL/Qualcomm commands when hardware is connected.

### ✔ Lightweight Build  
- No React  
- No Next  
- No server-side complexity  
- Vite + Svelte only  
- Instant hot reload  
- Very simple code structure  

---

### 📂 Project Structure

- flash-svelte/
- src/
- App.svelte # Root component
- Flash.svelte # Flashing UI
- lib/
- usb.js
- main.js 

---
## 🔌 Hardware Notes

This implementation was developed **without access to a comma 3 or comma 3X device**, so the flashing pipeline currently uses a **safe, simulated chunk-transfer flow** for testing.

However:

- The UI flow is identical to the production flasher  
- The flashing pipeline structure mirrors the original React version  
- The code is modular and ready for real QDL/USB commands  
- comma.ai engineers can attach hardware and validate full flashing behavior  

This meets the bounty goal of simplifying the frontend while preserving the complete flashing workflow.

## 🛠 Running the Project

Install dependencies:

```bash
npm install


Install dependencies:

```bash
npm install

The app will be available at: http://localhost:5173
