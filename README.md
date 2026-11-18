# Chord Stage

A live-performance chord helper for the AKAI MPK mini Plus II (works with any MIDI keyboard). One web page, no install.

- Pick a key and scale; wrong notes are corrected to the nearest note in the key.
- Optional bass keys on the far left for the piano left hand (single notes, octaves or root + 5th), kept in key. A bass-guitar sound on MIDI channel 2 is also available.
- Keys below the split play one-finger chords; keys above play melody.
- Pads 1–7 play the chords of the key. With a progression loaded, pad 8 plays the next chord.
- Type a progression per song (`Imaj7 vi7 ii7 V7`, `G D Em C`, `[Chorus] IV I V vi`) and the screen follows along as you play.
- Import MPC `.progression` files (Edit set list → **+ MPC progressions**, or drop them on the page). Each becomes a song with its key and chord chart filled in, and Chord lock, Sloppy mode and pad 8 play the file's exact voicings.
- A green box on the on-screen keyboard marks the key to press for the next chord.
- Beat: drum styles in 4/4 (neo soul, boom bap, slow jam, trap, pop, funk, gospel, jazz, bossa, click) and 3/4 (slow ride + brush, jazz waltz, click) with tempo, tap tempo, fills every 4 bars and **Start on first chord**. Space starts and stops it. Each song saves its own beat. **Drums to MPC** sends the beat as General MIDI drum notes on channel 10.
- Set list with per-song settings; switch with ◀ ▶, arrow keys, Page Up/Down (foot pedal) or knob 8.
- Built-in sounds, or send MIDI to MPC 3 (via the IAC Driver) or the MPK's 5-pin MIDI out.

## Songs

`songs/` holds ready-made charts. Import them with Edit set list → **+ MPC progressions** (or drop the file on the page).

- **Gymnopedie No 1.progression**: Satie's Gymnopédie No. 1, all 78 bars (with the repeat and both endings) and Satie's own left-hand voicings. Chords were read from the public-domain [Mutopia Project](https://www.mutopiaproject.org) edition. It loads in D major at 70 BPM with the Slow 3/4 beat, waiting for your first chord. Play the chords with Chord lock (one key per bar) and the melody on the upper keys.

A `.progression` file may carry an optional `chordStage` block (`bpm`, `beatStyle`, `beatAuto`, `sound`, …) and a `section` name per chord; MPC's own files simply don't have them.

## Run

Open `index.html` in Chrome (Safari has no Web MIDI) and allow MIDI access. Click once to start sound. **Esc** stops all notes.

Set lists live in Chrome's local storage. Use **Export backup** to keep a copy.

## Guide

A color-coded quick guide with an annotated screenshot: open **Guide** next to the logo, or `docs/guide.html`. A printable copy is in `docs/Chord Stage Guide.pdf`.
