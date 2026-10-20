# Piper Voice Models

High-quality Piper voice models trained using **F5-TTS**, **VoiceBox** and **TextyMcSpeechy**.

The goal of this project is simple: create high-quality custom Piper voices that sound as natural as possible while preserving the personality of the original character.

---

# How this started

It all started because I was looking for a good **Homer Simpson** voice for my Piper + Home Assistant setup.

There isn't much documentation available on how to create high-quality custom Piper voices. My first attempts used audio from an audiobook, but no matter what I tried, I could never completely get rid of the robotic sound.

Then I discovered **[Simoniz0r's Piper Voice Models](https://github.com/simoniz0r/piper-voice-models)** and heard an incredibly clean Eminem voice. That was the moment I realized this level of quality was actually possible.

Looking through his repository, I saw he was using **F5-TTS** together with **TextyMcSpeechy**, so I started experimenting with those tools myself.

My results improved significantly, but I still wasn't completely satisfied. I kept refining every step of the workflow until I consistently achieved the quality I was aiming for.

From what I've seen in the Piper community so far, I can confidently say these voices are among the best custom Piper voices currently available.

---

# My workflow

For every voice I create, I roughly follow the same workflow.

1. Learn the target voice using **F5-TTS**.
2. If F5-TTS struggles with a particular voice, switch to **VoiceBox**.
3. Generate approximately **200–300 Harvard sentences** for clean, natural speech.
4. Add iconic catchphrases, emotional lines, laughs, shouts and character-specific expressions.
5. Train a Piper model using the combined dataset.

The result is a voice that sounds natural during everyday speech while still being able to reproduce the character's most memorable moments.

Homer's famous **"D'oh!"** and **"Woohoo!"** were the original reason this project started. Once I heard how well those clips worked, I decided to apply the same approach to every character I created.

---

# Available Voices

| Voice | Sample | Model | Iconic Phrases |
|:------|:------:|:-----:|----------------|
| **Barney Gumble** | 🎧 [Listen](https://raw.githubusercontent.com/Code-Genious/Piper-voices/main/Samples/BarneyGumble.ogg) | 📦 [Download](https://github.com/Code-Genious/Piper-voices/releases/download/v1.0.0/BarneyGumble.zip) | **BURP!**, **OW!** |

*More voices will be added over time.*

---

# Using Iconic Phrases

Many of these models have been trained with iconic catchphrases, emotional expressions and character-specific sounds in addition to normal speech.

To reproduce these correctly, the phrase should be generated as a separate sentence or utterance.

For example, instead of embedding a catchphrase inside a normal sentence, let Piper finish the current sentence first and then generate the iconic phrase separately.

This allows Piper to build the correct phonemes and intonation for the expression. When the same word is used as part of a normal sentence, Piper will naturally pronounce it as regular speech rather than using the iconic delivery that was learned during training.

Examples:

✔️ Hello everybody. D'OH!
❌ Hello everybody D'OH!

✔️ The beer is gone. BURP!
❌ He made me burp after dinner.

---

# Installation

1. Download the ZIP archive of the desired voice.
2. Extract the archive.
3. Copy the `.onnx` and `.onnx.json` files into your Piper voices directory.
4. Select the voice in your application.

---

# Credits

A huge thank you to everyone whose work made this possible.

- **[Simoniz0r](https://github.com/simoniz0r/piper-voice-models)**
- F5-TTS
- TextyMcSpeechy
- VoiceBox
- Piper

Without these amazing projects, this repository would never have existed.
