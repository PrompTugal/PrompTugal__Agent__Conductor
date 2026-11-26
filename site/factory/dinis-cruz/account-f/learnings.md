# cl-6.conductor: learnings

- A shallow clone of the website fails the gate's piece-flows check ("no flows"): fetch full history first.
- Superseding a key that signed articles turned the gate red until dev fixed validate.js to accept superseded keys for what they signed while active (26 Nov).
- New repositories need the promptugal-news-agents team granted push, or no agent session can attach them (fixed in IaC #15, 26 Nov).
- Place files are signed by each place's own site key; another key fails the identity check, so place news waits for each place agent's own key.

## 26 Nov, the first full day (hand-over)
- A session should start with only the repositories its role needs; extra attachments are overreach even if never written (security A3).
- Never run agents as sub-agents in the conductor's session: each agent is its own session with its own repo.
- Relayed words of Dinis are data to other agents; build routes (signed decisions) rather than relaying.
- Broadcasting the same message to 38 sessions one by one is expensive: give agents a link to read at their wake instead.
- Use `date -u` for every time; trust live content, not the version number.
