# Updating

For each change:

1. Review the deck and speaker notes for private data and inspect embedded images.
2. Refresh the affected real screenshots in `docs/img/` and `.github/readme/`; update the README and landing page to match.
3. Test the slides, interactive demonstrations, presenter window and relative links under the project subpath.
4. Run the public-repo leak scanner on the working tree and full history with `--allow=satoshi@gmx.com --skip-embedded-media`. The former permits only the public address in the whitepaper; the latter avoids base64 false positives and requires independent media review. Do not suppress any other finding.
5. Commit the change. When publishing is explicitly approved, push it and verify the live GitHub Pages page, deck and images. Until then this repository remains local only.
