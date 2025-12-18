# Known Limits

Detto is designed for specific use cases and does not attempt to solve everything.

Limits are documented here because transparency is part of the design.

---

## What Detto does NOT do

### No speaker recognition
Detto cannot distinguish your voice from other voices in the room.
If the TV is on or someone else is speaking, their words may be transcribed.

### No real-time call transformation
Detto processes recorded audio, not live calls.
For real-time voice transformation during calls, see [Whispp](https://whispp.com).

### No clinical AAC replacement
Detto is not a certified assistive communication device.
It does not replace clinical AAC systems for users who need them.

### No offline mode
Detto requires internet connection for ASR, LLM, and TTS processing.

### No account or history
Nothing is saved server-side. Closing the browser clears the session.
Only localStorage persists (abbreviations, phrases, preferences).

---

## What may still happen

### Background speech affects output
If other voices are audible, they may be partially transcribed.
The warning "Altre voci rilevate" will appear, but cannot fully prevent this.

### Very low volume reduces accuracy
If voice is too soft, ASR may miss words.
The warning "Volume basso" will appear.
Consider using a closer microphone or headset.

### Some words will be lost
When audio is unclear, words are omitted rather than guessed.
This is intentional. Gaps are preferable to fabrication.

### Format/style is approximate
LLM transformations (WhatsApp, Email, LinkedIn, Mio stile, Neutro)
are best-effort interpretations, not guarantees.

---

## Hardware considerations

### Microphone distance
Phone microphone at arm's length captures room noise.
A headset or closer mic significantly improves results.

### Ventilator/respirator noise
Noise suppression helps but does not eliminate device sounds.
The system is tuned to tolerate this, but very loud environments remain challenging.

---

## Philosophical limits

### Detto does not pretend certainty
When something is unclear, it says so.
"[…]" in output means: this part was not understood.

### Detto does not optimize for speed
Processing takes a few seconds.
This is acceptable. Rushing creates errors.

### Detto does not scale to enterprise
This is a personal tool, not a platform.
No multi-user, no admin panel, no analytics dashboard.

---

## Summary

| Limit | Reason |
|-------|--------|
| No speaker recognition | Not technically feasible without biometrics |
| No live calls | Different architecture needed (see Whispp) |
| No offline | Requires cloud ASR/LLM/TTS |
| Background noise affects output | Physics of sound |
| Words may be lost | Intentional: omit > invent |

These limits are explicit by design.
Detto prefers transparency over false promises.
