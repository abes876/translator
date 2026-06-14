# Voice Translator

Real-time English-centered voice translator built as a single-page HTML app.

**Live:** [abes876.github.io/translator](https://abes876.github.io/translator/)

## How It Works

1. Pick the non-English language from the **English ↔** menu
2. Tap **English** or the selected language to start listening
3. Speak in the selected language
4. The app translates to the other side of the pair and speaks the translation aloud
5. Tap **Stop** to end

You can also type text and translate it in either direction when voice input is not available.

## Languages

- English ↔ Spanish
- English ↔ Mandarin Chinese (Taiwan, Traditional Chinese)
- English ↔ Taiwanese Hokkien
- English ↔ Taiwan Hakka
- English ↔ Japanese

Browser speech recognition support varies by language. Spanish, Mandarin Chinese, and Japanese are broadly supported in modern browsers; Taiwanese Hokkien and Taiwan Hakka are available through typed translation and may fall back to typed input for speech recognition.

## Tech Stack

- **Speech-to-text:** Web Speech API (`SpeechRecognition`)
- **Translation:** Anthropic Claude API (streaming, Haiku with Sonnet fallback)
- **Text-to-speech:** Browser `SpeechSynthesis` API
- **UI:** Single `index.html`, no dependencies, no build step

## Setup

No installation needed. You'll need an [Anthropic API key](https://console.anthropic.com/).

**Option 1 — Pass the key in the URL (recommended for mobile shortcuts):**
```
https://abes876.github.io/translator/?key=YOUR_API_KEY
```
On iPhone: open the URL in Safari, tap Share > Add to Home Screen.

**Option 2 — Enter manually:**
Open the app and you'll be prompted to paste your key on first use.

**Local development:**
```bash
python3 -m http.server 8080
```

## Browser Support

- Safari (macOS, iOS)
- Chrome (desktop)
- Edge (desktop)

Requires microphone permission and a browser with Web Speech API support.
