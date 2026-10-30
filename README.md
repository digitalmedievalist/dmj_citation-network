# DMJ citation network

Static page built by `python -m citations.network --site` in thodel/dmj_management
(data as of 30 October 2026). Do not edit by hand: rebuild and replace the folder.

Embed in Lodel (OpenEdition) with:

    <iframe src="https://digitalmedievalist.github.io/dmj_citation-network/?embed" title="Digital Medievalist citation network"
            width="100%" height="1100" style="border:0" loading="lazy"></iframe>

In an iframe the page wears the journal's OpenEdition theme (Georgia, #104239 rules, #A2403D
links; `?skin=plain` switches it off, `?skin=oe` shows it outside a frame, `?notitle` hides the
heading) and leaves the mouse wheel to the host page
(Ctrl/Cmd + wheel, two fingers or the +/- buttons zoom the network). A host page that
listens for `message` events receives {type: "dmj-citation-network:height", height}.
d3 7.9.0 is bundled (ISC licence, d3-LICENSE); the page makes no third-party requests.
