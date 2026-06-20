# Speak & Express

Live speech-to-text with expressive emoji detection and a modern UI.

Speak & Express is a small front-end app (single HTML file) that uses the Web Speech API to convert spoken words into live transcript text. It augments the transcript by detecting keywords and emoticons and converting them into emoji, provides interim results, a lightweight expressive sidebar (avatar + detected chips), and controls to save / clear transcripts.

---

## Features

- Real-time speech-to-text using the Web Speech API
- Interim and final transcripts (continuous recognition)
- Keyword and emoticon detection → emoji injection
- Visual expressive output: avatar and emotion chips
- Save transcript to a TXT file
- Clear transcript
- Language selection (English US/UK, Spanish, French)
- Small, responsive, modern UI with floating action buttons
- Keyboard shortcut (Space) to toggle listening (when not typing)

---

## Demo / Screenshot

Open `speech to text converter.html` in a Chromium-based browser (Chrome or Edge recommended).  
Note: This repo contains a single HTML file — no build tools required.

---

## Quick start

1. Clone or download the repository.
2. Open the HTML file directly in the browser:
   - Double-click `speech to text converter.html` or open it via your browser's File → Open.
   - OR serve it from a local static server (recommended for better permissions behavior):

     ```bash
     # Python 3
     python -m http.server 8000
     # Then open http://localhost:8000/<path-to-file>/speech%20to%20text%20converter.html
     ```

3. Allow microphone access when prompted.
4. Click the mic button (or press space) to start/stop listening.
5. Use "Save" to download the transcript or "Clear" to reset.

---

## Usage notes & settings

- Language: Choose recognition language from the Settings panel.
- Interim results: Toggle whether intermediate (in-progress) transcripts are shown.
- Expressions: Toggle expression/emoji injection on/off using the Expressions toggle.
- Word count and auto-scroll keep the transcript view usable for longer sessions.

---

## Browser support & limitations

- Recommended: Chrome and Microsoft Edge for best Web Speech API support.
- Not supported: Firefox (as of writing) has limited or no implementation of the Web Speech Recognition API.
- The app relies entirely on the browser's speech recognition — audio and transcript processing may be handled by the browser/vendor.
- Accuracy depends on microphone quality, language model, and ambient noise.

---

## Privacy & security

- This is a client-side app. No server component is included by default.
- The Web Speech API may send audio to the browser vendor's servers for processing depending on implementation — review your browser's privacy policy if this is a concern.
- The app uses navigator.mediaDevices.getUserMedia to request microphone access. Only grant access when you trust the environment and browser.

---

## Customization

- Keyword → emoji mapping is defined in the `keywordMap` array in the HTML. Edit to add/remove keywords or map them to different emoji.
- Emoticon detection regexes are in the `emoticons` array.
- UI styles are in the `<style>` section at the top of the HTML — modify colors, spacing, or typography as desired.
- To change the downloaded filename, edit the `a.download = 'transcript.txt';` line in the script.

---

## Accessibility

- The app includes ARIA labels for the main components and an `aria-live="polite"` region for the transcript.
- Keyboard shortcut: Space toggles the mic unless typing in an input/textarea.

---

## Troubleshooting

- "SpeechRecognition not supported": Use a Chromium-based browser (Chrome/Edge). Ensure the browser is up-to-date.
- Microphone permission denied: Check OS/browser settings and site permissions.
- Recognition stops unexpectedly: The Web Speech API's behavior varies across implementations; try restarting recognition (click the mic again).

---

## Contributing

Small tweaks, additional language options, or improved expression rules are welcome. Suggested contributions:
- Expand keyword/emoji lists
- Improve emoticon and phrase detection (phrases like "not sure" are currently matched using keywords)
- Add persistence (localStorage) for transcripts or preferences
- Add multi-language emoji keyword maps

If you open issues or PRs, please include:
- Browser/version tested
- Steps to reproduce any bug
- Suggested change or patch

---

## License

MIT License — see LICENSE file or add one to your repo.  
(If you want, you can reuse/modify this file under the MIT terms.)

---

## Acknowledgements

- Built using the Web Speech API and standard web technologies (HTML, CSS, JavaScript).
- UI inspiration: simple floating action button patterns and modern glassy card styles.
