# OSINT - DAY 0 - 8 January 2024

## SCOPE

(Open Source Intelligence) is the practice of gathering freely available information on a target from various sources as well as their team/collaborators. Please note that hacking these humans or their Twitter accounts is not part of the challenge scope. This is only for information gathering purposes within the scope of the challenge - breaking the ZenGo wallet with the 10 BTC in it. Never deviate from the scope of an engagement

### TWITTER HANDLES

@ZenGo (Main company account)

@OurielOhayon (CEO)@TalBeerySec (CTO)

@ArielMGore (Head of Comms)

@EladBleistein (CMO)

@leontiad (Head of Cryptography)

@UriKelman (Director of Design)


### TAL'S TWITTER THREADS

Tal wrote about AWS authenticaion (Oct): https://twitter.com/TalBeerySec/status/1660590475902853121

Tal's post about bruteforce and MPC: https://medium.com/@TalBeerySec/a-short-note-on-aws-key-id-f88cc4317489

Tal's post on Bitcoin JS entropy fail: https://twitter.com/TalBeerySec/status/1724724767154975019

Tal asking a researcher about MPC: https://twitter.com/TalBeerySec/status/1724798374308966808

Tal thread on entropy: https://twitter.com/TalBeerySec/status/1728475427889434876

Tal on the 83.7 BTC fee tx: https://twitter.com/TalBeerySec/status/1729203234244567462

Tal on KeyGen and ZenGo's MPC: https://twitter.com/TalBeerySec/status/1729285995315487023

Tal - Bitcoin as a Dark Forest: https://twitter.com/TalBeerySec/status/1729888311739908109

Tal on seed recovery: https://twitter.com/TalBeerySec/status/1732082746736922974

Tal on AWS token replay: https://twitter.com/TalBeerySec/status/1732766961212194978

Tal on iOS 0 day and ZenGo: https://twitter.com/TalBeerySec/status/1737266927897297296

Tal's overview of CertiK audit of ZenGo: https://twitter.com/TalBeerySec/status/1643246607272476675

More Tal: https://twitter.com/TalBeerySec/status/1741478982686478806

### Twitter curiosity

Following the iOS 0 day post a discussion with @flyryan on Dec 31, 2023: https://twitter.com/flyryan/status/1741483830584754452

"Ryan Duff @flyryan
So there is no communication with Facetec? You're just running their software stack on your servers?"

"Tal Be'ery @TalBeerySec
Yes, Facetec solution is hosted on our cloud."


### Leontiad Twitter OSINT

@leontiad - Head of Cryptography at ZenGo

Iraklis pointing to potential partnership with Anjuna.io
https://twitter.com/leontiad/status/1587478608100167682

Iraklis back-n-forth with @henrlihenrli about MPC
https://twitter.com/henrlihenrli/status/1600494948540977152

Iraklis on Rust and zero code duplication within ZenGo
https://twitter.com/leontiad/status/1719030711083057219

External link to Iraklis' Github Pages: https://leontiad.github.io
(list of publications may be of use later)



## MEDIUM BLOG ANALYSIS

### 21 April 2022 - first mention of #3FA on ZenGo

"The real vulnerability: Single-factor authentication, not cloud storage"
https://medium.com/zengo/demystifying-icloud-security-wallets-e348516914d9

"To access a ZenGo account, you’d need access and control of the email (magic link) of the user, the recovery kit, and a live private biometric scan.
...
both the client (the app) and the server is required
...
the cloud is immaterial as an attack vector."

The April 2022 blog has an embedded video that is a now 'private' demoing this recovery

Reversing the url in the webpage code this is the clean link to it:

I am guessing it was out of date - see new one:

two tweets linked in April 2022 medium by @OurielOhayon around hacks relating to users backing their singlesig seed phrase on iCloud

https://twitter.com/OurielOhayon/status/1517009834356453378
+
"In less than 1h someone took the backup file made with a hardware wallet seed"
https://twitter.com/OurielOhayon/status/1517070604607885314?t=xN-knyoegK1iUHJtsOv32Q

That 2nd tweet related to a challenge in the blog

Someone claimed the iCloud backup in 1 hour

The 0.03242868 ETH are still in the 2nd bounty wallet bounty wallet which uses their MPC system:

0x7BA1428Aac3987b5eE3048713230efaBD2D89cf4

Important to note that in that challenge all that was provided was 1 of the 3 necessary factors for the wallet

that 1/3 recovery kit is still accessible:

Unsure how the current 10 BTC challenge will differ from this one, we'll see tomorrow

Last paragraph of the 2022 medium post

Would like to comment about 'air gapping' your private key here for those that do not know

since 2022 the tech stack for having your private keys on an offline device have greatly improved

e.g. Dynamic QRs to sign PSBTs


### 27 Feb 2023

Interesting work by @MHamilis on a bug in SIGHASH_SINGLE type within Bitcoin

I don't believe it will be relevant to the current challenge

just worth sharing it and his code:
https://github.com/MatanHamilis/bitcoin-sighash-scan
https://medium.com/zengo/a-bug-in-bitcoin-50f3e7d62a9

### 17 May 2023

In the aftermath of the Ledger #Recover firmware launch fiasco, @TalBeerySec writes a post about it

"Hardware Wallets are actually Firmware Wallets"

"The recovery of private keys is THE real issue"

https://medium.com/zengo/firmware-wallets-sunlight-is-the-best-disinfectant-f49feb6b7e43

"We (@ZenGo) solved this issue since our inception and provide a free guaranteed recovery solution that is already working flawlessly for more than four years."

Linked is a page to their website on access guarantees:

https://zengo.com/how-zengo-guarantees-access-to-customers-funds/

For those unaware some wallets offer a 'distributed private key storage' service:

Ledger Recover being the one referenced above, sharing an encrypted shared of a private key into a 1/3 multisig.

FOUNDATIONdvcs does something similar, but way more sovereign.

These above different to what ZenGo is doing

Will dig into what MPC in entropy generation really means further in this thread...

Just want to share that what Foundation is doing, and schemes such as Shamir's Secret Sharing, are not the same thing as an MPC wallet.


### 24 June 2023

The next post is a perfect segway into exactly that

"we have to eliminate all “Single Points of Failures”
... include the private key and its backup: The notorious seed phrase."

https://medium.com/zengo/vires-in-numeris-why-adding-more-parties-boosts-security-df35663a189c

Sharing 2 screenshots that are the best TL;DR

Do read the whole blog post to get a good handle of the differences in self-custody setups

Links to this: https://zengo.com/aa-and-mpc-frens-with-benefits/

"ZenGo’s solution consists of two MPC parties"

user’s device + remote ZenGo server

Different hardware and software architecture: Mobile devices and cloud servers

Device ownership: Users and ZenGo

Physical location: User pockets and a remote cloud datacenter


### 29 Nov 2023

Read this to better understand #Entropy & the problem of true random number generation

"This blog is split into two sections: Beginner and Advanced."

I'll comment things relevant to the 10 BTC challenge

https://medium.com/zengo/do-you-know-how-keys-are-made-cd342093b709

ZenGo's MPC architecture as defined here

2/2 Multi-Party Computation (MPC) framework

Zengo Server + Zengo App
each generate their own Secret Share (SS)

Zengo App SS = Personal Share
tied to the device using hardware based random generator (TRNG) where applicable

Zengo Server SS = Remote Share

Only the Personal Share (Zengo App SS) can initialize and sign transactions

All of which are verified by the device’s hardware (Secure Enclave or Trusted Execution Environment)

[Screenshot of how design solves all SPOF]

privkey gen = 2 parties using 2 different methods

privkey use = 2 shares computed together

seed phrase recovery = #3FA 'Secure Recovery'

"orthogonal ways"

// something to consider during challenge

Orthogonality - Wikipedia 

https://wikipedia.org/wiki/Orthogonality

//something to consider

2nd reference I come across to Drand

"distributed randomness beacon daemon written in Golang.

Servers running drand can be linked with each other to produce [random values]... and threshold cryptography."

Threshold cryptography

Drand documentation The home page for developer documentation for drand, a distributed randomness beacon. https://drand.love

There is a lot I could comment on regarding the bold statement in this last section of the medium post

my opinions are not relevant to the challenge

will just say that 'Don't Trust, Verify' is hard to achieve

// why brain wallets are a bad idea

In the blog and on twitter @TalBeerySec cited the excellent work of @ryancdotorg on cracking wallets with bad entropy as presented at DEFCON years ago

Never use your brain to generate entropy

r/ZengoWallet is the subreddit: https://www.reddit.com/r/ZengoWallet

Lurking through the last 6 months of post, this surfaced

- roadmap to add Ethereum L2s (only Polygon confirmed)

- Zengo Pro adds a 'legacy transfer' feature which leverages Dropbox

"The recovery file is actually a decryption key that is used to unlock an encrypted copy of your Personal Secret Share during the recovery process.

This decryption key is 'unlocked' using your 3D FaceLock verification."


## OSINT REDDIT AMA OF TODAY

In lead up to this Challenge they hosted an AMA on r/CryptoCurrency

>> 287 comments therein

will screenshot a few relevant ones

https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/hack_a_zengo_wallet_win_10_bitcoin_ama

Q: Can we see the code?
"We host the world's largest open-source MPC cryptographic library on our GitHub and our Zengo X Research Team has a telegram channel focused on MPC cryptography (most folks in the MPC space participate there."

Q: Where are the servers? secure how?
"Even if someone was able to get access to the server, they still cannot spend your wallet.
Only your Personal Share can initiate a transaction.
The Remote Share on the Zengo server is there to co-sign, but cannot initiate."


u/Self_Blumpkin throws down their 1337 skillz
u/ZenGoOfficial references this response to many questions around the architecture and entropy:
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgvjy94


//Guaranteed Access as a potential attack vector

"The 3rd party (EscrowTech) can help you recover your wallet, but they cannot access your wallet or collude with others to access your wallet... "
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgvlqew/

Wallet has:
- Personal Share (unencrypted)
- Remote Share copy (encrypted)

If GA were to activate > EscrowTech releases this Remote Share Decryption Key to #GitHub

> Github push the decryption key of your encrypted Remote Share to your device

Now you wallet has both Shares unencrypted

Your device has 2/2 keys for the multisig

wallet creates the private key *for the first time*

spend coins

Attack vectors to consider:
- spoofing GA alert process
- Compromising Github access:

https://github.com/Zengo-Trustee

Additional theoretical attack vector, most probably outside the scope of this Challenge

Compromise the systems / tech stack of the Trustees listed in

Release GA / get decryption key

*meow* this is illegal kids, don't pwn others *meow*

https://github.com/ZenGo-Trustee/reports

FOR THE LULZ
Noticed the /Server-key-release repository has no code but it does have an active Issue in the tracker:
" Ha "
https://github.com/ZenGo-Trustee/Server-key-release/issues/1


## OSINT REDDIT AMA

"We are committed to putting our money where our mouth is and continuing to improve our security."

exchange between u/kuri-kuma and ZenGo
"Recovery: Your Personal share is locked to you with your 3D FaceLock (private biometric verification scan). It is protected by a 600,000 bug bounty and is only 1 of 3 parts of your wallet recovery"
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgrihyk/

u/Roman_Scoggins asking the hard questions
How do you make money?
Where is your server located and how is it secured?
Can we see the code to verify it?
Answered with links to above screenshoted posts
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgujjo6/

responding to u/nanooverbtc
"Their Primary share initiates signing, gets co-signed by the remote share, and then broadcasts the transaction to the network). Let us know if that is clear or if you have further questions about this!"
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/hack_a_zengo_wallet_win_10_bitcoin_ama

u/flyryan
"You've stated on your site that you generated the single master private key that protects all user's server shares with a Raspberry Pi and destroyed the Pi after." 👀
No answer as of yet to this question
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgx0365/
