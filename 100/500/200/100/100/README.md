# 100 - OBS Scene Compositions

a. Add NDI Source:
   - Click '+' in Sources
   - Select 'NDI Source'
   - Choose your BirdDog stream from dropdown
   - Set Resolution to match source (1080p)

b. Configure Virtual Camera:
   - Tools → VirtualCamera
   - Start Virtual Camera
   - Set output resolution to 1080p

## Scene 1: Professional Presentation

Layout Hierarchy:

1. Background (1920x1080 neutral gradient)
2. Webcam Feed (16:9 aspect ratio)
3. iPad Overlay
4. Lower Third Banner (optional)
   
## Scene 2: Interactive Teaching

Layout Hierarchy:

1. iPad Feed (Main display)
2. Webcam (Picture-in-Picture)
3. Custom Frame
4. Status Indicators
   
## Scene 3: Discussion Mode

Layout Hierarchy:

1. Split Screen Base
2. Webcam (Left)
3. iPad (Right)
4. Transition Overlays

## OBS Advanced Settings

### Video Settings
Base Resolution: 1920x1080
Output Resolution: 1920x1080
Downscale Filter: Lanczos (best quality)
FPS: 60

### Advanced Settings
Process Priority: High
Video Memory: 2048 MB
Color Format: NV12
Color Space: 709
Color Range: Partial
Recommended Filters
Webcam Source:

### Noise Suppression

### Color Correction
Gamma: 1.1
Contrast: 1.1
Brightness: 0.0
Saturation: 1.2
iPad Source:

### Sharpness
Sharpness: 2
Color Correction
Saturation: 1.1
Gamma: 1.0

### NDI Source Settings
Sync: Network (low latency)
Hardware Acceleration: Enabled
Low Bandwidth Mode: Disabled
Buffer: 1-2 frames
