---
name: bitesize
description: Make a narrated product demo video (a screen recording of a web app, 16:9 MP4) from a short description — storyboard, film a real browser, narrate, zoom, frame. Use whenever someone asks to record, film or make a demo video, walkthrough, feature video, tutorial or screen recording of a website or web app.
---

# Product demo video

You turn one sentence ("show how X works") into a finished, narrated demo video of a web app. These are the laws a good demo follows. They were each learned from a rejected take. Follow them all.

## 1. The story (write it before anything films)

- **Budget.** 30 to 45 seconds. 6 to 10 beats. 8 to 14 words per narration line. Never over 90 seconds.
- **Open with a framing line** for someone who is not inside the product yet ("Let's see how to find any article and jump straight to the part you need."). Never open on a UI detail.
- **Narrate the path.** Before every navigation, scroll or drill-down, say where we are going and why, in the beat before it.
- **Linger.** Every beat holds at least its own line plus a breath (words ÷ 2.6 seconds + 0.8 s). A beat that navigates away can carry only one line; say things about a page after you land on it.
- **Never split a sentence across beats, never speak a fragment without context** ("All data." is forbidden; a line is a full clause).
- **Speak the product's own words.** Read the live page's headings, button labels and menu names first; every noun in the narration must appear on screen.
- **Perform actions to the end.** A demo shows the thing happening, never "here you would see". Reversible actions are performed for real and undone after filming. Irreversible actions (payments, emails to real people, deletes) are pointed at and named, never pressed.
- **Cancel is never a beat.** Never zoom on Cancel or Close.
- **Never show an empty state or a screen you did not reach.**

## 2. Filming

- Film a real browser at **1920×1080**. Dry-run the whole flow headless first, off camera, and fix every selector before the real take.
- **The first frame is a fully loaded page.** Wait for network idle plus a beat, and cut everything before it (no white flash, no skeletons). Cut the tail after the last beat.
- **Driven browsers render no cursor.** The viewer must see one. Record the cursor as data (position and type — arrow, pointing hand, text I-beam — at every moment) and draw it crisply in post, so it stays sharp when the camera zooms. Move it like a hand: an eased glide to each target, never a teleport. The real mouse follows the drawn cursor so hover states fire.
- **Know exactly when things happened in the video.** Video timestamps drift from your action log. Measure the offset (for example flash a coloured beacon in the page at known wall-clock times and find the flashes in the recording) and map every action to video time. Zooms and narration are placed from this clock; if it is off, everything lands late.
- For every beat record **what the camera should look at**: the rectangle of the control you hover or click, and, after a click, the rectangle of what it opened (menu, dialog, new section).
- Hide chat widgets and cookie banners with CSS. A page change mid-take is cut with a short fade, never watched loading.

## 3. The camera (zooms)

- Every beat is **close** or **wide**. A field, button, menu item, toggle, row = close. Landing on a page, a chart, a table, search results, a section = wide. What Enter or a navigation reveals is wide.
- **How tight:** the subject should fill 60% of the frame's width or 75% of its height, whichever is smaller; clamp the zoom between 1.25× and 3.0×. The zoomed view never shows anything outside the recording (clamp it inside the frame).
- **Motion is the cost, tightness is the budget.** If one framing can hold two neighbouring subjects (within 4 s of each other) while giving up less than 0.75× of tightness (and staying at least 1.35×), use one steady shot instead of two zooms. If the next subject is near (within 85% of the zoomed view), pan to it while holding the zoom, travelling with the cursor. If it is far, pull out only as far as the union of both, then tighten on arrival.
- **Chained shots overlap by 0.5 s** so the camera travels from one subject to the next instead of pulling out to 1.0 in between. A wide shot ends the previous zoom exactly where it begins.
- **Scrolling means breathe out:** the camera is wide while the page slides.
- No zoom on closing clicks (Cancel, Close, Back, Dismiss). Every shot holds at least 0.9 s. No zoom in the first 0.5 s; the video always ends wide (last 0.8 s).
- **The cursor is inside the frame on every frame.** Simulate the camera against the cursor track; wherever the cursor would leave the view, widen that shot by 1.15× and check again.
- **Moves:** interpolate the translate and the scale together with easing cubic-bezier(0.4, 0, 0.2, 1). A move lasts 0.5 s + min(0.5 × magnitude, 0.7 s), where magnitude is the larger of |Δscale| ÷ 2 and the normalised pan distance.

## 4. The voice

- One audio file per narration line (ElevenLabs), measured. Place each line at its beat; if the previous line is still speaking, start after it with a 0.25 s gap — never on top. The first line starts 0.3 s after its beat. The video ends 0.8 s after the last word (hold the last frame if needed). Normalise to −16 LUFS.
- Write a captions file (SRT) beside the video from the placed lines.

## 5. The look

- 1920×1080, 30 fps, H.264 + AAC, fast start.
- The recording sits **centre stage in a browser window**: 1600×900 of content under a 68 px bar with the three traffic-light dots and a URL pill, corners rounded 24 px, a soft shadow, on a dark gradient background. The camera zooms inside the window; the window stays put.
- The cursor is 2% of the frame width tall, grows with the zoom but never past 1.6× its size, and dips to 0.88× for 0.4 s on a click. No click ripples.

## 6. Deliver

Put the finished MP4 where you were asked, with the captions beside it, and report its length and what it shows.
