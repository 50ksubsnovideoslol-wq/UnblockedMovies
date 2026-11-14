# Unblocked movies

Independent cinema, short films, and original documentaries curated for effortless browser streaming.

Generated with CineForge. This is a complete, standalone movie streaming website project.

## Folder Structure

```
CineForge-Website/
├── index.html               # Homepage (Hero, Recent, Most Viewed, Recommended, Categories)
├── movies.html              # Full catalog with instant search & category filtering
├── most-viewed.html         # Ranked Most Viewed chart & popularity insights
├── recommendations.html     # Personalized "Recommended For You" page
├── movie.html               # Dedicated HTML5 MP4 video player & related movies
├── assets/
│   ├── css/style.css        # Customized dark cinematic theme
│   └── js/
│       ├── app.js           # Catalog loader, search routing, click & view tracking
│       ├── movies.js        # Page renderers & video playback view recorder
│       └── recommendations.js # AI & local fallback recommendation engine
├── images/posters/          # Movie poster images
├── videos/uploaded-movies/  # MP4 video files
├── data/movies.json         # Movie metadata & site configuration
├── server/index.js          # Optional Node.js + Express backend (views + Groq AI proxy)
├── package.json
└── .env.example
```

## Quick Start (Recommended: Full Server Mode)

Running the included Node.js server enables HTTP Range streaming for large MP4 files, persistent server-side view counts, and secure Groq AI recommendations without exposing any API key in frontend JavaScript.

1. Install dependencies:
   ```bash
   npm install
   ```
2. (Optional) Configure Groq AI recommendations:
   ```bash
   cp .env.example .env
   ```
   Open `.env` and add your `GROQ_API_KEY`.
3. Start the website:
   ```bash
   npm start
   ```
4. Open `http://localhost:4000` in your browser.

## Static Preview Mode

You can also serve this folder with any static HTTP server (such as `npx serve .` or Nginx/Netlify/Vercel). In static mode:
- View counts are persisted in browser `localStorage`.
- Search, playback, Most Viewed ranking, and local theme-matching recommendations work automatically without a backend.


