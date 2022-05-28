---
title: Gas Station
summary: Gas stations are decentralized apps which perform the operation of distributing Gas to whitelisted EVM wallets.
tags:
- Blockchain
date: "2022-01-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: "https://github.com/BhuiyanSaif18/GasStation"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

* The DAPP validate ECDSA (EVM) public keys over REST and store them in an array (whitelist).

* The DAPP holds it's own ECDSA private key to sign EVM transactions. 

* The DAPP polls the FTM gas sender tracker https://ftmscan.com/gastracker#gassender once every minute and persist the Fast Gas value.

* The DAPP continuously rpc scans all its received public keys on the fantom opera testnet network.

* The DAPP instantly sends FTM amounting to the exact Fast Gas price to all the Public Keys which do not yet have a transaction record.

* The DAPP shows the difference between available FTM and current Fast Gas to all the Public Keys which do have a transaction record.