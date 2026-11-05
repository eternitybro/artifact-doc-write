# Artifact docs

An agent skill for writing HTML documents people can read, screenshare, or open from a link. It provides a numbered chapter rail, scroll progress, reading time, optional talking points, and light and dark themes.

The template keeps the document in one reading column. Headings use Inter. Navigation uses DM Mono. Body links stay monochrome and underlined; chapter links use text color to show their state.

## Use it

Place the complete [skills/artifact-doc-write](skills/artifact-doc-write/SKILL.md) folder in your agent's supported skill directory. Preserve any existing skill with that name before installing it.

Give the agent the source material and the document's purpose:

> Use $artifact-doc-write to turn this proposal into a reading document for our next review. Keep the open questions visible and deliver a local HTML file.

The agent fills the template, checks the document at desktop and phone widths, and returns the HTML source. Hosting is optional and requires an available destination you authorize.

## What's included

- Instructions for source-backed content, document structure, and visual checks.
- One HTML template with inline CSS and JavaScript.
- Chapter navigation, a progress meter, reading time, and a talking-points toggle.

The template contains sample labels and text. Replace them when creating a document. It needs no build step or server. Open the HTML file in a browser.

## Dependencies and references

The skill does not require another skill or a private publishing tool. The template requests Inter and DM Mono from Google Fonts and includes local font fallbacks. Font files are not included in this repository. Remove the font requests when preparing an offline document, or use licensed local fonts you supply.

The visual references are [Linear Method](https://linear.app/method/introduction), [CPU Learn](https://stable.clearsol.network/learn/use-cases), and the [Claude developer blog sidebar](https://claude.dev/blog/solving-code-review-at-anthropic/). They inform the reading hierarchy. Their text, fonts, and assets are not bundled here.

## Verification

The template passed 23 browser checks at desktop and phone viewport sizes, in light and dark mode. Checks covered overflow, link styles, contents navigation, talking points, and reading time. Desktop and phone screenshots were also inspected.

This checks the template, not the accuracy or usability of documents an agent creates with it. Review the content and render each finished document before sharing it.

## License

[MIT](LICENSE). The license covers this repository's files. External fonts and linked reference material retain their own terms.
