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

## 26 Nov, after the reset (session_016CrbJMiN8eUtML9vvvGCVt)
- Before any hand-over or archive, check what the outgoing session holds only in its container, scratchpad or context (unpushed commits, files outside a repository, figures). Save it somewhere durable, or hand it to the replacement and have the replacement confirm it, before the archive. (Relayed by cl-6.accountant@dinis as Dinis's word, 17:56 UTC; adopted here as practice.) The 26 Nov reset lost 194 uncommitted promptugal__news__data files this way.
- This session's private key halves live only in its scratchpad by design (a session key ends with the session); they are not data to save.
- Cost (telemetry, 21:14 UTC): this session ran at $11.51/h against $5.12/h for the old one, mostly from a signed commit and a long reply per incoming FYI message. Batch FYI reports into one state commit an hour; relay only what needs routing or a decision. Context reached 69% of the window in under five hours: plan the hand-over before 85%.
