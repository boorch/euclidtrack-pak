# EUCLIDTRACK for TrimUI Brick

EUCLIDTRACK is an experimental synth workstation with a singular focus: generating melodies through euclidean sequencing and pitch modulation using LFOs. Four tracks, each with its own synth voice, euclidean sequencer, and effect chain, all driven from the Brick's buttons. Sixty four scenes, four modulators per track, twelve performance macros, generous saturation with many drive algorithms, a hybrid morphing delay/reverb with a resonator and a shimmer stage, and a mixer that lets you build a feedback network for unique organismic (and slightly dangerous) results!

![EUCLIDTRACK boot splash](https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/screenshots/01.png)

## A short history

EUCLIDTRACK started life as DRONAGE-S4, a project sideloaded onto the Torso S-4 to run alongside its vanilla OS. That version never went public: running it required some distinctly user-unfriendly steps, like replacing the CM4 inside the S-4 with one that has more RAM, and hacking the audio configuration of the S-4 OS. So the project gained a new life on the TrimUI Brick, a platform anyone can actually own, as the instrument you are holding now.

---

## Installing

**On NextUI:**

- Install or update EUCLIDTRACK through the **PakStore**. That is the easiest route and updates are one press.

**On other firmware:**

1. Download the latest `EUCLIDTRACK.pak.zip` from the [releases page](https://github.com/boorch/euclidtrack-pak/releases).
2. Unzip it and copy the `EUCLIDTRACK.pak` folder to your SD card under `Tools/tg5040/`.
3. Reinsert the card and launch **EUCLIDTRACK** from the Tools menu.

Your projects live in `/mnt/SDCARD/EUCLIDTRACK/`, outside the app folder. They survive updates and reinstalls. Back up that folder to back up your music.

## Launching and quitting

- Launch **EUCLIDTRACK** from the Tools menu.
- The device volume buttons work as usual. Master volume inside the app is a separate control (R3 plus dpad up/down) and always starts at unity on launch.
- To quit: press MENU, choose QUIT.

## Making sound: two switches stand between you and audio

A fresh boot is silent on purpose. Three things have to happen:

1. Most important thing: **Hold SELECT to bring up minimap**, use dpad to focus on a cell, release SELECT to jump on that view.
2. **Start the transport.** Tap and release START (a quick tap, not a hold). The tempo light starts flashing. Tap again to stop.
3. **Open at least one track's gate.** Hold START (or R3) and press a face button: West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> is track 1, North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> is track 2, East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> is track 3, South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> is track 4. While you hold, the bottom row shows each track's gate state: ▶ means open, ■ means closed. A track with a closed gate makes no sound, no matter what else is set.
4. **Give the sequencer something to play.** On the EUCLID view, either raise **Triggers** so the pattern has hits in it, or set **Steps** all the way down to **Drone** for a continuous, infinite tone.

Transport running, a gate open, and a pattern with hits (or a drone): now you have sound.

---

## The screen

- **Top bar**: scene number, root note, scale, tempo. The small light next to the tempo flashes green on the downbeat and yellow on the other beats. While recording it turns into a dot and the downbeat flashes red instead.
- **Canvas**: the middle of the screen, showing a visualization of the active device (step grid, scope, mixer meters, and so on). It is a live picture of the current parameter state, not something you touch directly: all editing happens through the eight parameter cells below.
- **Param panel**: eight parameter cells in two rows of four, K1 to K4 on top, K5 to K8 below. The focused cell shows its label in bright white.
- **Corner icon**: the top right of the panel always shows where you are, prefixed by who owns the view. Track views read T1 to T4 before the icon, and a MODULATOR view that belongs to PERFORM or MIX shows that scope's icon in front instead, so two modulator views that look alike can always be told apart. An icon with a braille mark shows the page: ⠈ is page 1, ⠘ is page 2. In the MODULATOR view the icon takes the color of the active modulator.

| Icon | View |
|---|---|
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0536.svg" height="16" alt="EUCLID"> | EUCLID, the sequencer |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF067D.svg" height="16" alt="ENGINE"> | ENGINE, the voice |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0F9E.svg" height="16" alt="DIMENSION"> | DIMENSION, flanger and chorus |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0232.svg" height="16" alt="FILTER"> | FILTER, eight band filterbank |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF1853.svg" height="16" alt="COLOR"> | COLOR, drive and texture |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0AC4.svg" height="16" alt="DRIFT"> | DRIFT, morphing delay/reverb |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0EA2.svg" height="16" alt="MIX"> | MIX, the mixer |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0803.svg" height="16" alt="PERFORM"> | PERFORM, macros |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0FCF.svg" height="16" alt="SCENES"> | SCENES |
| <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF095B.svg" height="16" alt="MODULATOR"> | MODULATOR (colored by slot) |

---

## Controls at a glance

**The face buttons are named by position:** B is South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> · Y is West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> · X is North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> · A is East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> 

| Button | Tap | Hold |
|---|---|---|
| Select | | **view map**, the navigation hub: jump anywhere, copy, paste, reset (see below) |
| dpad | move focus, navigate lists | key repeat |
| South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> (B) | confirm in dialogs | EDIT: hold and use dpad to tweak the focused param (left/right fine, up/down coarse) |
| West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> (Y) | knob push, opens popups | |
| North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> (X) | TEMP scratchpad on/off | in PERFORM: macro picker |
| East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> (A) | cancel in dialogs, reset the focused param elsewhere, delete a character in text entry | in the LOAD browser: delete the project |
| L1 | | SHAPES layer: the four face buttons become the on screen action buttons; the deck row shows what each does |
| L2 | | CLEAR layer: faces become UNDO, REDO, RESET MOD, RESET PARAMS |
| L2 + R2 | randomize the current device | |
| R1 | MODULATOR view on/off | MOD assign · inside the MODULATOR view: + dpad left/right browses the four slots (release then stays in the view) |
| R2 | PERFORM view on/off | MACRO assign |
| R3 | | + faces: track gates 1 to 4 · + dpad up/down: master volume · + dpad left/right: tempo down/up 1 BPM |
| L3 | | + West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> tap: copy the current view · + West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> held about 1.5 s: copy the whole track · + North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> tap: paste into the current view |
| Start | play / stop | + faces: track gates 1 to 4 |
| MENU | project menu: SAVE, SAVE AS, LOAD, NEW, START RECORDING, OPTIONS, QUIT | |
| L1+L2+R1+R2 | **sends panic**: every ring send snaps to zero instantly | |

Every layer announces itself on screen: hold L1, L2, L3, Start or R3 and the bottom row lists what the face buttons do right now (shapes, the CLEAR stack, COPY and PASTE, or each track's gate state). Release the layer and the row returns to the device tab bar.

---

## The core loop

1. Use the **dpad** to focus one of the eight parameter cells.
2. **Hold South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> and press the dpad** to change the value. Left and right are fine steps, up and down are coarse.
3. **West** <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> pushes the knob. Cells with lists (engine type, waveform, scale) open a popup: dpad to choose, West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> or South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> to confirm, East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> to cancel.
4. **East** <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> resets the focused parameter to its default.

Pressing up from the top row of cells moves focus into the top bar: SCENE, ROOT, SCALE, TEMPO. The same South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> plus dpad gesture tweaks them. SCENE steps switch scenes instantly, with no quantize wait. Down returns to the parameter cells.

---

## The view map (hold Select)

Hold **Select** to open the map. It is the navigation hub: every view, page, track and modulator is a cell.

```
T1   󰔶  󰙽⠈ 󰙽⠘  󰾞  󰈲  󱡓  󰫄⠈ 󰫄⠘ · 󰥛⠈ 󰥛⠘ 󰥛⠙ 󰥛⠛
T2   ...
T3   ...
T4   ...
MIX  󰺢⠈ 󰺢⠘ 󰺢⠙                     󰥛⠈ 󰥛⠘ 󰥛⠙ 󰥛⠛
PRF  󰠃                            󰥛⠈ 󰥛⠘ 󰥛⠙ 󰥛⠛
SCN  󰿏
```

![The view map](https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/screenshots/05.png)

- Dpad steers. Up and down change row, left and right walk along a row, from a device through its pages to the modulators.
- **Release Select** to open the highlighted cell. Releasing without moving does nothing, so peeking is always safe.
- The white cell is where you came from. Modulator cells are colored: red, blue, green, yellow for modulators 1 to 4.
- While the map is open:
  - **South** <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> sets the highlighted modulator as the active one without closing the map.
  - **West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> tap** copies the highlighted cell's settings. **West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> held about 1.5 s** copies the whole track of that row.
  - **North** <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> pastes into the highlighted cell.
  - **East** <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> resets the highlighted cell's device, parameters and modulation both.

Copy and paste are smart: a device pastes onto the same device on another track, a modulator pastes onto any modulator cell, a whole track pastes onto a whole track.

---

## Tracks and gates

- **Start** toggles the transport.
- **Start (or R3) held plus a face button** toggles a track's gate: West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> is track 1, North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> is track 2, East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> is track 3, South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> is track 4.
- A gated off track fades by its FadeOut time and its reverb tail rings out naturally.
- Track selection follows the view map rows: open any cell on T3's row and track 3 becomes the selected track.

---

## The devices

### <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0536.svg" height="16" alt="EUCLID"> EUCLID, the sequencer

![The EUCLID view with its step grid](https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/screenshots/04.png)

| Cell | Does |
|---|---|
| Steps | pattern length. The first choice below 2 is **Drone**: the gate holds open for a continuous tone and the pattern controls go inert |
| Triggers | how many hits, spread evenly (the euclidean part) |
| Rate | clock division of this track |
| Probability | chance that each hit actually plays |
| Shift | rotates the pattern |
| Pad | appends silent steps after the pattern: the loop becomes Steps plus Pad long, with the padding always resting. Great for odd loop lengths and breathing room |
| Reset Beat | restarts the pattern every N beats |
| Shuffle | swing |

### <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF067D.svg" height="16" alt="ENGINE"> ENGINE, the voice

Page 1:

| Cell | Does |
|---|---|
| Engine | the synthesis model. Each model repurposes the three knobs below in its own way |
| Harmonics | the model's first macro control |
| Timbre | the model's second macro control |
| Morph | the model's third macro control |
| Cutoff | the voice filter's frequency |
| Resonance | the voice filter's resonance |
| Filter Type | morphs the filter continuously: lowpass at 0, bandpass in the middle, highpass at full |
| Pitch | the note, quantized to the global root and scale |

Page 2:

| Cell | Does |
|---|---|
| FadeIn | how long the track takes to fade in when its gate opens |
| FadeOut | how long it takes to fade out when the gate closes. The DRIFT tail rings out past the fade |
| LPG Decay | the plucked envelope's decay per hit |
| LPG Color | the pluck's character, from soft and dark to snappy and bright |
| Velocity | in euclidean mode: how hard each hit strikes, sampled once per trigger, so a modulator here makes accent patterns. In Drone mode: a continuous level control, so a modulator here makes smooth swells |
| Out | which of the model's two outputs feed the chain: their mix, either one alone, or a true stereo split |

### <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0F9E.svg" height="16" alt="DIMENSION"> DIMENSION

A flanger and a chorus in series. Each has its own Wet, so you can run either alone or both.

| Cell | Does |
|---|---|
| Fl Mode | the flanger's flavor |
| Fl Rate | flanger sweep speed |
| Fl Depth | flanger sweep depth |
| Fl Wet | flanger dry/wet |
| Ch Mode | the chorus's flavor |
| Ch Rate | chorus movement speed |
| Ch Depth | chorus movement depth |
| Ch Wet | chorus dry/wet |

### <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0232.svg" height="16" alt="FILTER"> FILTER

Eight fixed bands, one cell per band, cut and boost around the middle. All eight are modulation targets, so a modulator can sweep the whole bank.

| Cell | Band |
|---|---|
| A | 90 Hz |
| B | 122 Hz |
| C | 225 Hz |
| D | 418 Hz |
| E | 777 Hz |
| F | 1.4 kHz |
| G | 2.7 kHz |
| H | 4 kHz |

### <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF1853.svg" height="16" alt="COLOR"> COLOR

| Cell | Does |
|---|---|
| Algo | picks the saturation algorithm from a generous menu of drive flavors |
| Drive | how hard the signal pushes into the algorithm |
| Bias | asymmetry: skews the drive for even-harmonic, pushed-transformer character |
| Comp | the per track compressor, sitting at the very end of the track's chain |
| Base | low corner of the drive's tone filter |
| Width | how many octaves above Base stay open |
| Dirt | tape hiss and vinyl crackle, added after the reverb so it stays a dry surface layer |
| Wet | dry/wet of the drive section |

### <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0AC4.svg" height="16" alt="DRIFT"> DRIFT, the hybrid morphing delay/reverb

DRIFT is one machine that morphs between two identities: at low Morph it is a clean stereo delay with ping pong cross feedback, at high Morph a dense diffused reverb wash, and everywhere in between is playable space.

Page 1:

| Cell | Does |
|---|---|
| Size | room size, with a tape style pitch glide when moved |
| Damp | high frequency decay of the tail |
| Feedback | tail length. The top of the range goes over unity and self sustains into a saturating wall, on purpose |
| Morph | crossfades clean stereo delay into diffused reverb wash. Low Morph with high Feedback is a ping pong echo |
| Shift | frequency shifter in the feedback path, in Hz, inharmonic by nature |
| Motion | modulates the delay line lengths with a slow internal LFO, rate and depth rising together on one knob: subtle settings breathe and shimmer the tail, high settings bend it into detuned, seasick movement |
| Duck | the wet output ducks under the dry input and blooms back in the gaps |
| Mix | dry/wet. At zero nothing of DRIFT is heard, including the resonator and the shimmer |

Page 2:

| Cell | Does |
|---|---|
| Width | stereo width of the wet, mono to very wide |
| Saturation | brightness and drive of the wet top end |
| Shimmer Fbk | how much pitch shifted signal recirculates through the tail. Zero is off |
| Shimmer Amt | the shimmer blend, bipolar. Center is off. Turning right fades in an octave up, then an octave down joins past halfway. Turning left fades in a fifth plus the octave together, then two octaves up join past halfway for the full choir |
| Reso Tune | the resonator's pitch, quantized to root and scale |
| Reso Drift | spreads the resonator's upper voices away from pure harmony |
| Reso Fbk | resonator ring length and brightness |
| Reso Amt | how much of the reverb input runs through the resonator. At full, the space breathes pure resonator |

The resonator is a three voice tuned comb bank sitting in front of the reverb. The shimmer is a granular pitch shifter inside the reverb's feedback loop, so every pass climbs through the chosen intervals.

---

## <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0EA2.svg" height="16" alt="MIX"> MIX

Page 1: Volume and Tone per track. Page 2: Pan per track, then the master strip:

| Cell | Does |
|---|---|
| Master Comp | bipolar: negative pumps (sidechain duck), zero bypasses, positive glues. The row under it is a live gain reduction meter |
| SC Source | what the compressor listens to: the master sum, or one track (point it at your kick for classic pumping) |
| SC Filter | tone tilt on the listening signal only |
| Bass Mono | collapses the low band to mono, crossover 30 to 200 Hz |

In MIX view, the shape layer (hold L1) mutes and unmutes tracks. Mute is a hard cut after everything; gates fade and leave tails.

### The feedback network (MIX page 3)

Page 3 turns the four tracks into a network. Eight **ring sends**, both directions around the circle:

```
K1..K4  forward:  SEND T1>T2   T2>T3   T3>T4   T4>T1
K5..K8  reverse:  SEND T2>T1   T3>T2   T4>T3   T1>T4
```

The rows are aligned so every COLUMN is a mutual pair: the cell under
T1>T2 is T2>T1, and so on. Raise both knobs in one column and you have
an instant two track feedback loop.

The network, drawn out:

```
    ┌───────────────────◄── T4>T1 ──◄───────────────────┐
    │                                                   │
  ┌─▼──┐   T1>T2   ┌────┐   T2>T3   ┌────┐   T3>T4   ┌──┴─┐
  │    │ ────────► │    │ ────────► │    │ ────────► │    │
  │ T1 │           │ T2 │           │ T3 │           │ T4 │
  │    │ ◄──────── │    │ ◄──────── │    │ ◄──────── │    │
  └─┬──┘   T2>T1   └────┘   T3>T2   └────┘   T4>T3   └──▲─┘
    │                                                   │
    └───────────────────►── T1>T4 ──►───────────────────┘
```

And where a send lands inside the receiving track:

```
  neighbor sends ─────┐
                      ▼
  OSC ───────────────(+)─► DIMENSION ► FILTER ► COLOR ► DRIFT ─┐
                                                               │
       out ◄── fader ◄──┬──────────────────────────────────────┘
                        │
                        └─► tap feeding this track's own sends
```

Each knob feeds that track's finished sound (taken before its fader) into the start of the named track's chain, so the sent signal rides the whole destination chain: filter, color, drive, reverb, everything. Because both rings close the circle, sends can feed back into themselves through the other tracks. A high-pass and a soft-clip guard every injection, so the network saturates musically instead of running away.

Things to know:

- The tap is **pre-fader**: pulling a track's volume mutes its direct sound but keeps it feeding the network. That is a feature: a track can become a silent processor for its neighbors.
- A **gated-off track silences whatever is sent through it**. The send rides the target's gate, so playing gates live also plays the network.
- All eight sends are **modulation targets**.
- Escape hatches: East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> on a focused send resets it, the CLEAR layer's RESET PARAMS in MIX view zeroes the whole page, and **gripping all four shoulders at once (L1+L2+R1+R2) snaps every send to zero from anywhere**. That grip is the big red button: when the network gets away from you, grab everything.

**Recipes to start with:**

- **Delay into reverb.** Set T1's DRIFT to low Morph with high Feedback (its delay mode) and T2's to high Morph with Feedback around 70 and a generous Size, then raise SEND T1>T2. T1's hits echo in its own delay, and every echo drifts onward into T2's reverb: the classic delay feeding a reverb, split across two tracks with separate tone controls over each stage.
- **Ethereal delay lines.** Both tracks on low Morph, high Feedback, slightly different Sizes, sends raised both ways between them. The two delays feed each other and the echoes stagger into long irregular trails that never quite repeat. Add a touch of Shimmer on one side and the trails start climbing.
- **The silent processor.** Turn T4's Triggers to zero so it plays nothing of its own, then dial its filter, COLOR and DRIFT as an effect chain and send T3 into it. You just built a return channel.
- **The breathing mix.** Map a slow LFO onto one send with a small amount. The cross-bleed swells and fades and the whole mix starts to move on its own.
- **The ecosystem.** Raise several sends to around 30 or 40 percent with DRIFT wet and Feedback high on every track, then perform with the track gates: every gate you open or close reroutes the whole network. This is the deep end.

**A warning about extreme feedback.** With several sends high and DRIFT Feedback past its self-sustain point, the network becomes a self oscillating instrument. The output is always limited and cannot clip or run away, but it can jump from quiet to VERY loud in an instant, and screaming resonances are part of the deal. Turn the master volume down before you go exploring, be gentle with headphones, and remember the fast exits: grab all four shoulders at once (every send snaps to zero), or stop the transport. What happens in the network is your responsibility. Have fun.

The master bus ends in a lookahead limiter. It is always on and not a knob; four loud tracks cannot clip the output.

---

## <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0FCF.svg" height="16" alt="SCENES"> Scenes and TEMP

A scene is a full snapshot of everything. Sixty four slots.

- In SCENES view: dpad up/down moves the cursor, West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> launches or selects. With the shape layer (hold L1): West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> LAUNCH, North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> LOCK, East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> RANDOM (launch a random saved scene), South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> CHAIN (add the scene to the chain).
- Left/right move across the CHANCE, RULE and QUANTIZE cells, which control automatic scene advancing: chance to fire, what to launch, and the launch quantize grid.
- Launches wait for the quantize boundary; the top bar shows the queued jump. For instant switching use the SCENE slot in the top bar.
- **TEMP** (North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> tap) is a scratchpad: experiment freely, tap North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> again and everything reverts. Saving is blocked while TEMP is active.

**LOCK freezes a scene.** Normally, edits you make while a scene is active are written back into it when you switch away, so scenes remember what you did. A locked scene refuses that write back: tweak it as hard as you like during a performance, and relaunching it snaps back to exactly the state you locked. Unlock to make edits stick again.

---

## <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF095B.svg" height="16" alt="MODULATOR"> Modulation

Four modulators per track, four for MIX, four for PERFORM. Each is an LFO with waveform, rate, phase, skew, smoothing and more. The four slots have fixed colors everywhere in the app: **1 red, 2 blue, 3 green, 4 yellow**.

![A sample and hold modulator: route it to pitch and the rhythm becomes a melody](https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/screenshots/03.png)

- **Tap R1**: the MODULATOR view for the active slot, with a live scope. The main encoder cell cycles waveforms. With the shape layer (hold L1), West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> opens the waveform category menu and South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> rerolls random shapes.
- Waveforms: Sine, Tri, Saw up, Saw down, Square, sample and hold (random and seeded), Noise, plus follower shapes that react to another track's audio or gates, and step sequence shapes.
- Rates are clock synced. The square wave rises at the start of its cycle, like a clock gate.
- **Pick the active modulator** in the view map: highlight a <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF095B.svg" height="16" alt="MODULATOR"> cell and press South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> or just open the cell. Inside the MODULATOR view, hold R1 and press dpad left/right to browse the four slots directly; releasing R1 after browsing stays in the view, while a plain R1 tap still exits.
- **Hold R1 to assign**: while held, focus any parameter cell with the dpad and dial its modulation amount with South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> plus dpad. West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> flips the cell between unipolar and bipolar. East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> clears the cell's assignment. Release R1 when done.
- The MODULATOR view is scope aware: opened from MIX it edits the MIX modulators, from PERFORM the PERFORM modulators.

## <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0803.svg" height="16" alt="PERFORM"> Macros

Twelve performance macros: M1 to M8 are sliders, M9 to M12 are momentary action buttons.

- **Tap R2**: the PERFORM view. Dpad focuses a slider, South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> plus dpad moves it. With the shape layer (hold L1), the faces fire M9 to M12, and they stay active only while held.
- **Hold North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> in PERFORM** to open the macro picker: dpad chooses any of the twelve, release confirms. That macro becomes the active one.
- **Hold R2 to assign** on any device view: focus a cell, dial the amount, West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> flips polarity, East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> clears. Release when done.
- The same hold works inside a MODULATOR view: assign a macro to a track or MIX modulator's own knobs (Rate, Phase, and the rest), so one slider can, say, sweep a modulator's speed. The one exception is PERFORM's own modulators, since they drive the macros themselves; trying it there just shows a toast explaining why.

A macro can drive dozens of parameters at once across every track.

---

## The CLEAR layer

Hold **L2** and the face buttons become:

| Face | Action |
|---|---|
| West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> | UNDO |
| North <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E38.svg" height="16" alt="north"> | REDO |
| East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> | RESET MOD: clear the current view's modulation assignments |
| South <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E34.svg" height="16" alt="south"> | RESET PARAMS: reset the current view's parameters |

The deck row shows these while L2 is down. Undo history covers parameter edits, resets, randomize, paste and scene operations.

**L2 plus R2 together randomizes the current device.** It is curated per device: on EUCLID it rolls the pattern but never Probability, Reset Beat or Drone, and never lands on silence.

---

## Projects

Press **MENU**: SAVE, SAVE AS, LOAD, NEW, OPTIONS, QUIT.

- **SAVE** overwrites after a confirm. A never saved project routes to SAVE AS.
- **SAVE AS**: left/right move the cursor, up/down cycle the character, West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> confirms, East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> deletes a character, MENU cancels.
- **LOAD**: dpad chooses, West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> loads. **Hold East <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E37.svg" height="16" alt="east"> about 1.5 s on a project to delete it**, with a confirm dialog. MENU backs out.
- **NEW** starts fresh after a confirm.
- Tempo is saved with the project.

**Template**: save a project, then copy it on the SD card to `/mnt/SDCARD/EUCLIDTRACK/template/template.euclidtrack`. It becomes the startup state, the NEW project state, and the target of every reset. A template is never overwritten by SAVE.

## Recording

Press MENU and choose **START RECORDING**. The app records its final stereo output, exactly what you hear, into a WAV file. Choosing it closes the menu right away and a toast confirms RECORDING STARTED, so you are back on your instrument with the tape already rolling. The menu entry flips to STOP RECORDING while recording, and the beat light next to the tempo becomes a dot with a red downbeat so you always know recording is live.

- Files land in `/mnt/SDCARD/EUCLIDTRACK/recordings/`, named after the current project plus a timestamp, like `MYTRACK_20260718_143059.wav`.
- Recordings are 16 bit, 48 kHz, and automatically normalized to a healthy level when you stop.
- Stopping also closes the menu right away, and a toast shows RECORDING STOPPED with the file name. Long names scroll back and forth so you can read the whole thing; any button dismisses the toast early.
- Stopping within 5 seconds cancels and deletes the file instead (the toast says RECORDING CANCELLED), so accidental taps leave no litter.
- Length is unbounded: record a whole set. The file is written as it goes, so even a dead battery leaves a playable WAV up to that moment.

## Options (MENU, then OPTIONS)

| Row | Does |
|---|---|
| PITCH MOD RANGE | how far modulation can push pitch: about 1.5 octaves, or the full range |
| EUC PITCH S&H DELAY | a tiny wait before each hit samples its pitch, so modulation has settled first. Pure utility: mostly you won't need to touch the default value |
| PREVIEW PARAM ON FIRST EDIT | when on, the first tweak of a cell only reveals its value instead of changing it |
| THEME | DARK or LIGHT. LIGHT inverts the whole grayscale look; accent colors stay put |

Options are saved with the project, so a template project (see the Projects section) carries its option values into every new project too.

---

## Tips

- The randomizer (L2 plus R2) plus undo (West <img src="https://raw.githubusercontent.com/boorch/euclidtrack-pak/main/.github/icons/uF0E35.svg" height="16" alt="west"> with L2 held) is a fast idea machine: roll, listen, undo, roll again.
- DRIFT's Feedback above 85 percent self sustains forever. Park a drone track into it, gate the track off, and play over the wall of sound.
- Set Steps to Drone and modulate Velocity with a slow LFO for evolving pads that breathe on their own.
- An LFO on Shimmer Amt morphs the shimmer choir while it blooms.
- The map plus copy chords make sound design fast: build one great track, hold Select, copy the whole row, paste it onto another track, then vary.

## Troubleshooting

- **Rare tiny audio crackle, about once a minute**: this is the device's wifi radio interrupting audio. Turn wifi off in the system settings when recording or performing.
- **No sound**: check the transport (tap START), the track gates (hold START and look at the bottom row), Triggers on the EUCLID view (a pattern with zero hits plays nothing), MUTE on the mixer (MIX view, hold L1: the faces show MUTE or UNMUTE per track), the master volume (R3 plus dpad up), and DRIFT's Mix on a track that seems silent but is running.
- **Stuck or strange state**: quit via MENU and relaunch. Projects are safe on the SD card once saved.
