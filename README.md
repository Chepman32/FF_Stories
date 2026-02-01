# FableFlow Stories Repository

This repository contains remote stories for the FableFlow app.

## Structure

```
FF_Stories/
├── manifest.json                    # Index of all stories with versions
├── stories/
│   ├── story-remote-001/
│   │   ├── story.json              # Full story data
│   │   └── i18n/
│   │       ├── en.json             # English translations
│   │       ├── ru.json             # Russian translations
│   │       └── ...                 # Other languages
│   └── story-remote-002/
│       └── ...
└── README.md
```

## Adding a New Story

1. Create a new folder in `stories/` with a unique ID (e.g., `story-remote-003`)
2. Add `story.json` with the full story data
3. Add translations in `i18n/` folder for each supported language
4. Update `manifest.json` with the new story metadata

### manifest.json Entry

```json
{
  "id": "story-remote-003",
  "version": "1.0.0",
  "title": "Story Title (for preview)",
  "genre": "fantasy",
  "isPremium": false,
  "thumbnailUrl": "https://images.unsplash.com/...",
  "availableLanguages": ["en", "ru"],
  "lastUpdated": "2026-02-01T12:00:00Z",
  "size": 50000
}
```

### story.json Format

```json
{
  "id": "story-remote-003",
  "title": "The Adventure",
  "description": "A thrilling adventure...",
  "coverImageUrl": "https://images.unsplash.com/...",
  "thumbnailUrl": "https://images.unsplash.com/...",
  "author": "Author Name",
  "genre": "fantasy",
  "involvement": "medium",
  "estimatedDuration": 15,
  "isPremium": false,
  "version": "1.0.0",
  "createdAt": "2026-02-01",
  "updatedAt": "2026-02-01",
  "totalNodes": 10,
  "totalEndings": 3,
  "startNodeId": "node-1",
  "nodes": [...]
}
```

### i18n/{lang}.json Format

```json
{
  "title": "Translated Title",
  "description": "Translated description",
  "author": "Translated Author Name",
  "nodes": {
    "node-1": {
      "title": "Node Title",
      "narration": "Node narration text...",
      "choices": {
        "choice-1": {
          "text": "Choice text",
          "description": "Optional description"
        }
      }
    }
  }
}
```

## Supported Genres

- fantasy
- scifi
- mystery
- romance
- horror
- adventure
- detective

## Supported Languages

en, ru, es, de, fr, pt, ja, zh, ko, uk, it, ar, hi, nl, pl, tr

## GitHub Pages Setup

1. Go to repository Settings
2. Navigate to Pages
3. Set Source to "Deploy from a branch"
4. Select "main" branch and root folder
5. Save

The stories will be available at: `https://chepman32.github.io/FF_Stories/`
