# Globe Data Visualization

An interactive 3D globe visualization showing data points for different countries using Globe.gl.

## Features

- **Interactive 3D Globe**: Navigate around a realistic Earth globe
- **Country Data Points**: Visual markers for each country in your dataset
- **Animated Connections**: Dynamic arcs connecting related countries with flowing animations
- **Color-coded by Count**: 
  - 🔴 Red: High count (50+)
  - 🟢 Teal: Medium count (10-49)  
  - 🔵 Blue: Low count (1-9)
- **Smart Connection Algorithm**: 
  - Major countries (50+ count) connect globally
  - Regional proximity connections (< 3000km)
  - Hub connections for medium-traffic countries
- **Hover Information**: Detailed tooltips for both points and connections
- **Click to Focus**: Click any point or connection to center the globe
- **Auto-rotation**: Gentle automatic rotation of the globe
- **Pulsing Animation**: Points pulse subtly to draw attention
- **Flowing Arcs**: Animated dashed lines showing data flow between countries

## Data

The visualization includes data for 63 countries with the following information:
- Country name
- Count value
- Geographic coordinates (latitude, longitude)
- Smart-generated connections between countries

Total countries: 63
Total count: 829
Dynamic connections: Generated based on proximity and traffic volume

## How to Run

### Method 1: Python Server (Recommended)
```bash
python3 server.py
```
This will start a local server on port 8000 and automatically open your browser.

### Method 2: Direct File Opening
You can also try opening `index.html` directly in your browser, though some browsers may block external resources when opening local files.

### Method 3: Any HTTP Server
If you have Node.js installed:
```bash
npx http-server
```

Or if you have PHP installed:
```bash
php -S localhost:8000
```

## Controls

- **Mouse drag**: Rotate the globe
- **Mouse wheel**: Zoom in/out
- **Click on points**: Center the globe on that country
- **Click on connections**: Center the globe between connected countries
- **Hover over points**: See detailed country information
- **Hover over connections**: See connection details and distance

## Technical Details

- Built with [Globe.gl](https://github.com/vasturiano/globe.gl)
- Uses Three.js for 3D rendering
- Responsive design that works on desktop and mobile
- No external dependencies beyond the Globe.gl CDN

## Customization

You can easily modify the visualization by editing `index.html`:

- **Colors**: Change the `getPointColor()` function
- **Sizes**: Modify the `getPointSize()` function  
- **Animation**: Adjust the pulsing effect in the `animate()` function
- **Data**: Replace the `countryData` array with your own dataset
- **Globe appearance**: Modify globe textures and atmospheric effects

## Browser Compatibility

Works in all modern browsers that support WebGL:
- Chrome 9+
- Firefox 4+
- Safari 5.1+
- Edge 12+

## License

This project is open source. The Globe.gl library is MIT licensed.
