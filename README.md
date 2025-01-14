# 🎬 MovieDock

A responsive React application that allows users to search for movies using the OMDB (Open Movie Database) API. Search for your favorite movies, view details, ratings, and more!

## ✨ Features

- Search movies by title
- View detailed movie information
- Responsive design for all devices
- Movie posters and ratings display
- Advanced search filters
- Loading states and error handling
- Infinite scroll for search results

## 🚀 Live Demo

[Add your live demo link here]

![MovieFinder Screenshot](/path-to-your-screenshot.png)

## 🛠️ Built With

- React.js
- Create React App
- React Hooks
- Axios
- CSS Modules
- OMDB API
- React Icons
- React Router (for detailed movie pages)

## 📋 Prerequisites

- Node.js (version 14 or later)
- npm/yarn
- OMDB API key

## 🔑 API Setup

1. Visit [OMDB API](http://www.omdbapi.com/)
2. Request an API key
3. Create a `.env` file in the root directory
4. Add your API key:
```env
REACT_APP_OMDB_API_KEY=your_api_key_here
```

## ⚙️ Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/movie-finder.git
```

2. Navigate to project directory:
```bash
cd movie-finder
```

3. Install dependencies:
```bash
npm install
# or
yarn install
```

4. Start the development server:
```bash
npm start
# or
yarn start
```

## 📁 Project Structure

```
movie-finder/
├── public/
├── src/
│   ├── components/
│   │   ├── Header/
│   │   ├── MovieCard/
│   │   ├── SearchBar/
│   │   ├── MovieDetails/
│   │   └── LoadingSpinner/
│   ├── pages/
│   │   ├── Home/
│   │   ├── MoviePage/
│   │   └── NotFound/
│   ├── hooks/
│   │   └── useDebounce.js
│   ├── services/
│   │   └── api.js
│   ├── utils/
│   ├── App.js
│   └── index.js
└── README.md
```

## 💻 Usage

```jsx
// Example API service
const searchMovies = async (query) => {
  try {
    const response = await axios.get(`${API_URL}?apikey=${API_KEY}&s=${query}`);
    return response.data;
  } catch (error) {
    console.error('Error searching movies:', error);
    throw error;
  }
};

// Example component
function MovieCard({ movie }) {
  return (
    <div className="movie-card">
      <img src={movie.Poster} alt={movie.Title} />
      <h3>{movie.Title}</h3>
      <p>{movie.Year}</p>
    </div>
  );
}
```

## 🌟 Key Features Implementation

### Search Functionality
- Debounced search input
- Error handling for API calls
- Loading states

### Movie Details
- Comprehensive movie information
- Ratings from multiple sources
- Cast and crew details

### Responsive Design
- Mobile-first approach
- Fluid layouts
- Optimized images

## 🔍 Available Scripts

```bash
# Start development server
npm start

# Build for production
npm run build

# Run tests
npm test

# Eject from Create React App
npm run eject
```

## 📱 Environment Support

- Modern browsers
- Mobile devices
- Tablets
- Desktop

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/NewFeature`)
3. Commit changes (`git commit -m 'Add NewFeature'`)
4. Push to branch (`git push origin feature/NewFeature`)
5. Create a Pull Request

## 📈 Future Enhancements

- [ ] User authentication
- [ ] Watchlist functionality
- [ ] Movie recommendations
- [ ] Advanced filtering options
- [ ] Personal ratings and reviews
- [ ] Social sharing features

## 🐛 Troubleshooting

**API Issues**
- Verify API key is correct
- Check API call limit
- Confirm network connectivity

**Build Issues**
- Clear npm cache
- Update dependencies
- Check node version

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 👏 Acknowledgments

- OMDB API for movie data
- React community
- Create React App team
- [Add other acknowledgments]

