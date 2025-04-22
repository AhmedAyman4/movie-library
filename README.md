````md
# Movie Library

A React-based movie library application that allows users to search for movies, view trending movies, and explore detailed movie information. The app integrates with **The Movie Database (TMDb)** API and **Appwrite** for backend services.

## Features

- **Search Movies**: Search for movies by title using the TMDb API.
- **Trending Movies**: View a list of trending movies based on search popularity.
- **Debounced Search**: Prevent excessive API calls by debouncing user input.
- **Responsive Design**: Optimized for various screen sizes using TailwindCSS.
- **Appwrite Integration**: Tracks search term popularity and trending movies.

## Tech Stack

- **Frontend**: React, Vite, TailwindCSS
- **Backend**: Appwrite
- **API**: TMDb API

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/movie-library.git
   cd movie-library
   ```
````

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env.local` file in the root directory and add the following environment variables:

   ```env
   VITE_TMDB_API_KEY=<your_tmdb_api_key>
   VITE_APPWRITE_PROJECT_ID=<your_appwrite_project_id>
   VITE_APPWRITE_DATABASE_ID=<your_appwrite_database_id>
   VITE_APPWRITE_COLLECTION_ID=<your_appwrite_collection_id>
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open the app in your browser at `http://localhost:5173`.

## Scripts

- `npm run dev`: Start the development server.
- `npm run build`: Build the app for production.
- `npm run preview`: Preview the production build.
- `npm run lint`: Run ESLint to check for code quality issues.

## Folder Structure

```
myFirstReactApp/
├── src/
│   ├── components/       # Reusable React components
│   │   ├── Search.jsx    # Search bar component
│   │   ├── Spinner.jsx   # Loading spinner component
│   │   └── MovieCard.jsx # Movie card component
│   ├── App.jsx           # Main application component
│   ├── appwrite.js       # Appwrite integration logic
│   ├── main.jsx          # Entry point for the React app
│   ├── index.css         # Global styles
│   └── App.css           # Component-specific styles
├── public/               # Static assets
├── .env.local            # Environment variables
├── vite.config.js        # Vite configuration
├── eslint.config.js      # ESLint configuration
├── package.json          # Project metadata and dependencies
└── README.md             # Project documentation
```

## API Integration

### TMDb API

- **Base URL**: `https://api.themoviedb.org/3`
- **Endpoints**:
  - Search Movies: `/search/movie`
  - Discover Movies: `/discover/movie`

### Appwrite

- **Base URL**: `https://cloud.appwrite.io/v1`
- **Features**:
  - Track search term popularity.
  - Fetch trending movies based on search counts.

## ESLint Configuration

The project uses ESLint with the following plugins:

- `eslint-plugin-react-hooks`: Enforces React Hooks rules.
- `eslint-plugin-react-refresh`: Ensures proper usage of React Fast Refresh.

## TailwindCSS

TailwindCSS is used for styling with custom utilities and layers defined in `index.css`.

## Known Issues

- Ensure valid API keys are provided in `.env.local`.
- Appwrite backend must be properly configured for search tracking.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- [TMDb API](https://www.themoviedb.org/documentation/api) for movie data.
- [Appwrite](https://appwrite.io/) for backend services.
- [Vite](https://vitejs.dev/) for fast development builds.
- [TailwindCSS](https://tailwindcss.com/) for utility-first styling.
