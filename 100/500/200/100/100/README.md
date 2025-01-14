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

## Initial Scene Creation

### 1. Full Code Scene
1. Click '+' in Scenes panel
2. Name it: "Code Full"
3. Optional: Create scene collection named "Full Code Scene"
4. Sources (Bottom to Top):<br />

1. Background
   - Color: #1E1E1E (VSCode dark theme)
   - Size: 1920x1080

2. Display Capture (Monitor 1)
   - Capture Settings:
     * Display: Monitor 1 (Coding Display)
     * Method: Windows Graphics Capture
   - Transform:
     * Resize to 1920x1080
     * Position: Center
   
3. Camera Small
   - Size: 320x180
   - Position: Bottom Right
   - Filters:
     * Round Corners: 10px
     * Border: 2px white

Layout Properties:
- No dead zones
- Terminal visible
- File explorer accessible

### 2. Split Code and Webcam
1. Click '+' in Scenes panel
2. Name it: "Code Split"
3. Optional: Create scene collection named "Split Code and Webcam"
4. Sources (Bottom to Top):<br />

1. Display Capture (Monitor "VS Code")
   - Transform:
     * Size: 1280x1080
     * Position: Left
   - Crop:
     * Left: 0
     * Right: Adjust to hide unnecessary UI

2. Webcam
   - Transform:
     * Size: 640x1080
     * Position: Right
   - Filters:
     * Border: Left only, 2px white

### 3. Code with Drawing Overlay
1. Click '+' in Scenes panel
2. Name it: "Code Annotate"
3. Optional: Create scene collection named "Code with Drawing Overlay"
4. Sources (Bottom to Top):<br />

1. Display Capture (Monitor "VS Code")
   - Full screen

2. iPad NDI
   - Chroma Key Filter
   - Transform:
     * Size: 1920x1080
     * Position: 0,0

3. Drawing Tools Indicator
   - Text Source
   - Position: Top Right
   - Shows current drawing mode

### 2. Add Sources in Order

Bottom → Top Layer Order:<br/>
1. Background (optional)
2. Webcam NDI Source
3. iPad NDI Source
4. Status Elements (optional)

### Detailed Source Configuration

1. Background (Optional)
   
Add → Color Source:<br/>
- Name: "Solid Background"
- Color: Dark Gray (#222222)
- Size: 1920x1080
  
2. Webcam NDI Source
   
Add → NDI Source:<br/>
- Name: "Main Camera"
- Source Name: [Your BirdDog Stream]
- Transform:
  * Right-click → Transform → Fit to Screen
  * Scale with CTRL+ALT for perfect 16:9

Filters to Add:<br/>
1. Color Correction
   - Saturation: 1.2
   - Contrast: 1.1
   - Brightness: -0.1
   - Gamma: 1.1

2. Sharpen
   - Sharpness: 0.3
     
3. iPad NDI Source
   
Add → NDI Source:<br/>
- Name: "iPad Drawing Layer"
- Source Name: [Your iPad Stream]
- Transform: Fit to Screen

Essential Filters (In Order):

1. Color Correction
   - Saturation: 1.0
   - Contrast: 1.1
   - Gamma: 1.0

2. Chroma Key
   - Key Color Type: Custom
   - Key Color: #00FF00
   - Similarity: 400
   - Smoothness: 80
   - Key Color Spill Reduction: 100
   - Opacity: 100
   - Edge Feather: 2

3. Sharpen
   - Sharpness: 0.2

4. GPU Delay (If needed)
   - Delay: 1-2 frames


## 100 - Advanced Filter Configurations

See [README.md](./100/README.md)

## 200 - Performance Optimization

See [README.md](./200/README.md)

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


## Scene Variations

1. Full Screen Drawing
   
Transform iPad Source:<br />
- Size: 1920x1080
- Position: 0,0
- Crop: None
  
2. Side Drawing Panel

Transform iPad Source:<br />
- Size: 640x1080
- Position: Right
- Add Edge Fade Filter:
  * Edge: Left
  * Smoothness: 20px
    
3. Floating Drawing Window
   
Transform iPad Source:<br />
- Size: 800x600
- Position: Top Right
- Add Round Corner Filter:
  * Corner Radius: 20
  * Feather: 2

### Additional Elements

Status Indicators

Add Text Sources:<br />

1. Drawing Mode Indicator
   - Font: Arial Bold
   - Size: 24px
   - Color: White
   - Position: Top-left

2. Color Palette Reference
   - Add Image Source
   - Size: 100x400
   - Position: Left edge
   - Opacity: 80%

## Advanced Monitor Layouts

### 1. Multi-Panel Development

Name: "Dev Layout"<br />
Regions:<br />

1. Main Code (70% left)
   - Display Capture
   - Crop to show only editor

2. Terminal (30% right top)
   - Display Capture
   - Region crop
   - Transform:
     * Size: 576x540
     * Position: 1344,0

3. File Explorer (30% right bottom)
   - Display Capture
   - Region crop
   - Transform:
     * Size: 576x540
     * Position: 1344,540

4. Camera Overlay
   - Size: 320x180
   - Position: Floating
   - Toggle Hotkey: CTRL+C
   - 
### 2. Tutorial Layout

Name: "Tutorial View"<br />
Regions:<br />

1. Code Editor (60%)
   - Left side
   - Crop unnecessary UI

2. Preview/Browser (40% top)
   - Second monitor capture
   - Transform to fit

3. Webcam (40% bottom)
   - Camera source
   - Picture-in-Picture

4. Drawing Layer
   - Full screen overlay
   - Toggle with hotkey
  
### 3. Debug View

Name: "Debug Mode"<br />
Layout:<br />

1. Main Debug Window (70%)
   - Display Capture
   - Focus on debug panel

2. Variable Watch (30% right)
   - Region capture
   - Auto-scroll enabled

3. Quick Actions Panel
   - Bottom overlay
   - Shows keyboard shortcuts

## OBS Advanced Settings

### Video Settings
Base Resolution: 1920x1080<br/>
Output Resolution: 1920x1080<br/>
Downscale Filter: Lanczos (best quality)<br/>
FPS: 60<br/>

### Advanced Settings
Process Priority: High<br/>
Video Memory: 2048 MB<br/>
Color Format: NV12<br/>
Color Space: 709<br/>
Color Range: Partial<br/>
Recommended Filters<br/>
Webcam Source:<br/>

### Noise Suppression

### Color Correction
Gamma: 1.1<br/>
Contrast: 1.1<br/>
Brightness: 0.0<br/>
Saturation: 1.2<br/>
iPad Source:<br/>

### Sharpness
Sharpness: 2<br/>
Color Correction<br/>
Saturation: 1.1<br/>
Gamma: 1.0<br/>

### NDI Source Settings
Sync: Network (low latency)<br/>
Hardware Acceleration: Enabled<br/>
Low Bandwidth Mode: Disabled<br/>
Buffer: 1-2 frames<br/>
