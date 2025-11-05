# Virtual Card - Provincial Guide

A beautiful virtual business card for Gonzalo Emilio Frías Ojeda, a tour guide in Torres del Paine, Patagonia.

## Features

- 📇 Professional vCard with contact information
- 🌤️ Real-time weather forecast for Torres del Paine
- 🏔️ List of tour services
- 💳 Payment and booking options
- 📱 Mobile-responsive design

## Weather Forecast Feature

The vCard includes a weather forecast widget powered by **OpenWeatherMap API**, which displays:
- Current weather conditions
- 5-period forecast (15 hours ahead)
- Temperature in Celsius
- Weather descriptions in Spanish
- Wind speed in km/h
- Weather icons

### Setting Up the Weather API

#### Free API Key (Recommended)

1. Visit [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up for a free account
3. Go to your API keys section
4. Copy your API key
5. Open `index.html` and replace `YOUR_API_KEY_HERE` with your actual API key:

```javascript
const API_KEY = 'your_actual_api_key_here';
```

**Note on Security**: API keys placed in client-side JavaScript are visible to users. For personal use with the free tier (1,000 calls/day), this is acceptable. For production applications with sensitive data or higher usage, consider implementing a backend proxy to keep your API key secure.

#### Free Tier Benefits
- ✅ Up to 1,000 API calls per day
- ✅ 5-day/3-hour forecast data
- ✅ Current weather data
- ✅ No credit card required

### Demo Mode

If no API key is configured, the weather widget automatically displays demo weather data typical for Torres del Paine, allowing you to see the functionality immediately.

## How to Use

1. Clone or download this repository
2. Open `index.html` in a web browser
3. (Optional) Configure your OpenWeatherMap API key for real-time weather data

## Technologies Used

- HTML5
- CSS3 (with CSS Grid and Flexbox)
- Vanilla JavaScript (ES6+)
- Font Awesome icons
- OpenWeatherMap API

## Benefits of Weather Integration

Adding weather forecasts to the vCard helps:
- Keep customers engaged longer on the page
- Provide valuable information for trip planning
- Demonstrate professionalism and attention to detail
- Increase booking likelihood by helping customers plan ahead

## Customization

To customize the location for weather data, edit the coordinates in `index.html`:

```javascript
const lat = -51.0;  // Latitude for Torres del Paine
const lon = -73.0;  // Longitude for Torres del Paine
```

## License

This is a personal vCard project for Gonzalo Emilio Frías Ojeda.
