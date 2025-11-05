# Virtual Card - Provincial Guide

A beautiful virtual business card for Gonzalo Emilio Frías Ojeda, a tour guide in Torres del Paine, Patagonia.

## Features

- 📇 Professional vCard with contact information
- 🌤️ Real-time weather forecast for Torres del Paine
- 💱 Live USD-CLP exchange rate converter
- 🛏️ Real-time availability tracker
- 🏷️ Weekly offers and promotions
- 🏔️ List of tour services
- 💳 Payment and booking options
- 📱 Mobile-responsive design

## Dynamic Data Widgets

### 1. Weather Forecast

The vCard includes a weather forecast widget powered by **OpenWeatherMap API**, which displays:
- Current weather conditions
- 5-period forecast (3-hour intervals)
- Temperature in Celsius
- Weather descriptions in Spanish
- Wind speed in km/h
- Weather icons

**Note**: API keys in client-side code are visible to users. For personal use with the free tier, this is acceptable. For production use with sensitive data, consider a backend proxy.

### 2. Exchange Rate Converter (USD-CLP)

Live currency exchange rate widget using **ExchangeRate-API** (free tier):
- Real-time USD to Chilean Peso conversion
- Interactive calculator
- Auto-updates with latest rates
- No API key required for basic tier

#### API Information
- **Service**: [ExchangeRate-API](https://www.exchangerate-api.com/)
- **Free Tier**: 1,500 requests/month
- **No credit card required**
- **Automatic fallback** to demo data if unavailable

### 3. Availability Dashboard

Real-time service availability tracker showing:
- Tours available this week
- Bed/accommodation capacity
- Group size limits
- Animated counters for visual appeal

**Customization**: Update availability numbers in the JavaScript section of `index.html`:

```javascript
animateCounter('tours-available', 8, 1500);      // 8 tours available
animateCounter('beds-available', 24, 1500);      // 24 beds available
animateCounter('group-capacity', 12, 1500);      // 12 people per group
```

### 4. Weekly Offers System

Dynamic promotional offers section featuring:
- Discount badges and percentages
- Original and sale prices
- Savings calculator
- Direct WhatsApp booking links
- Easy-to-update offer data

**Updating Offers**: Edit the `offers` array in `index.html`:

```javascript
const offers = [
    {
        title: 'Trekking Base Torres',
        discount: '15% OFF',
        description: 'Tour completo con guía experto',
        originalPrice: 85000,
        salePrice: 72250,
        available: true,
        badge: 'Popular'
    },
    // Add more offers...
];
```

## Excel VBA Integration

These widgets can be integrated with Excel for business analytics:

### Example VBA Macros

#### 1. Fetch Exchange Rate to Excel

```vba
Sub GetExchangeRate()
    Dim http As Object
    Dim json As Object
    Set http = CreateObject("MSXML2.XMLHTTP")
    
    http.Open "GET", "https://api.exchangerate-api.com/v4/latest/USD", False
    http.send
    
    Set json = JsonConverter.ParseJson(http.responseText)
    Range("A1").Value = "USD to CLP"
    Range("B1").Value = json("rates")("CLP")
End Sub
```

#### 2. Update Availability Dashboard

```vba
Sub UpdateAvailability()
    ' Read from your booking system
    Range("A2").Value = "Tours Available"
    Range("B2").Value = 8  ' Update this from your database
    
    Range("A3").Value = "Beds Available"
    Range("B3").Value = 24
    
    Range("A4").Value = "Group Capacity"
    Range("B4").Value = 12
End Sub
```

#### 3. Generate Weekly Offers Report

```vba
Sub GenerateOffersReport()
    Dim offers As Collection
    Set offers = New Collection
    
    ' Add offers to collection
    Dim offer1 As New Dictionary
    offer1.Add "title", "Trekking Base Torres"
    offer1.Add "discount", "15% OFF"
    offer1.Add "price", 72250
    offers.Add offer1
    
    ' Export to sheet
    Dim i As Integer
    For i = 1 To offers.Count
        Range("A" & i).Value = offers(i)("title")
        Range("B" & i).Value = offers(i)("discount")
        Range("C" & i).Value = offers(i)("price")
    Next i
End Sub
```

## Setting Up APIs

### Weather Forecast API

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
