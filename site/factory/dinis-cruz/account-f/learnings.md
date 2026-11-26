# cl-6.conductor: learnings

- A shallow clone of the website fails the gate's piece-flows check ("no flows"): fetch full history first.
- Superseding a key that signed articles turned the gate red until dev fixed validate.js to accept superseded keys for what they signed while active (26 Nov).
- New repositories need the promptugal-news-agents team granted push, or no agent session can attach them (fixed in IaC #15, 26 Nov).
- Place files are signed by each place's own site key; another key fails the identity check, so place news waits for each place agent's own key.
