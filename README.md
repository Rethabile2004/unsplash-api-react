# Unsplash Image Gallery

A responsive React application that allows users to search and view high-quality images from Unsplash. It features dark mode support, global context management, and efficient data fetching using React Query.

## Figma Design

View the design prototype on [Figma](https://www.figma.com/file/O2MaAAlr4nznh7m53azatL/Unsplash-images?node-id=0%3A1&t=cYDOCgqOs9IX2If0-1)

## Getting Started

### Setup

```bash
npm install
npm run dev
```

## Project Structure

### Components

- `ThemeToggle`: Handles dark mode switching.
- `SearchForm`: Captures user input for image search.
- `Gallery`: Displays fetched images.

All components are rendered in `App.jsx` and managed via global context.

## Features

### Dark Theme Support

- State variable `isDarkTheme` toggles between light and dark modes.
- `toggleDarkTheme` function updates the theme state.
- Icons from React Icons (sun and moon) are used in `ThemeToggle`.
- `.dark-theme` class is added/removed from the `body` element based on theme state.
- CSS variables define background and text colors for both themes.
- Media query detects system preference for dark mode.

### Search Functionality

- `SearchForm` includes a text input and submit button.
- On submit, the input value is logged and used to query Unsplash.
- `searchValue` state is stored in `context.jsx`.

### Unsplash API Integration

- Sign up at [Unsplash Developers](https://unsplash.com/developers) to obtain an API key.
- Register an app and use public authentication.
- Use the search endpoint to fetch images.
- Test API endpoints using Thunder Client (VS Code extension).

### Data Fetching with React Query

- `useQuery` is used in `Gallery` to fetch images.
- `searchValue` is included in the `queryKey` to trigger re-fetching.
- React Query Dev Tools are installed for debugging and inspection.

### Theme Persistence

- User's theme preference is stored in `localStorage`.
- JavaScript checks system preference for dark mode on initial load.

### Environment Variables

- Store your Unsplash API key in `.env` file.
- Ensure `.env` is listed in `.gitignore`.

### Deployment

- Deploy the app to Netlify.
- Set environment variables in Netlify dashboard to enable API access.

## Styling

- CSS variables and transitions are used for smooth theme switching.
- Additional styles can be added to enhance UI components.

## Code Snippets

### Toggle Dark Theme

```js
const body = document.querySelector('body');
body.classList.toggle('dark-theme', isDarkTheme);

// Alternative
document.body.classList.toggle('dark-theme', isDarkTheme);
```

### Form Elements Access

```js
const searchValue = e.target.elements.search.value;
```

### React Query Notes

- `useQuery` caches results to reduce API calls.
- `queryKey` ensures data is re-fetched when search input changes.

### Vite Environment Setup

- Create a `.env` file for sensitive keys.
- Example:
  ```
  VITE_UNSPLASH_API_KEY=your_api_key_here
  ```

