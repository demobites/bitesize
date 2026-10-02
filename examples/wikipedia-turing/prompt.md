# The prompt

Both runs received exactly this prompt, word for word. The only difference between them was whether the `bitesize` skill was installed.

```
Make a short narrated demo video of Wikipedia (https://en.wikipedia.org). Show how someone looks up the article on Alan Turing and jumps straight to the section about the Turing test using the article's table of contents.

Save the finished video as ~/out/demo.mp4. For the voice, use ElevenLabs — the API key is in the ELEVENLABS_API_KEY environment variable.

You are working alone on a fresh Linux machine: install whatever you need, make every decision yourself, and do not stop until ~/out/demo.mp4 exists. Nobody will answer questions.
```

## The setup

- Fresh Linux machines (Vercel Sandbox, Ubuntu, Node 24, 4 vCPU), nothing preinstalled beyond Claude Code.
- Claude Code 2.1.283, headless (`claude -p`), model Claude Opus 5.5.
- Same ElevenLabs account for both runs.
- Run on 2026-09-29.
