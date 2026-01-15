# ⚡ Reaction Timer

A polished, interactive reaction time game built with Three.js featuring 3D graphics and smooth animations. Test your reflexes and track your performance with detailed statistics.

## 🎮 Live Demo

[Play the game here](#) *(Add your deployed URL)*

## ✨ Features

- **Accurate Timing** — Millisecond-precise reaction measurement using `performance.now()`
- **3D Graphics** — Animated icosahedron with dynamic lighting and particle effects powered by Three.js
- **False Start Detection** — Prevents cheating by detecting early clicks
- **Session Statistics** — Tracks attempts, best time, and running average
- **Recent History** — Color-coded performance history for your last 10 attempts
- **Responsive Design** — Works seamlessly on desktop, tablet, and mobile devices
- **Keyboard Support** — Play using Space or Enter keys
- **Touch Support** — Optimized for mobile touch interactions

## 🚀 Getting Started

### Prerequisites

None! This is a static HTML application with no build process required.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/reaction-timer.git
   ```

2. Open `index.html` in your browser, or serve it locally:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve
   ```

3. Navigate to `http://localhost:8000`

## 🎯 How to Play

1. Click **"Start Game"** to begin a round
2. Watch the 3D shape — it will turn **amber** while waiting
3. When the shape turns **green**, click as fast as you can!
4. Your reaction time is displayed in milliseconds
5. Don't click too early — false starts are detected

### Performance Ratings

| Time | Rating |
|------|--------|
| < 200ms | 🔥 Incredible |
| < 300ms | ⚡ Excellent |
| < 400ms | 👍 Good |
| 400ms+ | 💪 Keep practicing |

## 🛠️ Technical Details

### Built With

- **Three.js** (r128) — 3D graphics and WebGL rendering
- **Vanilla JavaScript** — No frameworks, clean ES6+ code
- **CSS3** — Custom properties, flexbox, grid, animations
- **Google Fonts** — Outfit (headings) & Inter (body)

### Architecture

```
reaction-timer/
├── index.html      # Single-file application
├── favicon.png     # Site favicon
└── README.md       # Documentation
```

### Key Implementation Details

- **State Machine** — Clean game state management (IDLE → WAITING → READY → RESULT)
- **IIFE Pattern** — Encapsulated code preventing global namespace pollution
- **Performance Optimized** — Pixel ratio limiting and efficient render loop
- **Memory Safe** — Proper cleanup handlers for animations and timeouts
- **Accessible** — High contrast ratios and keyboard navigation support

### Game States

| State | Shape Color | Description |
|-------|-------------|-------------|
| Idle | Blue | Waiting for user to start |
| Waiting | Amber | Random delay (1-5 seconds) |
| Ready | Green (pulsing) | Click now! |
| Result | Blue | Displaying reaction time |
| False Start | Red | Clicked too early |

## 📱 Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

*Requires WebGL support for 3D rendering*

## 🧪 Performance

The game maintains accurate timing despite 3D rendering by:

- Using `performance.now()` for high-resolution timestamps
- Separating game logic from render loop
- Limiting pixel ratio to prevent GPU overload
- Using efficient Three.js practices (reusing geometries/materials)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

<p align="center">
  Made with ❤️ and Three.js
</p>