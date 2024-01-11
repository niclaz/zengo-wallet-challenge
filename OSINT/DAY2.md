# OSINT - DAY 2 - 10 January 2024

DAY 2 - CODE GLORIOUS CODE

## GITHUB FOR FIRST TIMERS

Github is a lot of things these days, but what counts here is understanding 'git' and code repositories... git?

git is a distributed version control system that tracks changes to files, usually used for coordinating and sharing their work

Zengo's website links to this repository

https://github.com/ZenGo-X

for convenience in this thread I will use /zengo

the '/' denoting a code repository

this saves me characters in posts and as you will see there are many different repositories (120) linked here...


So what do we see here?

120 repositories
1 user account under 'people'
most used topics: rust, ecdsa

Also 238 followers of the organization profile and a contact email + link to their website

pretty clean, sometimes you don't find this much information on Github

Tip: how to search Github

Here I searched 'zengo' > 153 repos

That's a lot you might be thinking...

well you could improve the search with keywords but also by selecting 'rust' or other filters in left hand menu

or improve the search parameter to 'zengo wallet'

the results show all 153 repositories with the word zengo in name or description

not all are relevant to the ZenGo Wallet

so we should filter the information gathered to see if anything is useful *outside of the /zengo main repo*

yes... more OSINT kittens

OSINT - GITHUB

/ZenGo-Trustee

Separated from /Zengo is a different user account (not an organisation) that has 2 repos:

/server-key-release
/reports

the first has no code and 1 issue (ha)
the second has 22 PDFs of trustee letters uploaded

https://github.com/ZenGo-Trustee/reports


Firstly, the intention here is OSINT

to understand better the setup of the 10 BTC wallet

Hacking / phishing the Trustees listed here is most def not in the Challenge scope / parameters

"Never deviate from the scope of an engagement"


With that said... 

what can we discover in these PDFs?

1) first off that /repos can contain more than just code - PDFs as well as pretty much any other file

2) one law firm has validated the ZenGo business accounts for the last 5 years: http://jrgtax.co.il


Could JRG be the custodian of a shard backup?

Doubtful

My assumption is they audit the business' accounts and ensure liquidity of operations - only the books, no shards or MPC computation on their end.

That said 2 particular PDFs stick out from the bunch


1) JRG statement of private key release simulation
https://github.com/ZenGo-Trustee/reports/blob/master/KZEN%20release%20simulation.pdf

2) "KZEN verification_escrowtech_220519.txt"

"BTC 8692, 27 MAY 2019"

public key + signature of message therein

https://github.com/ZenGo-Trustee/reports/blob/master/KZEN%20verification_escrowtech_220519.txt

👀 Did ZenGo have 8,692 BTC in custody in 2019?

We could do more OSINT here

- on JRG and their relationship to ZenGo

- follow the breadcrumbs of the 17 followers of the pretty empty /ZenGo-Trustee repository
https://github.com/ZenGo-Trustee?tab=followers

Both don't seem relevant to the Challenge

going to avoid this rabbit hole


## OSINT - GITHUB 

Continuing our search for repos outside of /zengo

It needs to be noted here that @ZenGo
 and collaborators have been doing some awesome work on building #MPC and releasing Open Source libraries 

helping developers to grow the MPC ecosystem 

None more so that the /zengo/multi-party-ecdsa

904 stars and 316 forks on this repo

Rust implementation of 
TSS (Threshold Signature Scheme) 
on ECDSA (elliptic curve digital signature algorithm)

> code that runs the ZenGo wallet design

http://github.com/ZenGo-X/multi-party-ecdsa

but...

and this is a big BUT

the repo is no longer maintaned as noted in the http://readme.md file (always read the readme)

which means 2 things:

ZenGo doesn't use this anymore in production

All searched repos that use /multi-party-ecdsa are not relevant

We will return to /multi-party-ecdsa in future

as well as GG18 / GG20 / Lindell17 when we look into the potential exploits around the cryptography used

This will come later kitten...

//note: I doubt attacking the crypto of the ZenGo wallet will lead to success


## OSINT - GITHUB

So other interesting repos without /multi-party-ecdsa

...

@FireblocksHQ
 is another company in the MPC space

They have an MPC library for ECDSA
https://github.com/fireblocks/mpc-lib

Probably NOT the same as ZenGo 

but it is written in C++ / is updated / AGPL licensed

/transumption

https://github.com/transumption

This one-coder organization had forked several ZenGo repos for coding to adapt it to the Aleph0 project

albeit they are /multi-party-ecdsa forks, my ears perk

ping @yanateras  want to join forced to pwn a wallet for 10 BTC?

/backend-mpc-wallet

https://github.com/hcheng826/backend-mpc-wallet

this project (last updated a year ago) is also a fork of /multi-party-ecdsa but I share it as it could be interesting to those looking at a specific attack surface

//attacking the software of the ZenGo wallet

/newyorkcity_tss_server

https://github.com/ezsyfi/newyorkcity_tss_server

In a similar vein as above - this is older code for a TSS server that uses /multi-party-ecdsa

It also had a mobile app:

/newyorkcity_tss_client
https://github.com/ezsyfi/newyorkcity_tss_client

Both GPL licensed - project is inactive

/IdoBenEzri

https://github.com/IdoBenEzri/ZenGo

It contains two bits of code:

index.js 
template.yaml

Just following a hunch there may be some information in the AWS setup of ZenGo's product ... 

why would I think this?

well... Ido works at ZenGo
http://linkedin.com/in/ido-ben-ezri


## OSINT - GITHUB - ZENGO

Now that we did that quick review of repositories outside of /zengo (we will use GitHub search again)

Let us sniff around the 120 repositories within /zengo

to see what is what 

but more importantly what is relevant to the Challenge.

I'm back from the deep dive

Collected the names of all 120 repos 

Arranged them in subsets of relevance 

Following order:

- Bitcoin related
- Potential Tech Stack of Wallet
- ZenGo code & crypto
- Rust related 

What got filtered?
36 'web3' related 
5 older ones

### Observations

- Tale of many Cities (ZenGo naming convention)
> gotham / emerald / white / vice / paradise-city
Useful in describing decentralized architectures

- Lots of older repos (3+ years and unmaintained) 
> be selective

- lots of Node JS

- lots of React Native 
> combined with Node JS this could be the wallet code

- many cryptography libraries to investigate:

curv
mutli-party-...
thresh-sig-js
zk-paillier
bulletproofs
kms-secp256k1
multi-party-bls
class
ShareLock
multi-hop-locks
fs-dkr

Lastly
Seeing the most recent commit history and description of the  top packages - what to expect on Day 3:

gotham-engine
gotham-city
two-party-ecdsa
public-docs
round-based-protocol
kms-secp256k1
ks-dkr
curv
gotham-public
rust-gmp
multi-hop-locks
ShareLock
zk-paillier
