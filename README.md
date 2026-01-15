# Wave Claude Forecast

A sleek, modern wave and surf forecast application powered by the Open-Meteo API.

## Features

- 🌊 Real-time wave height, period, and direction
- 🌤️ Weather conditions including wind, temperature, and precipitation
- 📊 48-hour timeline forecast
- 📅 7-day outlook
- ⭐ Save favorite surf spots
- 🎨 Dark, minimalist UI
- 💾 Offline caching support
- 🔊 Optional ambient audio

## Setup & Usage

### Important: Local Web Server Required

**DO NOT** open `wave_claude_forecast.html` directly in your browser using `file://` protocol. Modern browsers block cross-origin API requests from local files for security reasons (CORS).

### Option 1: Python (Recommended)

If you have Python installed:

```bash
# Navigate to the directory
cd /path/to/wave_claude_forecast.html

# Start a local web server on port 8000
python3 -m http.server 8000

# Open your browser to:
# http://localhost:8000/wave_claude_forecast.html
```

### Option 2: Node.js (npx serve)

If you have Node.js installed:

```bash
# Navigate to the directory
cd /path/to/wave_claude_forecast.html

# Start a local web server
npx serve

# Follow the URL shown in the terminal (usually http://localhost:3000)
```

### Option 3: VS Code Live Server

1. Install the "Live Server" extension in VS Code
2. Right-click on `wave_claude_forecast.html`
3. Select "Open with Live Server"

### Option 4: Other HTTP Servers

Any local HTTP server will work:
- PHP: `php -S localhost:8000`
- Ruby: `ruby -run -ehttpd . -p8000`
- Node.js http-server: `npm install -g http-server && http-server`

## How to Use

1. **Search for a location**: Use the search bar at the top
2. **Quick access**: Click on one of the featured surf spots (Pipeline, Nazare, etc.)
3. **View forecast**: See current conditions, surf quality rating, and forecasts
4. **Save favorites**: Click the star icon to save locations for quick access
5. **Adjust settings**: Click the settings icon to change units and preferences

## API Information

This application uses the free Open-Meteo API:
- **Marine Weather API**: Wave data, swell information
- **Weather Forecast API**: Temperature, wind, precipitation
- **Geocoding API**: Location search

No API key is required. The API is free for non-commercial use.

## Troubleshooting

### "Failed to load forecast" or "Network error"

**Problem**: The app can't connect to the Open-Meteo API.

**Solutions**:
1. **Check if you're using a local web server** (not `file://` protocol)
   - Open browser console (F12) and check for CORS errors
   - Look for the warning: "⚠️ Running from file:// protocol"
   - Solution: Use one of the local server methods above

2. **Check your internet connection**
   - The app requires internet to fetch forecasts
   - Cached data will be used if available offline

3. **Check the browser console**
   - Press F12 to open Developer Tools
   - Go to the "Console" tab
   - Look for detailed error messages

4. **Check API status**
   - Visit https://open-meteo.com/ to verify the service is operational

### No search results

- Verify your spelling
- Try searching for larger cities or well-known surf spots
- Check your internet connection

### Blank/white page

- Make sure you're running from a web server (not file://)
- Check the browser console for JavaScript errors
- Try a different browser (Chrome, Firefox, Safari, Edge)

## Browser Console Debugging

The application now includes detailed console logging to help debug issues. To view:

1. Open Developer Tools (F12 or Ctrl+Shift+I / Cmd+Option+I)
2. Go to the "Console" tab
3. You'll see logs like:
   - `Wave Claude Forecast initializing...`
   - `Protocol: http:` (should NOT be `file:`)
   - API request and response details
   - Error messages if something fails

## License

This is a demonstration project using the Open-Meteo free API.

## Attribution

- Powered by [Open-Meteo](https://open-meteo.com/) - Free Weather Forecast API
- Marine Weather API
- Weather Forecast API
- Geocoding API
