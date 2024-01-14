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


# What did we discover DAY 0-1?

Tal (CTO) knows his cryptography and entropy, is respected by other security experts, and has tweeted around AWS authentication vulnerabilities + we know the FaceTec lock is hosted on their cloud (flyryan thread)

Will dig into #FaceTec of ZenGo further in the thread, but from first reading it seems it is part of their Theft Protection feature of the Pro version of ZenGo

Putting 2+2 together we can assume in the ZenGo infrastructure is AWS and a private could

Potential partnerships / infrastructure with Anjuna and/or ZeroNetworks

Part of the FaceTec stack uses a private cloud managed by ZenGo

ZenGo CTO seems to know AWS intimately

Company has worked with leading crytographers
There are some connections between C-suite team members and @ZeroNetworks which offers MPC services - could potentially be part of the ZenGo stack

*this is an assumption*

