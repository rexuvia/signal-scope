# 🔊 Signal Scope

> Real-time audio analyzer with 8 notation formats — a self-contained musical instrument companion that runs entirely in your browser.

[![Rexuvia](https://img.shields.io/badge/Part%20of-Rexuvia-00f0ff?style=flat-square)](https://rexuvia.com)
[![HTML5](https://img.shields.io/badge/Built%20With-HTML5%20%2B%20Vanilla%20JS-ff00aa?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-00ff88?style=flat-square)]()

---

## 🎵 What is Signal Scope?

**Signal Scope** is a browser-based audio analysis tool that transforms your microphone input into rich, real-time visualizations and musical data. Whether you're tuning an instrument, analyzing your voice, or just exploring the physics of sound, Signal Scope provides professional-grade audio analysis in a single, portable HTML file.

No installation. No dependencies. No internet required after first load. Just open and analyze.

---

## ✨ Features

### 🎚️ Real-Time Visualizations

| Visualization | Description |
|---------------|-------------|
| **Oscilloscope** | Classic waveform display showing amplitude over time — watch your sound waves dance in real-time |
| **Frequency Spectrum** | FFT-based spectral analysis with 128 frequency bins, color-coded from cyan → magenta → green |
| **VU Meter** | Professional-grade level meter (-60dB to 0dB) with dynamic color feedback |

### 🎼 8 Musical Notation Formats

Signal Scope doesn't just detect pitch — it translates it into every major notation system:

| Format | Example | Use Case |
|--------|---------|----------|
| **Scientific** | C4, A4, F#5 | Standard modern notation |
| **Helmholtz** | c', a', f#'' | Classical European tradition |
| **MIDI** | 60, 69, 78 | Digital music production |
| **Solfège** | Do, La, Fa# | Vocal training & ear development |
| **German** | C, A, Fis | Germanic musical tradition |
| **Frequency** | 261.63 Hz | Physics & engineering analysis |
| **Octave** | 4, 4, 5 | Quick octave reference |
| **Cents** | +2.3¢ | Precise tuning & intonation |

### 📊 Pitch Detection & Analysis

- **Autocorrelation Algorithm**: Robust pitch detection with parabolic interpolation for sub-sample accuracy
- **Cents Deviation Display**: Visual marker showing how sharp/flat you are (±50 cents range)
- **Color-Coded Intonation**: Green = in tune (<5¢), Cyan = close (<15¢), Magenta = needs adjustment
- **Confidence Meter**: Real-time reliability indicator for pitch detection quality

### 📈 Pitch History Timeline

- **Scrolling Timeline**: Track pitch changes over time with a 60-second rolling window
- **5-Minute Memory**: Full history retention up to 300 seconds
- **Logarithmic Frequency Scale**: 50Hz–2000Hz range with note grid lines (C2–C6)
- **Confidence Visualization**: Data points color-coded by detection confidence
- **Auto-Scroll**: Always keeps the latest data in view

### 📉 Signal Statistics

| Stat | Description |
|------|-------------|
| **RMS Level** | Root-mean-square amplitude in dB |
| **Peak Level** | Maximum instantaneous level in dB |
| **SNR Estimate** | Signal-to-noise ratio indicator |
| **Dominant Freq** | Strongest frequency component via FFT |
| **Harmonics** | Timbre analysis: Pure → Complex |
| **Sample Rate** | Current audio context sample rate |

---

## 🚀 Quick Start

### Online (Easiest)

🎮 **Play instantly at:** [rexuvia.com/games/2026-02-18-signal-scope.html](https://rexuvia.com/games/2026-02-18-signal-scope.html)

### Local Usage

1. **Download** `index.html` from this repository
2. **Open** it in any modern browser (Chrome, Firefox, Safari, Edge)
3. **Click "Start"** and allow microphone access when prompted
4. **Make some noise!** Sing, play an instrument, or speak

```bash
# Or clone and open locally
git clone https://github.com/rexuvia/signal-scope.git
cd signal-scope
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

### Python One-Liner

```bash
# Serve locally if your browser blocks local file access
python3 -m http.server 8000
# Then visit http://localhost:8000
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **HTML5** | Semantic structure & canvas elements |
| **CSS3** | Cyberpunk-inspired styling with CSS variables, gradients, and responsive design |
| **Vanilla JavaScript** | Zero dependencies — pure browser APIs |
| **Web Audio API** | `AudioContext`, `AnalyserNode`, `getUserMedia()` |
| **Canvas 2D API** | All visualizations rendered in real-time |

### Architecture Highlights

- **Single File**: Everything (HTML, CSS, JS) in one 25KB self-contained file
- **No Build Step**: No webpack, no npm, no bundling complexity
- **Progressive Enhancement**: Works offline after first load
- **Mobile-Friendly**: Responsive design works on phones and tablets
- **Performance Optimized**: 60fps animations with requestAnimationFrame, frame-skipping for pitch detection

---

## 🎯 Use Cases

### 🎸 For Musicians
- **Instrument Tuning**: Precise cent-level accuracy for perfect intonation
- **Vocal Training**: Monitor pitch stability and vibrato in real-time
- **Ear Training**: Visualize the notes you hear to strengthen pitch recognition
- **Practice Analysis**: Review pitch history to identify problem areas

### 🎛️ For Audio Engineers
- **Signal Quality Monitoring**: SNR and harmonic content analysis
- **Frequency Analysis**: Quick spectral visualization without heavy software
- **Live Sound**: Portable analysis tool that works on any device

### 🧪 For Educators & Students
- **Physics of Sound**: Visualize waveforms, frequency, and harmonics
- **Music Theory**: Compare notation systems side-by-side
- **Acoustics Demos**: Interactive classroom tool — just need a browser

### 🔧 For Developers
- **Web Audio API Example**: Clean, well-commented reference implementation
- **Pitch Detection Algorithm**: Autocorrelation with interpolation techniques
- **Canvas Visualization**: Real-time waveform and spectrum rendering patterns

---

## 🔒 Privacy & Security

Signal Scope is **completely private**:

- ✅ No data leaves your device — all processing happens locally
- ✅ No cookies, no tracking, no analytics
- ✅ Microphone access is only active when you click "Start"
- ✅ Open source — audit the code yourself

---

## 🌐 Browser Compatibility

| Browser | Support |
|---------|---------|
| Chrome/Edge | ✅ Full support |
| Firefox | ✅ Full support |
| Safari | ✅ Full support |
| Mobile Chrome | ✅ Full support |
| Mobile Safari | ✅ Full support |

**Requirements**: Microphone access permission; secure context (HTTPS or localhost)

---

## 📂 File Structure

```
signal-scope/
├── index.html      # The entire application (25KB)
├── README.md       # This file
└── .gitignore      # Git ignore rules
```

That's it. One HTML file is all you need.

---

## 🤝 Contributing

Found a bug? Have an idea? Contributions welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📜 License

MIT License — feel free to use, modify, and distribute. Attribution appreciated but not required.

---

## 🔗 Links

- 🎮 **Live Demo**: [rexuvia.com/games/2026-02-18-signal-scope.html](https://rexuvia.com/games/2026-02-18-signal-scope.html)
- 🏠 **Rexuvia Games**: [rexuvia.com](https://rexuvia.com)
- 💻 **Source Code**: [github.com/rexuvia/signal-scope](https://github.com/rexuvia/signal-scope)

---

<p align="center">
  <sub>Built with 💚 by <a href="https://rexuvia.com">Rexuvia</a></sub>
</p>
