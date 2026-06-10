# ⚡ Quick Software Installer

A Windows PowerShell GUI tool that lets you **batch install multiple software files** (.exe, .msi, .inf drivers) in one click — with smart silent install support and auto-fallback to interactive mode.

---

## ✨ Features

- 📂 **Folder Browser** — Select any folder; tool auto-scans all `.exe`, `.msi`, `.inf` files recursively
- 🌲 **TreeView + ListView** — Dual-panel view: folder tree on left, file list (with icons, size, version) in center
- ☑️ **Batch Selection** — Select All / Clear All / individual checkboxes in both panels (fully synced)
- 🤫 **Smart Silent Install** — Tries silent flags automatically:
  - MSI: `/quiet` → `/passive` → Interactive fallback
  - EXE: `/S` → `/VERYSILENT` → `/silent` → `/quiet` → Interactive fallback
  - INF Drivers: `pnputil /add-driver` (always silent)
- 🔄 **Auto-Fallback** — If silent install fails, automatically opens the normal installer window
- 📋 **Live Install Log** — Real-time log box shows each step, exit codes, and results
- 📊 **Progress Bar** — Marquee animation during installation
- ✅ **Auto-Close Option** — Checkbox to auto-close the tool after all installs finish
- 🛡️ **Admin Auto-Elevation** — Automatically re-launches as Administrator if not already

---

## 🚀 How to Use

1. **Right-click** `Quick_Software_Installer_Fixed.ps1` → **Run with PowerShell**  
   *(Tool will auto-request Administrator privileges)*

2. Click **"Select Software Location"** → choose the folder with your installers

3. Check the software you want to install (from TreeView or ListView)

4. Click **"Install Selected"**

5. Watch the log — done! ✅

---

## 🗂️ Supported File Types

| Type | Method |
|------|--------|
| `.exe` | Smart silent flags with interactive fallback |
| `.msi` | MSI quiet/passive with interactive fallback |
| `.inf` | PnPUtil driver install (silent) |

---

## ⚙️ Requirements

- Windows 10 / 11
- PowerShell 5.1 or later
- Administrator privileges (auto-requested)
- No external dependencies

---

## 💡 Use Cases

- Fresh Windows setup — install all software in one go
- IT technicians setting up multiple PCs
- Offline software deployment from a USB/folder
- Driver batch installation

---

## 📄 License

MIT License — free to use and modify.

---

## 👨‍💻 Author

Made by **[Your Name]** | [GitHub Profile Link]
