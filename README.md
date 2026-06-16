# Awesome Beat Sync Video Editors [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, templates, and resources for editing videos that cut on the beat — synced automatically to the music drops.

Beat sync editing is the technique behind almost every viral TikTok, Reel, and YouTube Short you've seen since 2023 — cuts that hit exactly on the drop, transitions that snap to the bass, lyric punches that land on the syllable. This list tracks the best **free** and paid tools for doing it, the open templates, and the niche communities pushing the format.

## Contents

- [What is beat sync editing?](#what-is-beat-sync-editing)
- [Free browser-based editors](#free-browser-based-editors)
- [Free desktop editors](#free-desktop-editors)
- [Paid editors with auto-beat-sync](#paid-editors-with-auto-beat-sync)
- [Beat sync templates by niche](#beat-sync-templates-by-niche)
- [Open-source beat detection libraries](#open-source-beat-detection-libraries)
- [Tutorials](#tutorials)
- [Communities](#communities)
- [Trending sounds for beat-sync edits](#trending-sounds-for-beat-sync-edits)

## What is beat sync editing?

Beat sync editing aligns video cuts to the beats (or drops) of a music track. Instead of cutting on a clock — say, every 1.5 seconds — you cut on the kick, the snare, the bass drop, or a lyric punch. The result feels musical and grabs viewer attention in the first 1.3 seconds, which is the window YouTube's data says viewers decide whether to keep watching a Short.

The technique started in AMV (anime music video) and dance edit communities in the early 2010s, exploded with TikTok in 2020, and went fully automated in 2024-2026 as AI onset-detection libraries (librosa, Essentia, Web Audio's AudioWorklet) became fast enough to run in a browser tab.

## Free browser-based editors

These need no install, no signup, no watermark.

- **[Cutflux](https://cutflux.app)** — Drop a video, drop a song, the AI snaps every cut to the beat. Runs entirely in your browser (ffmpeg.wasm + Web Audio). Free, no login, no watermark. Best for: anyone who wants the actual beat-sync feature without a paywall. Niche labs for glitch-on-beat, photo-montage-on-beat, and VS-maker on the same site.
- **[Clipchamp](https://clipchamp.com)** — Microsoft-owned web editor with beat markers. Free tier exports up to 1080p. Manual beat alignment, not automatic.
- **[Kapwing](https://kapwing.com)** — Browser editor with a free tier (with watermark). Has a beat-detect tool but it's behind login.

## Free desktop editors

- **[DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve)** — Industry-grade free editor. Has manual beat markers via Fairlight; no auto-sync.
- **[CapCut Free tier](https://www.capcut.com)** — The classic. Auto-beat-sync was free until early 2026; in the 2026 Pro restructure ($19.99/mo), advanced beat features got tiered up.
- **[Shotcut](https://shotcut.org)** — Open-source, manual beat markers.
- **[OpenShot](https://openshot.org)** — Open-source, basic editing, no auto-beat-sync.

## Paid editors with auto-beat-sync

- **CapCut Pro** — $19.99/mo as of 2026. Auto-beat-sync, AI Auto-Edit, AI Effects Generator.
- **Veed.io Pro** — Browser-based, ~$25/mo. More focused on AI text-to-video and AI presenters than beat sync.
- **Descript** — $24/mo. Excellent for podcasts and text-based video editing; weak on music-driven cuts.
- **Submagic** — $16-$48/mo. Captions + hooks specialist, not a beat-sync tool.
- **OpusClip** — Repurposing long-form to shorts. AI-driven, not beat-first.
- **Klap** — Similar to OpusClip. Long-form-to-short workflow.

## Beat sync templates by niche

Each niche has its own format. Here are the patterns that consistently hit.

### Dance edits
- 4-beat slow intro → drop → 8 rapid cuts to choreo highlights → freeze on final pose.
- Recommended sounds: sped-up house, jersey club, Afrobeat instrumentals.

### Sports edits (NBA, soccer, gym PR)
- Slow-mo zoom on the athlete → drop hits exactly on the dunk/goal/lift → glitch transition → repeat with 3 more clips.
- Recommended sounds: phonk, drift phonk, "Sahara" by Hensonn, Travis Scott instrumentals.

### AMV (Anime Music Videos)
- 2-second establishing shot → drop → cuts on every kick across a fight scene → lyric punches on character close-ups.
- Recommended sounds: Linkin Park remixes, j-rock chorus drops, lofi anime piano.

### Sneaker reveals
- Mystery shot of feet → bass drop → reveal cut → 360 spin → drip-stack flex.
- Recommended sounds: Brooklyn drill, NY drill, Detroit slap beats.

### Car edits
- Engine rev synced to beat-1 → drop → angle cuts on each beat → drift on the bass roll.
- Recommended sounds: phonk, eurobeat, hyperpop.

### Lyric punch-outs
- Cut B-roll on every stressed syllable. Hardest format; needs lyric-aware editing. Cutflux has an experimental version of this.

### Glow-up / before-after
- Before shot held → drop hits → after shot lands → 3 more before/after pairs each on a beat.
- Recommended sounds: "Young Hearts Run Free" sped-up, Charli XCX remixes.

## Open-source beat detection libraries

For developers building their own beat-sync tools.

- **[librosa](https://librosa.org)** — Python, the gold standard for music information retrieval. `onset_detect()` and `beat_track()` are the workhorses.
- **[Essentia](https://essentia.upf.edu)** — C++ with Python bindings, extremely accurate beat tracking via `RhythmExtractor2013`.
- **[madmom](https://github.com/CPJKU/madmom)** — Python, deep-learning-based beat tracker. State of the art accuracy.
- **[Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)** — Built into every browser. Pair with a spectral-flux onset detector for client-side beat detection (this is how Cutflux does it).
- **[Tone.js](https://tonejs.github.io)** — JavaScript audio framework, not a beat detector but useful for the surrounding audio scheduling.
- **[ffmpeg](https://ffmpeg.org)** — Not a beat detector, but the universal video toolkit you'll use to apply the cuts.
- **[auto-editor](https://github.com/WyattBlue/auto-editor)** — CLI tool that auto-cuts videos by silence or volume. Can be repurposed for beat cuts.

## Tutorials

- "How to make beat sync edits in CapCut" — YouTube has hundreds; the basic workflow is: import audio, tap to add beat markers, snap clips to markers.
- "How beat detection works in the browser" — Web Audio + spectral flux + 280ms minimum spacing is the standard recipe. The Cutflux source on GitHub (when open) is a clean reference.
- "AMV editing the right way" — r/AnimeMusicVideos wiki has a beat-sync section.

## Communities

- **[r/VideoEditing](https://reddit.com/r/VideoEditing)** — General editor community, beat-sync questions come up daily.
- **[r/CapCut](https://reddit.com/r/CapCut)** — Largest CapCut-specific community; post-Pro-hike, lots of "free alternative?" threads.
- **[r/NewTubers](https://reddit.com/r/NewTubers)** — Short-form creators.
- **[r/AnimeMusicVideos](https://reddit.com/r/AnimeMusicVideos)** — AMV community, 700k+ members.
- **Discord — Video Editor Hub** — 40k+ members, neutral on tools.
- **Discord — Creator Now** — Short-form creator community.

## Trending sounds for beat-sync edits

(Updated monthly. Last update: 2026-06.)

- Charli XCX — "Rock Music" (glitch edits)
- Candi Staton — "Young Hearts Run Free" sped-up (glow-up edits)
- Travis Scott instrumentals (sneaker/car edits)
- Phonk / Drift Phonk (sports/gym edits)
- Hensonn — "Sahara" (sports edits)
- Saxboy Billy — "The Puerto Rico Song" (general TikTok)

## Contributing

PRs welcome. If you maintain a beat-sync editor, template pack, or tutorial, open a PR with a one-line description and a link.

## License

[CC0](LICENSE) — Public domain. Use anything here however you want.

---

Maintained as a public reference for the short-form editing community. If you spot something missing, [open an issue](../../issues).
