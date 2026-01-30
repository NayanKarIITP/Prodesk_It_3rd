#  Project Workflow: Human Core + AI Assist

**Development Split:**
* **70% Human:** Project structure, HTML skeleton, CSS styling, and core DOM manipulation logic.
* **30% AI:** Advanced asynchronous patterns (`Promise.all`), API error handling refinement, and specific algorithm implementation for "Battle Mode."

This document records the specific prompts used to bridge the gap between the basic implementation and the final Level 3 features.


## 1. Refining the Data (Level 2)
*Context: I had the basic API fetch working and displaying raw JSON data, but the dates were unreadable and I needed to sort repositories.*

**Prompt:**
> "I have a JavaScript function fetching GitHub user data. The date comes back as `2023-01-25T12:00:00Z`, which looks bad on the UI.
>
> 1. Write a small helper function to convert this ISO string into a format like '25 Jan 2023'.
> 2. Also, how do I modify my fetch URL to get the user's repositories sorted by the 'latest update' instead of the default order?"


## 2. Implementing "Battle Mode" (Level 3)
*Context: I built the UI for the 'Battle' tab and the input forms, but I wasn't sure how to handle two API requests efficiently at the exact same time.*

**Prompt:**
> "I am building a 'Battle Mode' where two users are compared. I currently have a function `getUserData(username)`.
>
> I need to run this function for two different users simultaneously when the 'Fight' button is clicked.
>
> Please show me how to use `Promise.all` to fetch both users at once. If *either* user doesn't exist, the whole operation should fail and show an error."


## 3. Winner Logic & Dynamic Styling
*Context: I had the data for both users, but needed a clean logic to determine the winner and apply the green/red classes I wrote in my CSS.*

**Prompt:**
> "I have two user objects, `user1` and `user2`, returned from the API.
>
> Write a logic block to compare them based on `followers`.
> - If User 1 has more followers, add the CSS class `.winner` to their card and `.loser` to User 2.
> - Handle the reverse case.
> - Return the HTML string for both cards so I can inject it into my container."


## 4. Debugging & Cleanup
*Context: The app was working, but if I searched for a user that didn't exist, the console threw an uncaught error.*

**Prompt:**
> "My `async/await` function crashes the app when the GitHub API returns a 404 error.
>
> Wrap this existing fetch code in a `try...catch` block so that it updates the UI with a 'User Not Found' message instead of freezing the page." spinner that appears during fetch requests and disappears afterwards.
> 3. Consolidate CSS into a single `<style>` block and JS into a `<script>` block for a single-file solution."
