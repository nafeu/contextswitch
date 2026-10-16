# contextswitch

A tiny single-page app for juggling the things you're paying attention to. Add the
contexts you're switching between (tasks, projects, people, whatever you're
context-switching across), then hit switch to get picked one at random.

Live at **[nafeu.com/contextswitch](https://nafeu.com/contextswitch)**.

## How it works

- Type a name and hit add to drop it into the cloud.
- Pick a rule for how the next context gets chosen:
  - **No duplicates** — deals through every context once before reshuffling (deck-style).
  - **No back-to-back** — random, but never repeats the context you just left.
  - **Most neglected** — picks whichever context has gone longest without a turn.
  - **Pure chaos** — fully random every time.
- Hit the switch button (or press `S`) to draw the next context.
- Every switch is logged for the day — open the trail in the top-left to review or clear it.

Everything is stored locally in the browser (`localStorage`) — no backend, no accounts,
no network calls.

## Running locally

It's a static, single-file app. Just open `index.html` in a browser, or serve the
directory with anything that can host static files, e.g.:

```sh
python3 -m http.server
```

## Stack

Plain HTML, CSS, and JavaScript — no build step, no dependencies.
