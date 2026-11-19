# Chord Stage

A live-performance chord helper for the AKAI MPK mini Plus II (works with any MIDI keyboard). One web page, no install.

- Pick a key and scale; wrong notes are corrected to the nearest note in the key.
- Optional bass keys on the far left for the piano left hand (single notes, octaves or root + 5th), kept in key. A bass-guitar sound on MIDI channel 2 is also available.
- Keys below the split play one-finger chords; keys above play melody.
- Pads 1–7 play the chords of the key. With a progression loaded, pad 8 plays the next chord.
- Type a progression per song (`Imaj7 vi7 ii7 V7`, `G D Em C`, `[Chorus] IV I V vi`) and the screen follows along as you play.
- Import MPC `.progression` files (Edit set list → **+ MPC progressions**, or drop them on the page). Each becomes a song with its key and chord chart filled in, and Chord lock, Sloppy mode and pad 8 play the file's exact voicings.
- A pulsing green key marked L on the on-screen keyboard is the key to press for the next chord. It stays close to where your left hand last played; the same note in other octaves gets a faint dashed outline.
- Beat: drum styles in 4/4 (neo soul, boom bap, slow jam, trap, pop, funk, gospel, jazz, bossa, click) and 3/4 (slow ride + brush, jazz waltz, click) with tempo, tap tempo, fills every 4 bars and **Start on first chord**. Space starts and stops it. Each song saves its own beat. **Drums to MPC** sends the beat as General MIDI drum notes on channel 10.
- Set list with per-song settings; switch with ◀ ▶, arrow keys, Page Up/Down (foot pedal) or knob 8.
- Built-in sounds, or send MIDI to MPC 3 (via the IAC Driver) or the MPK's 5-pin MIDI out.

## Aerophone (wind)

Chord Stage can use a Roland Aerophone mini (or another wind controller) for the melody while the MPK plays chords and the beat runs.

1. Pair it on the Mac: open **Audio MIDI Setup**, choose **Window → Show MIDI Studio**, click the **Bluetooth** button and connect the Aerophone. Chrome then sees it like any other MIDI input.
2. Turn the Aerophone's own speaker down so only Chord Stage sounds.
3. Pick a voice under **Wind (Aerophone)**: Recorder, Flute, Clarinet, or Same as Sound. Use **Octave up/down** if it sits too high or low.

When the Aerophone is connected, the on-screen keyboard switches to **Aerophone fingering** diagrams, which follow Roland's AE-01 chart. There's a button to switch back, and one on the keyboard to switch over by hand.
- **Now:** the notes of the chord that's playing, each drawn as a fingering. The root has a green border.
- **Next:** the next chord's notes, dimmed.
- **You're playing:** the note you're blowing. It glows green when it's in the chord and gets a red border for a passing note.

Filled keys mean press. The gold small keys are the side keys: the upper one makes a note sharp, the lower one makes it flat.

With **Root plays next chord** on (the default), the Aerophone drives the progression, since both your hands are on it. Blow the next chord's root note and hold it briefly; quick passing notes don't count. Chord Stage moves to that chord, plays it as backing, and lights its button. The chord rings until the next one. The Next card tells you which note to blow.

If the notes come out shifted, the Aerophone's transpose is set away from C. On this one, a C fingering sent C#. Click **Tune** under Wind, finger C and blow. The app learns the offset and corrects every note; the button then shows it, e.g. "Tuned +1".

Connect it by **USB**. Bluetooth MIDI kept failing on this Mac. Quit Chrome before plugging it in, and untick **Discover USB devices** on `chrome://inspect`. Otherwise Chrome (or a running `adb`) grabs the Aerophone and no MIDI port appears.

Its notes always play one note at a time in the wind voice. They never trigger chords or move the progression. Breath sets the volume while you blow; Chord Stage reads breath from CC2, CC11 or aftertouch. The app recognises it by name ("Aerophone", "AE-01") or as soon as it sends breath. The status shows "MPK + Aerophone connected". If you send MIDI out, the wind part goes on channel 3, so the MPC can give it its own track.

## Songs

`songs/` holds ready-made charts. Import them with Edit set list → **+ MPC progressions** (or drop the file on the page).

- **Gymnopedie No 1.progression**: Satie's Gymnopédie No. 1, all 78 bars (with the repeat and both endings) and Satie's own left-hand voicings. Chords were read from the public-domain [Mutopia Project](https://www.mutopiaproject.org) edition. It loads in D major at 70 BPM with the Slow 3/4 beat, waiting for your first chord. Play the chords with Chord lock (one key per bar) and the melody on the upper keys.

A `.progression` file may carry an optional `chordStage` block (`bpm`, `beatStyle`, `beatAuto`, `sound`, …) and a `section` name per chord; MPC's own files simply don't have them.

## Run

Open `index.html` in Chrome (Safari has no Web MIDI) and allow MIDI access. Click once to start sound. **Esc** stops all notes.

Set lists live in Chrome's local storage. Use **Export backup** to keep a copy.

## Guide

A color-coded quick guide with an annotated screenshot: open **Guide** next to the logo, or `docs/guide.html`. A printable copy is in `docs/Chord Stage Guide.pdf`.
