# Kari Blogg

Blogg for Kari - AI-resepsjonist som snakker norsk.

## Oppsett

Bloggen bruker Hugo som static site generator og er designet for å matche hovedapplikasjonens design med Pico CSS 2 (Pink theme).

### Utviklingsmiljø

```bash
# Start Hugo dev server
hugo server -D
hugo server -D --bind 0.0.0.0 --port 1313 --baseURL http://localhost:1313

# Bygg produksjonsversjon
hugo
```
Obs: -D inkluderer drafts. Og om en post har dato i framtiden vises den ikke.

### Struktur

- `content/posts/` - Blogginnlegg
- `layouts/` - Hugo templates
  - `_default/baseof.html` - Hovedlayout
  - `_default/list.html` - Liste over blogginnlegg
  - `_default/single.html` - Enkeltinnlegg
  - `partials/` - Header, footer og andre gjenbrukbare deler
- `static/css/` - Custom CSS som matcher Kari-appen
- `public/` - Genererte statiske filer (git-ignored)

### Design

Bloggen bruker:
- **Pico CSS 2 (Pink theme)** - Samme som hovedappen
- **Custom CSS** - Matcher hovedappens layout og fargeskjema
- **Header** - Med logo og navigasjon til hovedsiden
- **Footer** - Med lenker til priser, personvern, etc.

### Legge til nye innlegg

```bash
hugo new content/posts/navn-pa-innlegg.md
```

Eller opprett en fil manuelt i `content/posts/` med følgende frontmatter:

```markdown
---
date: 2025-11-04T12:00:00+02:00
draft: false
params:
    author: Navn
title: "Din tittel her"
description: "En kort beskrivelse"
---

Innledning her (vises i lister)

<!--more-->

## Hovedinnhold

Resten av innlegget...
```

### Deployment

Generer statiske filer med `hugo` og server `public/`-mappen.

## Lenker

- Hovedside: https://heikari.no
- Blogg: https://heikari.no/blogg/

