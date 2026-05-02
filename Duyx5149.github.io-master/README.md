# Yixuan Du — Personal Homepage

Personal academic homepage for **Yixuan Du (杜奕轩)**.

🔗 Live at: [https://duyx5149.github.io](https://duyx5149.github.io)

## How to Update Content

All content is stored in **`data.json`** — just edit this file to update your homepage. No need to touch `index.html`.

### `data.json` Structure

| Section | What to edit |
|---|---|
| `profile` | Name, title, affiliation, email, bio, social links, photo path |
| `news` | Add/remove news items with `date` and `content` (supports HTML) |
| `publications.papers` | Add papers with title, authors, venue, tags, links, badge, note |
| `publications.filters` | Category buttons (must match `tags` in papers) |
| `education` | Degree, school, date range |
| `internship` | Title, organization, supervisor, date range |

### Adding a New Paper

Add a new object to the `publications.papers` array:

```json
{
  "title": "Your Paper Title",
  "authors": "Author A, <me>Your Name</me>, Author B",
  "venue": "ICML 2027",
  "tags": ["Graph Neural Networks"],
  "thumbnail": "images/paper-icml27.png",
  "badge": "Oral",
  "note": "",
  "links": [
    { "label": "PDF", "url": "https://..." },
    { "label": "Code", "url": "https://github.com/..." }
  ]
}
```

- Wrap your name in `<me>...</me>` to make it bold
- `badge` shows a red tag (e.g., "Oral", "Spotlight") — leave `""` if none
- `note` shows a red note below links — leave `""` if none
- `thumbnail` is optional — leave `""` to show placeholder

### Adding Social Links

Add to `profile.social`. Supported icons: `scholar`, `github`, `linkedin`, `twitter`.

```json
{ "name": "LinkedIn", "icon": "linkedin", "url": "https://linkedin.com/in/..." }
```

## File Structure

```
├── index.html      # Template (reads from data.json, rarely needs editing)
├── data.json       # ✏️ All content lives here — edit this!
├── images/
│   └── profile.png # Profile photo
├── .nojekyll       # Tells GitHub Pages to skip Jekyll
└── README.md
```

## Deployment

1. Fork this repo as `<your-username>.github.io`
2. Edit `data.json` with your info
3. Replace `images/profile.png` with your photo
4. Push — your site goes live at `https://<your-username>.github.io`

## License

MIT License — feel free to use and adapt.
