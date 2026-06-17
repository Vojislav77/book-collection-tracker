## Book Collection Tracker

A lightweight, single-file web application for organizing and managing your personal book library. Everything runs locally in your browser — no server, no database, no dependencies.

<img width="1280" height="640" alt="media" src="https://github.com/user-attachments/assets/dd32418d-b5b6-4a7d-8580-898f7b8629e0" />


## Overview

Book Collection Tracker helps you keep a clean inventory of your books with detailed metadata, visual cover images, and quick search tools. It was designed to be fast, private, and portable: just open index.html and start cataloging.

## Features

    Complete book records: Store book name, author, category, publisher, cover type, language, page count, condition, and cover image
    Inline editing: Click any cell in the table to edit data directly
    Image upload: Click the picture frame to upload a cover photo. Images are resized and stored as data URLs in the browser session
    Smart search: Instant search across title, author, and publisher
    Advanced filtering: Filter by category, condition, and cover type
    Sortable columns: Sort by name, author, category, cover type, pages, or condition
    Custom dropdowns: Add, manage, and remove your own categories, conditions, and cover types. Changes are saved to localStorage
    Undo history: Revert the last change to options or data (up to 20 steps)
    Statistics panel: Live counters for total books, hardcovers, and paperbacks
    CSV export: Export your entire collection to a CSV file with a custom filename
    Responsive design: Works on desktop, tablet, and mobile
    Zero setup: Pure HTML, CSS, and vanilla JavaScript in a single file

## Getting Started

    Download or clone this repository
    Open index.html in any modern browser
    Start adding books with the Add Book button

No installation or build step is required.

## Usage

Adding a book

    Click Add Book
    Fill in the form fields and submit
    The book appears instantly in the table

Editing

    Click any text cell to edit inline, or use the Edit action
    Changes are applied immediately

Adding a cover image

    Click the placeholder frame in the Cover Image column
    Select an image file from your device
    The image is automatically cropped to 300x450

Filtering and searching

    Use the search box at the top for free-text search
    Use the three dropdowns to filter by category, condition, or cover type
    Combine filters for precise results

Managing options

    In any filter dropdown, select Add new to create a custom option
    Select Manage to rename or delete existing options
    Select Undo to revert the last change

Exporting data

    Click Export
    Enter a filename (defaults to book_collection.csv)
    A CSV file containing all current records will download

CSV columns: Book Name, Author, Category, Publisher, Cover Type, Language, Pages, Condition

## Data Storage

    Book data is loaded from the initial dataset included in the HTML file
    Custom categories, conditions, and cover types are persisted in browser localStorage under the key bookCollectionOptions
    Images are stored in memory as base64 data URLs for the current session
    For permanent storage, use the Export function regularly to back up your data

Note: This version does not automatically save book edits to localStorage. To keep data between sessions, export to CSV and re-import by modifying the initial books array in the script, or extend the app with localStorage persistence.

## Customization

The app is built for easy modification:

    Colors and theme: Edit the CSS variables in :root at the top of the style block
    Default categories: Modify the DEFAULT_OPTIONS object in the script
    Sample data: Replace the books array with your own collection
    Favicon: The included favicon.png uses a book tag icon and can be replaced

## File Structure

    /
    ├── index.html # Complete application (HTML, CSS, JS)
    ├── favicon.png # App icon
    └── README.md # This file


## Browser Compatibility

Tested on:
- Chrome 110+
- Edge 110+
- Firefox 115+
- Safari 16+

Requires JavaScript enabled. No external libraries are loaded.

## Privacy

All data stays on your device. The app does not send data to any server, use analytics, or require an account.

## License

This project is released for personal use. You are free to modify and distribute with attribution to the original author.

Copyright 2026 Vojislav Korać

<img width="1372" height="1207" alt="bct" src="https://github.com/user-attachments/assets/9bfebfa2-51f7-4d95-98ba-be79fe887c14" />

## Roadmap Ideas

- Automatic localStorage save for books
- Import from CSV
- Reading status and rating fields
- Dark mode toggle
- PWA support for offline installation
