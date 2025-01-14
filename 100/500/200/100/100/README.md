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

### 1. Create Base Scene

1. Click '+' in Scenes panel
2. Name it "Interactive Drawing Scene"
3. Optional: Create scene collection named "iPad Overlay Setup"

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
