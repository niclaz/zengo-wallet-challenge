# OSINT - DAY 3 - 11 January 2024

Time to sniff around the /zengo repos listed above and see what we can find out about the tech stack of the wallet and the cryptography used...

/gotham-city 

/gotham-engine 

/gotham-public

As already noted it seems ZenGo uses a naming convention based around famous cities...  Gotham is the most visited one of these and it's inviting the all us jokers, riddlers & catpersons to bring chaos...

## OSINT - What is Gotham?

/gotham-city

"fully functional client/server application for issuing two party ECDSA signatures"

Cryptographic libraries:
- /secp256k1 - used in Bitcoin secp256k1 signing
- /two-party-ecdsa - Lindell's Crypto17 paper?

[TO ADD]
Image of design from the repo: https://github.com/ZenGo-X/gotham-city/raw/master/misc/ecdsa-illustration.png 

> note: all three /gotham repos are all 100% Rust code

The Whitepaper for the design can be found in the repo: "Bitcoin Wallet Powered by Two-Party ECDSA"

https://github.com/ZenGo-X/gotham-city/tree/master/white-paper

The paper is 6 years old and references the /KZen-networks repository ... KZen is the former name of ZenGo

> outdated?

### OSINT - /gotham-city/cargo.toml

4 members (potential attack surfaces)
- demo-wallet
- gotham-server
- gotham-client
- integration-tests

/gotham-city dependencies:
- gotham-server = { path = "gotham-server" }
- gotham-client = { path = "gotham-client" }
- serde = { version = "1", features = ["derive", "serde_derive"] }
- serde_json = "1"
- log = "0.4"
- reqwest = "0.9.5"
- failure = "0.1"
- floating-duration = "0.1.2"
- rocket = { version = "0.5.0-rc.1", default-features = false, features=["json"]}
- config = "0.9.2"
- uuid = { version = "0.7", features = ["v4"] }
- jsonwebtoken = "8"
- hex = "0.4"
- secp256k1 = {version = "0.21.0", features = ["global-context"]}
- rand = "0.8"
- two-party-ecdsa = { git = "https://github.com/ZenGo-X/two-party-ecdsa.git", branch="compatibility_gotham_engine" }
- gotham-engine = { git = "https://github.com/ZenGo-X/gotham-engine.git" }

To see all the various cargo.toml within the /gotham-city repo:

https://github.com/niclaz/zengo-wallet-challenge/tree/niclaz/CODE/ZenGo-X/gotham-city/All%20cargo.toml

To see a list of just all the dependencies from the 5 different cargo.toml files here:

https://github.com/niclaz/zengo-wallet-challenge/tree/niclaz/CODE/ZenGo-X/gotham-city/All%20cargo.toml

### OSINT - /gotham-city subfolders

- /demo-wallet
- /gotham-client
- /gotham-server
- /integration-tests
- /misc
- /white-paper

> the first 3 contain code to run the gotham-city program - the 'members' in the cargo.toml

> integration-tests is for testing if the code works well after building it on your OS

> whitepaper contains PDF and .txt versions of a 2018 paper linked in this post and misc has a bunch of images for the app (.png)

### OSINT - /gotham-city README.md commit history

After discovering a 'demo.gif' in the /misc folder I went down the rabbit hole of reviewing the commit history of the README.md of /gotham-city

See this section of the repo: https://github.com/niclaz/zengo-wallet-challenge/tree/niclaz/OSINT/Github/gotham-city
- (hidden) README.md
- (uncommented) README.md
- gotham-city-demo.gif

> hidden is the just the text that was commented out
 
> uncommented is with the commented back in

> .gif is a copy

first 'commit' was on Dec 12, 2018 and we can view all changes since... looking through them, regular changes till Jan 19, 2021

then nothing till 6 months ago when a commit changes a bunch of the content and 'project status' from work in progress to 'use at your own risk'

Was that the Launch?

[ADDED COMMIT COMMENTS TO REPOSITORY - EXTRACT SELECTION HERE IN FUTURE]
