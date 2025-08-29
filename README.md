# Custom Speed Video Player

A modern, cross-platform desktop video player built with Electron and React, featuring advanced custom speed controls and a sleek user interface.

## ✨ Features

### 🎬 Video Playback

- **Multiple Formats**: MP4, AVI, MKV, MOV, WMV, FLV, WebM, M4V
- **Hardware Acceleration**: Optimized performance with GPU support
- **Fullscreen Mode**: Immersive viewing experience
- **Custom Controls**: Intuitive video controls with progress tracking

### ⚡ Advanced Speed Controls

- **Preset Speeds**: 0.25x, 0.5x, 0.75x, 1x, 1.25x, 1.5x, 2x, 3x, 4x
- **Custom Speed Slider**: Fine-tune from 0.1x to 16x
- **Quick Adjustments**: +/- buttons for 0.25x increments
- **Real-time Display**: Shows current playback speed

### 🎛️ User Experience

- **Keyboard Shortcuts**: Space (play/pause), F (fullscreen), M (mute), arrows (skip/volume)
- **Volume Control**: Slider with mute toggle
- **Playlist Support**: Queue multiple videos
- **Modern UI**: Dark theme with Material-UI components
- **File Association**: Set as default video player (Windows)

## 🚀 Quick Start

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Development Setup

```bash
# Clone the repository
git clone <repository-url>
cd custom-speed-video-player

# Install dependencies
npm install

# Start development server
npm start
```

### Building for Production

```bash
# Build for all platforms
npm run dist

# Build for specific platform
npm run dist:win    # Windows
npm run dist:mac    # macOS
npm run dist:linux  # Linux
```

## 📖 Usage

### Opening Videos

1. Click "Open Video File" button
2. Select a video file from your computer
3. The video will load and start playing

### File Association (Windows)

Set the app as your default video player to double-click any video file:

#### Automatic Setup

File associations are automatically registered during installation for common video formats.

#### Manual Setup

```bash
# Run setup script (requires admin privileges)
npm run setup-associations-windows
```

#### Alternative Methods

- **Windows Settings**: Right-click video file → "Open with" → "Choose another app" → Select "Custom Speed Video Player"
- **Command Prompt** (admin):
  ```cmd
  assoc .mp4=CustomSpeedVideoPlayer.mp4
  ftype CustomSpeedVideoPlayer.mp4="C:\path\to\Custom Speed Video Player.exe" "%1"
  ```

### Speed Controls

- **Preset Buttons**: Click speed control button for preset options
- **Custom Slider**: Drag for precise speed control (0.1x - 16x)
- **Quick Buttons**: Use +/- buttons for 0.25x increments
- **Keyboard**: Access speed menu for quick changes

### Keyboard Shortcuts

| Key     | Action            |
| ------- | ----------------- |
| `Space` | Play/Pause        |
| `F`     | Toggle Fullscreen |
| `M`     | Toggle Mute       |
| `←/→`   | Skip 10 seconds   |
| `↑/↓`   | Volume up/down    |

## 🏗️ Project Structure

```
custom-speed-video-player/
├── electron/                 # Electron main process
│   ├── main.js              # Main process entry point
│   ├── preload.js           # Preload script for IPC
│   └── assets/              # Icons and assets
├── src/                     # React application
│   ├── components/          # React components
│   │   └── VideoPlayer.js   # Main video player component
│   └── App.js               # Main application component
├── scripts/                 # Build and utility scripts
│   ├── setup-file-associations-windows.js
│   └── ...
├── public/                  # Static assets
└── dist/                    # Built applications
```

## 🛠️ Development

### Available Scripts

```bash
npm start                    # Start development server
npm run build               # Build React application
npm run dist                # Build for distribution
npm run dist:win            # Build Windows executable
npm run setup-associations-windows  # Setup file associations
```

### Technology Stack

- **Electron**: Cross-platform desktop framework
- **React**: User interface library
- **Material-UI**: Component library
- **HTML5 Video API**: Native video playback

## 🌍 Cross-Platform Support

### Windows

- ✅ File association setup
- ✅ Single instance application
- ✅ Command line support
- ✅ Drag & drop support

### macOS & Linux

- ✅ Command line arguments
- ✅ Drag & drop support
- ⚠️ Manual file association setup required

## 🔧 Troubleshooting

### Common Issues

1. **Video not playing**: Ensure format is supported (MP4, AVI, MKV, etc.)
2. **Speed controls not working**: Check video element is properly loaded
3. **File associations not working**: Run setup script with admin privileges
4. **Build errors**: Ensure all dependencies are installed

### Performance Tips

- Enable hardware acceleration for better performance
- Use supported video formats for optimal playback
- Close other applications to free up system resources

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 💬 Support

For support and questions, please open an issue on the GitHub repository.
