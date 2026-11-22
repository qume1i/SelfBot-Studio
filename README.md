<div align="center">

# SelfBot Studio

**Turn your Discord account into a local AI companion powered by LM Studio — with a full-featured Web UI, all packed into a single `.py` file.**

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LM Studio](https://img.shields.io/badge/LM%20Studio-Local%20LLM-6366F1?style=for-the-badge)
![Interface](https://img.shields.io/badge/Web%20UI-RU%20%2F%20EN-EC4899?style=for-the-badge)
![Single File](https://img.shields.io/badge/Architecture-Single%20File-10B981?style=for-the-badge)

</div>

> [!CAUTION]
> **Disclaimer:** Using a selfbot violates [Discord's Terms of Service](https://discord.com/terms) and may result in account suspension or termination. This project is provided for educational and local experimentation purposes only. Use at your own risk.

---

## Preview

<p align="center">
  <img width="1706" height="1008" alt="SelfBot Studio Web UI" src="https://github.com/user-attachments/assets/91e795b5-03d5-43ef-9bfe-391743346321" />
</p>

---

## Key Features

* **Single-File Architecture & Built-in Web UI** — Live SSE updates, bilingual interface (**Russian / English**) with startup language picker, custom themes & CSS, Command Palette (`Ctrl+K`), and a real-time GPU / VRAM / RAM HUD.
* **Vision & Media Awareness** — Understands attached images, animated GIF frames, and Tenor / Klipy / Giphy links. Supports a local `memes/` reaction folder with Vision auto-tagging, plus Giphy & Nekos.best GIF replies.
* **Long-Term Memory & Personalization** — SQLite + **FTS5** full-text memory search, automatic memory compaction, user dossiers, dynamic Affinity (`-10..+10`) & mood tracking, personal events/birthdays tracker, and chat reminders.
* **Roles, Sandbox & A/B Arena** — Separate DM / Server personas, custom presets, priority role overrides (`User > Channel > Server > Default`), interactive Vision sandbox, and side-by-side A/B prompt/model testing.
* **Analytics, Social Graph & Mini-Games** — Built-in dialog analytics with PNG report export, interactive drag-and-drop Social Graph, and chat mini-games (*Word Chain*, *20 Questions*, *Yes/No Riddles*, *Truth or Dare*) with a leaderboard.
* **Safety & Humanization** — Anti-flood / anti-raid **GPU Guard**, Anti-Jailbreak & Anti-Cliché filters, Ghost-Ping detector, message burst splitting & debounce, Windows DPAPI token encryption, and strict localhost CSRF/CSP middleware.

---

## Recommended Models

For the best balance of speed, chat quality, and Vision support in **LM Studio**:

| Component | Purpose | Download |
| :--- | :--- | :--- |
| **Main Model (GGUF)** | Chat & reasoning (`Gemma 4 E4B Q4_0`) | [gemma-4-E4B_q4_0-it.gguf](https://huggingface.co/google/gemma-4-E4B-it-qat-q4_0-gguf/blob/main/gemma-4-E4B_q4_0-it.gguf) |
| **Vision Projector (mmproj)** | Optional — lets the bot see images & GIFs *(skip if you only need text)* | [gemma-4-E4B-it-mmproj.gguf](https://huggingface.co/google/gemma-4-E4B-it-qat-q4_0-gguf/blob/main/gemma-4-E4B-it-mmproj.gguf) |

---

## Quick Start

1. **Start LM Studio:**
   Load the model in **LM Studio** and start the local OpenAI-compatible server (check your server port in LM Studio — usually `http://127.0.0.1:1234` or `1235`).

2. **Install dependencies:**
   > [!TIP]
   > If you previously installed standard `discord.py`, remove it first (`pip uninstall -y discord.py`) so it doesn't conflict with `discord.py-self`.

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the bot:**
   ```bash
   python selfbot.py
   ```
   The Web Control Panel will open automatically at `http://127.0.0.1:8787` (if running from a terminal and you want to see console output, set `HIDE_CONSOLE=0`).

4. **Configure in the browser:**
   * Choose your interface language (**English** or **Russian**).
   * Paste your Discord user token in the banner or **Settings** tab (stored locally in SQLite).
   * Check your LM Studio endpoint URL in **Settings**, add whitelisted channels, and enjoy!

---

## Credits

* 98% of the code was generated with **Gemini** (neon xhigh).
