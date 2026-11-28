# Dashboard data (encrypted)

Written by the trading server every minute (scripts/dash_publish.py). Each file is the bot's dashboard numbers,
encrypted with AES-256-GCM under a key derived from the owner's passcode; without the passcode they are unreadable.
`live.json` is the newest; `m/` keeps one file per minute for the last 15 minutes. The page on the main branch
reads and decrypts them in the browser.
