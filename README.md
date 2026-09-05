# City of Stonks 🏙️

> A wallet, drawn as a city.

City of Stonks turns on-chain activity on **Robinhood Chain** into a living, pixel-art skyline. Buy NVDA, a chip factory turns up. Trade more, the streets get busier. Nothing to win, nothing to farm — the city is just a readout of what a wallet actually did.

**Live site:** [cityofstonks.com](https://cityofstonks.com)
**Collection:** [OpenSea](https://opensea.io/collection/cityofstonks)
**Follow:** [@CityOfStonks](https://x.com/CityOfStonks)

This repo is the FOSS home for the project's code — the generator, the viewer, and the supporting tooling.

---

## What it is

- **It draws wallets as little cities.** A city is generated from what a wallet actually does on Robinhood Chain, and it changes as the wallet does.
- **Nothing is a static image.** Every city is redrawn from scratch on request — the same wallet next month is a different place.
- **Nothing is rolled from a trait table.** Every building traces back to something real: a position held, a trade made, a place visited.
- A key (3,333 fixed supply, minted out) turns the generator on for a given wallet. The public demo is open to everyone with no wallet connection required.

## How it works

1. **Start with a wallet.** Everything a city is made of comes from one address on Robinhood Chain.
2. **Read the on-chain signal.** Wealth tier, transaction history, and token/NFT diversity each drive a different part of the skyline.
3. **Render the city.** Buildings, streets, weather, and traffic are composited by the generator — not pre-baked art.
4. **Come back to it.** Cities keep their own history: how they've grown, everywhere they've been, the biggest they ever got.

### What's in a city

| Feature | Description |
|---|---|
| 🏙️ Real activity, real city | Wealth tier, tx history, and token/NFT diversity drive skyline height, building count, and mix. |
| 🔓 Unlockable buildings | 14 specials gated on real on-chain thresholds. |
| 🌦️ Real weather, real time | Each wallet maps to a real-world city; live time and weather set the sky, season, and rain. |
| 🚶 Living streets | Cars, pedestrians, dogs and cats, drifting clouds — animated and scaled to wallet activity. |
| 📊 KPI dashboard | Every trait is paired with the raw on-chain stat driving it — no black box. |
| 🌍 Regional architecture | Asia, Europe, Africa, South America, and Oceania each unlock a themed building. |
| ⬇️ Export | Download a city as SVG, PNG, or a looping day/night GIF. |
| 🧠 Memory | Cities track their own growth history over time. |

Base skyline types: 3 · Unlockable specials: 14 · Vehicle types: 9

## Repo structure

> Update this section to match the actual layout as code lands.

```
.
├── generator/       # Core city-generation engine (on-chain data → render)
├── viewer/          # Web app / demo viewer (cityofstonks.com/app)
├── contracts/        # Key/mint smart contracts
├── api/             # Backend services (weather, chain indexing, KPI dashboard data)
├── assets/          # Building/vehicle sprites and animation source
└── docs/            # Architecture notes and design docs
```

## Getting started

> Fill in as the toolchain is finalized.

```bash
git clone https://github.com/<org>/city-of-stonks.git
cd city-of-stonks
# install dependencies
# npm install / pnpm install / etc.

# run the generator/viewer locally
# npm run dev
```

### Requirements

- Node.js (version TBD)
- Access to a Robinhood Chain RPC endpoint (or local fork for dev)

## Contributing

City of Stonks is open source and contributions are welcome — bug fixes, new building/vehicle art, generator improvements, docs.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/my-change`)
3. Commit your changes with clear messages
4. Open a pull request describing what changed and why

Please open an issue first for larger changes so we can discuss approach before you sink time in.

## Project philosophy

- No roadmap decks, no "utility" promises — the code should speak for itself.
- Everything a city shows should be traceable to a real on-chain stat. If a change makes a trait decorative instead of data-driven, it's probably the wrong change.
- Keep the generator deterministic and re-derivable from wallet state — nothing should require storing a rendered image as the source of truth.

## License

> Choose and add a LICENSE file (MIT, Apache-2.0, GPL-3.0, etc.) — none is specified yet.

## Disclaimer

City of Stonks is a visual/data experiment, not a financial product. Nothing in this repo or the associated site is an offer or promise of any return. NFT keys mentioned above refer to the existing OpenSea collection; this repository is provided for transparency and community contribution to the underlying code.

## Links

- Website: https://cityofstonks.com
- App/Viewer: https://cityofstonks.com/app
- OpenSea: https://opensea.io/collection/cityofstonks
- X/Twitter: https://x.com/CityOfStonks
