Network Map — interactive web viewer and dataset (built 2026-09-25 PT, connectivity pass)

OPEN IT
  Double-click index.html. It is fully self-contained (all code, styles and data are inside the file),
  works offline, and makes no network requests. It also works as a static page on any web host.
  Use a current Chrome / Edge / Firefox (WebGL required). The file is large (~18 MB); give it a few seconds to load.

WHAT IT SHOWS
  A map for postulating possible conflicts of interest, not proving them.
  3,942 entities (people + organizations) and 61,595 connections:
    stated relationships from the researcher's vault (OCR of screenshots + notes) and X posts: 1,586
    stated relationships found in a second pass over the source text: 42
    same as (probable name variants; both entities kept): 37
    co-mentioned with Jeffrey Epstein (same screenshot / note / X post): 790
    co-mentioned (same screenshot / note / X post): 56,976
    derived shared affiliations (shared board / same employer / co-investor / shared affiliation via an organization): 2,164
  Status: verified (green) = the source states it; corrected (blue) = the source states it but the machine reading was fixed;
  alleged (orange) = not confirmed by the source. Every co-mention, name-variant guess and derived link is alleged unless marked.
  Loose links are straight lines coloured by type: red = co-mentioned with Epstein, grey = co-mentioned, black = same as,
  teal = shared board, brown = same employer, pink = co-investor, light blue = shared affiliation.
  Distance to Jeffrey Epstein: 1 step 831 · 2 steps 2,450 · 3+ steps 508 · not connected 152.
  Nothing here asserts wrongdoing or a conflict of interest.

HOW TO USE
  - Search: type 2+ letters of a name or alias; Enter or click a suggestion.
  - Click a node: its neighbourhood is highlighted and the side panel lists every connection grouped by type, with status and
    quoted evidence (screenshot file name, X post link, or the organization a derived link runs through, with both underlying citations).
  - Filters (all on by default): connection type, distance to Jeffrey Epstein, status, origin, node type, hide isolated nodes.
    Untick "co-mentioned" to declutter.
  - Overlap finder: people who share organizations via cited ties (respects the filters).

DATA FILES (data/)
  graph.json          nodes + connections + layout x/y (co-mention evidence shortened), X mentions
  nodes.json/.csv     id, name, type, org_type, aliases, degree, degree_stated, dist_epstein, cluster, note_path, ...
  edges.json/.csv     every connection: id, category, type, status, origin, via (derived), citations
  co_mentions.csv     every co-mention link with its sources and first quote
  network_map.gexf    for Gephi (colours by type; loose links dashed)
  CSV files are UTF-8 with BOM so Excel shows accented names correctly. note_path is relative to the Obsidian vault root.
