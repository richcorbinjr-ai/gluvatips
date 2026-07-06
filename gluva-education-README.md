# Gluva Health — Pilot Education Page

A simple, single-page education site for CGM pilot participants. Fast to read (30-40 seconds), with the lowest-hanging-fruit glucose tips and two embedded YouTube videos. Matches the main Gluva Health site style (navy / gold / lime).

## How to put your YouTube videos in

You don't need to know code. Each video is controlled by one short **video ID**. Here's how to find it and swap it in.

### Step 1 — Find your video's ID
Open your video on YouTube and look at the web address (URL):

```
https://www.youtube.com/watch?v=dQw4w9WgXcQ
                                  ^^^^^^^^^^^
                                  this part is the ID
```

The ID is the string of letters/numbers right after `v=`. In the example above it's `dQw4w9WgXcQ`.

(If you use a share link like `https://youtu.be/dQw4w9WgXcQ`, the ID is the part after the slash — same thing.)

### Step 2 — Paste it into the page
Open `index.html` in any text editor and search for `VIDEO_ID_1`. You'll see this:

```html
src="https://www.youtube.com/embed/VIDEO_ID_1"
```

Replace `VIDEO_ID_1` with your first video's ID. For the example it becomes:

```html
src="https://www.youtube.com/embed/dQw4w9WgXcQ"
```

Do the same for `VIDEO_ID_2` with your second video. That's it — save the file.

### Step 3 — (Optional) Change the titles under each video
Right below each video, change the text in `<h3>` and `<p>` to match what your videos are actually about.

### Notes
- The video **must be public or unlisted** on YouTube (not private) for the embed to play.
- The `/embed/` in the address is required — that's the format YouTube uses for embedding. Don't paste the normal `watch?v=` link into the `src`; just swap the ID.
- The videos are responsive — they resize automatically on phones.

## Editing the tips

Each tip is a `<div class="tip">` block in `index.html`. To change wording, edit the `<h3>` (the tip) and `<p>` (the explanation). The little green tag is the `<span class="why">`. Tip #1 has an extra `hero-tip` class that gives it the gold highlight — leave that on whichever tip you want to feature.

## Hosting it on GitHub Pages

1. Create a new repository on GitHub.
2. Upload `index.html` (and this README).
3. Go to **Settings → Pages → Build from branch**, pick your main branch, save.
4. Your page goes live at `https://<your-username>.github.io/<repo-name>/`.
5. Link to that address from your main Gluva site (a "Pilot Education" or "Learn" button).

## A note on the content

The tips are written as general wellness habits, not medical advice, and the page includes a disclaimer to that effect. Keep it that way — avoid adding claims that the program treats, cures, or prevents diabetes or any disease. If you add or change tips, keep them lifestyle-level and non-prescriptive.
