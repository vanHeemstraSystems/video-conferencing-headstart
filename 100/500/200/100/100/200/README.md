# 200 - Performance Optimization

## Source Buffer Settings

For Both NDI Sources:<br />
- Sync: Network
- Hardware Acceleration: Enabled
- Low Bandwidth Mode: Disabled
- Buffer: 1-2 frames

## Scene Buffer

Right-click scene → Properties:<br />
- Buffer Size: 2 frames
- Enable Performance Mode

## Per-Scene Settings

1. Code Focus Scene<br />
   - Display Capture: 60 FPS
   - High Quality scaling

2. Terminal Scene<br />
   - Display Capture: 30 FPS
   - Performance mode

3. Drawing Scene<br />
   - VSCode: 30 FPS
   - iPad: 60 FPS
