![Version](https://img.shields.io/badge/Version-1.1_ADV-blue)
![Hardware](https://img.shields.io/badge/Hardware-Cardputer-orange)
![Platform](https://img.shields.io/badge/Platform-M5Stack-red)
![License](https://img.shields.io/badge/License-Proprietary-gray)
[![Boosty](https://img.shields.io/badge/Support-Boosty-orange)](https://boosty.to/zeloksa)

# 🧠 AI Offline Chat ADV (V1.1)

**AI Offline Chat ADV** is a modern, fully autonomous, and offline implementation of the legendary **ELIZA**—the world’s first artificial intelligence therapist, originally created at MIT in 1966. Re-engineered from the ground up for the **M5Stack Cardputer**, this firmware uses advanced C++ optimizations, JIT-compiled Regular Expressions (RegEx), and hardware-level memory protection to run a pure NLP (Natural Language Processing) engine directly on the ESP32-S3 chip, without requiring Wi-Fi or cloud APIs.

> [!IMPORTANT]
> **Source Code Status:** This project is proprietary. The source code is private. 
> **Distribution:** Binary (`.bin`) only via the **Releases** tab.

---

## ⚠️ Expectations (Must Read Before Use)

**This is NOT ChatGPT.** Please understand what you are installing:
* **No Cloud, No Servers:** The AI runs 100% locally on the microcontroller's limited SRAM.
* **Not an Encyclopedia:** If you ask her *"What is the capital of France?"* or *"Write code for me"*, she will not answer. She has no external knowledge base.
* **The Rogerian Therapist:** ELIZA is a psychological simulation. She uses a technique called "active listening." Her purpose is to analyze your grammar, reflect your statements back as questions, and encourage you to talk about your feelings, relationships, and problems.
* **The Illusion of Understanding:** She doesn't "think" in neural weights; she processes language via complex linguistic rules. The magic happens when you engage with her as if she were a real listener.

---

## ⚡ Technical Highlights

* **True Offline NLP Engine:** Processes Natural Language offline using a custom C++ parsing core, bypassing the need for heavy LLM models.
* **JIT-Compiled Regex System:** Employs Just-In-Time compilation for over 30 complex psychological trigger rules. The engine dynamically scans input and instantly flushes memory to prevent Heap fragmentation.
* **Hardware-Level Stack Protection:** Embedded C++ `<regex>` engines are notoriously dangerous on microcontrollers. This firmware features a custom sanitizer that truncates infinite quantifiers (`.*`), physically preventing RTOS Stack Overflows during deep recursive sentence analysis.
* **Long-Term SD Memory:** ELIZA remembers. She saves your name, family members, specific objects you mention, the overall "emotional tone" of your last session, and your system volume preferences to the SD card.

---

## 🛠 Installation
### Method 1: M5Burner (Recommended)
1. Open **M5Burner**.
2. Search for `AI Offline Chat ADV` or `Zeloksa`.
3. Select version **V1.1**.
4. Burn to your M5Stack Cardputer.

### Method 2: Manual Flashing
1. Go to the **[Releases]** tab of this repository.
2. Download the **`ELIZA1.1.bin`** (full 4B flash dump) or the standard app bin.
3. Flash to your Cardputer using **M5Burner** (Local File) or **esptool**.

---

## 🕹 Controls
* **[ Full Keyboard ]**: Type your thoughts normally.
* **[ ENTER ]**: Send message to ELIZA.
* **[ DEL ]**: Backspace / Delete character.
* **[ ; / . ]**: Scroll chat history Up/Down (if the chat exceeds screen height).
* **[ - / _ ]**: Decrease typing volume / Mute.
* **[ = / + ]**: Increase typing volume.
* **[ ESC / \` ]**: Open System Menu (Start New Session / Wipe Memory).

---

## 📖 Operational Guide

### 🗣 Engaging with ELIZA
For the best experience, type in full English sentences. Use pronouns (`I`, `My`, `You`) and express states or emotions.
* **Bad Input:** *"apple"* or *"hello bot"*
* **Good Input:** *"I feel really anxious about my new job today."* or *"My mother never listens to me."*

### 💾 Persistent Memory (SD Card Required)
An SD Card must be inserted for the long-term memory to function. The system creates a tiny profile (`/eliza_v7.txt`) where it stores:
1.  **Named Entities:** Your name and specific objects you care about.
2.  **Emotional Context:** If your session focuses on grief (`TOPIC_GRIEF`), the UI will adapt (green text, lower tone frequency), and ELIZA will remember your state across power cycles.
3.  **Color-Coded History:** The chat history is saved along with its specific emotional color coding.
4.  **Hardware States:** Your preferred typing volume level is permanently saved.

### 🧠 The JIT "Thinking" Indicator
When you submit a complex sentence, the ESP32-S3 must compile and test multiple Regex patterns. You will see an `ELIZA: ...` indicator. This is not a fake animation; it represents the actual CPU blocking time required for the NLP engine to calculate its response before rendering it via a typewriter effect.

### 🔄 System Reset
If you wish to erase your psychological profile and start fresh, press `ESC` or ``` ` ``` to open the System Menu. From there, you can select the option to wipe the SD card memory and reset her context variables.

---

## 🆕 Changelog
### V1.1
* **Added:** Adjustable typing volume using `-` and `=` keys (includes full mute option).
* **Added:** Volume level state is now persistently saved to the SD card profile.
* **Fixed:** Eliminated screen tearing during the boot animation by implementing dynamic double-buffering (M5Canvas).

---

## ☕ Support the Project
Support the development of advanced offline tools and engines for the Cardputer ecosystem:
* **[https://boosty.to/zeloksa]**

---
*Developed by Engineer Zeloksa. Strictly optimized for Cardputer ADV.*
