# Voice Translator

Real-time bilingual voice translator (English <-> Spanish) built as a single-page HTML app.

**Live:** [abes876.github.io/translator](https://abes876.github.io/translator/)

## How It Works

1. Tap **English** or **Spanish** to start listening
2. Speak in the selected language
3. The app translates and speaks the translation aloud
4. Tap **Stop** to end

- English input -> Spanish translation (male voice)
- Spanish input -> English translation (female voice)

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
