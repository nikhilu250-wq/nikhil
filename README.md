# Speech to Text Converter with Punctuation

A real-time speech-to-text application that converts spoken words into text and automatically adds punctuation marks (commas, periods, question marks, exclamation marks) and other expressions.

## Features

- 🎤 Real-time speech recognition using Web Speech API
- ✨ Automatic punctuation and capitalization
- 🎯 Support for commas, periods, question marks, exclamation marks
- 🔄 Live transcript display
- 📋 Copy to clipboard functionality
- 🎨 Modern, responsive UI
- 🚀 Fast and lightweight

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: Node.js, Express.js
- **APIs**: Web Speech API (Browser native)

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- Modern web browser with Web Speech API support (Chrome, Edge, Safari)

### Installation

1. Clone the repository
```bash
git clone https://github.com/nikhilu250-wq/nikhil.git
cd nikhil
```

2. Install dependencies
```bash
npm install
```

3. Start the server
```bash
npm start
```

4. Open your browser and navigate to `http://localhost:3000`

## Usage

1. Click the **Start Recording** button
2. Speak clearly into your microphone
3. The app will transcribe your speech in real-time
4. Automatic punctuation will be added
5. Click **Stop Recording** when finished
6. Use **Copy to Clipboard** to copy the text
7. Click **Clear** to reset

## How Punctuation Works

The app uses intelligent pattern recognition to:
- Add periods at the end of sentences
- Insert commas in natural pauses
- Add question marks when question patterns are detected
- Add exclamation marks for emphatic statements
- Capitalize the first letter of sentences

## Project Structure

```
nikhil/
├── index.html          # Main HTML file
├── css/
│   └── style.css       # Styling
├── js/
│   └── script.js       # Frontend logic and speech recognition
├── server.js           # Express server
├── package.json        # Dependencies
└── README.md          # This file
```

## Supported Browsers

- ✅ Chrome/Chromium
- ✅ Edge
- ✅ Safari (iOS 14.5+)
- ✅ Opera
- ❌ Firefox (limited support)

## License

MIT License - feel free to use this in your projects

## Contributing

Feel free to fork, modify, and submit pull requests!
