# Smart Farm Dashboard (React + Vite + Tailwind)

## Quick start

1. Extract the ZIP and `cd` into the folder.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run dev server:
   ```bash
   npm run dev
   ```
4. Build:
   ```bash
   npm run build
   ```

## Usage with ESP32 WebSocket server

- Upload the provided WebSocket server sketch to your ESP32. After connecting to WiFi, open Serial Monitor to find the IP printed (e.g., `192.168.1.120`).
- In the dashboard, enter the WebSocket URL e.g. `ws://192.168.1.120:81` and click **Connect**.
- The dashboard will display live sensor readings sent as JSON by the ESP32. Example JSON the ESP32 should send:
```json
{
  "soilMoisture": 45,
  "temperature": 28.3,
  "humidity": 65,
  "waterLevel": 70,
  "pumpOn": false
}
```

## Weather API Key

The dashboard uses OpenWeatherMap for weather & forecast. The API key you provided has been embedded into the project. To change it, edit `src/App.jsx` and update the `WeatherCard` apiKey prop.
