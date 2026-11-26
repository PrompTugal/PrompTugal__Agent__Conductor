# cl-6.conductor: restart

If this session ends, a new one:
1. Clones PrompTugal/PrompTugal__Agent__Conductor and PrompTugal/PrompTugal__News__Website (dev, full history: the gate's piece flows need it).
2. Makes a new key (openssl P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository), publishes it at `site/keys/cl-6.conductor.json` alone in its own commit, adds it to the website's `board/keys.json`, and marks the old one superseded.
3. Sets ssh signing in each clone (gpg.format ssh, gpg.ssh.program ssh-keygen, user.signingkey, commit.gpgsign true).
4. Reads `agent.json`, `now.md`, `decisions.md`, `learnings.md` here, then the website's CLAUDE.md and board/guidance/README.md.
