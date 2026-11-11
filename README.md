![Version](https://img.shields.io/badge/Version-1.2_ADV-blue)
![Hardware](https://img.shields.io/badge/Hardware-Cardputer-orange)
![Platform](https://img.shields.io/badge/Platform-M5Stack-red)
![License](https://img.shields.io/badge/License-Proprietary-gray)
[![Boosty](https://img.shields.io/badge/Support-Boosty-orange)](https://boosty.to/zeloksa)

# 🧠 AI Offline Chat ADV (V1.2)

**AI Offline Chat ADV** is a modern, fully autonomous offline remake of **ELIZA** - the world's first psychological AI, originally created at MIT in 1966. Built from scratch for the **M5Stack Cardputer**, this firmware runs a custom natural language engine, procedural eye animations, and a live psychological profiler directly on the ESP32-S3 chip - 100% offline, with no Wi-Fi, no cloud APIs, and no subscriptions.

> [!IMPORTANT]
> **Source Code Status:** This project is proprietary. The source code is closed.  
> **Distribution:** Flash directly in your browser via **[burner.m5stack.com](https://burner.m5stack.com)** or download the `.bin` file from the **Releases** tab.

---

## ⚠️ Expectations (Read Before Installing)

**This is NOT ChatGPT.** Please understand what you are installing:
- **No Cloud, No Internet:** Everything runs locally inside the microcontroller's internal memory.
- **Not an Encyclopedia:** If you ask her *"What is the capital of France?"* or *"Write Python code for me"*, she won't do it. She is not a search engine or a coding assistant.
- **Active Listening Companion:** ELIZA is a Rogerian psychotherapist simulation. Her job is to listen, catch emotional nuances, track your relationships, and ask questions that help you untangle your own thoughts.
- **Built for Real Talk:** The more naturally and honestly you talk about your day, stress, work, relationships, or feelings, the more alive she feels.

---

## ✨ Key Features

### 👁️ Expressive Procedural Eyes (Cozmo / Vector Style)
A compact eye widget in the top-right corner reacts to everything happening on screen without blocking the chat:
- **Live Cursor Tracking:** Her eyes look down at your input line and follow your cursor as you type.
- **Natural Blinking & Sleep Mode:** Features double-blinking and falls asleep (`zZz`) after 22 seconds of inactivity - waking up startled when you press a key.
- **Rich Emotional States:**
  - **Empathy & Sadness:** Drooping eyelids and a falling cyan tear during moments of grief or deep sadness.
  - **Affection & Flirting:** Beating pixel-art heart eyes with neon blush when the conversation turns warm or romantic.
  - **Betrayal Shock (Shattered Hearts):** If you build trust and affection with her and suddenly insult her, her heart eyes crack and shake in orange.
  - **Anger & Glitching:** Angry eyebrows, red pin-point pupils, eye-rolling, and CRT screen glitches if you keep insulting her.
  - **Skeptical Squint:** Raises one eyebrow when you give one-word answers, ask questions, or erase what you just typed.
  - **Laser Scan:** Scans back and forth while processing your message (`...`).

### 📋 Interactive Patient Dossier (`[TAB]` Key)
Press **`TAB`** at any time to open ELIZA's internal clinical terminal (3 pages):
- **Page 1 - Clinical Profile:** Shows your name, current emotional state (9 clinical states), detected thinking pattern (e.g., Catastrophizing, All-or-Nothing, Self-Censoring), current focus, family members, and hobbies.
- **Page 2 - Social Attachment Graph:** A live bipolar bar chart (`-10` to `+10`) showing how you feel about the people in your life (mom, boss, partner, friends) - plus your current trust level with **ELIZA** herself.
- **Page 3 - Subconscious Memory & Telemetry:** Displays repressed thoughts she is saving for later, free RAM, message count, and session uptime.
- **Live EEG & Heart Rate (BPM):** The bottom panel renders a real-time brainwave oscilloscope and a dynamic BPM pulse that speeds up during anxiety/anger and slows down in sadness.

### 🧠 Smarter Offline Language & Psychology
- **Slang, Typos & Contractions:** Understands casual typing (`idk`, `wanna`, `gonna`, `im`, `dont`, `gf`, `bf`, `thx`, `sry`, `my bad`) and automatically fixes common typos in emotional words.
- **Context-Aware Meaning:** Knows the difference between *"my phone died"* / *"died laughing"*, angry outbursts (*"go die"*), and actual grief or personal crisis.
- **Negation Understanding:** Correctly handles phrases like *"I am not sad"*, *"I don't want to die"*, or *"I am not okay"* without triggering false alarms.
- **Self-Censorship & Hesitation Detection:** If you type a long thought, delete it all with Backspace, and stay quiet for 6 seconds, she will gently ask what you were afraid to say. She also checks in if you freeze mid-sentence for 30 seconds.
- **Trust, Boundaries & Apologies:** If you curse at your job or life, she supports you. If you attack *her* directly, she pushes back firmer each time - and calms down if you apologize (*"sorry"*, *"my bad"*).
- **Everyday & Deep Topics:** Ready to talk about work burnout, bad bosses, exams, ADHD/procrastination, feeling behind in life, loneliness, breakups, family pressure, habits, or simple first-time small talk (*"how are you?"*, *"tell me a joke"*, *"I'm fine"*).

### 🎙️ Dynamic Voice & Retro CRT Feel
- **1966 IBM CRT Boot Screen:** Powers on like a vintage green-phosphor monitor with a BIOS module check and retro audio.
- **Voice Intonation:** Her typing sound shifts pitch naturally - rising at the end of questions (`?`), dropping on periods (`.`), and pausing briefly on commas and sentence endings.
- **On-Screen Volume Bar (OSD):** Adjust volume anytime from `0%` (Mute) to `100%` with a retro overlay.

---

## 🛠 Installation

### Method 1: Web M5Burner (Recommended - No App Needed)
1. Open **[burner.m5stack.com](https://burner.m5stack.com)** in Chrome, Edge, or Opera.
2. Connect your Cardputer to your PC via USB-C.
3. Search for `AI Offline Chat ADV` or `Zeloksa`.
4. Select version **V1.2** and flash it directly from your browser.

### Method 2: Manual Flashing (`.bin` / M5Launcher)
1. Go to the **[Releases]** tab of this repository and download the latest `.bin` file.
2. Load it onto your SD card for **M5Launcher**, or flash it manually via **[burner.m5stack.com](https://burner.m5stack.com)** / **esptool**.

---

## 🕹 Controls

| Key | Action |
| :--- | :--- |
| **[ Keyboard ]** | Type your message normally |
| **[ ENTER ]** | Send message / **Skip typing animation** while ELIZA is speaking |
| **[ DEL ]** | Backspace / Delete character |
| **[ TAB ]** | Open / Close the **Patient Dossier** (`<` `,` `A` and `>` `/` `D` to switch pages 1-3) |
| **[ ; ]** / **[ . ]** | Scroll chat history Up / Down (when input is empty or holding `Fn`) |
| **[ - ]** / **[ = ]** | Volume Down (Mute) / Volume Up (when input is empty or holding `Fn`) |
| **[ ESC ]** / **[ ` ]** | Close Dossier / Open **New Session** dialog (`Y` / `N` or `A` / `D` to select) |

---

## 📖 Tips for the Best Experience

### 🗣 How to Talk to Her
Write in normal English sentences or casual chat style. You can introduce yourself (*"Call me Alex"*), talk about people (*"My boss stresses me out"*), share hobbies (*"I love playing guitar"*), or just say how your day went.
- If you want to wipe her memory via chat, type: `wipe memory` or `reset memory` (or use the `ESC` menu).

### 💾 SD Card Memory
Insert a MicroSD card (FAT32) so ELIZA can remember you after power-off. She automatically saves:
1. Your name, hobbies, and family members.
2. Your relationship graph (`-10..+10`) and trust level.
3. Unfinished thoughts in her subconscious memory stack.
4. Your recent color-coded chat history, last emotional state, and volume level.

---

## 🆕 Changelog

### V1.2 (Major Update)
- **Added:** Cozmo/Vector-style procedural eyes with cursor tracking, double-blinking, sleep mode (`zZz`), tear animation, beating heart eyes, shattered heart eyes, and angry glitch effects.
- **Added:** 3-page Interactive Patient Dossier (`[TAB]`) with clinical profile, relationship graph (`-10..+10`), subconscious memory view, live EEG wave, and dynamic BPM heart rate monitor.
- **Added:** Self-censorship detector (reacts when you type a long message and erase it all) and hesitation prompts.
- **Added:** Trust & Betrayal mechanics, multi-stage boundary setting on repeated insults, and apology recognition.
- **Added:** 1966 CRT terminal boot animation, dynamic voice intonation (question/statement pitch shifts), and retro volume OSD bar.
- **Added:** Press `[ENTER]` while ELIZA is typing to instantly finish the message.
- **Improved:** Major upgrade to language comprehension - added slang/contraction expansion, negation handling (*"not sad"*, *"don't want to die"*), 4-way context separation for the word *"die"*, and dozens of new conversation rules for work, study, procrastination, relationships, and casual onboarding.
- **Fixed:** Resolved mood lock issues, pronoun reflection bugs, and keyboard navigation conflicts with punctuation.

### V1.1
- **Added:** Adjustable typing volume using `-` and `=` keys (includes full mute option).
- **Added:** Volume level state is now persistently saved to the SD card profile.
- **Fixed:** Eliminated screen tearing during the boot animation by implementing dynamic double-buffering.

---

## ☕ Support the Project
If you enjoy this project and want to support future offline tools and games for the Cardputer ecosystem:
- **Boosty:** [https://boosty.to/zeloksa](https://boosty.to/zeloksa)

---
*Developed by Engineer Zeloksa. Optimized for M5Stack Cardputer & Cardputer ADV.*
