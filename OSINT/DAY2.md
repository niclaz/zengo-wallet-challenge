# OSINT - DAY 2 - 10 January 2024

## OSINT - https://github.com/ZenGo-X

ZenGo's main repository for convenience in future notes I will use /zengo to indicate it

also using the '/' denoting a code repository

120 repositories

1 user account under 'people'

most used topics: rust, ecdsa

Also 238 followers of the organization profile and a contact email and a link to their website

## OSINT - REPOS OUTSIDE OF /ZENGO

Filtering the Github searching to anything useful **outside of the /zengo main repo**

### /ZenGo-Trustee

Separated from /Zengo is a different user account (not an organisation) that has 2 repos:

/server-key-release

/reports

the first has no code and 1 issue (ha)

the second has 22 PDFs of trustee letters uploaded

https://github.com/ZenGo-Trustee/reports

Note: the intention here is OSINT to understand better the setup of the 10 BTC wallet, hacking / phishing the Trustees listed here is most def not in the Challenge scope / parameters. **Never deviate from the scope of an engagement**

With that said... what can we discover in these PDFs?

1) first off that /repos can contain more than just code - PDFs as well as pretty much any other file

2) one law firm has validated the ZenGo business accounts for the last 5 years: http://jrgtax.co.il

Could JRG be the custodian of a shard backup? Doubtful

My assumption is they audit the business' accounts and ensure liquidity of operations - only the books, no shards or MPC computation on their end.

That said 2 particular PDFs stick out from the bunch

1) JRG statement of private key release simulation
https://github.com/ZenGo-Trustee/reports/blob/master/KZEN%20release%20simulation.pdf

2) "KZEN verification_escrowtech_220519.txt"

"BTC 8692, 27 MAY 2019"

public key + signature of message therein

https://github.com/ZenGo-Trustee/reports/blob/master/KZEN%20verification_escrowtech_220519.txt

👀 Did ZenGo have 8,692 BTC in custody in 2019?

We could do more OSINT here:
- on JRG and their relationship to ZenGo
- follow the breadcrumbs of the 17 followers of the pretty empty /ZenGo-Trustee repository: https://github.com/ZenGo-Trustee?tab=followers

> Both don't seem relevant to the Challenge... going to avoid this rabbit hole

Continuing our search for repos outside of /zengo It needs to be noted here that ZenGo and collaborators have been doing some awesome work on building #MPC and releasing Open Source libraries helping developers to grow the MPC ecosystem None more so that the /zengo/multi-party-ecdsa

http://github.com/ZenGo-X/multi-party-ecdsa

904 stars and 316 forks on this repo

Rust implementation of TSS (Threshold Signature Scheme) on ECDSA (elliptic curve digital signature algorithm)

but... the repo is no longer maintaned as noted in the README.md file (always read the readme)

> This repository is no longer maintained. Most specifically, Zengo will not provide any security updates or hotfixes (should an issue arise). This library was originally created to enable users to experiment with MPC and TSS functionality using different protocols, including such that are not used in production by Zengo wallet. Zengo wallet’s production MPC code can be found in https://github.com/ZenGo-X/gotham-city/master

which means 2 things:

1) ZenGo doesn't use this anymore in production

2) All searched repos that use /multi-party-ecdsa are not relevant

We will return to /multi-party-ecdsa in future research as well as GG18 / GG20 / Lindell17 when we look into the potential exploits around the cryptography used

> note: I doubt attacking the crypto of the ZenGo wallet will lead to success


## OSINT - Other interesting repos without /multi-party-ecdsa

### /FireblocksHQ/mpc-lib

FireblocksHQ is another company in the MPC space and they have an MPC library for ECDSA

https://github.com/fireblocks/mpc-lib

Probably NOT the same as ZenGo but it is written in C++ / is updated / AGPL licensed

### /transumption

https://github.com/transumption

This one-coder organization had forked several ZenGo repos for coding to adapt it to the Aleph0 project albeit they are /multi-party-ecdsa forks, my ears perk

### /backend-mpc-wallet

https://github.com/hcheng826/backend-mpc-wallet

this project (last updated a year ago) is also a fork of /multi-party-ecdsa but I share it as it could be interesting to those looking at a specific attack surface

> attacking the software of the ZenGo wallet

### /newyorkcity_tss_server

https://github.com/ezsyfi/newyorkcity_tss_server

In a similar vein as above - this is older code for a TSS server that uses /multi-party-ecdsa

It also had a mobile app: https://github.com/ezsyfi/newyorkcity_tss_client

Both GPL licensed - project is inactive

### /IdoBenEzri

https://github.com/IdoBenEzri/ZenGo

It contains two bits of code:
- index.js 
- template.yaml

Just following a hunch there may be some information in the AWS setup of ZenGo's product ... why would I think this?

well... Ido works at ZenGo: http://linkedin.com/in/ido-ben-ezri


## OSINT - GITHUB - ZENGO

Now that we did that quick review of repositories outside of /zengo (we will use GitHub search again)

Let us sniff around the 120 repositories within /zengo, to see what is what, but more importantly what is relevant to the Challenge.

...

Collected the names of all 120 repos, I then sorted and arranged them in subsets of relevance with the following order:

- Bitcoin related
- Potential Tech Stack of Wallet
- ZenGo code & crypto
- Rust related 

What got filtered out? **36 'web3' related and 5 older ones**

[See the sorted list here on Github](https://github.com/niclaz/zengo-wallet-challenge/blob/niclaz/OSINT/Github/zengo-repos-sorted.md)

[Or the unedited list arranged in alphabetical order](https://github.com/niclaz/zengo-wallet-challenge/blob/niclaz/OSINT/Github/zengo-repos-alphabetical.txt)

### What did we learn on DAY 2? 

- Tale of many Cities (ZenGo naming convention) currently identified:
  - gotham
  - emerald
  - white
  - vice
  - paradise-city

> Useful in describing decentralized architectures

- Lots of older repos (some have not been updated in 3+ years or are unmaintained) 

> need to be selective in code review / future rabbitholes

- lots of Node JS can be seen in code
- lots of React Native as well

> Attack vector: These two be the base of the wallet code

- several repositories of cryptography libraries to investigate:
  - curv
  - thresh-sig-js
  - zk-paillier
  - bulletproofs
  - kms-secp256k1
  - multi-party-bls
  - class
  - ShareLock
  - multi-hop-locks
  - fs-dkr

Lastly the most recent commit history and description of the top packages indicates we should not ignore the following repositories:
  - gotham-engine
  - gotham-city
  - two-party-ecdsa
  - public-docs
  - round-based-protocol
  - ks-dkr
  - gotham-public
  - rust-gmp
