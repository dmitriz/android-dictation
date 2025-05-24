# Android Dictation Log

A structured record of experiments, tools, requirements, and insights for improving voice typing and dictation on Android. This project focuses on accuracy, reliability, system-wide integration, and evaluating alternatives to Gboard voice typing—especially for users with accents or those experiencing transcription interruptions.

---

## ✅ Core Requirements (Must-Have)

1. **Real-time transcription preview** — The user must see text appear *as they speak*, not after submitting or waiting for backend processing.
2. **High accuracy**, especially for non-native English accents.
3. **No random pauses** — the dictation should not stop automatically without user intention.
4. **System-wide use** — voice input should work inside any app (WhatsApp, Keep, Gmail, etc.).
5. **Minimal setup** — should be quick to install and test without developer tools unless chosen.
6. **Offline support preferred** — but not required if accuracy online is better.
7. **Security awareness** — tools must be vetted for privacy and stability.

---

## ⚡ Tools & Apps Evaluated (Quick Results)

### 1. **Gboard (Google Keyboard)**

- **Engine**: Google Speech-to-Text
- **Pros**: Pre-installed, fast, system-wide, simple UI
- **Cons**: Random auto-pauses, accuracy suffers with accents, poor offline behavior

### 2. **ChatGPT App Voice Mode**

- **Engine**: Whisper (OpenAI)
- **Pros**: Extremely high accuracy, handles accents well
- **Cons**: Not system-wide, no real-time preview during dictation, can lose long inputs

### 3. **Gboard Voice Recorder**

- **Engine**: Google
- **Issue**: Unpredictable failure to transcribe longer messages, no intermediate output, "black box" behavior

---

## 🧪 Tools Suggested for Testing (Deeper Trials)

### A. **WhisperInput**

GitHub: [alex-vt/WhisperInput](https://github.com/alex-vt/WhisperInput)

- **Pros**: Real-time, offline, open-source, system-wide when installed
- **Cons**: No Play Store version, must be built and signed manually (APK not provided), security review required

GitHub: <https://github.com/alex-vt/WhisperInput>

### B. **Speechkeys Smart Keyboard**

- **Engine**: Google Speech (same as Gboard)
- **Pros**: Larger mic button, no auto-pausing
- **Cons**: No accuracy improvement over Gboard, same limitations for accents

### C. **Futo Voice + SwiftKey**

- **Engine**: Unknown
- **Pros**: Anecdotal reports of better accuracy in some environments
- **Cons**: Not a true IME replacement, not confirmed better than Google

### D. **Sayboard / Heliboard (F-Droid)**

- **Engine**: Non-Google (open-source)
- **Pros**: Lightweight, privacy-friendly
- **Cons**: Limited features, unclear accuracy, experimental

---

## ⏳ What to Delay (Too Heavy for Now)

### AssemblyAI, Deepgram, RevAI (Cloud APIs)

- **Use case**: Real-time transcription with great accuracy
- **Setup required**: Dev account, API keys, mic streaming
- **Verdict**: Worth exploring later, too much for a quick test

### WhisperLive / Custom IME Development

- **Goal**: Full system keyboard using Whisper locally
- **Steps**: Build Android IME, integrate Whisper.cpp or use API
- **Verdict**: Complex but powerful, revisit in dev phase

---

## ⚙️ Android System Options Checked

- Found multiple "voice input" providers: Google, ChatGPT, Perplexity, Copilot, MacroDroid
- Many register as input methods but **do not** offer system-wide live transcription
- Some apps (like ChatGPT) **record audio silently** and transcribe only after stop—problematic for live use

---

## ️‍🔥 Summary of Findings

- **Gboard (Google)**
  - Real-Time: Yes
  - System-Wide: Yes
  - Accuracy: Medium
  - Offline: Partial
  - Notes: Frequent auto-pausing

- **ChatGPT Voice Mode**
  - Real-Time: No
  - System-Wide: No
  - Accuracy: High
  - Offline: No
  - Notes: Whisper, but no preview

- **WhisperInput**
  - Real-Time: Yes
  - System-Wide: Yes
  - Accuracy: High
  - Offline: Yes
  - Notes: Needs manual APK build

- **Speechkeys Keyboard**
  - Real-Time: Yes
  - System-Wide: Yes
  - Accuracy: Medium
  - Offline: Partial
  - Notes: Better mic button only

- **Sayboard / Heliboard**
  - Real-Time: Yes
  - System-Wide: Yes
  - Accuracy: Unknown
  - Offline: Yes
  - Notes: Open-source, basic UI

- **Futo Voice**
  - Real-Time: Partial
  - System-Wide: No
  - Accuracy: Variable
  - Offline: No
  - Notes: User-reported better

- **AssemblyAI / RevAI**
  - Real-Time: Yes
  - System-Wide: No (custom)
  - Accuracy: Very High
  - Offline: No
  - Notes: Dev API required

---

## ✅ What To Try Right Now

### 1. **Stick with Built-in Gboard** for now — but monitor accuracy and pauses

### 2. **Try enabling Google’s Voice Access**

- Go to **Settings > Accessibility > Voice Access**
- Might offer more responsive voice handling

### 3. **Review WhisperInput GitHub**

- Decide later if building APK is worth it

### 4. **Prepare for ChatGPT voice feedback**

- Highlighted limitations (no preview, long input loss)
- [WhisperInput](https://github.com/alex-vt/WhisperInput)
- [Study on ASR for Non-Native English](https://arxiv.org/abs/2503.06924)
- [⚠️ NOTE: The arXiv link for ASR study appears to reference a future date (2025). Please verify correct paper identifier]
- [OpenAI Whisper Model](https://github.com/openai/whisper)
- [Whisper.cpp](https://github.com/ggerganov/whisper.cpp)
- [AssemblyAI](https://www.assemblyai.com/)
- [Deepgram](https://www.deepgram.com/)
- [Speechmatics](https://www.speechmatics.com/)
- [Reddit discussion](https://www.reddit.com/r/androidapps/comments/1dkdy1m/alternative_keyboard_to_google_and_ms_that_still/)

---

## End of Log

- WhisperInput: <https://github.com/alex-vt/WhisperInput>
- Study on ASR for Non-Native English: <https://arxiv.org/abs/2503.06924>
- OpenAI Whisper Model: <https://github.com/openai/whisper>
- Whisper.cpp: <https://github.com/ggerganov/whisper.cpp>
- AssemblyAI: <https://www.assemblyai.com/>
- Deepgram: <https://www.deepgram.com/>
- Speechmatics: <https://www.speechmatics.com/>
- Reddit discussion: <https://www.reddit.com/r/androidapps/comments/1dkdy1m/alternative_keyboard_to_google_and_ms_that_still/>
