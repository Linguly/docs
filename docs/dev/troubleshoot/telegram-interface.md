---
title: Telegram Interface
parent: Troubleshoot
last_modified_date: 2.6.2025
---

# Troubleshoot Telegram Interface

## Support channels

- [Support group in telegram](https://t.me/TelegrafJSChat)
- [GitHub](https://github.com/telegraf/telegraf)
- [Docs](https://telegraf.js.org)

## General

If the messages and chat flow are acting weirdly, make sure you have followed the following:

- Don't forget to put `await` before any context change and does contexts are not changing in wrong order.
- If you want to leave a scene, that should be the last command.
- Except leaving the scene, if you are using `reply`, that should be the last command.
- Make sure all `reply`s and async functions are awaited, otherwise the session store update will happen before all the changes and you might loose the updates in Redis.

> Note: to debug Telegraf, you can use this environment variable: `DEBUG=telegraf:*` 