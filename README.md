# mpd-audiomixer

Client-side audio joiner + EBU R128 normalizer for the Money Patterns Decoded weekly pipeline.

Takes ElevenLabs output parts → sample-perfect join with crossfade → optional silence trim + breath removal → LUFS normalization → MP3/WAV export. Runs entirely in the browser, no server, no API keys.

## Live
https://ealihasnain.github.io/mpd-audiomixer/

## Files
- `MPD_Audio_Joiner.html` — the tool
- `index.html` — redirects root → joiner

## Pipeline
1. Upload audio parts (mp3/wav/m4a/ogg/flac, up to 20)
2. Select options (join crossfade / trim silence / breath removal / LUFS)
3. Process → waveform preview + A/B compare
4. Export MP3 (lamejs) or WAV (16-bit PCM)

## Stack
Pure HTML + vanilla JS. Web Audio API for decode/processing, lamejs for MP3 encode.
