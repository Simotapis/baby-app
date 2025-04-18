# Weather Dashboard React Application

A full-featured weather dashboard application built with React that allows users to:
- View current weather and forecasts for any location
- Save favorite locations
- Customize display settings
- Visualize weather data through interactive charts
- Export weather data in multiple formats

## Features

- **Navigation between pages**: Using React Router for seamless navigation
- **API Integration**: Connection to OpenWeatherMap API for real-time weather data
- **Data Persistence**: User preferences and saved locations stored in localStorage
- **Form Validation**: All user inputs are validated to ensure data integrity
- **Data Visualization**: Interactive charts using Recharts library
- **Export Functionality**: Export weather data as CSV, JSON, or PDF
- **Responsive Design**: Works on all screen sizes

## Installation

1. Clone the repository
   ```bash
   git clone [repository-url]
   cd weather-dashboard
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add your OpenWeatherMap API key
   ```
   REACT_APP_WEATHER_API_KEY=your_api_key_here
   ```

4. Start the development server
   ```bash
   npm start
   ```

## Required Dependencies

```json
{
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-router-dom": "^6.14.0",
    "recharts": "^2.7.2"
  }
}
```

## Project Structure

```
weather-dashboard/
├── public/
├── src/
│   ├── assets/
│   │   └── images/
│   ├── components/
│   │   ├── common/
│   │   │   ├── ErrorMessage.js
│   │   │   ├── ExportButton.js
│   │   │   └── LoadingSpinner.js
│   │   ├── layout/
│   │   │   ├── Header.js
│   │   │   └── Sidebar.js
│   │   └── features/
│   │       ├── ForecastChart.js
│   │       ├── ForecastTable.js
│   │       ├── LocationSearch.js
│   │       ├── WeatherCard.js
│   │       └── WeatherDataVisualizations.js
│   ├── context/
│   │   └── WeatherContext.js
│   ├── hooks/
│   │   └── useLocalStorage.js
│   ├── pages/
│   │   ├── Dashboard.js
│   │   ├── ForecastDetails.js
│   │   ├── SavedLocations.js
│   │   └── Settings.js
│   ├── services/
│   │   └── weatherApi.js
│   ├── utils/
│   │   ├── exportUtils.js
│   │   └── themeUtils.js
│   ├── App.js
│   └── index.js
└── package.json
```

## How to Use

1. **Dashboard**: The main page shows current weather information and a brief forecast
2. **Search**: Enter a city name in the search box to get weather data for that location
3. **Save Locations**: Click "Save Location" to add a city to your favorites
4. **View Saved Locations**: Access all your saved cities from the sidebar
5. **Settings**: Customize units (metric/imperial) and toggle dark mode
6. **Export Data**: Use the export buttons to download weather data in your preferred format

## API Integration

The application uses the OpenWeatherMap API for fetching weather data. The relevant API endpoints are:

- Current Weather: `/weather`
- 5-Day Forecast: `/forecast`

## Data Visualization

The application provides multiple visualizations for weather data:

- Temperature trends (line chart)
- Humidity levels (area chart)
- Wind speed and gusts (bar chart)
- Pressure readings (line chart)
- Weather type distribution (pie chart)

## Extending the Application

To add more features to this application:

1. **Additional Weather Data**: Extend the API service to fetch more data points
2. **User Authentication**: Add login/register functionality to sync preferences across devices
3. **Weather Alerts**: Implement notification systems for severe weather
4. **Location Detection**: Add geolocation support for automatic local weather
5. **Historical Data**: Add functionality to view past weather conditions

## License

MIT
