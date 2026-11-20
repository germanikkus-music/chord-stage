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

## Record & loop

**⏺ Rec** (or the R key) records what Chord Stage plays: chords, arp, strum and melody. Press it again to stop, and the loop starts playing so you can solo over yourself. **▶ Loop** (L) starts and stops it, **✕ Clear** throws it away, and **⬇ MIDI file** downloads it as a .mid at the current tempo to drop into the MPC.

- With the **beat running**, recording starts on the next bar 1 and the loop is a whole number of bars, so it stays in time with the drums. Stopping just after a downbeat ends on that downbeat.
- With **no beat**, recording starts on your first note and the loop is exactly as long as you played.
- A waiting Rec blinks yellow. If you don't play a note within 20 seconds, it cancels itself, so a stray tap can't start recording later.
- The progression display follows the loop, so the chips, Up next and the green key show where the loop is.
- **🎵 Melody over** (M) turns the whole keyboard into a solo instrument: every key plays one note in the key, an octave higher, with no chords. Tap it again to go back. It turns itself off when you Clear or start a new recording, and Up next shows a reminder while it is on.
- The loop plays a little softer than you (70%), and your sustain pedal only holds what you play, not the loop.
- The loop isn't saved with the song; download the MIDI file to keep it. Bass-guitar keys and the Aerophone aren't recorded.

## Stage view

On a phone, Chord Stage switches to **Stage view** by itself: the song, the big chord with Up next, the progression and song form, the chord tiles, Beat, Rec / Loop and STOP ALL, in that order, with the settings hidden. On a tablet or computer, press **▣ Stage view** next to the Piano/Horn button. **⚙ All controls** brings everything back.

## Song form

**Song form** (under the progression) plays the progression as a song instead of one loop, then starts over:

- **3×, then down a step**: three times as written, once a whole step lower.
- **3×, then lift a half step (twice)**: the gospel-style key change, up a half step, then another.
- **3×, then up a 4th**: a key change up four steps (Eb to Ab).
- **3×, then a bridge**: a 4-chord bridge in the song's key (IV V iii vi in major, VI VII iv v in minor).
- **2×, bridge, down a step, home**.
- **Custom…**: type your own, parts separated by commas. `Main` is the whole progression, a `[Section]` name from the progression plays just that section, and `Bridge` uses your `[Bridge]` section or writes one. `x3` repeats a part, and `+2` / `-2` moves it up or down that many half steps. Example: `Main x3, Main -2, Bridge, Main +1`.

The bar shows each part, with the one you're in highlighted (and which pass, like 2/3), and the chord chips show that part's chords. Moved parts keep MPC voicings, shifted. Sloppy mode, pad 8 and Chord lock all follow the moved chords. Saved with each song.

## Smooth voicing

**Smooth voicing** (Piano, on by default) plays each chord in the inversion closest to the chord before it, so changes glide from one to the next instead of jumping up and down the keyboard, the way neo soul and gospel players voice-lead. The chord sits from E3 up and the bass note (or the slash-chord bass) sits in C2–B2 underneath. In a ii–V–I–vi–IV–V–I the notes move about a quarter as far as before. Untick it for plain root-position chords. Chords imported from MPC keep their exact voicings.

## Strum

**Strum** (Piano) rolls each chord from the bottom note up, like a classical pianist's rolled chord: Light (18 ms between notes), Medium (40 ms), Slow roll (80 ms) or Harp (140 ms). Let go early and the notes not yet played are skipped. Saved with each song. When Arp is on, Arp wins.

## Arp

**Arp** (Piano) plays every chord one note at a time, in time with the **Tempo**, from any keyboard. Choose Up, Down, Up & down or Random; 1/8, 1/8 triplet or 1/16; and 1 or 2 octaves. A low root under the chord holds as the bass while the rest arpeggiates. With the beat playing, the notes line up with the drums. Arp settings are saved with each song.

A keyboard's own arpeggiator works too. The MPK's **ARP** button just re-presses the key you hold, fast, so Chord Stage plays the whole chord on the first hit and then steps through its notes on each repeat. The speed comes from the MPK's tempo (tap tempo on the MPK), not Chord Stage's.

## Aerophone (wind)

When Chord Stage opens it asks **Piano** or **Horn**. Each one shows only its own controls. Piano has the key modes, split, bass keys and the on-screen keyboard. Horn has the horn sound, octave, chord-follow, Tune and the fingering view. The 🎹/🎺 button next to Guide switches between them.

Chord Stage can use a Roland Aerophone mini (or another wind controller) for the melody while the MPK plays chords and the beat runs.

1. Pair it on the Mac: open **Audio MIDI Setup**, choose **Window → Show MIDI Studio**, click the **Bluetooth** button and connect the Aerophone. Chrome then sees it like any other MIDI input.
2. Turn the Aerophone's own speaker down so only Chord Stage sounds.
3. Choose **Horn** at the start, then pick a voice under **Horn sound**: Recorder, Flute, Clarinet, Trumpet, Violin, Saw lead, Wind synth, Wind pad, or Same as Sound. Breath sets the volume of every horn sound. Trumpet, Saw lead and Wind synth also get brighter the harder you blow, and Wind synth has the resonant filter sweep of classic breath synths. Use **Octave up/down** if it sits too high or low.

When the Aerophone is connected, the on-screen keyboard switches to **Aerophone fingering** diagrams, which follow Roland's AE-01 chart. There's a button to switch back, and one on the keyboard to switch over by hand.
- **Now:** the notes of the chord that's playing, each drawn as a fingering. The root has a green border.
- **Next:** the next chord's notes, dimmed.
- **You're playing:** the note you're blowing. It glows green when it's in the chord and gets a red border for a passing note.

Filled keys mean press. The gold small keys are the side keys: the upper one makes a note sharp, the lower one makes it flat.

The Aerophone drives the progression, since both your hands are on it. Blow the next chord's root note and hold it briefly; quick passing notes don't count. Chord Stage moves to that chord and lights its button. The setting next to Tune picks what you hear:
- **Root moves chords (silent)**, the default: only your wind instrument sounds.
- **Root moves + plays chords**: the chord also plays as backing and rings until the next one.
- **One note = one chord (C = key)**: each fingering plays a whole chord in the horn sound, and your breath swells it. The seven main fingerings C D E F G A B, closing the keys from the top down, are the key's chords I to vii in whatever key the song is in, so C is always home. Sharp and flat fingerings play the chord a half step away. With **Sloppy mode** on, the fingering for the next chord's root plays that exact chord from the progression and moves on, like the piano. The fingering view shows a **Chord map** of all seven, and the Blow next card shows which one to finger. Quick notes the Aerophone sends while your fingers are landing are skipped, so only the note you settle on sounds.
- **Melody only**: the Aerophone doesn't move the chords at all. A pulsing green **Blow next** fingering, first in the row, shows the note to blow, like the green L on the piano. For a slash chord such as Cmaj7/G, the bass note (G) works too.

If the notes come out shifted, the Aerophone's transpose is set away from C. On this one, a C fingering sent C#. Click **Tune** under Wind, finger C and blow. The app learns the offset and corrects every note; the button then shows it, e.g. "Tuned +1".

Connect it by **USB**. Bluetooth MIDI kept failing on this Mac. Quit Chrome before plugging it in, and untick **Discover USB devices** on `chrome://inspect`. Otherwise Chrome (or a running `adb`) grabs the Aerophone and no MIDI port appears.

Its notes always play one note at a time in the wind voice. They never trigger chords or move the progression. Breath sets the volume while you blow; Chord Stage reads breath from CC2, CC11 or aftertouch. The app recognises it by name ("Aerophone", "AE-01") or as soon as it sends breath. The status shows "MPK + Aerophone connected". If you send MIDI out, the wind part goes on channel 3, so the MPC can give it its own track.

## Songs

`songs/` holds ready-made charts. Import them with Edit set list → **+ MPC progressions** (or drop the file on the page).

- **Gymnopedie No 1.progression**: Satie's Gymnopédie No. 1, all 78 bars (with the repeat and both endings) and Satie's own left-hand voicings. Chords were read from the public-domain [Mutopia Project](https://www.mutopiaproject.org) edition. It loads in D major at 70 BPM with the Slow 3/4 beat, waiting for your first chord. Play the chords with Chord lock (one key per bar) and the melody on the upper keys.

A `.progression` file may carry an optional `chordStage` block (`bpm`, `beatStyle`, `beatAuto`, `sound`, …) and a `section` name per chord; MPC's own files simply don't have them.

## Install (Android, Mac)

Chord Stage is live at **https://germanikkus-music.github.io/chord-stage/** (GitHub Pages, from `main`). Open it in Chrome and choose **⋮ → Install app** (Android) or the install icon in the address bar (Mac). It opens full screen with its own icon and works offline; each push to `main` shows up the next time it opens with internet. Songs live in each browser separately, so move them with **Export** / **Import**. On Android, connect keyboards and the Aerophone by USB (OTG), and use wired audio: a Bluetooth speaker adds about 0.2 s of delay.

## Run

Open `index.html` in Chrome (Safari has no Web MIDI) and allow MIDI access. Click once to start sound. **Esc** stops all notes.

Set lists live in Chrome's local storage. Use **Export backup** to keep a copy.

## Guide

A color-coded quick guide with an annotated screenshot: open **Guide** next to the logo, or `docs/guide.html`. A printable copy is in `docs/Chord Stage Guide.pdf`.
