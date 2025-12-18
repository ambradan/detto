# Features

Complete feature list for Detto.

---

## Input

| Feature | Description |
|---------|-------------|
| Audio upload | Drag & drop, supports mp3/m4a/wav/ogg/webm |
| In-app recording | Tap to start, tap to stop |
| Manual text input | "Oppure scrivi qui" field as voice alternative |
| Optional context | Text or voice field to guide interpretation |
| Voice context | Audio recording available for context field |
| Personal abbreviations | Custom definitions (e.g., "thx = Grazie"), persistent |

---

## Audio Processing

| Feature | Description |
|---------|-------------|
| Noise suppression | Active during recording |
| Echo cancellation | Reduces environmental echo |
| Auto gain control | Automatic amplification for low voice |
| Audio level indicator | Visual feedback during recording |
| Low volume warning | "Volume basso — avvicina il microfono se possibile" |
| Background voice warning | "Altre voci rilevate — il risultato potrebbe variare" |

---

## NIV / Ventilator Mode

Specific handling for users with respiratory support devices.

| Feature | Description |
|---------|-------------|
| No auto-stop | Long pauses and silence do not interrupt recording |
| Protected turn-taking | Only explicit Stop tap ends recording |
| "Non ho finito" button | Visual confirmation that recording continues |
| Ventilator noise filter | Removes medical device background noise |
| Non-verbal sound removal | Sighs, groans, unintentional vocalizations removed |
| Communicative sounds preserved | "eh no", "mmm sì" kept if they carry meaning |

---

## LLM Processing

| Feature | Description |
|---------|-------------|
| Semantic cleaning | Removes hesitations, repetitions, false starts |
| Abbreviation expansion | Automatic from context + user abbreviations |
| Sentence completion | Only if meaning is clearly recoverable |
| Uncertainty handling | Unclear words omitted or marked with "[…]" |
| No invention | Never fabricates content, never adds words |
| Context-aware | Uses context to disambiguate, not to invent |

---

## Output

| Feature | Description |
|---------|-------------|
| Editable output | Textarea is manually editable |
| WhatsApp format | Brief, direct, informal |
| Email format | Structured, with greeting and closing |
| LinkedIn format | Formal, professional tone |
| "Mio stile" style | Preserves irony, personal tone, expressions |
| "Neutro" style | Standard professional tone |
| Draft label | If low quality: "Bozza — verifica prima di copiare" |

---

## Actions

| Feature | Description |
|---------|-------------|
| Copy text | With "Detto ✓" feedback |
| Read (TTS) | Generates audio and plays automatically |
| Auto-play | No additional click needed to listen |
| Replay | Player visible for re-listening |
| Rewrite clearer | LLM reformulates while preserving meaning |
| Undo | Reverts to previous version |
| Retry | Restarts from recording/input |

---

## Text-to-Speech

| Feature | Description |
|---------|-------------|
| Italian male voice | ElevenLabs default |
| Auto-play on Read | Starts immediately without extra click |
| Inline player | Play/pause controls visible after generation |

---

## Quick Phrases

| Feature | Description |
|---------|-------------|
| 5 default phrases | Pre-configured for common situations |
| One-tap action | Tap = copy to clipboard + append to output |
| Add custom | User can create personal phrases |
| Persistence | Saved in localStorage |

**Default phrases:**
1. "Un attimo, preparo la risposta"
2. "Preferisco rispondere via vocale, ti mando un messaggio audio"
3. "Possiamo sentirci in call? Per me è più facile"
4. "Scusa il ritardo, faccio fatica a scrivere velocemente"
5. "Grazie per la pazienza"

---

## Persistence (localStorage)

| Data | Persisted |
|------|-----------|
| Personal abbreviations | ✅ |
| Custom quick phrases | ✅ |
| Collapsed section states | ✅ |
| Context | Current session only |

---

## Error Handling

| Feature | Description |
|---------|-------------|
| Generic error | "Non è stato possibile elaborare l'audio. Riprova." |
| Mic permission error | "Serve il permesso per accedere al microfono." |
| MediaRecorder error | Disables voice only, keeps text input |
| Graceful fallback | If audio constraints unsupported, records anyway |

---

## UX Principles Applied

| Principle | Implementation |
|-----------|----------------|
| User control | Output always editable, never auto-sent |
| No blame | Neutral messages, never "repeat more clearly" |
| Minimum effort | One-tap where possible, auto-play |
| Transparency | "Bozza" if uncertain, "[…]" if words missing |
| Preserve identity | "Mio stile" does not flatten personality |

---

## Summary

| Category | Count |
|----------|-------|
| Input | 6 |
| Audio Processing | 6 |
| NIV Mode | 6 |
| LLM Processing | 6 |
| Output | 7 |
| Actions | 7 |
| TTS | 3 |
| Quick Phrases | 4 |
| Persistence | 4 |
| Error Handling | 4 |
| UX Principles | 5 |
| **Total** | **58** |
