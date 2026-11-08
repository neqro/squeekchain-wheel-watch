# 🐹 Squeektoshi Wheel Watch

A live, single-file community dashboard for **[Squeekchain](https://squeekchain.com)**, the hamster-powered proof-of-work toychain on Ethereum.

It reads the public [Squeekchain API](https://docs.squeekchain.com/developers/api/) (`https://api.squeekchain.com/v1`) straight from the browser, with no backend and no keys.

## What it shows

- **Is Squeektoshi running?** Live wheel status, speed (km/h), rpm and today's distance, with a wheel that spins at the real rpm (`/v1/status`).
- **Squeek blocks**: settled block height, progress to the next block, difficulty and queued work.
- **$SQK supply**: live supply vs the 2.1B cap, SQK mined by the wheel and burned (`/v1/economy/state`).
- **Last 7 days**: work per day chart plus records: top speed, best day, longest run, streak (`/v1/measurement/stats?range=7d`).
- **Squeeks**: live and burned NFTs, total NFT power, mining stage.
- **Account lookup**: paste any address to see its Squeeks (wallet or staked), power and claimable SQK (`/v1/accounts/{address}`).
- **Live activity feed**: settlements, checkpoints, claims, stakes, deposits, merges and wheel milestones (`/v1/events`).

Refresh: status every 5 s, feed every 15 s, economy every 30 s, stats every 2 min, staying inside the API's published rate limits and cache windows. "Unavailable" responses are shown as unknown, never as zero, as the docs ask.

## Run it

Open `index.html` in a browser, or serve the folder with any static host (GitHub Pages works out of the box).

## Notes

- Squeekchain currently runs on Sepolia; this is an unofficial community build, not affiliated with the Squeekchain team.
- Nothing here signs or sends transactions.

Built by [@neqro_61](https://x.com/neqro_61) for the Squeekchain Genesis builder program.

License: MIT
