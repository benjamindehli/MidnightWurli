# Midnight Wurli

Midnight Wurli is a sampled Wurlitzer 200A electric piano instrument that focuses on capturing the character of the instrument played softly at low volume. It uses two signal sources: the direct line out from the Wurlitzer and a contact microphone attached to the instrument. The contact microphone captures the mechanical noises, such as key clicks, release sounds, and pedal movements which results in a more intimate, close-up sound.

The instrument includes both tonal samples and mechanical noise samples. It also features built-in effects including tremolo, tape echo, room reverb, and multiple amplifier impulse responses. Each key includes velocity-based round robins to enhance realism.

## Release notes

### Version 2.0.0 (2026-07-19)

- Added a plugin version. See the section "The plugin version".
- Effect bindings now use effectIndex, and a misleading type="percent" attribute was removed.
- Fixed the loNote value for the keyboard colors.

### Version 1.0.0 (2025-08-13)

- First version released.

## Included formats

- VST3 (macOS)
- AU (macOS)
- Standalone application (macOS)
- Decent Sampler (macOS, Windows and Linux)

The plugin version is currently released for macOS only.
Windows and Linux versions are planned.
Until then, the Decent Sampler version covers those platforms.

## The plugin version

The plugin is a self-contained instrument, available as VST3, AU and Standalone.
Samples, graphics and impulse responses are all embedded in the plugin itself, losslessly compressed, so there are no external files to install or locate.
Only the samples for the selected preset are loaded into memory, and a fresh instance lets you choose which preset to load before anything is decoded.

The plugin has all the controls and features from the Decent Sampler version, including MIDI learn, the master volume fader with output meter, value readouts for the knobs and full DAW automation.
On top of that, the plugin version adds:

- Drift wheels next to the pitch and modulation wheels, adding a subtle random pitch and volume drift to each voice.
- A velocity curve setting in the settings menu.

## Technical specification

|                                    | Sample rate | Bit depth | Channels   | Number of files | File size |
| ---------------------------------: | ----------: | --------: | ---------- | --------------: | --------: |
|                        **Samples** |      48 kHz |    24 bit | 1 (mono)   |            2332 |   1.20 GB |
| **Impulse responses (Amplifiers)** |      48 kHz |    24 bit | 1 (mono)   |               4 | 356.00 KB |
|    **Impulse responses (Effects)** |      48 kHz |    24 bit | 2 (stereo) |               2 | 481.00 KB |

## Instrument Presets

### Midnight Wurli

|![Midnight Wurli](/Screenshots/midnight-wurli.png)|
|:--:|
|Midnight Wurli|

- Full version of the instrument with 36 samples per key.
- 18 note-on samples and 18 release samples per key.
- Round robin samples per velocity group to avoid repetition.
- Includes mechanical noises (release and damper).
- Includes all six impulse responses: four amplifiers, one echo, and one room reverb.
- 28 damper pedal samples.

### Midnight Wurli (Lite)

|![Midnight Wurli (Lite)](/Screenshots/midnight-wurli-lite.png)|
|:--:|
|Midnight Wurli (Lite)|

- A lightweight version of the instrument designed for lower CPU and RAM usage.
- Contains a single sample per velocity group for each key (no round robin).
- Impulse responses (amplifiers, echo, room) are disabled.
- Still includes basic mechanical sounds but with simplified behavior.

## User Interface

### Proximity

|![Mix controls for proximity](/Screenshots/proximity.png)|
|:--:|
|Mix controls for proximity|

- Crossfades between the direct line out and contact microphone audio.
- Turning the knob toward "Close" emphasizes the contact mic (mechanical sounds).
- Turning toward "Distant" emphasizes the clean line out signal.
- Affects the balance of both tonal and mechanical elements.

### Mechanics

|![Volume controls for the mechanical noise](/Screenshots/mechanics.png)|
|:--:|
|Volume controls for the mechanical noise|

#### Release

- Controls the volume of the key release noise.
- The audio is affected by the current setting of the Proximity knob.
- Represents the subtle mechanical sound of a key returning after being released.

#### Damper

- Controls the volume of the damper (sustain pedal) noise.
- Includes pedal down and pedal up samples.
- Also influenced by the Proximity setting.

### Tremolo

|![Controls for the tremolo depth](/Screenshots/tremolo.png)|
|:--:|
|Controls for the tremolo depth|

- Controls the depth of the built-in tremolo effect, which is named vibrato on the original Wurlitzer 200A.
- Tremolo is applied after sample playback and before amplifier, tape echo and room reverb, emulating the original instrument’s modulation circuit.

### Amplifier

|![Amplifier select list](/Screenshots/amplifier.png)|
|:--:|
|Amplifier select list|

- Selects one of five amplifier settings:
  - Direct (bypasses all amp simulation)
  - American (Fender Twin Reverb)
  - British (Vox AC15H1TV)
  - Japanese (Roland JC-120 Jazz Chorus)
  - Norwegian (Tandberg Model 2 T)
- All amplifier impulse responses were recorded with a Shure SM57 and a Royer R-121 microphone.

### Echo

|![Mix controls for tape echo](/Screenshots/echo.png)|
|:--:|
|Mix controls for tape echo|

- Blends in a tape echo impulse response with a slapback delay characteristic.
- Positioned before the amplifier in the signal chain.

### Room

|![Mix controls for room reverb](/Screenshots/room.png)|
|:--:|
|Mix controls for room reverb|

- Adds stereo room reverb via an impulse response.
- Positioned after the amplifier in the signal chain.

### Volume

|![Controls for master volume](/Screenshots/volume.png)|
|:--:|
|Controls for master volume|

- Master volume control for the entire instrument.
- Applied after all effects in the signal path.

## Equipment used

|                                             Name                                             |                                                    Image                                                     |
| :------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------: |
|                               [Wurlitzer 200A][Wurlitzer 200A]                               |                               ![Wurlitzer 200A](/Equipment/wurlitzer-200a.jpg)                               |
|           [Hairball Audio FET/RACK Revision D][Hairball Audio FET/RACK Revision D]           |           ![Hairball Audio FET/RACK Revision D](/Equipment/hairball-audio-fet-rack-revision-d.jpg)           |
| [DIY Recording Equipment G Bus VCA Compressor][DIY Recording Equipment G Bus VCA Compressor] | ![DIY Recording Equipment G Bus VCA Compressor](/Equipment/diy-recording-equipment-g-bus-vca-compressor.jpg) |
|                          [Handsome Audio Zulu][Handsome Audio Zulu]                          |                          ![Handsome Audio Zulu](/Equipment/handsome-audio-zulu.jpg)                          |
|                           [Fender Twin Reverb][Fender Twin Reverb]                           |                           ![Fender Twin Reverb](/Equipment/fender-twin-reverb.jpg)                           |
|                                 [Vox AC15H1TV][Vox AC15H1TV]                                 |                                 ![Vox AC15H1TV](/Equipment/vox-ac15h1tv.jpg)                                 |
|                    [Roland JC-120 Jazz Chorus][Roland JC-120 Jazz Chorus]                    |                    ![Roland JC-120 Jazz Chorus](/Equipment/roland-jc-120-jazz-chorus.jpg)                    |
|                           [Tandberg Model 2 T][Tandberg Model 2 T]                           |                           ![Tandberg Model 2 T](/Equipment/tandberg-model-2-t.jpg)                           |
|                      [Fulltone Tube Tape Echo][Fulltone Tube Tape Echo]                      |                      ![Fulltone Tube Tape Echo](/Equipment/fulltone-tube-tape-echo.jpg)                      |
|           [Chase Bliss Audio & Meris CXM 1978][Chase Bliss Audio & Meris CXM 1978]           |          ![Chase Bliss Audio & Meris CXM 1978](/Equipment/chase-bliss-audio-and-meris-cxm-1978.jpg)          |

## About this repository

This repository contains the source for both the Decent Sampler library (the DecentSampler folder) and the plugin version.
The plugin is a thin wrapper around the shared Dehli Musikk sampler engine, and a converter translates the Decent Sampler library into the engine's native preset format at build time.
The audio files are not part of this repository, since the samples are a paid product.
The full version is available from [store.dehlimusikk.no][Gumroad profile].

[Gumroad profile]: https://store.dehlimusikk.no/
[Wurlitzer 200A]: https://www.dehlimusikk.no/equipment/instruments/wurlitzer-200a/
[Hairball Audio FET/RACK Revision D]: https://www.dehlimusikk.no/equipment/effects/hairball-audio-fet-rack-revision-d/
[DIY Recording Equipment G Bus VCA Compressor]: https://www.dehlimusikk.no/effects/diy-recording-equipment-g-bus-vca-compressor/
[Handsome Audio Zulu]: https://www.dehlimusikk.no/equipment/effects/handsome-audio-zulu/
[Fender Twin Reverb]: https://www.dehlimusikk.no/equipment/amplifiers/fender-twin-reverb/
[Vox AC15H1TV]: https://www.dehlimusikk.no/equipment/amplifiers/vox-ac15h1tv/
[Roland JC-120 Jazz Chorus]: https://www.dehlimusikk.no/equipment/amplifiers/roland-jc-120-jazz-chorus/
[Tandberg Model 2 T]: https://www.dehlimusikk.no/equipment/amplifiers/tandberg-model-2-t/
[Fulltone Tube Tape Echo]: https://www.dehlimusikk.no/equipment/effects/fulltone-tube-tape-echo/
[Chase Bliss Audio & Meris CXM 1978]: https://www.dehlimusikk.no/equipment/effects/chase-bliss-audio-and-meris-cxm-1978/
