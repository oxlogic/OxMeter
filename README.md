# OxMeter (OxLogic DMM)

**Professional On-Screen Digital Multimeter (DMM) Overlay for Smartphone & Electronics Repair**

---

### Overview

**OxMeter** is a specialized, lightweight on-screen digital multimeter designed specifically for **smartphone repair technicians, chip-level instructors, and YouTube/live-stream trainers**.

It allows instructors and technicians to overlay a fully functional, realistic digital multimeter right on top of schematics and boardviews (such as Borneo Schematics, ZXW, XinZhiZao, Pragmafix, Wuxinji), displaying real-time diode readings, voltages, resistance, and continuity beeps during tutorials and live classes.

---

### 📥 Download Portable Release

If you just want to use the software without compiling source code:

* **[Download OxMeter v1.0.0 Portable (Latest Release)](https://github.com/oxlogic/OxMeter/releases/latest)**

Simply extract the ZIP archive and double-click `OxMeter.exe`. No installation required!

---

### Key Features

* **Realistic DMM Hardware Experience:** Authentic dial rotation animation with audible mechanical switch clicks, 7-segment LCD digital readouts with realistic digit flicker, and continuity beep tones.
* **Interactive Magnetic Probes:** Fully draggable Red and Black probes with dynamic wiring that magnetically dock/holster directly to the meter's test probe sockets.
* **Measurement Modes:**
  * **DCV** (DC Voltage: e.g., VPH_PWR `3.82V`, VREG `1.80V`)
  * **ACV** (AC Voltage)
  * **Ohm (Ω)** (Resistance: e.g., `10.2 Ω`, `4.70k`, `1.45M`)
  * **Diode** (Forward & Reverse Bias: `0.420`, `OL`, `0.002` Short)
  * **Continuity** (Short detection with real-time buzzer sound: `0.001` + Beep)
* **Global Hotkey Control:**
  * Control presets on-the-fly while working inside any schematic software using `Numpad 1-9`, `Ctrl + 1-9`, or `Alt + 1-9`.
  * Instant clear to idle (`OL` / `0.000`) with `Numpad 0`, `Ctrl + 0`, or `Alt + 0`.
  * Windows chime suppression ensures silent hotkey triggering without annoying system beeps.
* **Live Preset Editor & Quick Actions:**
  * Built-in Control Panel to customize, add, edit, or delete presets on-the-fly.
  * Changing mode, name, or value in the editor immediately reflects on the multimeter in real-time.
* **Multi-Monitor Support:** Easily assign the overlay to primary or secondary displays.

---

### Hotkeys & Global Shortcuts

| Hotkey | Action | Description |
| :--- | :--- | :--- |
| **Numpad 1 - 9** | Measurement Presets | Trigger measurement preset for current slot |
| **Ctrl + 1 - 9** | Global Shortcut | Alternative global hotkey for preset slots |
| **Alt + 1 - 9** | Global Shortcut | Alternative global hotkey for preset slots |
| **Numpad 0 / Ctrl+0 / Alt+0** | Clear Reading | Reset display back to idle (`OL` / `0.000`) |
| **Spacebar** | Toggle Reading | Toggle active reading ON / OFF inside Control Panel |
| **Escape** | Idle Reset | Clear meter display back to idle state |

---

### How to Build from Source

#### Prerequisites
* Windows 10 / 11 (64-bit)
* [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)

#### Clone & Build
```bash
# 1. Clone the repository
git clone https://github.com/oxlogic/OxMeter.git
cd OxMeter

# 2. Build the project
dotnet build

# 3. Run the application
dotnet run

# 4. Publish a single-file standalone executable
dotnet publish -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -o ./publish-standalone
```

---

### Project Structure

```
OxMeter/
├── Audio/                 # Authentic mechanical dial clicks and continuity buzzer audio
├── Controls/              # Multimeter body, LCD display, dial knob, and probe UI elements
├── Models/                # Multimeter state, presets, and configuration models
├── Native/                # Win32 window styles, monitor detection, and global low-level hooks
├── Windows/               # Overlay window and Control Panel & Settings window
├── app.ico                # High-resolution multi-size application icon
├── app.png                # High-resolution PNG logo
├── presets.json           # Measurement presets database
└── OxMeter.csproj         # WPF .NET 8 project file
```

---

### Author & Community

Developed by **Muhammad Tazmir (OxLogic)**

Connect and follow for latest updates, smartphone repair tutorials, and upcoming tools:

* 📺 **YouTube:** [@OxLogicTech](https://www.youtube.com/@OxLogicTech)
* ✈️ **Telegram:** [@OxLogicTech](https://t.me/OxLogicTech)
* 🐙 **GitHub:** [mdtazmir1](https://github.com/mdtazmir1)
* 🌐 **Facebook:** [Muhammad Tazmir](https://www.facebook.com/muhammadtazmir)

---

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
