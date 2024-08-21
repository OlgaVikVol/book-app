# 📚 Book Library Application

## 🚀 Overview

This project is a **Book Library application** that allows users to search for books and manage their favorite books. The application is built with vanilla JavaScript, following a modular approach using ES6 modules. It leverages the Open Library API to search for books and dynamically updates the UI based on user interactions.

## ✨ Features

- **🔍 Book Search:** Users can search for books using the Open Library API.
- **❤️ Favorites Management:** Users can add and view their favorite books.
- **📱 Responsive UI:** The application provides a responsive user interface for a seamless user experience.
- **🧩 Modular Architecture:** The application is organized into reusable components and views.

## 🗂 Project Structure

The project structure follows a modular architecture, organizing components and views in separate folders.

```plaintext
src/
│
├── components/
│   ├── card-list/
│   │   └── card-list.js
│   ├── card/
│   │   └── card.js
│   ├── header/
│   │   └── header.js
│   └── search/
│       └── search.js
│
├── common/
│   └── view.js
│
└── views/
    ├── favorites-view.js
    └── main-view.js
```

## 🧱 Components
-  CardList: Renders a list of books.
-  Card: Renderы a book.
-  Header: Displays the application header.
-  Search: Provides the search bar for querying books.
  
## 🌄 Views
-  FavoritesView: Manages and displays the user's favorite books.
-  MainView: Handles the main search functionality and displays search results.

## 🛠️ Common
-  AbstractView: Base class for all views, providing common functionality like setting the page title and managing the main app container.

## 💻 Installation

Install dependencies:

`npm install`

Run the application:

`npm start`

This will start the application using live-server and open it in your default browser.

## 🛠 Usage
- 🔍 Search for Books

Enter a search query in the search bar on the main page.
The application will fetch and display results from the Open Library API.
You can add books to your favorites.
- ❤️ View Favorites
  
Navigate to the "Favorites" page to view your saved books.
- 🗃️ State Management
  
The application uses the onChange library to handle state changes. It automatically re-renders components when the state is updated, providing a reactive user interface without the need for a more complex state management library.

## FavoritesView
The FavoritesView class extends AbstractView and renders the user's favorite books. It listens for changes in the favorites state and re-renders the view when favorites are updated.

## MainView
The MainView class handles the search functionality. It manages the search query and book list in its state, triggering API requests and re-rendering the view when the search results are updated.

## 🎨 CSS and Styling
The application’s styles are compiled using rollup-plugin-import-css. All styles are bundled into a single bundle.css file, which is located in the dist directory. 
This ensures that no extra folders or versioned CSS files are generated during the build process.

To modify or add styles, update the relevant CSS files in the src directory and recompile using the npm run build command.

## 📦 Build Process
This project uses Rollup for bundling. All JavaScript and CSS files are bundled into the dist folder. To build the project, run:

`npm run build`

This command will bundle your JavaScript and CSS files into the dist directory, ready for deployment.
