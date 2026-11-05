---
name: artifact-doc-write
description: Create HTML reading documents with a numbered chapter rail, scroll progress, sans-serif headings, and monochrome body links. Use for an artifact, explainer, walkthrough, report, plan, RFC, or document to screenshare. Not for slide decks, live dashboards, or product UI inside a repository.
---

# Artifact docs

An artifact is a document people read, on a screenshare or from a link. Write it like a spec with plain prose and a clear reading order. It is never a slideshow.

Use [references/template.html](references/template.html) as the starting point. Its visual references are [Linear Method](https://linear.app/method/introduction), [CPU Learn](https://stable.clearsol.network/learn/use-cases), and the [Claude developer blog sidebar](https://claude.dev/blog/solving-code-review-at-anthropic/). Borrow their reading hierarchy. Keep the template's monochrome links.

## Content and copy

Use facts from the user and the supplied or authorized sources. Label assumptions, reconstructions, and outdated material on the page. Do not invent screenshots, quotes, comments, or claims.

Write in a neutral voice unless the user asks otherwise. Use short sentences and plain words. Remove filler, promotional claims, and repeated summaries. Do not add first-person opinions on the user's behalf.

Check links with the available browser or service connector. Report links you could not verify. Do not send private source URLs to public search services.

## Build the document

Copy the template to the session's local scratch directory. Fill in the content and replace the sample title, date, audience, chapter labels, and breadcrumb. Remove controls and sections that do not serve the document. Keep the tokens, fonts, and layout unless the user requests another style.

- Start with a breadcrumb, title, one- or two-sentence introduction, and a line for date, status, and audience.
- Number the chapters. Keep the rail, phone contents list, and chapter headings in sync. Each rail entry is one line without a subtitle.
- Use prose by default, tables for row-and-column information, and ordered lists for sequences.
- Put caveats in `.note`, at most one per chapter. Put optional presenter notes in `.tp`, controlled by the "Talking points" toggle.
- For a meeting script, put issue and PR links in `.rail-links` below the chapters. Put document previews in `.rail-previews` at the bottom of the rail. Repeat these links at the end for phone readers.
- Use `.pager` links between pages in a document set.

Use an inline SVG diagram when a flow, state change, or structure needs explanation. Put it in a `.fig` figure. The template provides `.box`, `.ask` for decisions, `.group` for containers, `.hl` and `.hl-text` for an emphasized change, and `.edge` with `.arrowhead` for arrows. Label the arrows. State the diagram's claim in its caption and accessible label.

When prose names a source issue, document, or asset, link that phrase. Link its diagram box too when appropriate. Give external links `target="_blank" rel="noopener noreferrer"`.

## Visual rules

Body links stay monochrome and underlined in default, visited, hover, and focus states. This includes tables, link lists, pagers, and linked diagram labels. Rail links and the phone contents list have no underline. They use secondary ink at rest and foreground ink for hover and the current chapter.

The rail has a mono "Contents" label, a tree of numbered chapters, a dithered progress meter, and a percentage. Reading time is estimated from the document's word count at 230 words per minute.

| Token | Light | Dark | Use |
|---|---|---|---|
| `--paper` | `#ffffff` | `#111111` | Page |
| `--ink` | `#0a0a0a` | `#fafafa` | Text and links |
| `--ink-2` | `#636363` | `#a1a1a1` | Secondary text |
| `--rule` | `#e5e5e5` | `#ffffff1a` | Hairlines |
| `--wash` | `#f1eeee` | `#1a1a1a` | Notes, pager, hover |
| `--blue` | `#0a39e5` | `#7d93ff` | Non-link highlights and controls |

Use Inter for headings, body text, and controls. Use DM Mono for rail text, labels, issue keys, code, and numbers. The template requests these fonts from Google Fonts and includes local fallbacks. For an offline or network-restricted document, remove the font requests and use the fallbacks, or use licensed local font files the user supplies.

The template sets body text to 18px, a reading column up to 720px, responsive headings, and a phone contents list below 960px. Preserve these defaults unless the content calls for a change.

Avoid hero sections, badges, card grids, decorative icons, gradients, glass effects, drop shadows, and emoji. Do not turn chapters into full-height slides or add arrow-key paging. Keep borders and diagrams restrained.

## Check and deliver

Inspect the filled document at desktop and phone widths. Check chapter navigation, the progress meter, talking points when present, body and rail link styles, diagrams, and horizontal overflow. Check light and dark mode when the document will use both. Report any rendering limitation instead of claiming a visual check passed.

Deliver the local HTML source and a short account of what was checked. If the user requests hosting, use an available authorized destination and preserve the requested privacy. Do not change sharing or upload to another host without authorization. If no suitable publishing tool exists, provide the local document and state the limitation.

This skill requires no other skill or private service. Its only included resource is the HTML template.
