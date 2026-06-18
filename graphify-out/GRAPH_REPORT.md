# Graph Report - ./  (2026-04-17)

## Corpus Check
- Corpus is ~348 words - fits in a single context window. You may not need a graph.

## Summary
- 11 nodes · 9 edges · 4 communities detected
- Extraction: 78% EXTRACTED · 22% INFERRED · 0% AMBIGUOUS · INFERRED: 2 edges (avg confidence: 0.88)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Tokenization & Scopes|Tokenization & Scopes]]
- [[_COMMUNITY_Core Theme Extension|Core Theme Extension]]
- [[_COMMUNITY_Theme Generation Tools|Theme Generation Tools]]
- [[_COMMUNITY_Project Metadata|Project Metadata]]

## God Nodes (most connected - your core abstractions)
1. `Color Theme Extension` - 4 edges
2. `themes/Try theme-color-theme.json` - 2 edges
3. `Token Colorization` - 2 edges
4. `Scopes` - 2 edges
5. `Try's Syntax Theme` - 2 edges
6. `package.json` - 1 edges
7. `TextMate Themes` - 1 edges
8. `Inspect TM Scopes Command` - 1 edges
9. `Workbench Colors` - 1 edges
10. `Generate Color Theme From Current Settings Command` - 1 edges

## Surprising Connections (you probably didn't know these)
- `Color Theme Extension` --conceptually_related_to--> `Try's Syntax Theme`  [INFERRED]
  vsc-extension-quickstart.md → README.md
- `Try's Syntax Theme` --cites--> `try-theme Extension`  [INFERRED]
  README.md → CHANGELOG.md

## Hyperedges (group relationships)
- **Theme Development Workflow** — vsc_extension_inspect_tm_scopes, vsc_extension_workbench_colors, vsc_extension_generate_color_theme_command [INFERRED 0.80]

## Communities

### Community 0 - "Tokenization & Scopes"
Cohesion: 0.5
Nodes (4): Token Colorization, Inspect TM Scopes Command, Scopes, TextMate Themes

### Community 1 - "Core Theme Extension"
Cohesion: 0.67
Nodes (3): Color Theme Extension, package.json, Workbench Colors

### Community 2 - "Theme Generation Tools"
Cohesion: 1.0
Nodes (2): Generate Color Theme From Current Settings Command, themes/Try theme-color-theme.json

### Community 3 - "Project Metadata"
Cohesion: 1.0
Nodes (2): try-theme Extension, Try's Syntax Theme

## Knowledge Gaps
- **6 isolated node(s):** `package.json`, `TextMate Themes`, `Inspect TM Scopes Command`, `Workbench Colors`, `Generate Color Theme From Current Settings Command` (+1 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Theme Generation Tools`** (2 nodes): `Generate Color Theme From Current Settings Command`, `themes/Try theme-color-theme.json`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Project Metadata`** (2 nodes): `try-theme Extension`, `Try's Syntax Theme`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Color Theme Extension` connect `Core Theme Extension` to `Theme Generation Tools`, `Project Metadata`?**
  _High betweenness centrality (0.289) - this node is a cross-community bridge._
- **Why does `themes/Try theme-color-theme.json` connect `Theme Generation Tools` to `Core Theme Extension`?**
  _High betweenness centrality (0.111) - this node is a cross-community bridge._
- **Why does `Try's Syntax Theme` connect `Project Metadata` to `Core Theme Extension`?**
  _High betweenness centrality (0.111) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `Try's Syntax Theme` (e.g. with `try-theme Extension` and `Color Theme Extension`) actually correct?**
  _`Try's Syntax Theme` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `package.json`, `TextMate Themes`, `Inspect TM Scopes Command` to the rest of the system?**
  _6 weakly-connected nodes found - possible documentation gaps or missing edges._