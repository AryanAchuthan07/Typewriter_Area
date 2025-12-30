# Typewriter Arena

Typewriter Arena is a clean, offline-first typing test application that measures **Words Per Minute (WPM)** and **accuracy**, with local user profiles and per-user leaderboards.

The project is intentionally simple, privacy-focused, and fully client-side.

---

## Overview

Typewriter Arena is designed to feel professional and distraction-free. All data is stored locally on the user’s device, and the entire application runs from a single HTML file.

There is no backend, no tracking, and no external dependencies.

---

## Features

* Typing test with real-time WPM and accuracy calculation
* Early test completion when the passage is fully typed
* Local username-based sign-in (no passwords)
* Per-user leaderboard storing best 3 scores
* Fully offline support
* Responsive, minimal UI

---

## Running the Project

### Option 1: Open Directly

Clone the repository and open the HTML file:

```bash
git clone https://github.com/YOUR_USERNAME/typewriter-arena.git
cd typewriter-arena
open index.html
```

### Option 2: Local Server (Optional)

```bash
python3 -m http.server
```

Then navigate to:

```
http://localhost:8000
```

---

## Project Structure

```
.
├── index.html   # Entire application (HTML, CSS, JavaScript)
└── README.md    # Documentation
```

The application is intentionally kept in a single file for clarity and portability.

---

## How It Works

### Sign-In

* Users enter a username (up to 16 characters)
* The username is saved locally in the browser
* Each username maintains its own independent scores

### Gameplay

* The timer starts on the first keystroke
* Characters are validated in real time
* WPM and accuracy update continuously

### Test Completion

A test ends when:

* The timer reaches zero, or
* The full passage is typed correctly

Once completed, input is disabled and the score is saved automatically.

---

## Leaderboard Logic

* Scores are stored using `localStorage`
* Each user has a separate leaderboard
* Only the top three scores are retained
* Scores are sorted by highest WPM

---

## WPM and Accuracy Calculation

WPM calculation:

```
WPM = (charactersTyped / 5) / minutesElapsed
```

Accuracy calculation:

```
accuracy = correctCharacters / typedCharacters
```

---

## Data and Privacy

* All data is stored locally in the browser
* No network requests are made
* No analytics or external services are used

Clearing browser storage will remove all users and scores.

---

## Deployment

The project can be deployed as a static site on any platform that serves HTML files.

For Vercel:

1. Push the repository to GitHub
2. Import the project into Vercel
3. Select framework preset: Other
4. Deploy

---

## License

MIT License

---

## Notes

This project is well-suited for portfolios, internships, and learning exercises. It demonstrates clean UI design, client-side state management, and thoughtful handling of user data.
