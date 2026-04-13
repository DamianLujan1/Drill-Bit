# DRILLBIT

**AI Petroleum Drilling Simulation Engine**

An interactive 3D drilling simulator powered by Claude AI. Control a virtual drilling rig, navigate geological layers, and let AI make real-time safety decisions based on sensor telemetry.

## Features

- **3D Geological Visualization**: Four distinct geological layers (Topsoil, Sandstone, Shale, Oil Reservoir) rendered in real-time with Three.js
- **Real-Time Sensor Simulation**: Pressure, RPM, temperature, mud weight, and depth tracking
- **AI Safety Engineer**: Claude AI analyzes sensor data at layer transitions and issues drilling decisions (GO/SLOW/ABORT)
- **Interactive Controls**: Adjust drill speed, bit pressure, and mud weight via real-time sliders
- **Live Telemetry HUD**: Monitor all drilling parameters with visual status indicators
- **Blowout Simulation**: Dynamic incident scenarios with AI-generated formal incident reports
- **Oil Detection**: Successfully navigate to the oil reservoir at 5000 ft depth
- **Responsive 3D Camera**: Orbit controls with mouse and scroll zoom

## How It Works

1. **Set Parameters**: Use the side panel to configure drill speed (10-100 ft/hr), bit pressure (1000-6000 PSI), and mud weight (8.5-18 ppg)
2. **Start Drilling**: Click "START DRILL" to begin the simulation
3. **AI Decisions**: As you drill through each geological layer, Claude AI analyzes your sensor readings and issues real-time guidance
4. **Monitor Telemetry**: Watch the HUD for pressure spikes, temperature increases, and formation changes
5. **Reach Oil**: Navigate carefully to 5000 ft to strike oil successfully, or trigger a blowout if conditions exceed safety limits

## Technology Stack

- **Three.js**: 3D graphics and rendering
- **Claude AI (Anthropic)**: Real-time decision-making and incident reporting
- **HTML5/CSS3/JavaScript**: UI, styling, and simulation engine
- **WebGL**: Hardware-accelerated 3D graphics

## API Setup

1. Click the ⚙ (gear) icon in the top-right
2. Enter your Anthropic API key (stored locally in localStorage, never transmitted except to Anthropic)
3. API calls are made only during layer transitions and pressure anomalies

## Simulation Mechanics

- **Depth Scale**: 0–5000 ft (visible depth on HUD)
- **Layer Transitions**: AI activates at 800, 2400, and 4200 ft
- **Pressure Dynamics**: Base pressure varies by formation; speed increases risk
- **Temperature Gradient**: Increases 180°F from surface to oil reservoir
- **Blowout Triggers**: Pressure exceeds 5000 PSI or AI aborts drilling

## Controls

- **Mouse Drag**: Rotate 3D view
- **Scroll Wheel**: Zoom in/out
- **Sliders**: Adjust drill parameters in real-time
- **Buttons**: START DRILL, RESET, Save API Key

## File Structure

- `main` (HTML): Complete single-file application with embedded CSS and JavaScript
- `README.md`: This documentation

## Future Enhancements

- Multiple drilling scenarios and mission types
- Real drilling data integration
- Advanced particle effects for blowouts
- Multiplayer drilling simulation
- Historical well data database

---

*DRILLBIT: Where petroleum engineering meets AI safety. Drill responsibly.* ⚙️🪨⛽