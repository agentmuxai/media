# AgentMux media

The AgentMux YouTube series and its sources: scripts, narration text, storyboards, the render pipeline, and the finished renders. YouTube is where people watch; this repository is where the videos are made and kept.

## Layout

```
episodes/<nn-slug>/
    script.md        beats: the narration line, the action, the zoom target, the chapter title
    narration.txt    the spoken text, one line per beat, exactly as the voice reads it
    storyboard.md    the shot list and the demo data the episode needs
    render/          finished files for an approved episode: <slug>.mp4, <slug>.srt, thumbnail.png, description.txt
pipeline/            the render pipeline (narration, recording, captions, privacy scan)
```

Text is plain git and reviewed in pull requests. Renders (`*.mp4`, `*.mov`, `*.wav`, `*.png`) are stored with Git LFS: see `.gitattributes`. Run `git lfs install` once in a clone before adding any of them.

## Rules

- Only finished material the operator has seen is pushed here. Drafts stay in the author's workspace.
- Every episode is narrated with an AI voice over demo data. Its description says so.
- No host names, personal data, notifications, real sign-ins or secrets on screen.
- Each approved episode is also attached to a GitHub Release as the stable download.

`episodes/00-lfs-test/lfs-test.png` is a tiny placeholder that proves LFS uploads work. It is removed with the first real episode.
