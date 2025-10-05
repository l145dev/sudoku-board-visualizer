# Sudoku Board Visualizer

> [!NOTE]
> This was developed to make visualizing a sudoku board easier for [Valid Sudoku (Neetcode)](https://neetcode.io/problems/valid-sudoku?list=neetcode150) problem. Written in spaghetti code and minimal error handling!

A tiny, dependency-free web app that renders a 9x9 Sudoku board from a JSON-style input. Open `index.html` in your browser, paste or edit a 9x9 array of strings in the textarea, and click "Update board" to redraw the grid.

## Features

- Renders a 9x9 Sudoku board using plain HTML/CSS/JavaScript.
- Empty cells are represented by `.` in the input and shown as blank cells in the UI.
- Simple, copy-paste-friendly input format (JSON array of arrays of strings).
- No build step or server required — just open the file locally.

## Files

- `index.html` — the complete app (UI, styles, and script) in a single file.

## Input contract (what the app expects)

- A 9x9 array (array of 9 arrays, each with 9 string values).
- Each inner value should be a string: a digit like `"1"`..`"9"` or `"."` for empty cells.
- Example (the default in the textarea):

```
[
	["1", "2", ".", ".", "3", ".", ".", ".", "."],
	["4", ".", ".", "5", ".", ".", ".", ".", "."],
	[".", "9", "1", ".", ".", ".", ".", ".", "3"],
	["5", ".", ".", ".", "6", ".", ".", ".", "4"],
	[".", ".", ".", "8", ".", "3", ".", ".", "5"],
	["7", ".", ".", ".", "2", ".", ".", ".", "6"],
	[".", ".", ".", ".", ".", ".", "2", ".", "."],
	[".", ".", ".", "4", "1", "9", ".", ".", "8"],
	[".", ".", ".", ".", "8", ".", ".", "7", "9"]
]
```

## How to use

1. Open the project folder and double-click `index.html` or open it from your browser.
2. Edit the JSON in the textarea to match your board (use `.` for empty cells).
3. Click the "Update board" button to redraw the board.

Try it (PowerShell):

```powershell
Start-Process .\index.html
```

Or, if you use VS Code, install the "Live Server" extension and click "Open with Live Server" for live reload.

## Behavior and validation

- The page attempts to clean simple formatting issues (extra spaces, trailing commas before `]`) before parsing.
- If JSON.parse fails, an alert is shown: "Invalid board format. Please check your input." Check the browser console for details.
- The app does not currently validate full 9x9 constraints (it assumes the input is a 9x9 array). Malformed sizes or non-string values may render incorrectly or throw parsing errors.

## Implementation notes

- Single-file app: `index.html` contains the HTML, CSS, and JavaScript.
- Minimal DOM manipulation: the script builds table rows and cells dynamically.
- Styling is intentionally simple and dark-themed.

## License

No license.

Feel free to use, adapt, or improve this small visualizer.

## Contact

- **Author:** Aryan Shah
- **Email:** [aryan.shah@l145.be](mailto:aryan.shah@l145.be)
- **GitHub:** [l145dev](https://github.com/l145dev/)
- **LinkedIn:** [Aryan Shah](https://www.linkedin.com/in/aryan-shah-l145/)
