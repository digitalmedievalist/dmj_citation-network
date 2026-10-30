# DMJ citation network

An interactive network of the references in the journal
[Digital Medievalist](https://journals.openedition.org/digitalmedievalist/): which works the
articles cite together, and where DMJ articles cite each other. Live at <https://digitalmedievalist.github.io/dmj_citation-network/>.

Data as of 30 October 2026: 101 articles, 2,383 references, 2,260 distinct works,
97 of them cited by two or more articles, 37 citations of DMJ articles in DMJ.

## Source

The bibliographies of all issues as recorded in the journal's Zotero group
[digitalmedievalist](https://www.zotero.org/groups/2138266) (collections "DM Journal" and
"DM Journal – Works cited"). Two references count as the same work where they were matched to one
Zotero item (DOI, ISBN, or author, year and title); unconfirmed duplicates are counted apart, so
shared citations are, if anything, undercounted. Only bibliographies are covered, not footnotes.
`network.json` holds the data behind the page.

## Embedding on OpenEdition (Lodel)

    <iframe src="https://digitalmedievalist.github.io/dmj_citation-network/?embed&notitle" title="Digital Medievalist citation network"
            width="100%" height="1100" style="border:0" loading="lazy"></iframe>

In an iframe (or with `?embed`) the page

- wears the journal's OpenEdition theme (Georgia, #104239 rules, #A2403D links);
- says at the top that it is embedded content from this site and links to the full page;
- uses the light theme and leaves the mouse wheel to the host page: Ctrl/Cmd + wheel, two
  fingers or the +/- buttons zoom the network, which fits itself to the frame;
- posts its height to the host as `{type: "dmj-citation-network:height", height}`.

URL options: `?notitle` hides the heading when the host page has its own, `?skin=plain` switches
the OpenEdition theme off (the page then looks as it does on its own), `?skin=oe` shows it outside a frame.

On its own the page follows the design of [digitalmedievalist.org](https://digitalmedievalist.org/):
Vollkorn and Source Sans, warm grey ground, white panels, slate teal.

No cookies, no tracking, no third-party requests: d3 7.9.0 (ISC licence, `d3-LICENSE`) and the fonts
Vollkorn and Source Sans 3 (SIL Open Font License, `fonts/OFL-*.txt`) are bundled.

## Updating

Everything here is generated: do not edit by hand. The page is built by
`python -m citations.network --site <this folder>` in the editors' dmj_management repository;
commit and push the result, and GitHub Pages serves `main` as it is.
