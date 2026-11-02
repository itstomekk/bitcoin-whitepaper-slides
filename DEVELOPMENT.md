# Development

`docs/deck.html` is the built, self-contained presentation. Its images, styles, scripts and speaker notes are embedded in the HTML. This release does not include a reproducible build system; edit the built file carefully or regenerate it from the original project's private build sources. `docs/index.html` is the relative-path landing page for GitHub Pages configured to serve `/docs` on `main`.

The demo signs and mines synthetic teaching transactions locally. It does not connect to Bitcoin or handle real funds.

To preview locally, run `python -m http.server 8000 --directory docs` and open the displayed local URL. The published URL is planned, not yet active.

Security review must include embedded imagery: a text scanner cannot inspect pixels. The leak scanner's email exception is specific to the public address printed in Satoshi’s paper; it does not authorize other personal data.
