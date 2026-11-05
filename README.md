# Ivy PvE — Badlands (JSON content edition)

This package is based on the current `Ivy_PvE-main` website supplied by the owner.
The existing theme, layout, navigation, fonts, colour scheme and artwork are retained.

## Background image confirmation
The supplied `assets/Ivy_Badlands_BG.png` IS already referenced by `assets/style.css` for the main homepage hero background:
`url('Ivy_Badlands_BG.png')`.
Because the stylesheet is in the `assets` directory, this correctly resolves to `assets/Ivy_Badlands_BG.png`.
The square `assets/ivy-badlands.png` remains used for the small header brand image and the subpage banner background.

## Content files
- `data/news.json` — news and announcements
- `data/news-sidebar.json` — News & Updates sidebar quick links and admin note
- `data/items.json` — custom items and categories
- `data/vehicles.json` — vehicle showcase and specifications
- `data/server.json` — server connection details, gameplay overview and rules

The pages read these JSON files in the browser. No database or server-side language is required.

## Add images
- Item images: upload to `assets/items/`, then set `"image": "assets/items/your-image.png"` in `data/items.json`.
- Vehicle images: upload to `assets/vehicles/`, then set `"image": "assets/vehicles/your-image.png"` in `data/vehicles.json`.
- Leave image as an empty string to use the built-in themed placeholder.

## Editing JSON
Keep double quotes around keys and string values. Separate entries with commas. Do not add a comma after the final entry. `news.json`, `items.json` and `vehicles.json` must remain JSON arrays (`[` ... `]`). `news-sidebar.json` is a JSON object: edit the `quickLinks` list to add/remove sidebar links, and change `adminNote.title` or `adminNote.content` to update the admin note. Each quick link has a `label` and `url` (for example, `server.html`).

Item filter category values: `medical`, `clothing`, `tools`, `weapons`.

## Updating GitHub Pages
Upload/replace the files in this package in your existing repository, preserving the folder structure, then commit the changes. Keep your existing repository Pages settings. GitHub Pages will publish the update automatically.

If you have already customised `assets/Ivy_Badlands_BG.png` or `assets/ivy-badlands.png`, keep your preferred image versions when uploading the update.

## Local preview
Opening `index.html` by double-clicking may block JSON fetches. From the website folder, open Command Prompt and run:
`py -m http.server 8000`
Then visit `http://localhost:8000/`.


### Vehicle sections

Vehicles are automatically grouped into sections by the `mod` field in `data/vehicles.json`. Give entries from the same mod the same value (for example `"mod": "Expansion Mod"`). A new section is created automatically for each new mod name. Entries without a `mod` value appear under `Unassigned`.
