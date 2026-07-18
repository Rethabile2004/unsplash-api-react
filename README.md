
# Unsplash Image Gallery

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![React Query](https://img.shields.io/badge/React_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)

Unsplash Image Gallery is a React-based web application that allows users to search and view high-quality photos from the Unsplash API. It features a responsive layout, dark mode support, global state management with context, and efficient data fetching using React Query.

## Features

- **Search & View Images:** Real-time search to explore the vast collection of Unsplash photos.
- **Dark Mode Support:** Built-in theme toggle to seamlessly switch between light and dark modes.
- **Efficient Data Fetching:** Utilizes **React Query** for caching, background updates, and optimized API requests.
- **Global State Management:** Uses React's Context API (`src/context.jsx`) to manage themes and global states cleanly without prop-drilling.
- **Responsive Design:** Fully responsive layout providing a native-like experience on desktop, tablet, and mobile.

## Getting Started

### Prerequisites

- Node.js (v18 or higher recommended)
- An Unsplash Developer API Key. You can get one at [Unsplash Developers](https://unsplash.com/developers).

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Rethabile2004/unsplash-api-react.git
   cd unsplash-api-react
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory and add your Unsplash API key:
   ```env
   VITE_UNSPLASH_API_KEY=your_access_key_here
   ```

4. **Start the development server:**
   ```bash
   npm run dev
   ```

## Project Structure

- `src/SearchForm.jsx` - The main input component for querying the Unsplash API.
- `src/Gallery.jsx` - Responsive grid component displaying fetched images.
- `src/ThemeToggle.jsx` - Component to toggle Dark/Light mode.
- `src/context.jsx` - Global Context provider managing the theme and app state.

## Built With

- [React](https://reactjs.org/) - UI Library
- [Vite](https://vitejs.dev/) - Next Generation Frontend Tooling
- [React Query](https://tanstack.com/query/v3/) - Data fetching and state synchronization
- [Unsplash API](https://unsplash.com/developers) - Image data source
