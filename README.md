#  Dev-Detective
# Live URL: https://prodesk-it-3rd.vercel.app/

**Dev-Detective** is a GitHub user search application that utilizes the GitHub API to fetch and display developer profiles in real-time. It features a robust search functionality and a "Battle Mode" to compare two developers head-to-head.

##  Features

This project was built in three difficulty levels, culminating in a full-featured application:

### Level 1: Core Search
- **User Search:** Fetch user data (Avatar, Bio, Join Date, Portfolio) via the GitHub API.
- **Error Handling:** Gracefully handles non-existent users (404 errors) with UI feedback.
- **Loading States:** Visual feedback while data is being fetched.

### Level 2: Deep Dive
- **Repository List:** Fetches and displays the top 5 most recently updated repositories.
- **Deep Linking:** Repositories link directly to GitHub.
- **Date Formatting:** ISO dates converted to human-readable format (e.g., "25 Jan 2023").

### Level 3: Battle Mode ⚔️
- **Comparison Arena:** A dedicated tab to input two usernames simultaneously.
- **Parallel Fetching:** Uses `Promise.all()` to fetch data for both users concurrently for optimal performance.
- **Winner/Loser Logic:** Compares users based on **Follower Count** and visually highlights the winner (Green) and loser (Red).

##  Tech Stack

- **HTML5:** Semantic structure.
- **CSS3:** Custom "Dev-Theme" styling with CSS Variables (Dark Mode).
- **JavaScript (ES6+):**
  - `async/await` for asynchronous operations.
  - `fetch` API for network requests.
  - `Promise.all` for parallel execution in Battle Mode.
  - DOM Manipulation for dynamic UI updates.

## ⚙️ How to Run

Since this project uses vanilla HTML/CSS/JS, no build step or package manager (npm/yarn) is required.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/dev-detective.git](https://github.com/your-username/dev-detective.git)
