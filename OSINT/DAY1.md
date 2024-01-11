# OSINT - DAY 1 - 9 January 2024


user formerly known as niclaz Profile picture
user formerly known as niclaz
@NicLazTweets
Jan 8 • 126 tweets • 55 min read •
Read on X
Megathread of #ZengoWalletChallenge @ZenGo

10 BTC up for grabs if you can break their MPC setup

Are you looking to start the challenge?

The thread below will have links and content to help you get started dear anon.

CC0 licensed - RT all you like - happy hackin'

    https://twitter.com/NicLazTweets/status/1744321339266118014

@ZenGo Why is this cat doing this megathread?

> showing the analysis stage of an exploit

> documenting possible exploit methodologies

> sharing for others to learn from it

> one thread to track of challenge updates

> one thread for MPC / cryptography links

> get sats from @ZenGo
@ZenGo *Important links*

Challenge description:

ZenGo website security page (linked in challenge description):

ZenGo's code:

Repo of /public-docs (includes their 3 whitepapers):

1/zengo.com/zengo-wallet-b…
zengo.com/security
github.com/ZenGo-X
Zengo - The Most Secure Crypto Wallet Zengo is the most secure crypto wallet: The only self-custodial wallet with no seed phrase vulnerability, powered by MPC. https://zengo.com/security
Zengo Wallet Challenge: Hack Zengo, Win 10 Bitcoin - Zengo Zengo Wallet Challenge: Hack Zengo, Win 10 Bitcoin Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/zengo-wallet-bitcoin-challenge
[Zengo X] Threshold cryptography for blockchains. Projects with "city" in name are work in progress. - [Zengo X] https://github.com/ZenGo-X
GitHub - ZenGo-X/public-docs: Zengo's repository of public docs, white papers, etc. Zengo's repository of public docs, white papers, etc. - GitHub - ZenGo-X/public-docs: Zengo's repository of public docs, white papers, etc. https://github.com/ZenGo-X/public-docs
@ZenGo OSINT

(Open Source Intelligence) is the practice of gathering freely available information on a target from various sources as well as their team/collaborators

Humans tend to be the weakest point of a digital security system, so lets see what we can find:

2/
@ZenGo Source:

@OurielOhayon (CEO)
@TalBeerySec (CTO)

Source: Twitter

@ArielMGore (Head of Comms)
@EladBleistein (CMO)
@leontiad (Head of Cryptography)
@UriKelman (Director of Design)

Tip: do check their 'replies' within Twitter


3/zengo.com/team/
About - Zengo Zengo is the most secure crypto wallet: The only self-custodial wallet with no private key vulnerability. Powered by MPC, always recoverable, never hacked. https://zengo.com/team/
https://twitter.com/Zengo/with_replies
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman NOTE: the challenge scope does not involve hacking these humans or their Twitter accounts!

This is only for information gathering purposes within the scope of the challenge - breaking the ZenGo wallet with the 10 BTC in it.

Never deviate from the scope of an engagement

4/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman OSINT observation:

Seems ZenGo runs an ambassador program on Twitter:
tag @PakZ_06 @FaeRecio @defifury @OxFrancesco_

For the challenge these accounts are probably not relevant but I discovered @Crypto_Kimi is/was a former Marketing Manager:



5/

    https://twitter.com/justprotocol/status/1724383424058703908

@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @PakZ_06 @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi OSINT Observation & flag for the @ZenGo team

Seems there are an account impersonating your customer support:

What seems is the 'legit' support is this:


Reported & Banned

to help the ecosystem I suggest you do the same anon

6/twitter.com/Zen_Go_2
https://twitter.com/Zen_Go_2
https://twitter.com/AskZenGo
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi OSINT from Twitter /with_replies (last 2 months)

Tal wrote about AWS authenticaion (Oct)


Note: He posts are normally under the ZenGo Medium (more later in this thread)

Tal's post about bruteforce and MPC


7/medium.com/@TalBeerySec/a…

    https://twitter.com/TalBeerySec/status/1660590475902853121

https://medium.com/@TalBeerySec/a-short-note-on-aws-key-id-f88cc4317489
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi [cont]

Tal's post on Bitcoin JS entropy fail


Tal asking a researcher about MPC


Tal thread on entropy


Tal on the 83.7 BTC fee tx

+


8/

    https://twitter.com/TalBeerySec/status/1724724767154975019


    https://twitter.com/TalBeerySec/status/1724798374308966808


    https://twitter.com/TalBeerySec/status/1728475427889434876


    https://twitter.com/TalBeerySec/status/1729203234244567462


    https://twitter.com/TalBeerySec/status/1729285995315487023

@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi [cont]

Tal on KeyGen and ZenGo's MPC


Tal - Bitcoin as a Dark Forest


Tal on seed recovery


Tal on AWS token replay


Tal on iOS 0 day and ZenGo


9/

    https://twitter.com/TalBeerySec/status/1729888311739908109


    https://twitter.com/TalBeerySec/status/1732082746736922974


    https://twitter.com/TalBeerySec/status/1732766961212194978


    https://twitter.com/TalBeerySec/status/1737266927897297296


    https://twitter.com/TalBeerySec/status/1741478982686478806

@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi [cont]

Following the iOS 0 day post there was an excellent question posted by @flyryan:


"The 3rd party (biometric auth) is hosted on the 2nd party (Zengo server), so even if 3rd party goes away no problem." @TalBeerySec

<screenshot>

10/

    https://twitter.com/flyryan/status/1741483830584754452


Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan [cont]

End of OSINT on Tal's accont

What did we discover?

Tal (CTO) knows his cryptography and entropy, is respected by other security experts, and has tweeted around AWS authentication vulnerabilities

+ we know the FaceTec lock is hosted on their cloud (flyryan thread)

11/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan Will dig into #FaceTec of ZenGo further in the thread, but from first reading it seems it is part of their Theft Protection feature of the Pro version of ZenGo


Putting 2+2 together we can assume in the ZenGo infrastructure is AWS and a private could

12/
Zengo - The Most Secure Crypto Wallet Zengo is the most secure crypto wallet: The only self-custodial wallet with no seed phrase vulnerability, powered by MPC. https://zengo.com/pro-theft-protection/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan OSINT Observation

There are some connections between C-suite team members and @ZeroNetworks which offers MPC services - could potentially be part of the ZenGo stack

*this is an assumption*



13/
Apply MFA to Anything https://zeronetworks.com/use-case/apply-mfa-to-anything/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks OSINT Observation

A quotable tweet from the CEO (@OurielOhayon)

"🚨 We're putting our balls on the table and our coins where our mouth is."

Source:

14/

    https://twitter.com/OurielOhayon/status/1744011091049394408

@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks OSINT from Twitter /with_replies of Iraklis

(@leontiad - Head of Cryptography at ZenGo)

Iraklis pointing to potential partnership with


Iraklis back-n-forth with @henrlihenrli about MPC


15/Anjuna.io

    https://twitter.com/leontiad/status/1587478608100167682


    https://twitter.com/henrlihenrli/status/1600494948540977152

Confidential Computing in one command line | Anjuna Security Anjuna's breakthrough confidential computing platform transforms your cloud into a high-trust environment where data is always encrypted and code is verified for authenticity. http://Anjuna.io
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli [cont]

Iraklis on Rust and zero code duplication within ZenGo


External link to Iraklis' Github Pages:
(list of publications may be of use later)


+ Tal's overview of CertiK audit of ZenGo


16/

    https://twitter.com/leontiad/status/1719030711083057219


leontiad.github.io

    https://twitter.com/TalBeerySec/status/1643246607272476675

https://leontiad.github.io/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli OSINT from Twitter

@ZenGo has a very good 'research' webpage:
where past research and researchers are listed.

I will not be going through all their accounts and past posts but will tag them here for posterity and visibility:

@OmerShlomovits

17/
Cryptography Research - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. http://zengo.com/research
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits [cont]

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

Do read the 'Our Projects' section of the webpage these cryptographers worked on with ZenGo:


18/
Cryptography Research - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/research
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 End of OSINT from Twitter

What have we learnt?

Potential partnerships / infrastructure with Anjuna and/or ZeroNetworks

Part of the FaceTec stack uses a private cloud managed by ZenGo

ZenGo CTO seems to know AWS intimately

Company has worked with leading crytographers

19/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 Caffeine break whilst reviewing the Medium blog posts for next section of this thread:



Take a break anon / touch grass / hug a friend

20/ medium.com/zengo
https://medium.com/zengo
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 OSINT - MEDIUM BLOG ANALYSIS

21 April 2022 - first mention of #3FA on @ZenGo

"The real vulnerability: Single-factor authentication, not cloud storage"



21/ medium.com/zengo/demystif…
Image
https://medium.com/zengo/demystifying-icloud-security-wallets-e348516914d9
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 [cont]

"To access a ZenGo account, you’d need access and control of the email (magic link) of the user, the recovery kit, and a live private biometric scan.
...
both the client (the app) and the server is required
...
the cloud is immaterial as an attack vector."

22/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 [cont]

The April 2022 blog has an embedded video that is a now 'private' demoing this recovery

Reversing the url in the webpage code this is the clean link to it:

I am guessing it was out of date - see new one:


23/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 [cont]

two tweets linked in April 2022 medium by @OurielOhayon around hacks relating to users backing their singlesig seed phrase on iCloud


+
"In less than 1h someone took the backup file made with a hardware wallet seed"


/24

    https://twitter.com/OurielOhayon/status/1517009834356453378


    https://twitter.com/OurielOhayon/status/1517070604607885314?t=xN-knyoegK1iUHJtsOv32Q

@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 [cont]

That 2nd tweet related to a challenge in the blog

Someone claimed the iCloud backup in 1 hour

The 0.03242868 ETH are still in the 2nd bounty wallet bounty wallet which uses their MPC system:

0x7BA1428Aac3987b5eE3048713230efaBD2D89cf4

25/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 [cont]

Important to note that in that challenge all that was provided was 1 of the 3 necessary factors for the wallet

that 1/3 recovery kit is still accessible:


Unsure how the current 10 BTC challenge will differ from this one, we'll see tomorrow

26/
ZenGo recovery kit.txt Shared with Dropbox https://www.dropbox.com/s/d8wwot0dt0lw5q8/ZenGo%20recovery%20kit.txt
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 [cont]

Last paragraph of the 2022 medium post

Would like to comment about 'air gapping' your private key here for those that do not know

since 2022 the tech stack for having your private keys on an offline device have greatly improved

e.g. Dynamic QRs to sign PSBTs

27/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 BONUS: OFFLINE SIGNING DEVICES

If PSBT doesn't mean anything to you read this:


... or watch it in action in this video by @btcuserguide using the awesome @SeedSigner + @bluewalletio



28/bitcoinops.org/en/topics/psbt/

    https://twitter.com/btcuserguide/status/1446873013518020612

Partially signed bitcoin transactions Partially Signed Bitcoin Transactions (PSBTs) are a data format that allows wallets and other tools to exchange information about a Bitcoin transaction and the signatures necessary to complete it. https://bitcoinops.org/en/topics/psbt/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio [cont]

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

29/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io [cont]

I probably missed other HW and Software wallets that leverage PSBTs for offline signing / airgapping seeds

Feel free to comment below anon, this cat is curious

The only other oneI know is anon/nero for Monero

Demo by @moneromars



/30

    https://twitter.com/moneromars/status/1685365155465404418

@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars OSINT - MEDIUM BLOG ANALYSIS

27 Feb 2023

Interesting work by @MHamilis on a bug in SIGHASH_SINGLE type within Bitcoin

I don't believe it will be relevant to the current challenge

just worth sharing it and his code:




/31github.com/MatanHamilis/b…
GitHub - MatanHamilis/bitcoin-sighash-scan: An educational tool to scan for SIGHASH_SINGLE vulnerable addresses on the blockchain using bitcoin-core An educational tool to scan for SIGHASH_SINGLE vulnerable addresses on the blockchain using bitcoin-core - GitHub - MatanHamilis/bitcoin-sighash-scan: An educational tool to scan for SIGHASH_SINGLE... https://github.com/MatanHamilis/bitcoin-sighash-scan
https://medium.com/zengo/a-bug-in-bitcoin-50f3e7d62a9
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis OSINT - MEDIUM BLOG ANALYSIS

17 May 2023

In the aftermath of the Ledger #Recover firmware launch fiasco, @TalBeerySec writes a post about it

"Hardware Wallets are actually Firmware Wallets"

"The recovery of private keys is THE real issue"



/32
https://medium.com/zengo/firmware-wallets-sunlight-is-the-best-disinfectant-f49feb6b7e43
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis [cont]

"We (@ZenGo) solved this issue since our inception and provide a free guaranteed recovery solution that is already working flawlessly for more than four years."

Linked is a page to their website on access guarantees:



33/
How Zengo Guarantees Access to Customers’ Funds - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/how-zengo-guarantees-access-to-customers-funds/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis [cont]

For those unaware some wallets offer a 'distributed private key storage' service:

@Ledger Recover being the one referenced above, sharing an encrypted shared of a private key into a 1/3 multisig.

@FOUNDATIONdvcs does something similar, but way more sovereign.

34/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

These above different to what ZenGo is doing

Will dig into what MPC in entropy generation really means further in this thread...

Just want to share that what Foundation is doing, and schemes such as Shamir's Secret Sharing, are not the same thing as an MPC wallet.

35/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger OSINT - MEDIUM BLOG ANALYSIS

24 June 2023

The next post is a perfect segway into exactly that

"we have to eliminate all “Single Points of Failures”
... include the private key and its backup: The notorious seed phrase."



36/
https://medium.com/zengo/vires-in-numeris-why-adding-more-parties-boosts-security-df35663a189c
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

Sharing 2 screenshots that are the best TL;DR

Do read the whole blog post to get a good handle of the differences in self-custody setups

Links to this:


ping @ZenGo - some url links here point to the wrong domain ()

37/ zengo.com/aa-and-mpc-fre…
wpstage.net
Image
Account Abstraction and MPC: Frens with benefits! - Zengo Account Abstraction and MPC: Frens with benefits! Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/aa-and-mpc-frens-with-benefits/
http://wpstage.net
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

"ZenGo’s solution consists of two MPC parties"

user’s device + remote ZenGo server

Different hardware and software architecture: Mobile devices and cloud servers

Device ownership: Users and ZenGo

Physical location: User pockets and a remote cloud datacenter

38/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger OSINT - MEDIUM BLOG ANALYSIS

29 Nov 2023

Read this to better understand #Entropy & the problem of true random number generation

"This blog is split into two sections: Beginner and Advanced."

I'll comment things relevant to the 10 BTC challenge



39/
https://medium.com/zengo/do-you-know-how-keys-are-made-cd342093b709
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

ZenGo's MPC architecture as defined here

2/2 Multi-Party Computation (MPC) framework

Zengo Server + Zengo App
each generate their own Secret Share (SS)

Zengo App SS = Personal Share
tied to the device using hardware based random generator (TRNG) where applicable

40/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

Zengo Server SS = Remote Share

Only the Personal Share (Zengo App SS) can initialize and sign transactions

All of which are verified by the device’s hardware (Secure Enclave or Trusted Execution Environment)

[image credit: diagram from Nov 2023 medium post]

41/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

Screenshot of how design solves all SPOF

privkey gen = 2 parties using 2 different methods

privkey use = 2 shares computed together

seed phrase recovery = #3FA 'Secure Recovery'

"orthogonal ways"

// something to consider during challenge

42/ wikipedia.org/wiki/Orthogona…
Image
Orthogonality - Wikipedia https://wikipedia.org/wiki/Orthogonality
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger //something to consider

2nd reference I come across to Drand

"distributed randomness beacon daemon written in Golang.

Servers running drand can be linked with each other to produce [random values]... and threshold cryptography."

Threshold cryptography

Drand documentation The home page for developer documentation for drand, a distributed randomness beacon. https://drand.love
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger [cont]

There is a lot I could comment on regarding the bold statement in this last section of the medium post

my opinions are not relevant to the challenge

will just say that 'Don't Trust, Verify' is hard to achieve

44/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @FaeRecio @defifury @OxFrancesco_ @Crypto_Kimi @flyryan @ZeroNetworks @henrlihenrli @OmerShlomovits @EliorBenC @claudiorlandi @ittayeyal @odedleiba @Istvan_A_Seres @PratyushRT @BagadSuyash @amanusk_ @getnitin15 @Elichai2 @Varun_2703 @btcuserguide @SeedSigner @bluewalletio @FOUNDATIONdvcs @Blockstream @COLDCARDwallet @Trezor @SparrowWallet @SamouraiWallet @ElectrumWallet @nunchuk_io @moneromars @MHamilis @Ledger // why brain wallets are a bad idea

In the blog and on twitter @TalBeerySec cited the excellent work of @ryancdotorg on cracking wallets with bad entropy as presented at DEFCON years ago

Never use your brain to generate entropy



45/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan OSINT REDDIT

r/ZengoWallet is the subreddit

Lurking through the last 6 months of post, this surfaced

- roadmap to add Ethereum L2s (only Polygon confirmed)

- Zengo Pro adds a 'legacy transfer' feature which leverages Dropbox



46/
https://www.reddit.com/r/ZengoWallet
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

"The recovery file is actually a decryption key that is used to unlock an encrypted copy of your Personal Secret Share during the recovery process.

This decryption key is 'unlocked' using your 3D FaceLock verification."



47/ reddit.com/r/ZengoWallet/…
Image
https://reddit.com/r/ZengoWallet/comments/14yk9iq/comment/jrsske1
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan OSINT REDDIT AMA OF TODAY

In lead up to this Challenge they hosted an AMA on r/CryptoCurrency

>> 287 comments therein

will screenshot a few relevant ones



48/
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/hack_a_zengo_wallet_win_10_bitcoin_ama
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan ZENGO AMA

Can we see the code?

"We host the world's largest open-source MPC cryptographic library on our GitHub and our Zengo X Research Team has a telegram channel focused on MPC cryptography (most folks in the MPC space participate there."



49/ github.com/ZenGo-X
Image
[Zengo X] Threshold cryptography for blockchains. Projects with "city" in name are work in progress. - [Zengo X] https://github.com/ZenGo-X
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan ZENGO AMA

Where are the servers? secure how?

"Even if someone was able to get access to the server, they still cannot spend your wallet.

Only your Personal Share can initiate a transaction.

The Remote Share on the Zengo server is there to co-sign, but cannot initiate."

50/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan ZENGO AMA

u/Self_Blumpkin throws down their 1337 skillz

u/ZenGoOfficial references this response to many questions around the architecture and entropy:



51/ reddit.com/r/CryptoCurren…
Image
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgvjy94
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan ZENGO AMA

//Guaranteed Access as a potential attack vector

"The 3rd party (EscrowTech) can help you recover your wallet, but they cannot access your wallet or collude with others to access your wallet... "



52/ reddit.com/r/CryptoCurren…
Image
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgvlqew/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

//GA attack vector

Wallet has:
- Personal Share (unencrypted)
- Remote Share copy (encrypted)

If GA were to activate > EscrowTech releases this Remote Share Decryption Key to #GitHub

> Github push the decryption key of your encrypted Remote Share to your device

53/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

Now you wallet has both Shares unencrypted

Your device has 2/2 keys for the multisig

wallet creates the private key *for the first time*

spend coins

Attack vectors to consider:
- spoofing GA alert process
- Compromising Github access:


54/
ZenGo-Trustee - Overview ZenGo-Trustee has 2 repositories available. Follow their code on GitHub. https://github.com/Zengo-Trustee
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

Additional theoretical attack vector, most probably outside the scope of this Challenge

Compromise the systems / tech stack of the Trustees listed in

Release GA / get decryption key

*meow* this is illegal kids, don't pwn others *meow*

55/
GitHub - ZenGo-Trustee/reports: Used by ZenGo's Trustee to upload reports Used by ZenGo's Trustee to upload reports. Contribute to ZenGo-Trustee/reports development by creating an account on GitHub. https://github.com/ZenGo-Trustee/reports
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan FOR THE LULZ

Noticed the /Server-key-release repository has no code but it does have an active Issue in the tracker:



" Ha "

56/ github.com/ZenGo-Trustee/…
Image
Ha · Issue #1 · ZenGo-Trustee/Server-key-release - https://github.com/ZenGo-Trustee/Server-key-release/issues/1
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan BACK TO REDDIT AMA

"We are committed to putting our money where our mouth is and continuing to improve our security."

"Tomorrow we reveal:
- The BTC address
- The ETH address
- The transaction hashes
- A video showing you the live wallet"

57/ Image
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

exchange between u/kuri-kuma and ZenGo

"Recovery: Your Personal share is locked to you with your 3D FaceLock (private biometric verification scan). It is protected by a 600,000 bug bounty and is only 1 of 3 parts of your wallet recovery"



58/ reddit.com/r/CryptoCurren…
Image
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgrihyk/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

u/Roman_Scoggins asking the hard questions

How do you make money?
Where is your server located and how is it secured?
Can we see the code to verify it?

Answered with links to above screenshoted posts



59/
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgujjo6/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

responding to u/nanooverbtc

"Their Primary share initiates signing, gets co-signed by the remote share, and then broadcasts the transaction to the network). Let us know if that is clear or if you have further questions about this!"



60/
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/hack_a_zengo_wallet_win_10_bitcoin_ama
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan [cont]

u/flyryan

"You've stated on your site that you generated the single master private key that protects all user's server shares with a Raspberry Pi and destroyed the Pi after."

👀👀👀

No answer as of yet to this question



61/
https://www.reddit.com/r/CryptoCurrency/comments/190s3uc/comment/kgx0365/
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan END OF OSINT SECTION

Tomorrow the Challenge parameters will be published

Check back in on this #ZengoWalletChallenge megathread for analysis of:

- hosted content

- digging into code on

- paws-crossed a Proof of Concept exploit zengo.com
github.com/orgs/ZenGo-X/r…
Zengo Wallet: Secure by default Zengo is the most secure crypto wallet: The only self-custodial wallet with no private key vulnerability. Powered by MPC, always recoverable, never hacked. http://zengo.com
[Zengo X] Threshold cryptography for blockchains. Projects with "city" in name are work in progress. - [Zengo X] https://github.com/orgs/ZenGo-X/repositories
@ZenGo @OurielOhayon @TalBeerySec @ArielMGore @EladBleistein @leontiad @UriKelman @Crypto_Kimi @flyryan >>> and we are back

@RampNetwork is hosting a Twitter space

@ZenGo to announce the launch of the #ZengoWalletChallenge

9AM EST - very soon anon

    https://twitter.com/ZenGo/status/1744705396885864932

@ZenGo CHALLENGE CONDITIONS

Soon this webpage will *hopefully* be updated with the addresses and conditions for the 10 BTC Challenge

Remember anon,

Never deviate from the challenge parameters

Do not hack things or people unless they consent



64/ zengo.com/zengo-wallet-b…
Image
Zengo Wallet Challenge: Hack Zengo, Win 10 Bitcoin - Zengo Zengo Wallet Challenge: Hack Zengo, Win 10 Bitcoin Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/zengo-wallet-bitcoin-challenge
@ZenGo [cont]

Do you want to know more?

@Hacker0x01's knowledge base articles:

What is a White Hat Hacker?



Why you need #responsible #disclosure and how?



65/hackerone.com/knowledge-cent…
https://www.hackerone.com/knowledge-center/why-you-need-responsible-disclosure-and-how-get-started
https://www.hackerone.com/knowledge-center/white-hat-hacker
@ZenGo @Hacker0x01 POST TWITTER SPACES

- Challenge wallet will use Thread Protection

- RECOVERY is 3FA (email, your face FaceTec, and the recovery file) but also system allows to add face or recovery email to an account.

// potential attack vector - new face + email



66/

    https://twitter.com/RampNetwork/status/1744720652609749210

@ZenGo @Hacker0x01 [cont]

- There are 'hints' shared about the account/ways in on challenge website during the week // check for HINTS

- If you are successful - "No need to send us anything, if you can get it the bitcoin they are yours"

- progressive rollout of HINTS

67/
@ZenGo @Hacker0x01 [cont]

- This is a unique engagement oppurtinty... but also a risk for all wallets, ZengGo assessed that wall is secure enough to test it and their brand.

- "in cybersecurity there is not thing as 100% (secure)"

- Social Engineering / Insider attack?
@mizi is on it

68/
@ZenGo @Hacker0x01 @mizi TANGENT: LEGACY SYSTEM

At the end of the Spaces the relatively new feature Legacy Transfer was cited.

Potential attack vector if this Challenge was *not time-limited.*

But quick read it seems it is a type of dead-man-switch which released shared for full privkey only...

69/
@ZenGo @Hacker0x01 @mizi [cont]

exploiting Legacy would require full access to private shards, email, and the face of owner

which I think is enough access privilege for tx signing

Even if you do add yourself as a beneficiary the dead-man-switch has to be activated

// skipping this attack vector

70/
@ZenGo @Hacker0x01 @mizi [cont]

That said if curious about @ZenGo Legacy Transfer protocol here is a direct link to the whitepaper [PDF]



It appears ZenGo are the first to implement this form of Legacy MPC recovery process

v.1 - August 2023 - authors: @TalBeerySec et al.

71/zengo.com/wp-content/upl…
@ZenGo @Hacker0x01 @mizi @TalBeerySec CHALLENGE WEBPAGE UPDATED

Day 1 – Launch Day: Tuesday, January 9th

Bitcoin address: 3NB5gbyhCQM92WUpHxfpK7PqC1KKTAYwpK

ETH address: 0x3ceb6a3eeb69a3b8fd4d1865dde9799310e547b7

Verified:
1.000000 BTC
0.006942 ETH
+ 1 Pudgy Penguin NFT

72/
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

PROOF OF BITCOIN + NEXT UPDATE

Day 6: Sunday, January 14th around 9AM EST:
- Security Factor Hint
- 4 more Bitcoin added

// What we can assume from video: Ari may be the owner of the Challenge wallet

// adding a search tab: Face mapping AI



73/
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE



Annual audits by Certik, Forta, Alchemy, Hacken

Features added to Pro wallet
- 3D Face Theft protection
- web3 firewall
- 24/7 support chat

Confirmed in Spaces that Theft Protection is active on the wallet being used in Challenge

74/
Zengo - The Most Secure Crypto Wallet Zengo is the most secure crypto wallet: The only self-custodial wallet with no seed phrase vulnerability, powered by MPC. https://zengo.com/security
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

#Recovery

FAQ: Can I lose my account...?

"... if both of these things were to happen:

1) You lose your device and need to recover it

and

2) You lose access to one or more of the 3 factors necessary to authenticate your wallet recovery."

[3FA screenshot]

75/ Image
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

FAQ: Can Zengo prevent certain transactions from happening?

"Zengo’s MPC security system requires that any transaction you make be validated by Zengo’s servers before being broadcasted to the blockchain...

While in theory..."

//TX validated before broadcasting

76/ Image
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

FAQ: Can Zengo know who I am?

"Zengo has no access to any private information about you besides your email, and this email can be non-nominative should you choose."

>> Their way of verifying you is your email and the FaceTec dependency/3rd party

//Inspect code

77/
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - AUDITS

AppSec 2019


Kudelski 2019


Kudelski 2019


Scorpiones 2021


Scorpiones 2022


Certik 2023


source: /security page

78/zengo.com/audit/audit-ap…
zengo.com/audit/audit-ku…
zengo.com/audit/audit-ku…
zengo.com/audit/audit-%2…
zengo.com/audit/audit-sc…
zengo.com/zengo-certik-a…
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE



@ZenGo can you confirm (as noted in Spaces) that for the #ZengoWalletChallenge this white hat policy is not being followed?

Would be great to have confirmation and reporting mechanism outline on challenge webpage

purrrrrrr

79/ zengo.com/white-hats

Image
Image
Bitcoin & Crypto White Hats - Zengo We Invite White Hats to Test Our Security - Zengo is the first keyless bitcoin and cryptocurrency wallet. Read more! https://zengo.com/white-hats
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE



Consideration that the Pro features + the wallet supporting multiple assets (not just BTC) could mean more attack surfaces for potential exploits

What iz attack surface?


80/zengo.com/pro/
Zengo Pro: The future of wallet security, today - Zengo Zengo is the crypto wallet secure by default: Self-custodial, no seed phrase vulnerability, and powered by MPC‏ https://zengo.com/pro/
What is an Attack Surface? | IBM An attack surface is the sum of an organization's vulnerabilities to cyberattack. https://www.ibm.com/topics/attack-surface
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

For those wishing to explore the #multiasset vector



Supported: Ethereum, Polygon, Arbitrum One & Optimism Mainnets

Not: BSC, Tron, Base, Bitcoin Cash and other Layer 2s.

81/
Multi Cryptocurrency wallet - Zengo With Zengo's Multi Cryptocurrency wallet you can buy, swap and sell hundreds of tokens such as: BTC, Doge, XTZ, Uniswap, SHIB, ALPHA, ETH, USDC, Binance, LUNA and many more. https://zengo.com/assets/
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

Another vector for accessing the Ethereum wallet could be smart-contract exploits / malicious signing

This would require subverting this 'web3 firewall' part of the Pro wallet version and also phishing the user



//not a feasible IMHO

82/
Firewall - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/firewall/
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE - #TSS



TSS = Threshold Signatures System

"The Zengo system is a “two out of two” party ECDSA threshold signatures system.

The two parties are the secure Zengo server and the Zengo user’s mobile device."

//how to construct 2/2 Tx

83/
Crypto & Bitcoin Wallet: Signature Security Standards - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/security-in-depth
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

Here would be a good place to briefly touch on #GG20

just after the above quote, we see this text

the 'Github' link to the audited text leads to:


This library is no longer maintained or used by ZenGo (see header in )

84/ github.com/ZenGo-X/multi-…
readme.md
Image
Today I Learned for programmers Today I Learned for programmers http://readme.md
GitHub - ZenGo-X/multi-party-ecdsa: Rust implementation of {t,n}-threshold ECDSA (elliptic curve digital signature algorithm). Rust implementation of {t,n}-threshold ECDSA (elliptic curve digital signature algorithm). - GitHub - ZenGo-X/multi-party-ecdsa: Rust implementation of {t,n}-threshold ECDSA (elliptic curve digital... https://github.com/ZenGo-X/multi-party-ecdsa
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

Questions

Where is the audit for the TSS?

If ZenGo moved from the /multi-party-ecdsa code due to exploits in GG20 MPC computation, was the new implementation /gotham-city audits?

By whom and when?

Is the content on the webpage about TSS out of date?

uhmm....

85/
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

Within an MPC cryptography related Telegram chat managed by ZenGo and team you can find details of a handful of moments when exploits were announced and team commented they were unaffected...

i.e. #BitForge



86/
BitForge: Fireblocks researchers uncover vulnerabilities in over 15 major wallet providers - Fireblocks The MPC vulnerabilities, dubbed BitForge, were discovered in popular legacy implementations, including GG-18, GG-20, and Lindell 17. Check with your provider or contact us. https://www.fireblocks.com/blog/bitforge-fireblocks-researchers-uncover-vulnerabilities-in-over-15-major-wallet-providers/
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

DISCLAIMER

As only a mere cat I only know some things

I do understand *some* cryptography but I am not an expert or speak of the soundness of the BitForge / GG20 / MPC vulnerabilites.

I know attacking the cryptography is not a valid approach to win this Challenge.

87/
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE



What is Open Sourced?

> not much & not the app

linked:
the /multi-party-ecdsa (see above)
and also a /curv code repository

We will dig into the code further in future

don't worry anon - staying non-technical for now

88/
Zengo and Open Source - Zengo Zengo and Open Source Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/zengo-and-open-source
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE



Probably most important page for how ZenGo's MPC differs from "more traditional" private key storage

FAQ quote:

"The best part of this process is no single entity can ever get access to any private key"

we shall see...

89/ zengo.com/mpc-wallet/
Image
MPC Wallet - What is MPC? - Zengo Zengo is the first MPC-powered crypto wallet: The most secure crypto wallet in Web3 https://zengo.com/mpc-wallet/
@ZenGo @Hacker0x01 @mizi @TalBeerySec [cont]

If you are digging the cryptography then check out:

+


Lots there, also a link to Telegram group exclusively for MPC related questions and academic discussion

gg to ZenGo for bringing these researchers together

90/zengo.com/research
Cryptography Research - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/research
Do you know how keys are made? - Zengo Do you know how keys are made? Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/how-keys-are-made/
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - WEBSITE

Last website post - I think all the important bits are covered, but you might ask...

how do I find out more?

enter sitemap.xml

ZenGo website uses Wordpress and has a sitemap.xml for SEO / better web navigation

/post-sitemap.xml has all blog posts

91/ Image
@ZenGo @Hacker0x01 @mizi @TalBeerySec OSINT - SUPPORT

Quick skim through the support docs to see if we missed something:

> About Zengo

"To recover your account, all you need is your email, your storage service (iCloud, google drive, or dropbox), and a selfie scan"

wait what's this...

92/
Zengo Help Center Zengo Help Center https://help.zengo.com
@ZenGo OPEN SOURCE LICENSES

... so like good developers that use certain Open Source software licenses the team has listed many here:



The next couple of tweets will be a dump of the names of the packages and services cited, for ease of use...

93/
Open Source Licences | Zengo Help Center https://help.zengo.com/en/articles/5190969-open-source-licences
@ZenGo //dump
Adler32
Aho-corasick
Ansi_term
Arrayvec
Ascii
Atty
Autocfg
Backtrace
Backtrace-sys
Base64
Bech32
Bellman
Bit-vec
Bitcoin, Rust
Bitcoin-bech32
Bitflags
Blake2-rfc
Block-buffer
Block-padding
Byte-Tools
Byteorder
Bytes
C2-Chacha
Cc
Cesu8
Cfg-If
Clap
Clear_On_Drop
Cloudabi
@ZenGo Combine
Config
Constant_Time_Eq
Cookie
Core-Foundation
Crc32Fast
Crossbeam
Crossbeam-Deque
Crossbeam-Epoch
Crossbeam-Queue
Crossbeam-Utils
Cryptoxide
Curve25519-Dalek
Devise
Devise_Codegen
Devise_Core
Digest
Dtoa
Either
Encoding_Rs
Error-Chain
Failure
Failure_Derive
Fake-Simd
@ZenGo Filetime
Fnv
Foreign-Types
Foreign-Types-Shared
Fsevent
Fsevent-Sys
Fuchsia-Zircon
Fuchsia-Zircon-Sys
Futures
Futures-Cpupool
Gcc
Generic-Array
Getrandom
H2
Hex
Http
Http-Body
Httparse
Hyper
Hyper-Tls
Idna
Indexmap
Inotify
Inotify-Sys
Iovec
Itertools
Itoa
Jni
Jni-Sys
Keccak
@ZenGo Kernel32-Sys
Language-Tags
Lazy_Static
Lazycell
Libc
Libflate
Linked-Hash-Map
Lock_Api
Log
Matches
Memchr
Memoffset
Merkle
Mime
Mime_Guess
Mio
Mio-Extras
Mio-Uds
Miow
Multi-Party-Ecdsa
Native-Tls
Net2
Nodrop
Nom
Notify
Num_Cpus
Num-Traits
Opaque-Debug
Openssl
Openssl-Probe
@ZenGo Openssl-Sys
Owning_Ref
Pairing
Parking_Lot
Parking_Lot_Core
Pear
Pear_Codegen
Percent-Encoding
Pkg-Config
Ppv-Lite86
Proc-Macro2
Quote
Rand
Rand_Chacha
Rand_Core
Rand_Hc
Rand_Isaac
Rand_Jitter
Rand_Os
Rand_Pcg
Rand_Xorshift
Rayon
Rayon-Core
Rdrand
Redox_Syscall
Regex
Regex-Syntax
@ZenGo Remove_Dir_All
Reqwest
Ring
Rle-Decode-Fast
Rocket
Rocket_Codegen
Rocket_Contrib
Rocket_Http
Rust-Crypto
Rust-Gmp
Rust-Ini
Rustc_Version
Rustc-Demangle
Rustc-Serialize
Ryu
Safemem
Same-File
Sapling-Crypto
Schannel
Scopeguard
Secp256K1
Security-Framework
Security-Framework-Sys
@ZenGo Semver
Semver-Parser
Serde
Serde_Derive
Serde_Json
Serde_Test
Serde_Urlencoded
Serde-Hjson
Sha2
Sha3
Slab
Smallvec
Spin
Stable_Deref_Trait
State
String
Strsim
Subtle
Syn
Synstructure
Take_Mut
Tempfile
Textwrap
Thread_Local
Time
Tokio
Tokio-Buf
Tokio-Codec
Tokio-Current-Thread
@ZenGo Tokio-Executor
Tokio-Fs
Tokio-Io
Tokio-Reactor
Tokio-Sync
Tokio-Tcp
Tokio-Threadpool
Tokio-Timer
Tokio-Udp
Tokio-Uds
Toml
Traitobject
Try-Lock
Typeable
Typenum
Unicase
Unicode-Bidi
Unicode-Normalization
Unicode-Width
Unicode-Xid
Untrusted
Url
Uuid
Vcpkg
Vec_Map
Version_Check
@ZenGo Walkdir
Want
Wasi
Winapi
Winapi-Build
Winapi-I686-Pc-Windows-Gnu
Winapi-Util
Winapi-X86_64-Pc-Windows-Gnu
Ws2_32-Sys
Yaml-Rust
Yansi
Zeroize
Zk-Paillier

//end dump

I realise that for some of you the above doesn't mean much, so let me give context to it and it may be useful

94/
@ZenGo DEPENDENCY

Making software is hard, especially from scratch

Open Source is awesome

& Open Source cryptography is very important

but in building the server and app there is a good chance ZenGo uses some of the above in their stack

> relevant xkcd


95/
https://www.explainxkcd.com/wiki/index.php/2347:_Dependency
@ZenGo [cont]

For someone who builds or reads code many of the above listed names will ring bells...

like the one and only ASCII <3

but also many Rust packages: rustc / safemem / etc

Bitcoin related: Rust Bitcoin / bech32 / secp256K1

and a bunch of cryptography libraries

96/
@ZenGo [cont]

Without looking too much into each right now...

my ears perked at the following:

winapi - rust package to call Windows API

cloudabi - ABI for UNIX-like OS
* note: project is unmaintained *

Lock_Api - wish I could call the @LockPickingLwyr

:D

//inspect code

97/
@ZenGo OSINT - SUPPORT

> How To Guides

"To ensure that only you can send funds from your ZenGo wallet, we require authentication through Apple’s built-in biometric or passcode authentication system."

[screenshot of security page of app]

98/ Image
@ZenGo [cont]

Screenshot from "How do I recover my Zengo account if I change my phone or delete the app?"

Leads to this good overview of Recovery Kit



//Recovery Spoofing is something I am considering as a viable attack of the wallet

99/ help.zengo.com/en/articles/26…
Image
What is Zengo's Recovery Kit | Zengo Help Center https://help.zengo.com/en/articles/2603673-what-is-zengo-s-recovery-kit
@ZenGo *100 tweets*

Have a snack dear kitty

maybe a nap as well

If you made it this far drop a meow in the comments

puuuuur

100/
@ZenGo OSINT - SUPPORT

"How to transfer your Zengo account from iOS to Android and vice-versa"

// Transfer of account ownership to new phone

Sync Recovery Kit
Access cloud storage
AI face replication

"You're In"

Hope this become a LeopardsAteMyFace situation

101/ Image
@ZenGo [cont]

> How To Guides

"the Zengo recovery file will remain locally stored on your device and in your personal cloud service/s but will be unusable once the account is deleted. After you have fully deleted your account, you can, if you want, remove this file manually."

/102
@ZenGo OSINT - SUPPORT

> Security > Biometrics

Provider: FaceTec ()
Product: 3D Facelock
Bounty: $600,000 Spoof Bounty Program


Support


Blog


In-house test


103/facetec.com
dev.facetec.com/spoof-bounty-p…
help.zengo.com/en/articles/28…
zengo.com/biometrics-in-…
Discover Our Biometric Crypto & Bitcoin Wallet - Zengo Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/biometrics-in-zengo-wallet
How secure are Zengo's biometric verifications? | Zengo Help Center How safe are ZenGo's biometric backups? https://help.zengo.com/en/articles/2898755-how-secure-are-zengo-s-biometric-verifications
https://dev.facetec.com/spoof-bounty-program
Can pictures break Zengo’s biometrics security? How does Zengo behave when you present high-quality pictures? We test our systems all the time, but here is a recent sample of our own experimentations https://zengo.com/can-pictures-break-zengos-biometrics-security
http://facetec.com
@ZenGo [cont]

> Security > How Zengo security model works

Good content about the overall security model

Answers common FAQ on the subject

Adds 7 points to "Are there any risks in using Zengo?"

Written by @OurielOhayon - Updated over a week ago



104/
How Zengo security model works | Zengo Help Center https://help.zengo.com/en/articles/2603678-how-zengo-security-model-works
@ZenGo OSINT - SUPPORT

> General

"The face verification technology used in Zengo should work even as your face changes naturally over time. If you gain or lose weight, start wearing eyeglasses, grow out your hair or beard, or grow older..."



105/ help.zengo.com/en/articles/38…
Image
What is an additional 3D FaceLock? | Zengo Help Center https://help.zengo.com/en/articles/3836341-what-is-an-additional-3d-facelock
@ZenGo [cont]

"What Bitcoin address formats does Zengo support?"

p2sh-p2wpkh

Noticed this when they revealed the Challenge address:

3NB5gbyhCQM92WUpHxfpK7PqC1KKTAYwpK

So all ZenGo BTC addresses start with a 3

Curious...



106/
What Bitcoin address formats does Zengo support? | Zengo Help Center https://help.zengo.com/en/articles/3123492-what-bitcoin-address-formats-does-zengo-support
@ZenGo [cont]

All Bitcoin addresses are backwards compatible

I just find it curious seeing that 97% of the network now transactions of SegWit native (bc1...) addresses

Not an expert on vulnerabilities in tx construction for p2sh-p2wpkh types...

might be worth looking into

107/ Image
@ZenGo > General > Assets

"If a token or NFT is important to you, please request it from our customer support agents, and we will try our best to add support for it."

Is this how the @pudgypenguins NFT is secured?

Additional verification by a human?

.... just like a bank?

108/ Image
@ZenGo @pudgypenguins [cont]

Can I use Zengo if my selfie camera is broken?

No. ish.

ZoOm Biometric link:
>> domain redirect to

ZoOm® is a FaceTec product (2017):


Sauce:

/109 zoomlogin.com
facetec.com
businesswire.com/news/home/2017…
help.zengo.com/en/articles/29…
Image
Can I use Zengo if my selfie camera is broken? | Zengo Help Center How to use Zengo if your iPhone camera is broken https://help.zengo.com/en/articles/2981103-can-i-use-zengo-if-my-selfie-camera-is-broken
FaceTec’s Universal 3D Facial Recognition Software Replaces Passwords in Any Mobile App FaceTec sets a new standard in mobile biometrics with the release of ZoOm®, the first universal 3D facial authentication software solution. https://www.businesswire.com/news/home/20170822005465/en/FaceTec%E2%80%99s-Universal-3D-Facial-Recognition-Software-Replaces
http://facetec.com
http://zoomlogin.com
@ZenGo @pudgypenguins > General

Lose your phone?



"All you need is to:
- Zengo app

- log in with the same email

- Access to your recovery kit on your cloud service

- pass the selfie scan to verify it's you.

"here is a quick video guide"
"video private" .... :/

110/
What happens if I lose my mobile device or my device is compromised? | Zengo Help Center https://help.zengo.com/en/articles/2830607-what-happens-if-i-lose-my-mobile-device-or-my-device-is-compromised
@ZenGo @pudgypenguins OSINT - SUPPORT

Zengo #Pro - Complete Guide

Since the Challenge Wallet has the Theft Protection and firewall feature active it must be a Pro version

//Reflection: how does ZenGo know what user is Pro

//Is there a db somewhere?



111/
Zengo Pro: Your Complete Guide to the best crypto wallet protection | Zengo Help Center Enhancing Your Digital Asset Security and Management: A Comprehensive Walkthrough of Zengo Pro Features https://help.zengo.com/en/articles/8105588-zengo-pro-your-complete-guide-to-the-best-crypto-wallet-protection
@ZenGo @pudgypenguins > General

WalletConnect

WalletConnect allows mobile apps to scan a QR and 'login' via a web3 RPC call - to be able to do degen stuff like defi and NFTs

This means the ZenGo wallet must have the WalletConnect stack integrated (more attack surface)



112/
Can I use Zengo on my desktop computer? | Zengo Help Center Zengo is a mobile wallet but it can be used in a few ways on your computer. https://help.zengo.com/en/articles/6876159-can-i-use-zengo-on-my-desktop-computer
@ZenGo *Made a misake*

p2sh-p2wpkh is a SegWit address, just not a 'Native SegWit' one - still an interesting design choice...

especially considering the license of bech32 is listed on the zengo website

... anyway
@ZenGo END OF DAY 1 - THREAD REVIEW

# DONE

- OSINT Twitter, Medium, Reddit, Website, Support
- Challenge updated, addresses verified
- Launch Twitter Space notes (check for HINTS)
- Overview of Legacy Transfer & 3FA FaceLock features
- found 6 audits (to review) and OS licenses

113/
@ZenGo Get some rest kittens

You earned it

Tomorrow we dig into the code available on


Be sure to check in on the Challenge webpage

their next scheduled update is Sunday, January 14th

#ZengoWalletChallenge

/114 github.com/ZenGo-X
zengo.com/zengo-wallet-b…
[Zengo X] Threshold cryptography for blockchains. Projects with "city" in name are work in progress. - [Zengo X] https://github.com/ZenGo-X
Zengo Wallet Challenge: Hack Zengo, Win 10 Bitcoin - Zengo Zengo Wallet Challenge: Hack Zengo, Win 10 Bitcoin Zengo is the first keyless bitcoin and cryptocurrency wallet — the most simple and secure way to manage your crypto assets. https://zengo.com/zengo-wallet-bitcoin-challenge/
