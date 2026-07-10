# 🎬 RateIT - Movie Review Application

**RateIT** is a fully-featured, native Android application built with Java and SQLite. It provides a complete, self-contained ecosystem for users to discover movies, leave reviews, and manage personalized watchlists without requiring an internet connection.

This project was developed to demonstrate core Android development fundamentals, including relational local database management (SQLite), user session handling, and complex UI implementations using `RecyclerViews` and Material Design.

## ✨ Key Features

* **🔐 User Authentication:** Secure Sign-up and Log-in flows with session persistence (using `SharedPreferences`).
* **🍿 Movie Catalog & Filtering:** Browse a rich catalog of movies, search by title, or filter dynamically by genre.
* **⭐ Interactive Ratings & Reviews:** Users can leave star ratings and write text reviews for individual movies. 
* **❤️ Personalized Lists:** Dedicated UI flows to add/remove movies to **Favorites** or **Watch Later** lists.
* **👤 User Profiles:** A dynamic profile dashboard tracking user statistics (total reviews, favorites, and saved movies).

## 🛠️ Tech Stack

* **Language:** Java
* **Environment:** Android Studio / Gradle
* **Database:** SQLite (Local Persistence)
* **Image Loading:** Glide
* **UI Components:** `RecyclerView`, Material Design, Custom Dialogs (`dialog_review.xml`)

## 🗄️ Database Architecture

The application relies on a custom `MoviesDBHelper` to manage a fully relational SQLite database. It handles complex queries and data integrity across 5 core tables:

1. `users`: Stores account data (name, email, password, gender, role).
2. `movies`: Stores catalog metadata (title, year, genre, poster, synopsis, aggregate ratings).
3. `reviews`: Links user reviews and individual star ratings to specific movies.
4. `favourites`: A junction table mapping users to their favorite movies.
5. `watch_later`: A junction table mapping users to their saved watch-later list.

## 🚀 Getting Started (Local Setup)

To run this project locally on your machine or Android emulator:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/RateIT-Movie-Review-App.git](https://github.com/YOUR_USERNAME/RateIT-Movie-Review-App.git)
   ```

2.**Open in Android Studio:**
* **Open Android Studio** and select "Open an existing Android Studio project".
* **Navigate** to the cloned folder and select it.

3.**Sync Gradle:**
* Allow Android Studio a moment to build the project and sync the Gradle dependencies (AndroidX, Glide, etc.).

4.**Run the App:**
* Click the green Run (▶) button to launch the app on an Android Emulator or a physical USB-connected Android device.

```📂 Core Project Structure
*/app/src/main/java/com/example/moviesreviewapp/

 MoviesDBHelper.java: The core SQLite engine managing all CRUD operations.

 MainActivity.java: The primary catalog screen handling RecyclerViews and search/filter logic.

 DetailMovie.java: The movie detail screen handling user interactions (rating, saving, reviewing).

 LoginActivity.java & SignupActivity.java: Authentication and session management.

*/app/src/main/res/

 layout/: Contains all XML layouts (Main screen, Detail views, Custom Row items).

 values/: Contains centralized strings, colors, and theme definitions.
```
Developed as a college project to demonstrate native Android development and local database architecture.
