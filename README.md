# Movie Swiper

Swipe right on movies you want to watch and left on the rest. Your picks are saved to a watchlist that stays on your device.

**Live:** https://kontraf.github.io/movie-swiper/

## Where the movies come from

- **Online (TMDB):** when a TMDB API key is set, each round loads 12 movies from a random page of popular movies, with real posters. Movies you already saved never come back, and "Show more movies" does not repeat movies you have seen in the same visit.
- **Built-in list:** 45 movies written into `index.html`. It is used when no key is set, or when TMDB cannot be reached (no internet, wrong key, rate limit). The page tells you which source is in use.

## Enable the online source

1. Create a free account at https://www.themoviedb.org and request an API key under Settings, API.
2. Open `index.html` and put the **API Key (v3)** in the constant near the top of the script:

   ```js
   const TMDB_API_KEY = 'your_key_here';
   ```

3. Commit and push.

The key is visible to anyone who opens the page source, so use a key made only for this project. If it is ever misused, generate a new one in your TMDB settings.

## Details

- The watchlist is stored in the browser (`localStorage`), so it stays on that device and browser.
- Text from the internet is escaped before it is shown.
- Built with HTML, JavaScript and Tailwind CSS (from a CDN). Works with mouse drag, touch and the two buttons.

This product uses the TMDB API but is not endorsed or certified by TMDB.
