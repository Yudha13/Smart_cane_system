# Smart Cane System — Dashboard Demo

Static, responsive dashboard preview for Netlify. This is a UI prototype only.

## Deploy to Netlify
1. Open Netlify and choose **Add new site → Import an existing project**.
2. Connect GitHub and select `Yudha13/Smart_cane_system`.
3. The repository-level `netlify.toml` sets the base directory to `demo-dashboard`, leaves the build command empty, and publishes the current directory.
4. Deploy the site.

Alternatively, drag and drop the `demo-dashboard` folder into Netlify Drop.

## Interactive sections
- Overview — operational snapshot and trend chart.
- Soil Monitoring — node readings with zone/status filters.
- Weather Station — simulated AWS readings and station health.
- Device Network — node inventory, detail actions, and simulated refresh.
- Data History — device filter and CSV export.
- Alerts & Events — acknowledge individual alerts or all alerts.
- System Overview — architecture and offline-first data flow.
- Settings — editable preferences, notification toggles, simulation parameters, save/reset using browser local storage.

## Important
All displayed readings, node identities, locations, alerts, weather values and infrastructure statuses are fictional demo data. No sensor, Raspberry Pi, LoRaWAN gateway, server, authentication or production API is connected. Settings are stored only in the current browser. Do not use the displayed values for operational decisions.
