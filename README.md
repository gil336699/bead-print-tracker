# Bead Print Tracker

**Live:** https://gil336699.github.io/bead-print-tracker/

A visual tracker for 3D-printing pony beads. It plans plates by color, tracks plates and beads printed, and can track filament and spools. It works on iPhone Safari and desktop, in light and dark mode.

## What it does
- **Groups beads by color** across all characters, so each color prints together. A big plate holds 12 beads and a small plate holds 25.
- **Up next:** shows the color and plate to print next, with one big **Plate printed** button and an Undo. Use the picker to switch colors.
- **Already printed:** type how many beads of a color were printed before you started using the tracker. The remaining plates are planned from what's left.
- **Plate size:** change how many beads go on the plates you haven't printed yet (for example 9 instead of 12).
- **Order:** colors are sorted by beads left (most first, or fewest first). Finished colors go last.
- **Filament tab:** grams used and still to print, spools per color (1 kg and 250 g), and a shopping list. Plate weights: 12 big beads 140.63 g, 9 big beads 105.81 g, 25 small beads 102.9 g.

## Sharing
Progress syncs live through a Firebase Realtime Database. Everyone who opens the same link, including its `#room=…` code, sees and edits the same tracker. Press **Share** to send the link. Anyone with the link can edit it, so share it only with people who should.

Database rules: only `rooms/<room>` can be read or written, and the whole database can't be listed.

## Changing the bead counts
Edit the `ORDERS` list near the top of the script in `index.html`. Each entry is `[character, color, size, quantity]`.
