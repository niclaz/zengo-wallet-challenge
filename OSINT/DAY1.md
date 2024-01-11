# OSINT - DAY 0 - 8 January 2024

# Megathread of #ZengoWalletChallenge @ZenGo
CC0 licensed - RT all you like - happy hackin'

10 BTC up for grabs if you can break their MPC setup
Are you looking to start the challenge?


### Why is this cat doing this megathread?

> showing the analysis stage of an exploit
> documenting possible exploit methodologies
> sharing for others to learn from it
> one thread to track of challenge updates
> one thread for MPC / cryptography links
> get sats from @ZenGo

### OSINT

(Open Source Intelligence) is the practice of gathering freely available information on a target from various sources as well as their team/collaborators

Humans tend to be the weakest point of a digital security system, so lets see what we can find:
@OurielOhayon (CEO)
@TalBeerySec (CTO)
@ArielMGore (Head of Comms)
@EladBleistein (CMO)
@leontiad (Head of Cryptography)
@UriKelman (Director of Design)

Tip: do check their 'replies' within Twitter

NOTE: the challenge scope does not involve hacking these humans or their Twitter accounts!

This is only for information gathering purposes within the scope of the challenge - breaking the ZenGo wallet with the 10 BTC in it.

Never deviate from the scope of an engagement

Seems ZenGo runs an ambassador program on Twitter

For the challenge these accounts are probably not relevant but I discovered @Crypto_Kimi is/was a former Marketing Manager https://twitter.com/justprotocol/status/1724383424058703908

Tal wrote about AWS authenticaion (Oct): https://twitter.com/TalBeerySec/status/1660590475902853121

Note: He posts are normally under the ZenGo Medium (more later in this thread)

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
https://twitter.com/TalBeerySec/status/1741478982686478806

Following the iOS 0 day post there was an excellent question posted by @flyryan: https://twitter.com/flyryan/status/1741483830584754452

"The 3rd party (biometric auth) is hosted on the 2nd party (Zengo server), so even if 3rd party goes away no problem." @TalBeerySec

<screenshot>

### End of OSINT on Tal's accont

What did we discover?

Tal (CTO) knows his cryptography and entropy, is respected by other security experts, and has tweeted around AWS authentication vulnerabilities + we know the FaceTec lock is hosted on their cloud (flyryan thread)

Will dig into #FaceTec of ZenGo further in the thread, but from first reading it seems it is part of their Theft Protection feature of the Pro version of ZenGo

Putting 2+2 together we can assume in the ZenGo infrastructure is AWS and a private could

OSINT Observation

There are some connections between C-suite team members and @ZeroNetworks which offers MPC services - could potentially be part of the ZenGo stack

*this is an assumption*

A quotable tweet from the CEO (@OurielOhayon)
"🚨 We're putting our balls on the table and our coins where our mouth is."
Source: https://twitter.com/OurielOhayon/status/1744011091049394408

OSINT from Twitter /with_replies of Iraklis

(@leontiad - Head of Cryptography at ZenGo)

Iraklis pointing to potential partnership with

Iraklis back-n-forth with @henrlihenrli about MPC

Anjuna.io
https://twitter.com/leontiad/status/1587478608100167682
https://twitter.com/henrlihenrli/status/1600494948540977152

Iraklis on Rust and zero code duplication within ZenGo
https://twitter.com/leontiad/status/1719030711083057219

External link to Iraklis' Github Pages: https://leontiad.github.io
(list of publications may be of use later)

+ Tal's overview of CertiK audit of ZenGo
    https://twitter.com/TalBeerySec/status/1643246607272476675

### OSINT from Twitter

ZenGo has a very good 'research' webpage: http://zengo.com/research
where past research and researchers are listed.

I will not be going through all their accounts and past posts but will tag them here for posterity and visibility:

@OmerShlomovits
@EliorBenC
@claudiorlandi
@ittayeyal
@odedleiba
@Istvan_A_Seres
@PratyushRT
@BagadSuyash
@amanusk_
@getnitin15
@Elichai2
@Varun_2703

Do read the 'Our Projects' section of the webpage these cryptographers worked on with ZenGo


### What have we learnt?

Potential partnerships / infrastructure with Anjuna and/or ZeroNetworks

Part of the FaceTec stack uses a private cloud managed by ZenGo

ZenGo CTO seems to know AWS intimately

Company has worked with leading crytographers


### OSINT - MEDIUM BLOG ANALYSIS

21 April 2022 - first mention of #3FA on ZenGo

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


BONUS: OFFLINE SIGNING DEVICES

If PSBT doesn't mean anything to you read this:

... or watch it in action in this video by @btcuserguide using the awesome @SeedSigner + @bluewalletio
https://twitter.com/btcuserguide/status/1446873013518020612

Other awesome HW wallets which can sign PSBTs:
@FOUNDATIONdvcs
@Blockstream Jade
@COLDCARDwallet
@Trezor

+ software wallets
@SparrowWallet
@SamouraiWallet
@ElectrumWallet
@nunchuk_io

PSBT is a Bitcoin protocol, because Bitcoin is 1337.

I probably missed other HW and Software wallets that leverage PSBTs for offline signing / airgapping seeds

Feel free to comment below anon, this cat is curious

The only other oneI know is anon/nero for Monero

Demo by @moneromars
https://twitter.com/moneromars/status/1685365155465404418

## OSINT - MEDIUM BLOG ANALYSIS

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

@Ledger Recover being the one referenced above, sharing an encrypted shared of a private key into a 1/3 multisig.

@FOUNDATIONdvcs does something similar, but way more sovereign.

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

[image credit: diagram from Nov 2023 medium post]

Screenshot of how design solves all SPOF

privkey gen = 2 parties using 2 different methods

privkey use = 2 shares computed together

seed phrase recovery = #3FA 'Secure Recovery'

"orthogonal ways"

// something to consider during challenge

Orthogonality - Wikipedia https://wikipedia.org/wiki/Orthogonality

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


# OSINT - DAY 1 - 9 January 2024

Soon this webpage will *hopefully* be updated with the addresses and conditions for the 10 BTC Challenge
https://zengo.com/zengo-wallet-bitcoin-challenge

Remember anon,
Never deviate from the challenge parameters
Do not hack things or people unless they consent

Do you want to know more?

@Hacker0x01's knowledge base articles: What is a White Hat Hacker?
https://www.hackerone.com/knowledge-center/white-hat-hacker
Why you need #responsible #disclosure and how?
https://www.hackerone.com/knowledge-center/why-you-need-responsible-disclosure-and-how-get-started


### POST TWITTER SPACES
https://twitter.com/RampNetwork/status/1744720652609749210

- Challenge wallet will use Thread Protection
- RECOVERY is 3FA (email, your face FaceTec, and the recovery file) but also system allows to add face or recovery email to an account.
// potential attack vector - new face + email
- There are 'hints' shared about the account/ways in on challenge website during the week // check for HINTS
- If you are successful - "No need to send us anything, if you can get it the bitcoin they are yours"
- progressive rollout of HINTS
- This is a unique engagement oppurtinty... but also a risk for all wallets, ZengGo assessed that wall is secure enough to test it and their brand.
- "in cybersecurity there is not thing as 100% (secure)"
- Social Engineering / Insider attack? @mizi is on it



TANGENT: LEGACY SYSTEM
At the end of the Spaces the relatively new feature Legacy Transfer was cited.
Potential attack vector if this Challenge was *not time-limited.*
But quick read it seems it is a type of dead-man-switch which released shared for full privkey only...
exploiting Legacy would require full access to private shards, email, and the face of owner
which I think is enough access privilege for tx signing
Even if you do add yourself as a beneficiary the dead-man-switch has to be activated
// skipping this attack vector
That said if curious about @ZenGo Legacy Transfer protocol here is a direct link to the whitepaper [PDF]
It appears ZenGo are the first to implement this form of Legacy MPC recovery process
v.1 - August 2023 - authors: @TalBeerySec et al.

## Video - Zengo Proof of Bitcoin / Penguin
What we can verify from video: 
Ari is not of the Challenge wallet 3d facelock owner - Confirmed by comments on Twitter by Ari
// attack vector: adding a search tab: Face mapping AI
Pin typed in during one video
// potential derivation of finger movement? glass reflection?
Security level of account seen in video of Penguin verification
//replicate status, it was not max


## OSINT - WEBSITE

Annual audits by Certik, Forta, Alchemy, Hacken

Features added to Pro wallet
- 3D Face Theft protection
- web3 firewall
- 24/7 support chat

Confirmed in Spaces that Theft Protection is active on the wallet being used in Challenge

### Recovery

FAQ: Can I lose my account...?

"... if both of these things were to happen:
1) You lose your device and need to recover it
and
2) You lose access to one or more of the 3 factors necessary to authenticate your wallet recovery."
[3FA screenshot]

FAQ: Can Zengo prevent certain transactions from happening?
"Zengo’s MPC security system requires that any transaction you make be validated by Zengo’s servers before being broadcasted to the blockchain...
While in theory..."
//TX validated before broadcasting

FAQ: Can Zengo know who I am?
"Zengo has no access to any private information about you besides your email, and this email can be non-nominative should you choose."
>> Their way of verifying you is your email and the FaceTec dependency/3rd party
//Inspect code


## OSINT - AUDITS

AppSec 2019
https://zengo.com/audit/audit-appsec_june2019.pdf

Kudelski 2019
https://zengo.com/audit/audit-kudelski_march2019.pdf

Kudelski 2019
https://zengo.com/audit/audit-kudelski_october2019.pdf

Scorpiones 2021
https://zengo.com/audit/audit-%20scorpiones_february2021.pdf

Scorpiones 2022
https://zengo.com/audit/audit-scorpiones_october2022.pdf

Certik 2023
https://zengo.com/zengo-certik-audit-2023/

source: /security page

## OSINT - WEBSITE

@ZenGo can you confirm (as noted in Spaces) that for the #ZengoWalletChallenge this white hat policy is not being followed? https://zengo.com/white-hats

Would be great to have confirmation and reporting mechanism outline on challenge webpage

## PRO

Consideration that the Pro features + the wallet supporting multiple assets (not just BTC) could mean more attack surfaces for potential exploits
What iz attack surface?
https://zengo.com/pro/

For those wishing to explore the #multiasset vector
Supported: Ethereum, Polygon, Arbitrum One & Optimism Mainnets
Not: BSC, Tron, Base, Bitcoin Cash and other Layer 2s.
https://zengo.com/assets/

Another vector for accessing the Ethereum wallet could be smart-contract exploits / malicious signing
This would require subverting this 'web3 firewall' part of the Pro wallet version and also phishing the user
//not a feasible IMHO
https://zengo.com/firewall/


## OSINT - WEBSITE - TSS
TSS = Threshold Signatures System

"The Zengo system is a “two out of two” party ECDSA threshold signatures system.
The two parties are the secure Zengo server and the Zengo user’s mobile device."
//how to construct 2/2 Tx
https://zengo.com/security-in-depth

Here would be a good place to briefly touch on #GG20
just after the above quote, we see this text
the 'Github' link to the audited text leads to: https://github.com/ZenGo-X/multi-party-ecdsa

This library is no longer maintained or used by ZenGo (see header in )


Questions
Where is the audit for the TSS?
If ZenGo moved from the /multi-party-ecdsa code due to exploits in GG20 MPC computation, was the new implementation /gotham-city audits?
By whom and when?
Is the content on the webpage about TSS out of date?
uhmm....

Within an MPC cryptography related Telegram chat managed by ZenGo and team you can find details of a handful of moments when exploits were announced and team commented they were unaffected...

i.e. #BitForge - https://www.fireblocks.com/blog/bitforge-fireblocks-researchers-uncover-vulnerabilities-in-over-15-major-wallet-providers/

DISCLAIMER
As only a mere cat I only know some things. I do understand *some* cryptography but I am not an expert or speak of the soundness of the BitForge / GG20 / MPC vulnerabilites. I know attacking the cryptography is not a valid approach to win this Challenge.


### OSINT - What is fully Open Sourced?

> not much & not the app

linked: 
the /multi-party-ecdsa (see above)
and also a /curv code repository

We will dig into the code further in future

don't worry anon - staying non-technical for now

https://zengo.com/zengo-and-open-source

Probably most important page for how ZenGo's MPC differs from "more traditional" private key storage
FAQ quote: "The best part of this process is no single entity can ever get access to any private key"

we shall see...
https://zengo.com/mpc-wallet/

If you are digging the cryptography then check out:
https://zengo.com/research
+
https://zengo.com/how-keys-are-made/

Lots there, also a link to Telegram group exclusively for MPC related questions and academic discussion
gg to ZenGo for bringing these researchers together

Last website post - I think all the important bits are covered, but you might ask...
how do I find out more?
enter sitemap.xml
ZenGo website uses Wordpress and has a sitemap.xml for SEO / better web navigation
/post-sitemap.xml has all blog posts


## OSINT - SUPPORT

Quick skim through the support docs to see if we missed something:
> About Zengo

"To recover your account, all you need is your email, your storage service (iCloud, google drive, or dropbox), and a selfie scan"

wait what's this...

... so like good developers that use certain Open Source software licenses the team has listed many here:

The next couple of tweets will be a dump of the names of the packages and services cited, for ease of use...

https://help.zengo.com/en/articles/5190969-open-source-licences

![Open Source Licenses](/Website/open-source-licenses.md)

I realise that for some of you the above doesn't mean much, so let me give context to it and it may be useful

DEPENDENCY
Making software is hard, especially from scratch
Open Source is awesome
& Open Source cryptography is very important
but in building the server and app there is a good chance ZenGo uses some of the above in their stack
> relevant xkcd
https://www.explainxkcd.com/wiki/index.php/2347:_Dependency


Without looking too much into each right now...

my ears perked at the following:

winapi - rust package to call Windows API
cloudabi - ABI for UNIX-like OS (note: project is unmaintained)
Lock_Api

//inspect code

## OSINT - SUPPORT

> How To Guides
"To ensure that only you can send funds from your ZenGo wallet, we require authentication through Apple’s built-in biometric or passcode authentication system."
[screenshot of security page of app]

Screenshot from "How do I recover my Zengo account if I change my phone or delete the app?"
Leads to this good overview of Recovery Kit
//Recovery Spoofing is something I am considering as a viable attack of the wallet
https://help.zengo.com/en/articles/2603673-what-is-zengo-s-recovery-kit

### OSINT - SUPPORT
"How to transfer your Zengo account from iOS to Android and vice-versa"
// Transfer of account ownership to new phone

Sync Recovery Kit
Access cloud storage
AI face replication

"You're In"

Hope this become a LeopardsAteMyFace situation

> How To Guides
"the Zengo recovery file will remain locally stored on your device and in your personal cloud service/s but will be unusable once the account is deleted. After you have fully deleted your account, you can, if you want, remove this file manually."

> Security > Biometrics
Provider: FaceTec ()
Product: 3D Facelock
Bounty: $600,000 Spoof Bounty Program
https://dev.facetec.com/spoof-bounty-program

Support
https://help.zengo.com/en/articles/2898755-how-secure-are-zengo-s-biometric-verifications

Blog
https://zengo.com/biometrics-in-zengo-wallet

In-house test
https://zengo.com/can-pictures-break-zengos-biometrics-security

> Security > How Zengo security model works
Good content about the overall security model
Answers common FAQ on the subject
Adds 7 points to "Are there any risks in using Zengo?"
Written by @OurielOhayon - Updated over a week ago
https://help.zengo.com/en/articles/2603678-how-zengo-security-model-works

> General
"The face verification technology used in Zengo should work even as your face changes naturally over time. If you gain or lose weight, start wearing eyeglasses, grow out your hair or beard, or grow older..."
https://help.zengo.com/en/articles/3836341-what-is-an-additional-3d-facelock

"What Bitcoin address formats does Zengo support?"
p2sh-p2wpkh
Noticed this when they revealed the Challenge address: 3NB5gbyhCQM92WUpHxfpK7PqC1KKTAYwpK
So all ZenGo BTC addresses start with a 3
Curious...
https://help.zengo.com/en/articles/3123492-what-bitcoin-address-formats-does-zengo-support

All Bitcoin addresses are backwards compatible
I just find it curious seeing that 97% of the network now transactions of SegWit native (bc1...) addresses
Not an expert on vulnerabilities in tx construction for p2sh-p2wpkh types... might be worth looking into

> General > Assets
"If a token or NFT is important to you, please request it from our customer support agents, and we will try our best to add support for it."
Is this how the @pudgypenguins NFT is secured?
Additional verification by a human? ... just like a bank?

> Support
Can I use Zengo if my selfie camera is broken?
No. ish.
https://help.zengo.com/en/articles/2981103-can-i-use-zengo-if-my-selfie-camera-is-broken

ZoOm Biometric link: http://zoomlogin.com > domain redirect to http://facetec.com

ZoOm® is a FaceTec product (2017): https://www.businesswire.com/news/home/20170822005465/en/FaceTec%E2%80%99s-Universal-3D-Facial-Recognition-Software-Replaces

Lose your phone?

"All you need is to:
- Zengo app

- log in with the same email

- Access to your recovery kit on your cloud service

- pass the selfie scan to verify it's you.
https://help.zengo.com/en/articles/2830607-what-happens-if-i-lose-my-mobile-device-or-my-device-is-compromised


Zengo #Pro - Complete Guide
Since the Challenge Wallet has the Theft Protection and firewall feature active it must be a Pro version
//Reflection: how does ZenGo know what user is Pro
//Is there a db somewhere?
https://help.zengo.com/en/articles/8105588-zengo-pro-your-complete-guide-to-the-best-crypto-wallet-protection
@ZenGo @pudgypenguins > General

WalletConnect
WalletConnect allows mobile apps to scan a QR and 'login' via a web3 RPC call - to be able to do degen stuff like defi and NFTs. This means the ZenGo wallet must have the WalletConnect stack integrated (more attack surface)
https://help.zengo.com/en/articles/6876159-can-i-use-zengo-on-my-desktop-computer
