# Arbuthnot Books — writing and previewing

## Run locally

```sh
bundle exec jekyll serve
```

Open http://localhost:4000. Stop the preview with Ctrl-C. If dependencies have not
been installed, run `bundle install` first. A build without a server is
`bundle exec jekyll build`. Restart the preview after changing `_config.yml`.

## Start writing in Obsidian

The three section folders are `notes`, `places`, and `people`. Each contains an
`index.md` listing all books and one folder per book. Open, for example,
`notes/event-horizon/index.md` to add a short introduction or a complete note
below the properties. The corresponding Places and People pages work the same
way. The website adds the section buttons and return/sample/purchase links.

These index pages are real Markdown files, so they can be edited in Obsidian.
The automatic lists and navigation appear in the Jekyll preview. Use standard
Markdown links rather than Obsidian-only wikilinks for published content.

The book identifier is its filename in `_books`, without `.md`, for example
`event-horizon`. Keep identifiers stable: they determine the section addresses.
For a new book, add its three section index files using an existing book as a
model, changing title, book_id and permalink. Top-level book lists update
automatically.

## Add a separate Note

Create `notes/event-horizon/topic-name.md`, for example, with:

```yaml
---
layout: companion-entry
title: A short explanatory title
book_id: event-horizon
permalink: /notes/event-horizon/topic-name/
---
```

Write the note below the properties. It will be listed automatically on that
book's Notes page. These are undated explanations, separate from `_posts`.
Existing dated essays retain their original addresses and are listed at
`notes/archive/index.md`. They are not automatically mixed into the spoiler-free
book sections.

## Add a Person

Write each portrait inside its book's folder, for example
`people/palace-of-tears/steve-percival.md`. Use the Person template:

```yaml
---
layout: book-person
title: Steve Percival
kind: Fictional character
person_id: steve-percival
book_id: palace-of-tears
permalink: /people/palace-of-tears/steve-percival/
---
```

Write that book's portrait below the properties. It is listed automatically
on the book's People page. Its footer links to that book's Notes, Places,
People, sample and purchase page.

- `book_id` is the book filename from `_books`, without `.md`.
- `person_id` is a stable name such as `steve-percival`. Reuse it when writing
  about the same person in another book.
- `kind` is `Fictional character` or `Historical / real person`.
- `permalink` must be unique and match the intended book/person address.

For another book, create another file in that book's folder and change
`book_id` and `permalink`. There are no `book_ids` or `book_anchors` properties
on the new portraits. Memoir portraits belong in `people/me-neither/`.

The existing `_people` files now serve only as selection pages for old links
such as `/people/entries/steve-percival/`. They list the available book-specific
portraits using `person_id`, without combining their prose. Existing book
anchors still land on the corresponding choice. You do not need an `_people`
file for a new person; the book's People list finds its portrait automatically.
If you want a selection page too, copy an existing `_people` file and change
its title, kind and person_id.

## Add a Place

Existing shared entries stay in `_places`, with their original public addresses.
Create `_places/place-name.md` with:

```yaml
---
layout: place
title: Place name
place_id: place-name
---
```

Write the sketch below the properties. Add `place-name` to the appropriate
book's `entity_places` list in `_books`. This supplies both its book-specific
Places listing and the place's “Appears in” links. `_data/places.yml` holds
optional naming/alias metadata used by the existing source-data helper;
Obsidian may hide this YAML file. It is not required just to create a page.

All places remain available at `places/all/index.md`. The source-data helper
can replace a book's place list: do not run it casually over curated choices.

## Editorial approach

- Select significant people, places and ideas; aim initially for 75–150 words.
- Use Publisher Toolkit reports as evidence, then write for a curious reader.
- Describe characters as first encountered. Avoid later relationships,
  revelations, outcomes, and hints about eventual significance.
- Distinguish fictional people from real people; verify historical claims.
- Keep evidence references and unfinished report extracts under `editorial/`,
  which is excluded from the generated website. Do not place private evidence
  in HTML comments: comments in published pages remain visible in page source.
- Existing essays and book descriptions have been preserved, not certified as
  spoiler-free. Review them separately if applying that policy site-wide.

## Review and publish

Build and inspect locally, including navigation, sample links and phone-width
layout. Empty book sections currently say that material is being prepared;
replace these with selected pieces before publishing the expansion.

Netlify builds are currently stopped by the site owner. Git commits and pushes
remain separate, deliberate steps. When the batch is ready, activate builds in
Netlify and trigger a deploy. Activating builds alone does not trigger one.
The generated `_site` directory is ignored by Git; publish the source files.

## Obsidian templates

The `Template` folder contains `Note.md`, `Person.md` and `Place.md`.
Set the built-in Templates plugin's template folder to `Template` in Obsidian.
Create an empty file in its destination folder, then use Insert template.
Replace the example property values and body text before publishing.

- **Note:** save in `notes/<book-id>/`. Set `book_id` to the book filename
  without `.md`, and give `permalink` a unique address such as
  `/notes/event-horizon/zettelkasten/`.
- **Person:** save in `people/<book-id>/`. Set `book_id`, `person_id`, and the
  matching `permalink`. Set `kind` to `Fictional character` or
  `Historical / real person`. Each file covers one book only.
- **Place:** save in `_places/`. Use a stable identifier for `place_id` and
  add that exact identifier to each relevant book's `entity_places` list.
  Optionally add `parent` for an existing parent place identifier.

Template files are excluded from the generated website. Keep source evidence
and working commentary in `editorial/`, rather than in the published entries.

## The Thieves of Time sequence

Edit `series/the-thieves-of-time/index.md` for the introduction and forthcoming
book notice. Published books are listed automatically when their `_books` file
has `series: the-thieves-of-time`; `order` sets their reading order. Covers and
short descriptions come from each book's existing `cover` and `lede` properties.
The book layout adds a link back to the sequence overview.

When Double Exposure has its own book page, give it the same series identifier
and `order: 4`, create its Notes, Places and People pages, and update the
forthcoming paragraph on the sequence page.

## Saved anchor experiment and migration

The local tag `anchor-experiment` preserves commit `bde2dec`. The refactoring
is on `codex/book-specific-people`. The original prose is recoverable from that
tag; the migration preserves it in book-specific files.

`editorial/people-migration.md` describes the assignments and outstanding
portraits. `editorial/people-migration.json` records each source, destination
and body checksum. Neither report is included in the website build.

Separating pages prevents accidental scrolling into another book's portrait.
It does not make the existing prose spoiler-free within its own book: editorial
revision remains separate from this structural change.
