# Tempestius 🌩️

**Conquer the elements, one forecast at a time.**

Tempestius is a blazing-fast weather dashboard built with **Next.js 15**, designed to deliver accurate weather forecasts while leveraging the **4 levels of caching** for optimal performance and user experience.

---

## 🌟 Features

- **Search Weather by City**: Instantly fetch current weather conditions for any city worldwide.
- **Favorites Management**: Save your favorite cities for quick access.
- **Cached Results**: Utilize browser, server-side, and client-side caching for fast and efficient weather data retrieval.
- **Recent Searches**: View previously searched cities with cached data.
- **Dynamic and Static Rendering**:
  - Frequently accessed data is pre-rendered using **ISR**.
  - On-demand rendering for lesser-used data with **SSR**.

---

## 🚀 Tech Stack

- **Frontend**: [Next.js 15](https://nextjs.org/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) for responsive and modern UI.
- **Data Fetching**: [SWR](https://swr.vercel.app/) for client-side caching and revalidation.
- **Backend API**: Next.js API routes for server-side caching.
- **External API**: [OpenWeatherMap](https://openweathermap.org/api) for weather data.
- **Server-Side Cache**: Redis (or an in-memory store).

---

## ⚡ Caching Layers Implemented

1. **CDN Caching**:
   - Static assets served via CDN with optimal caching strategies.

2. **Browser Caching**:
   - User preferences (e.g., favorite cities) stored in `localStorage`.
   - HTTP headers like `Cache-Control` ensure efficient caching for API responses.

3. **Server-Side Caching**:
   - Redis caching to reduce calls to external APIs.

4. **Client-Side Caching**:
   - SWR for caching and re-fetching API data on the client.

---

## 🎯 Getting Started

### Prerequisites

- **Node.js** (v16 or later)
- **Redis** (optional, for server-side caching)
- An API key from [OpenWeatherMap](https://openweathermap.org/api).

---

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/bryan936M/tempestius.git
   cd tempestius

2. Install dependencies:

   ```bash
   yarn install

3. Run unit tests for components:

   ```bash
   yarn run test
   
4. Create a .env.local file in the root directory and add the following:

   ```bash
   NEXT_PUBLIC_WEATHER_API_KEY=your_openweathermap_api_key
   REDIS_URL=your_redis_connection_url (optional)

5. Run the development server:

   ```bash
   yarn run dev

6. Open your browser at <http://localhost:3000>.

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

## 🛠️ Usage

1. Search Weather

   - Enter a city name in the search bar to fetch the current weather.
  
2. Manage Favorites

   - Click the “Save to Favorites” button to save a city.
   - Access saved cities from the “Favorites” section.
  
3. View Recent Searches

   - Cached weather data for your recent searches will be displayed automatically.

## 📚 Roadmap

- Add 7-day weather forecasts with visual charts.
- Push notifications for severe weather alerts.
- Dark mode toggle for improved accessibility.
- Multi-language support.

## 🛡️ License

  This project is licensed under the MIT License.
