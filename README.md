# The CCC Project

A minimalist website project with film grain aesthetic.

## Project Location
**Full Path:** `/Users/josephdeypalan/Desktop/trae/the-CC-project/`

## Quick Access
- **Open in Finder:** `~/Desktop/trae/the-CC-project`
- **Open in Terminal:** `cd ~/Desktop/trae/the-CC-project`
- **Open in Cursor:** Open this folder in Cursor

## Project Structure

```
the-CC-project/
├── index.html      # Main HTML file
├── styles.css      # CSS styling with film grain effect
├── script.js       # JavaScript functionality
├── README.md       # This file
├── css/            # (Optional) CSS folder
├── js/             # (Optional) JavaScript folder
└── assets/         # (Optional) Images, fonts, etc.
```

## Current Features

- White background with film grain/noise texture
- "Welcome" text in Owners XXWide font
- Clickable "c" linking to Twitter/X profile
- Live development server (port 3000)

## Running the Project

**Start live server:**
```bash
cd ~/Desktop/trae/the-CC-project
npx --yes live-server --port=3000 --open=/index.html
```

**Or simply open `index.html` in your browser**

## Files

- **index.html** - Main HTML structure
- **styles.css** - Styling with gradient, noise effect, and typography
- **script.js** - JavaScript for interactivity (currently minimal)

## Design Preferences & Decisions

### Visual Style
- **Background:** Pure white (no gradients, no colors)
- **Film Grain:** Subtle noise/texture overlay for film aesthetic
- **Typography:** Owners XXWide font (bold, black)
- **Minimalist:** Clean, simple design - no unnecessary elements

### Typography Details
- Font: "Owners XXWide" (installed locally, used in Premiere Pro)
- Weight: Bold (700)
- Color: Black
- Size: 4rem
- Letter spacing: -0.02em (tighter, less "sticky")
- Text: "Welcome" (capital W)

### Interactive Elements
- **Clickable "c":** The "c" in "Welcome" links to Twitter/X: https://x.com/deyjoeyo?s=21
- **No hover effects:** Link should look identical to regular text (no visual changes on hover)
- **Cursor:** Default cursor (not text cursor) - stays as arrow pointer even over text
- **Link behavior:** Opens in new tab (`target="_blank"`)

### Technical Preferences
- Prefers clean, organized file structure
- Wants live updates during development
- Uses fonts installed locally (like Premiere Pro fonts)
- Minimal JavaScript - keep it simple

### Development Notes
- Started as blank white page
- Added film grain texture for aesthetic
- Font changed from Helvetica Medium to Owners XXWide
- Made "c" clickable but invisible (no visual indication it's a link)
- Removed all hover effects and cursor changes for clean look

## Notes

- Font: Owners XXWide (installed locally, also used in Premiere Pro)
- Live server auto-reloads on file changes
- Project saved at: `/Users/josephdeypalan/Desktop/trae/the-CC-project/`
- User prefers minimal, clean design with subtle effects
