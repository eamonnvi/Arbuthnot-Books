# Book-specific People migration

Checkpoint: `anchor-experiment` at `bde2dec` (local tag).
Working branch: `codex/book-specific-people`.

## Prose assignments

- Steve Percival and Grace Mitchell: explicit Event/Horizon and Palace of Tears
  sections moved to their respective book folders. Their existing section
  headings are retained, as is all prose.
- Angie Barrett, Ginny Stern, Jon Chapman, Peter Newman and Rob Williams:
  unsectioned material assigned to Event/Horizon based on its narrative and
  end-of-book descriptions. This is an editorial inference, recorded for review;
  it has not been duplicated into later-book portraits.
- Seven single-book people: entire bodies moved to the associated book.
- Corrected `the=parallax-view` to `the-parallax-view` for Grace and Rob when
  creating their book-specific destinations.

No prose was rewritten. Historical/real-person labels were retained. Me Neither's
portraits now reside in its own folder.

## Portraits awaiting text

- Palace of Tears: Angie, Ginny, Jon, Peter and Rob.
- The Parallax View: Angie, Ginny, Grace, Jon, Peter, Rob and Steve.

These twelve pages say “This portrait is being prepared.” They are linked from
the corresponding People indexes so the structure can be tried locally. Fill
or review them before publishing.

## Compatibility

All fourteen existing `/people/entries/<person>/` addresses are selection pages.
They contain no shared biography. Old book anchors point to the appropriate
selection entry; follow its link to reach the new portrait.

The move preserves the supplied prose, including its plot details. It provides
book separation, not a spoiler edit. The original checkpoint remains the source
of truth for comparing text; JSON records provide destination body checksums.
