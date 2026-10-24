# PHANTOM PROTOCOL — Cyber Range Demo

## What's included
- `game.py`: small Flask server
- `templates/index.html`: complete responsive single-file frontend
- 8 playable simulated CTF challenges in Web Inspection, Cryptography, Forensics, Log Analysis, Password & Hashing, Network Basics, Reverse Engineering, and simulated OSINT
- Boot screen, mission dashboard, filters, challenge detail, evidence terminal, flag submission, progressive hints, XP/ranks, local scoreboard, journal, settings, keyboard command palette, localStorage persistence
- All data is fabricated or uses reserved documentation addresses. No external target is contacted.

## Run on Windows
1. Extract this ZIP.
2. Copy the included `templates` folder and `game.py` into your existing project folder:
   `C:\Users\HP\phantom-protocol\`
   Allow overwrite of `game.py` if prompted. The existing `.venv` can stay.
3. In Command Prompt:
   ```
   cd "%USERPROFILE%\phantom-protocol"
   .venv\Scripts\activate
   py game.py
   ```
   If activation is unnecessary or fails, `py game.py` is enough if Flask is installed in the Python environment you're using.
4. Open `http://127.0.0.1:5000` in Chrome. Keep Command Prompt open while playing.
5. If an old version is cached, use Ctrl+F5.

## Controls
- Click Enter Cyber Range, then open any challenge.
- Submit flags exactly in `CTF{...}` format.
- Hint buttons reveal clues and are saved.
- Add notes to the investigation journal.
- `Ctrl+K` or `Cmd+K`: command palette. `Esc`: close. `?`: briefing. `Alt+1`: dashboard, `Alt+2`: scoreboard, `Alt+3`: journal.
- Settings lets you change codename, enable reduced motion, export progress, or reset the local profile.

## Spoiler answer key
Do not read until testing:
- WEB-01: `CTF{headers_leave_traces}`
- CRY-02: `CTF{caesar_cipher_recovered}`
- FOR-03: `CTF{strings_tell_stories}`
- LOG-04: `CTF{correlate_the_timeline}`
- HASH-05: `CTF{password}`
- NET-06: `CTF{secure_by_default_443}`
- REV-07: `CTF{read_the_logic}`
- OSINT-08: `CTF{verify_every_source}`

## Demo limitations
This is a frontend/localStorage prototype. Since the expected flags live in client-side JavaScript, it is not suitable for a competitive environment where cheating matters. A production version should validate flags on a server, use real authenticated accounts, and store scores in a database. The scoreboard's other entries are fictional local demo rows.
