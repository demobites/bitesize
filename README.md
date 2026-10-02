# bitesize

**A skill that teaches your coding agent to film a narrated product demo you can actually post.**

Made by [DemoBites](https://www.demobites.com): video demos for everything you ship.

---

Ask a coding agent for a demo video and you usually get a raw screen capture: small, unzoomed, quiet, with a voice that talks over the wrong moment. `bitesize` is one `SKILL.md` file of rules we learned from rejected takes. It tells the agent how to write the story, film a real browser, move the camera, place the voice and frame the result. No scripts, no account, no service. Your agent builds the pipeline itself.

## Same prompt, with and without the skill

We gave the same prompt to Claude Code on fresh Linux machines, once without the skill and once with it. Nobody answered questions. A separate model judged both videos blind, without knowing which was which.

| | Without the skill | With `bitesize` |
|---|---|---|
| Resolution | 1280 × 720, raw capture | 1920 × 1080, framed in a browser window |
| Camera | no zooms | zooms on the search box, suggestions and contents |
| Loudness | −22 LUFS | −16 LUFS |
| Blind score | 5.0 / 10 | **7.6 / 10** |
| Post as is? | no | **yes** |



https://github.com/user-attachments/assets/d998d628-0cec-4dd5-8f32-027975a2dfd7

**With bitesize**

https://github.com/user-attachments/assets/e9373464-e109-4782-8015-f6cb92fe1bf8





The prompt both runs received, word for word, is in [examples/wikipedia-turing/prompt.md](examples/wikipedia-turing/prompt.md). The judge's notes are in [examples/wikipedia-turing/results.md](examples/wikipedia-turing/results.md).

## What the skill changes

- **Story first.** 30 to 45 seconds, 6 to 10 beats, a framing line for someone new to the product, and every move narrated before it happens. It uses the page's own words and never splits a sentence.
- **A real camera.** Every beat is close or wide. It zooms on the field you type in, pans between neighbours instead of bouncing, breathes out while the page scrolls, and keeps the cursor in frame.
- **A visible cursor.** Driven browsers render no cursor, so it records the pointer as data and draws it sharp, gliding like a hand.
- **Voice on time.** One line per beat, never on top of the previous one, normalised to −16 LUFS, with captions beside the video.
- **A finished look.** 1080p, the recording in a browser window on a backdrop, a clean first frame and a clean ending.

## Install

**Claude Code (plugin):**

```
/plugin marketplace add demobites/bitesize
/plugin install bitesize@bitesize
```

**Claude Code (manual):** copy `skills/bitesize` to `~/.claude/skills/bitesize` (for you) or to `.claude/skills/bitesize` in a project.

**Other agents:** the skill is a single Markdown file. Agents that read `SKILL.md` folders can use `skills/bitesize` as it is; for any other agent, add the file to its instructions.

Then ask for a demo in plain words: *"Make a short narrated demo of how to invite a teammate on localhost:3000."*

## What it needs

- A machine where the agent can install a real browser (Playwright and Chromium) and `ffmpeg`. On a fresh machine it installs them itself.
- A voice: the rules use ElevenLabs, with your key in `ELEVENLABS_API_KEY`.
- A model that can work for a while: the run above took about 14 minutes and about $1 of API usage, against 4 minutes without the skill.

## Honest notes

- This is one run of each version on one task, judged by one model. Your results will vary with the site and the agent.
- The skill has been tested with Claude Code. It makes no claims about other agents.
- It films web apps in a browser. It does not record native apps or your real screen.

## Want the finished version?

`bitesize` gives your agent the taste. [DemoBites](https://www.demobites.com) turns every feature you ship into a polished, narrated demo, and delivers it to your customers in your product, your update center and their inbox.

## Licence

[MIT](LICENSE). Made with love by [DemoBites](https://www.demobites.com).
