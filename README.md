<div align="center">

# ⏱️ KRON (FocusFlow)
### *Minimalist Chronobiology & Deep Work Intelligence*

[![Release](https://img.shields.io/badge/Release-v1.0.0_Official_Launch-09090b?style=for-the-badge&logoColor=white)]()
[![Platform](https://img.shields.io/badge/Platform-Linux_Desktop_•_Android_•_Web-18181b?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-27272a?style=for-the-badge)]()
[![Privacy](https://img.shields.io/badge/Data-100%25_Local_&_Offline-10b981?style=for-the-badge)]()

<p align="center">
  <b>An analytical deep work and circadian rhythm intelligence platform combining the biological sleep tracking of Rize with the precision focus logging of Toggl — 100% offline, local-first, and subscription-free.</b>
</p>

---

<!-- HERO SCREENSHOT -->
<img src="screenshots/hero_desktop.png" alt="Kron Desktop Hero" width="100%" style="border-radius: 12px; border: 1px solid #27272a;" />
*(Replace `screenshots/hero_desktop.png` with your desktop or immersive mode screenshot)*

---

</div>

## 📑 Table of Contents
1. [Why Kron?](#-why-kron)
2. [Visual Feature Walkthrough](#-visual-feature-walkthrough)
   - [1. Precision Focus Engine & Overtime Tracker](#1-precision-focus-engine--overtime-tracker)
   - [2. Visual Chronobiology Day Strip](#2-visual-chronobiology-day-strip)
   - [3. Automated Circadian Sleep & Rest Detection](#3-automated-circadian-sleep--rest-detection)
   - [4. Full-Screen Immersive Canvas & Scratchpad](#4-full-screen-immersive-canvas--scratchpad)
   - [5. Dual-Mode Notes: Study Notes & Checklists](#5-dual-mode-notes-study-notes--checklists)
   - [6. Kron Copilot (Gemini AI Chrono-Partner)](#6-kron-copilot-gemini-ai-chrono-partner)
3. [Installation & Setup](#-installation--setup)
   - [🐧 Linux Desktop (.deb Package)](#-linux-desktop-debianubuntukali)
   - [📱 Android Mobile (.apk Package)](#-android-installation)
   - [🌐 Web / Self-Hosted](#-web--local-development)
4. [Day 1 Quick-Start Workflow](#-day-1-quick-start-workflow)
5. [Keyboard & Navigation Shortcuts](#-keyboard--navigation-shortcuts)
6. [Data Architecture & Local Vault](#-data-architecture--local-vault)
7. [Author & Credits](#-author--credits)

---

## 💡 Why Kron?

Modern productivity apps are either bloated with project-management clutter or locked behind expensive monthly subscriptions ($15–$20/month for Rize or Toggl). Furthermore, most web timers fail on mobile because operating systems kill their timers when backgrounded.

**Kron solves this with three core design rules:**
1. **Biological Alignment**: Work output is tied directly to your circadian energy peaks and sleep debt.
2. **Timestamp-Delta Reliability**: Timers never freeze when your phone locks or when an app is backgrounded.
3. **Local Sovereignty**: All telemetry, notes, and session logs live on your device's hard drive—never in a proprietary cloud.

---

## 🖥️ Visual Feature Walkthrough

### 1. Precision Focus Engine & Overtime Tracker
<img src="screenshots/timer_overtime.png" alt="Focus Timer" width="100%" style="border-radius: 8px;" />

* **Timestamp-Delta Execution**: Instead of fragile interval loops, elapsed time is computed continuously from real-world wall clock time (`Date.now() - startTime`). Your timers continue accurately even if your device sleeps or the app is killed by the OS.
* **Continuous Overtime Counting**: When your target sprint reaches `00:00:00`, Kron chimes once and switches into **Overtime Mode** (`+00:01`, `+02:15` in amber warning). Your extended flow state is never discarded.
* **Tri-Tier Classification**: Categorize sprints into `Deep Work` (high-leverage cognitive focus), `Shallow Work` (admin/chores), and `Break` (prefrontal cortex recovery).

---

### 2. Visual Chronobiology Day Strip
<img src="screenshots/day_strip.png" alt="Day Strip Timeline" width="100%" style="border-radius: 8px;" />

* **Continuous 08:00 – 22:00 Timeline**: Chronological color-coded blocks (Emerald for Deep, Amber for Shallow, Indigo for Breaks) with a glowing real-time current-hour indicator.
* **Daily Focus Telemetry Score (0–100)**:
  $$\text{Score} = \text{Volume Score (60 pts)} + \text{Deep Ratio (30 pts)} + \text{Break Cadence (10 pts)}$$
* **Screen vs. Focus Efficiency Ratio**: Analyzes your total screen exposure against pure deep work to highlight distraction fatigue before it causes burnout.

---

### 3. Automated Circadian Sleep & Rest Detection
<img src="screenshots/sleep_detection.png" alt="Sleep Tracking" width="100%" style="border-radius: 8px;" />

* **Zero-Touch Overnight Detection**: Kron monitors device heartbeats upon app exit. When closed overnight and launched the next morning (4–14 hour inactivity window), Kron infers your sleep duration automatically.
* **1-Click Rest Adjustment Banner**: On launch, Kron presents:
  > `🌙 Rest Detected: 11:15 PM – 07:15 AM (8h 0m) • [Adjust ✏️]`
  Clicking *Adjust* allows instant 1-click fine-tuning without manual form entry.
* **Two-Way Target Sync**: Adjusting target sleep or deep work hours in Settings dynamically updates all Sleep tab telemetry, deficit models, and Copilot intelligence.

---

### 4. Full-Screen Immersive Canvas & Scratchpad
<img src="screenshots/immersive_mode.png" alt="Immersive Mode" width="100%" style="border-radius: 8px;" />

* **Atmospheric Canvas**: Ambient background scenery and a high-contrast timer for deep, single-tasking flow.
* **Floating Scratchpad Tasks (`Tasks X/Y`)**: Quick-access modal from the bottom dock to offload distracting thoughts or bugs without navigating away from your sprint.

---

### 5. Dual-Mode Notes: Study Notes & Checklists
<img src="screenshots/notes_view.png" alt="Notes Workspace" width="100%" style="border-radius: 8px;" />

* **Study Note Mode**: Formatted reading and writing environment supporting clean Markdown typography: `# H1`, `## H2`, `**bold**`, `*italics*`, and inline `` `code` ``.
* **Checklist Mode**: Dedicated task management with structured interactive checkboxes, completion progress counters (`0/0 completed`), and tag filtering.
* **Streamlined Mobile Toolbar**: A compact formatting strip (`[H1]`, `[H2]`, `[B]`, `[• List]`, `[Code]`) tailored for fast tap-insertion on mobile virtual keyboards without checklist redundancy.
* **Responsive Mobile Container**: Built with dynamic viewport-aware constraints (`max-h-[calc(100dvh-2rem)]`), preventing on-screen keyboards from compressing or overlapping dialogs.

---

### 6. Kron Copilot (Gemini AI Chrono-Partner)
<img src="screenshots/copilot_chat.png" alt="Kron Copilot" width="100%" style="border-radius: 8px;" />

* **Analytical Chrono-Intelligence**: Connected to Google Gemini Flash with zero filler phrases or canned robotic greetings.
* **Live Telemetry Injection**: Automatically aware of your active session minutes, sleep deficit, circadian phase, and target hours.
* **On-Demand Debriefs**: Ask *"generate my daily focus debrief"* or *"what is my target deep work"* for instant mathematical analysis of your day.

---

## 📦 Installation & Setup

### 🐧 Linux Desktop (Debian/Ubuntu/Kali)

Kron is packaged as an independent desktop application (`.deb`) running on a dedicated Chromium app shell with permanent on-disk storage:

1. **Download the Package**:
   Download `kron_1.0.2_amd64.deb` from the [Releases](https://github.com/Yohaleli/Kron/releases) section.

2. **Install via APT**:
   ```bash
   sudo apt install -y ./kron_1.0.2_amd64.deb
