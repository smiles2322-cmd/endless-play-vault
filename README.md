# Endless Play Vault

A standalone, installable web game app: 54 distinct games with 711 built-in puzzles, tracks and boards. Plays offline after the first visit.

Play: https://smiles2322-cmd.github.io/endless-play-vault/

The site is stored as base64 pieces in site/ (cat site/part-* | base64 -d | tar -xz). The Publish workflow unpacks it to the gh-pages branch.
