# JIP website event updates

## Source policy — Jaroslav, 2026-11-02

- Official JIP Facebook is authoritative for automatic event updates:
  https://www.facebook.com/profile.php?id=61578444160974
- Google Drive and the JIP Sheet are reference material only. Before applying any
  website change based on them, show Jaroslav the concrete proposed changes and
  obtain his explicit confirmation. A prior automatic synchronization is not approval.
- Independently verified Facebook changes may proceed without that confirmation.
- If Facebook cannot be read, preserve existing future events. Do not silently
  substitute Drive as the source of truth or invent missing details.

## Preserve the full upcoming program

- Select the featured performance by the earliest upcoming event date in
  Europe/Prague, never by which Facebook post was published most recently.
- Treat the featured card and Další hraní as one chronological, deduplicated set.
  When replacing the featured card, retain its former event in Další hraní if it
  is still upcoming. Preserve known titles, times, venues and verified links.
- An event missing from a Sheet or partial Facebook feed is not cancelled.
  Remove a future event only with explicit Facebook evidence of cancellation or
  a direct user instruction. Remove past events after their local event date.
- Before publishing, compare the before/after future-event sets. Reject any
  unexplained deletion. Check that the earliest event is featured, all later
  events remain listed once, and JSON-LD matches the visible featured event.
- Run git diff --check and validate JSON-LD and affected JavaScript. Verify the
  deployed page after publishing.

## Regression reference

The October 13, 2026 update c1ae7f9 replaced Superscene (November 10) with
Adventní detektivka (December 6) without retaining the November performance.
Commit e2e2103 restored it. Later publication on Facebook must never by itself
replace an earlier upcoming performance.
