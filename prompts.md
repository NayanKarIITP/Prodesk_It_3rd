### 2. prompts.md

This file documents the logical steps (or "prompts") one would use to build this application iteratively. This is great for documenting your thought process or for anyone trying to recreate the project using AI assistance.

```markdown
# 🤖 Project Prompts & Development Steps

This document outlines the prompt engineering strategy used to build "Dev-Detective," broken down by the difficulty levels assigned in the mission.

## Phase 1: The Skeleton & Search (Level 1)

**Goal:** Establish the UI structure and basic API fetching.

> **Prompt:** > "Create a vanilla JavaScript application called 'Dev-Detective'. 
> 1. **HTML:** Create a search bar and a main profile card container.
> 2. **CSS:** Style it with a dark 'developer' theme (dark blues, white text).
> 3. **JS:** Write a function that takes a username input, fetches data from `https://api.github.com/users/{username}`, and displays the Avatar, Name, Bio, and Join Date.
> 4. **Requirements:** Handle 404 errors (User not found) effectively."

## Phase 2: Enhanced Data & Formatting (Level 2)

**Goal:** Add repository data and fix formatting issues.

> **Prompt:**
> "Refine the existing code with these additions:
> 1. **Date Formatting:** The API returns dates like `2023-01-25T...`. Create a helper function to convert this to `25 Jan 2023`.
> 2. **Repositories:** After fetching the user, make a *second* API call to `repos_url`. Sort them by 'recently updated' and display the top 5 links below the profile bio.
> 3. **Links:** Ensure the website link and repository names are clickable and open in new tabs."

## Phase 3: "Battle Mode" Architecture (Level 3)

**Goal:** Implement the complex comparison logic and UI toggling.

> **Prompt:**
> "Add a 'Battle Mode' to the application:
> 1. **UI:** Add a toggle switch in the header to swap between 'Search Mode' and 'Battle Mode'.
> 2. **Battle Logic:** In Battle Mode, show two input fields. When 'FIGHT' is clicked, fetch *both* users simultaneously.
> 3. **Performance:** Use `Promise.all` to ensure both requests happen in parallel.
> 4. **Comparison:** Compare their `followers` count. Give the winner a Green border/badge and the loser a Red border with lower opacity.
> 5. **Error Handling:** If either user doesn't exist, fail the whole battle gracefully."

## Phase 4: Refinement & Optimization

**Goal:** Clean up code and ensure responsiveness.

> **Prompt:**
> "Review the code:
> 1. Ensure the CSS is responsive (cards should stack on mobile).
> 2. Add a loading spinner that appears during fetch requests and disappears afterwards.
> 3. Consolidate CSS into a single `<style>` block and JS into a `<script>` block for a single-file solution."