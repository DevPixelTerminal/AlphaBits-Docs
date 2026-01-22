# 📜 BarrelDAO Change Log

All notable changes to the **"Night Shift Terminal"** simulation engine.

> **Current Version:** v34.2 (Final Polish)
> **Engine:** Python 3.12 + OpenAI GPT-4o + MoviePy + OBS Integration
> **Status:** Production Ready

---

## [v34.2] - The "Broadcast Quality" Polish ✨
**Final visual style and UI refinement.**
* **Smart Topic Bar:** Implemented a complex layer system for the ticker tape. The **"TOPIC:"** label is now static, and the text smoothly scrolls out from underneath it, eliminating visual clutter.
* **Cinematic Static:** Slowed down the "NO SIGNAL" noise animation by 4x. The effect is now soft, "analog," and easy on the eyes, removing the strobe effect.
* **Bug Fixes:** Resolved critical `NameError` crashes when calling transition functions.

## [v33.2] - The "Golden Standard" & OBS Integration 🏆
**Major broadcast architecture update.**
* **Unified UI Design:** Introduced a consistent Golden Frame (40px) across all scenes (Interview, News, Transitions). Eliminated visual disparity between modes.
* **OBS Safe Zones:**
    * Redesigned the lower third overlay. The left 35% of the screen is now a dedicated "Black Box" reserved for overlaying CA text via OBS.
    * News elements ("LIVE", "BREAKING NEWS") were shifted to the right to prevent overlap with critical data.
* **Seamless Updates:** The new architecture allows for **instant** token CA updates on the livestream without reloading the Python script or interrupting the broadcast.

## [v31.0] - The "TV Experience" Update 📺
**Transforming the bot into a TV channel.**
* **Intro/Outro Sequences:** Added automatic broadcast transitions:
    * *News Intro:* Retro "Test Card" + Audio Jingle.
    * *Broadcast End:* "Signal Lost" effect (White Noise).
* **Console UX:** Completely rewrote the console output (CMD). Added render progress bars, cooldown timers, and clear display of the current discussion topic.

## [v28.0] - The "Clean Speech" Engine 🗣️
**Dialogue quality improvements.**
* **Regex Cleaner:** Implemented a strict text filter. The engine automatically strips LLM "stage directions" (e.g., `*sits down*`, `(laughs)`), leaving only clean spoken text for TTS generation.
* **Timing Logic:** Optimized dialogue length (30-35 lines) to hit the "Golden Minute" video duration (1:20 – 1:40).

## [v25.0] - The "Hybrid Core" Merge 🌍
**Merging the worlds.**
Combined the "Street Interview" engine and the "News Studio" engine into a single executable binary.
* **Context Switching:** The system automatically swaps asset dictionaries and lighting logic when changing scenes.
* **Weather Logic:** Weather (Rain/Snow) is automatically paused inside the Studio and resumes with the correct intensity upon returning to the Street.

## [v20.0] - Real World Integration 📡
* **RSS Scraper:** Integrated `urllib` to fetch live headlines from CoinTelegraph and BBC. Characters now react to real-world news within minutes of publication.

---

## [v8.5] - Legacy "High-Fidelity" Update 👑
* Added **ANSEM** character.
* Implemented the initial "Smart Upscale" pipeline for 1080p rendering on RTX 5070 hardware.