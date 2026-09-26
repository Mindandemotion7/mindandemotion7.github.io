Network Map — interactive web viewer and dataset (built 2026-09-25 PT)

OPEN IT
  Double-click index.html. It is fully self-contained (all code, styles and data are inside the file),
  works offline, and makes no network requests. It also works as a static page on any web host.
  Use a current Chrome / Edge / Firefox (WebGL required).

WHAT IT SHOWS
  3,942 entities (people + organizations) and 1,586 cited relationships:
  1,119 from the Obsidian vault (OCR of screenshots + notes) and 467 from X posts.
  Every citation has a review status:
    verified  (green)  - the source states it as extracted
    corrected (blue)   - the source states it, but the machine reading was fixed; the original reading is shown
    alleged   (orange) - not confirmed by the source as extracted (hedged, implied, surname-only, garbled, mis-paired)
  X-post relationships are drawn as purple curved edges (their status is shown in the side panel).
  Co-mentions (names appearing in the same source only) are NOT drawn; they are in data/co_mentions.csv.
  Nothing here asserts wrongdoing or a conflict of interest.

HOW TO USE
  - Search box: type 2+ letters of a name or alias; Enter or click a suggestion.
  - Click a node: its neighbourhood is highlighted and a side panel lists its connections grouped by type,
    with status badges and the quoted evidence (screenshot file name, or clickable X post link + date).
  - Click an edge: shows that relationship's evidence. Click empty space to clear.
  - Filters: status, origin (vault / X), node type, relationship type, hide isolated nodes.
  - Overlap finder: people who share organizations via cited ties (respects the filters).

DATA FILES (data/)
  graph.json          nodes + edges (with citations) + precomputed layout x/y, X mentions, ambiguous names
  nodes.json/.csv     id, name, type, org_type, aliases, source (vault/x/both), degree, cluster, note_path, ...
  edges.json/.csv     id, source, target, type, status, status_counts, origin, citations
                      (citation id, snippet, source file or X URL + date, "originally read as" for corrected)
  network_map.gexf    for Gephi (layout, colours; X edges marked dashed)
  co_mentions.csv     optional co-mention pairs (vault sources and X posts) - not part of the main graph
  CSV files are UTF-8 with BOM so Excel shows accented names correctly.
  note_path is relative to the Obsidian vault root.
