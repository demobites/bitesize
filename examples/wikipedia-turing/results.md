# Results

The two videos were judged blind by a separate Claude Opus 5.5 call. It saw a 16 frame contact sheet of each video, the narration transcript with timings, and the measured stats (resolution, length, loudness), with the labels shuffled. The scorecard was written before the runs.

| | Without the skill | With `bitesize` |
|---|---|---|
| Length | 37.1 s | 47.8 s |
| Resolution | 1280 × 720 | 1920 × 1080 |
| Loudness | −22 LUFS | −16 LUFS |
| Agent time | 4.3 min | 13.8 min |
| API cost | about $0.29 | about $1.03 |
| Story | 7 | 8 |
| Camera | 3 | 7 |
| Cursor | 5 | 8 |
| Look | 4 | 8 |
| Sync | 6 | 7 |
| **Overall** | **5.0** | **7.6** |
| Post as is? | no | **yes** |

## The judge's words

Quoted verbatim. "TOC" is the article's table of contents.

**Without the skill.** Camera: "No zooms at all. A static full-page 720p capture keeps the search box, suggestions and TOC tiny; only the orange highlight boxes guide the eye." Biggest flaw: "No zooms at 720p, so every key UI moment (search box, suggestions, TOC entry) is tiny and hard to read." Post as is: "Low resolution, no camera work and low loudness make it look amateur next to a proper feature video."

**With the skill.** Camera: "Zooms land well on the search box, suggestions, TOC expansion and the highlighted TOC entry. The article open and the section landing (≈15–18s, 30–33s) stay zoomed out and unreadable." Look: "1080p on a padded gradient backdrop, good −16 LUFS loudness, polished overall." Biggest flaw: "The payoff moment, landing on the section, is shown fully zoomed out, so the viewer can't read the heading they just jumped to." Post as is: "Minor timing slips, but it is clear, polished and complete. Shippable, though tightening the landing zoom would help."

## Narration

The narration each run wrote is in [without-skill.transcript.txt](without-skill.transcript.txt) and [with-skill.transcript.txt](with-skill.transcript.txt).

## Caveats

One run of each version, one task, one judge. Treat it as a demonstration, not a benchmark.
