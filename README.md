# Endless Play Vault

A standalone, installable web game app: 97 distinct games with 1099 built-in puzzles, tracks and boards. Plays offline after the first visit.

The site is stored as base64 pieces in site/ (cat site/part-* | base64 -d | tar -xz). The Publish workflow unpacks it to the gh-pages branch of this repo.

Staged only. Not pushed. Needs owner approval before any repo is created or pushed.
