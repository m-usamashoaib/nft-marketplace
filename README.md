# Auctioneer's Hub · NFT marketplace

The marketplace side of **Auctioneer's Hub**, where artists mint their work as NFTs and collectors buy them at a fixed price, in timed auctions or through open offers.

Final-year project, BS Computer Science, GC University Lahore (2023).

| Part | Repository |
|---|---|
| API server | [socialApp-server](https://github.com/m-usamashoaib/socialApp-server) |
| Social app | [socialApp-client](https://github.com/m-usamashoaib/socialApp-client) |
| **NFT marketplace** (this repo) | React · Recoil |

**👤 Built by** [Muhammad Usama Shoaib](https://m-usamashoaib.github.io) (most of the API and both front-ends) in a two-person team.

> **Credits:** the visual design is based on the *Gigaland* NFT marketplace HTML template, which I converted to React and connected to our API. The **MetaMask wallet flow** was built by my teammate and is not part of this repository; the wallet page here is the UI only.

## Features

- **Home:** featured NFTs, live auctions, collections and top collectors, all loaded from the API
- **Create NFTs:** single items or **multiple copies (editions)**, with image upload, collection, description and **royalties** (up to 70%)
- **Three ways to sell**
  - **Fixed price:** buy instantly
  - **Timed auction:** minimum bid, start and end dates, with a live **countdown**; the server hands the NFT to the highest bidder when the auction ends
  - **Open for offers:** collectors place bids at any time
- **Item details:** creator, owners, price or current bids, and bid history
- **Collections:** browse any collection, or your own
- **Active bids** and **saved** NFTs
- Shared login with the [social app](https://github.com/m-usamashoaib/socialApp-client): the same account works in both

## Tech stack

React 18 · React Router · Recoil (state) · Axios · Swiper · React Toastify · js-cookie

## Run locally

1. Start the [API server](https://github.com/m-usamashoaib/socialApp-server) on **port 4000**. This app proxies `/api/v1` calls to it (see `proxy` in `package.json`).
2. Run this app on **port 3001**, since the social app links to that address:
   ```bash
   npm install
   # macOS / Linux
   PORT=3001 npm start
   # Windows (PowerShell)
   $env:PORT=3001; npm start
   ```
3. Open http://localhost:3001 and log in with an account created in the social app.

## What I'd improve today

- Settle purchases and bids on-chain through the wallet, so ownership is verifiable
- Show the remaining copies and the full bid history more prominently on item pages
- Replace the template's jQuery plugins and hot-linked images with local React components and assets

## License

MIT
