# NTS CCTV Viewer

A modern, responsive web-based CCTV video viewer that allows synchronized playback of multiple camera feeds with advanced controls and zoom/pan functionality.

## Features

### 🎥 Multi-Camera Synchronized Playback
- **6 Camera Feeds**: View multiple camera angles simultaneously
- **Perfect Synchronization**: All videos are synchronized with precise time offsets
- **Master Timeline**: Single timeline control for all cameras
- **Automatic Sync Correction**: Intelligent sync monitoring and correction

### 🎮 Advanced Playback Controls
- **Play/Pause**: Control all cameras simultaneously
- **Seek Controls**: Jump forward/backward 15 seconds
- **Speed Control**: 0.5x and 1x playback speeds
- **Timeline Scrubber**: Visual timeline with time markers
- **Real-time Display**: Shows current time and total duration

### 🔍 Zoom and Pan Functionality
- **Click to Zoom**: Click any camera to view in fullscreen
- **Double-click/Tap**: Toggle zoom levels (1x to 2x)
- **Mouse Wheel**: Smooth zoom in/out
- **Drag to Pan**: Pan around when zoomed in
- **Touch Support**: Pinch-to-zoom and touch panning on mobile
- **Minimize Button**: Easy return to grid view

### 📱 Responsive Design
- **Desktop**: 3x2 grid layout
- **Tablet**: 2x3 grid layout  
- **Mobile**: Single column layout with optimized controls
- **Touch-Friendly**: Optimized for touch devices

### 🎯 Smart Features
- **Auto-Recovery**: Automatically recovers from video errors
- **Stuck Detection**: Detects and corrects stuck videos
- **Sync Monitoring**: Continuous monitoring of video synchronization
- **Error Handling**: Graceful handling of video loading issues

## Camera Layout

The viewer displays 6 synchronized camera feeds:

1. **Latura.E-S** - East-South camera
2. **Latura.V2-S** - V2-South camera  
3. **Latura.V1-N** - V1-North camera (Master timeline)
4. **Colt.SV-N** - Colt SV-North camera
5. **Colt.SE-V** - Colt SE-Vertical camera
6. **Poarta-N** - Gate-North camera

## Usage

### Basic Controls
- **Spacebar**: Play/Pause
- **Left Arrow**: Rewind 15 seconds
- **Right Arrow**: Forward 15 seconds
- **Click Camera**: Zoom to fullscreen
- **Double-click/Tap**: Toggle zoom level
- **Mouse Wheel**: Zoom in/out (when zoomed)
- **Drag**: Pan around (when zoomed)

### Mobile Controls
- **Tap Camera**: Zoom to fullscreen
- **Double-tap**: Toggle zoom level
- **Pinch**: Zoom in/out
- **Drag**: Pan around when zoomed

## Technical Details

### Synchronization
Each camera has a precise time offset to ensure perfect synchronization:
- Latura.E-S: +3.15s
- Latura.V2-S: +0.55s  
- Latura.V1-N: 0s (Master)
- Colt.SV-N: +2.4s
- Colt.SE-V: +3.35s
- Poarta-N: +12.1s

### Timeline
- **Duration**: 10 minutes (11:25:00 - 11:35:00)
- **Start Position**: 11:30:20 (5 minutes 20 seconds in)
- **Visual Timeline**: Color-coded scrubber with red zone indicators

### Browser Compatibility
- **Modern Browsers**: Chrome, Firefox, Safari, Edge
- **Mobile Browsers**: iOS Safari, Chrome Mobile
- **Video Format**: MP4 with H.264 codec
- **No Dependencies**: Pure HTML, CSS, and JavaScript

## File Structure

```
nts-cctv-viewer/
├── index.html          # Main application file
├── README.md           # This file
├── .gitignore          # Git ignore rules
├── Colt.SE-V.mp4       # Camera feed 1
├── Colt.SV-N.mp4       # Camera feed 2
├── Latura.E-S.mp4      # Camera feed 3
├── Latura.V1-N.mp4     # Camera feed 4 (Master)
├── Latura.V2-S.mp4     # Camera feed 5
└── Poarta-N.mp4        # Camera feed 6
```

## Getting Started

1. **Clone or Download** the project files
2. **Place Video Files** in the same directory as `index.html`
3. **Open** `index.html` in a modern web browser
4. **Start Viewing** - the application will automatically load and synchronize all videos

### Requirements
- Modern web browser with HTML5 video support
- MP4 video files in the same directory
- No server required - runs entirely in the browser

## Development

### Adding New Cameras
1. Add the video file to the project directory
2. Update the HTML structure in `index.html`
3. Add the camera offset to the `syncOffsets` object
4. Update the grid layout CSS if needed

### Customizing Synchronization
Edit the `setupSyncOffsets()` method to adjust timing:
```javascript
const offsets = {
  'Camera.Name': offsetInSeconds,
  // Add your camera offsets here
};
```

### Styling
The application uses CSS Grid for layout and CSS custom properties for theming. Main style sections:
- `.video-grid`: Grid layout configuration
- `.video-container`: Individual camera containers
- `.controls`: Playback control styling
- `@media` queries: Responsive breakpoints

## Troubleshooting

### Videos Not Loading
- Ensure video files are in the same directory as `index.html`
- Check that video files are valid MP4 format
- Verify browser supports HTML5 video

### Sync Issues
- The application automatically corrects sync issues
- If problems persist, check video file integrity
- Ensure all videos have the same duration

### Performance Issues
- Close other browser tabs to free up memory
- Use a modern browser for best performance
- Consider reducing video quality for mobile devices

## License

This project is provided as-is for educational and demonstration purposes.

## Support

For issues or questions:
1. Check the browser console for error messages
2. Verify all video files are present and valid
3. Test in a different browser
4. Ensure you have a stable internet connection

---

**Note**: This viewer is designed for synchronized CCTV footage analysis.