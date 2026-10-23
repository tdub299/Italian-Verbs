# Il Presente

A browser app for learning Italian present-tense verbs for travel: restaurants, cafés and bars, shops, talking about plans, and following conversations around you.

- **Patterns:** the 10 rules behind present-tense conjugation (-are/-ere/-ire, -isc- verbs, the irregular "boot", piacere, modal verbs).
- **Verbs:** 53 everyday verbs with full tables, notes and example sentences.
- **Phrases:** 116 sentences grouped by situation, with text-to-speech.
- **Practice:** conjugation drills, fill-the-gap, full-sentence translation, listening comprehension, and open writing tasks with model answers.

## Run it

It's one static file with no build step. Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

Progress is saved in your browser's local storage. Claude grading of free-form answers only works when the page is opened as a claude.ai artifact; everywhere else the app shows model answers instead.

## Editing

All content lives in the `<script>` block of `index.html`:

- `VERBS`: infinitive, English, family (`are`/`ere`/`ire`/`isc`/`irr`/`refl`), irregular forms, tags, note. Regular forms are generated.
- `S`: practice sentences `[scene, verb, person 0-5, Italian, English, accepted alternatives, hint]`.
- `FREE`: open writing tasks `[scene, task, model answer]`.
