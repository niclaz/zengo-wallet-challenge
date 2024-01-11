# OSINT - DAY 3 - 11 January 2024

2 more days till Hint announcement by ZenGo and we have more information gathering to do

Time to sniff around the /zengo repos listed above

See what we can find out about the tech stack of the wallet and the cryptography used...

/gotham-city 
/gotham-engine 
/gotham-public

As noted in post 143 it seems ZenGo uses a naming convention based around famous cities... 

Gotham is the most visited one of these and it's inviting the all us jokers, riddlers & catpersons to bring chaos

What is Gotham?

/gotham-city

"fully functional client/server application for issuing two party ECDSA signatures"

Cryptographic libraries:

/secp256k1 - used in Bitcoin secp256k1 signing
/two-party-ecdsa - Lindell's Crypto17 paper  

image of design from the repo:
https://github.com/ZenGo-X/gotham-city/raw/master/misc/ecdsa-illustration.png 

note: all three /gotham repos are all 100% Rust code

The Whitepaper for the design can be found in the repo

"Bitcoin Wallet Powered by Two-Party ECDSA"
https://github.com/ZenGo-X/gotham-city/tree/master/white-paper

The paper is 6 years old and references/KZen-networks

KZen is the former name of ZenGo

What's inside /gotham-city?

Follow me kitty

- open (no need to register an account)
https://github.com/ZenGo-X/gotham-city/blob/master/README.md
> notice the '/gotham-city/blob/master/' in the url ?

- Navigate with the menu on left hand side (Files)

- starting from bottom (http://launch-server.sh)

- launch-server.sh

< cd ./gotham-server && cargo run --release > 

are you screaming internally " nooooo code !!! "

DON'T PANIC

Cats don't need to code, nor do you to potentially access the 10 BTC in the Challenge wallet.

so... what is this file?

... filename: launch-server
> the intention is pretty clear

extension: .sh
> scripting file format, meant to be run as a command

command: cd ./gotham-server  
> Linux folder navigation

&&
> and

cargo run
> run a Rust program

--release
> flag for Rust
>
> I won't be commenting on code line-by-line like this much in this thread - it was just an intro for new kittens

What did we learn just from this file?

- /gotham-city code runs on #Linux operating systems
- Is written in the #Rust programming language

Rust is awesome
Rust is new
Rust is considered 'memory safe'

so Rust is safe?

right?

The fact that Rust is a relatively newer language can be source of code instability and dependency issues...

... and a Rust program lists all its dependencies in cargo.toml

/gotham-city/cargo.toml

so... what do we have here?

👀 4 members (potential attack surfaces)

dependencies:

gotham-server
gotham-client
serde
serde_json
log
reqwest
failure
floating-duration
rocket
config
uuid
jsonwebtoken
hex
secp256k1
rand
two-party-ecdsa
gotham-engine

We will come back to Rust dependencies in the cargo.toml files and what this means for the Challenge in coming posts kitten

> All will be easily searchable on Github soon

For now just remember:

- we know potential dependencies of the wallet
- multiple 'members'

Back to the top of /gotham-city:

Folders:

.github
demo-wallet
gotham-client
gotham-server
integration-tests
misc
white-paper

Files:

.gitignore
CHANGELOG
Cargo.toml
LICENSE
README
launch-server

Ignore all folders & files with a . before the name
Files first:

http://launch-server.sh we already saw

http://README.md is the text on main page of repo

LICENSE is for software license (not relevant)

Cargo.toml is an important file for Rust programs to run

http://CHANGELOG.md lists all the code updates

Folders now:

demo-wallet
gotham-client
gotham-server
integration-tests
misc
white-paper

> the first 3 contain code to run the gotham-city program - the 'members' in the cargo.toml

> integration-tests is for testing if the code works well after building it on your OS

> whitepaper contains PDF and .txt versions of a 2018 paper linked in this post: https://twitter.com/NicLazTweets/status/1745413337423151186

> misc has a bunch of images for the app (.png)

... but wait 

also a .gif ?

and it's called demo?

but I haven't seen this before

*curiosity intensifies*

ok... where is this demo.gif used? 

It must have a purpose if it's in the repo... 

going back to /gotham-city and using the search bar

It auto-fills 'repo:ZenGo-X/gotham-city' for me

typed 'demo.gif'

the screenshot is the result of that search

1 result in Code

did you see an animated gif on the http://README.md? the page of text you see when you are on /gotham-city?

I didn't... 

so here it is (thanks Github)

... but the result from Github under Code is for http://README.md ? ... how is it 'invisible'?

firstly... disclaimer that to 'search Code' in Github you need an account on the platform... I know, it sucks

with that said, how is there a .gif in the http://README.md ?

> Code Commenting

It's what programmers do to make notes in code or to 'mute' things


There are different types of Code Commenting

in Markdown (.md files) it's // 

in Rust (.rs or .toml files) it can be // or /*

If you go navigate to the http://README.md file:
https://github.com/ZenGo-X/gotham-city/blob/master/README.md

> See the three buttons at the top?

> click on 'Code'

scrolling down you will see lines in blue text such as:

[//]: # (some words here which are invisible)

These lines have been 'commented' out of the file

They are still 'there' but are not displayed on http://README.md when viewing it

... but they are there

## GITHUB - CHALLENGE REPO

We can all collaborate (if you have a Github account) 

and all the data and code I find during this challenge will be archived there for easy navigation 

and no more posting lists over many posts here...

Licensed CC0
http://creativecommons.org/public-domain/cc0

"that's a lot of text/code ... hard to read... ohhh no"

well part of the process is OSINT and OSINT takes time

Lucky for you kitty you are following me down this rabbit hole and I have made a place for you to play

Check out this repo:
https://github.com/niclaz/zengo-wallet-challenge

/zengo-wallet-challenge/OSINT/Github/gotham-city

You will find:

(hidden) http://README.md
(uncommented) http://README.md
gotham-city-demo.gif

> hidden is the just the text that was commented out
> uncommented is with the commented back in
> .gif is a copy

Going back to http://README.md with the commented code on /zengo/gotham-city

so we know some text was added and then later commented out - what else can we learn? 

Well remember when I briefly introduced 'git' ?

'version control system'

so using this system we can go to this url:
https://github.com/ZenGo-X/gotham-city/commits/master/README.md

... or clicking on 'History' when viewing a file

here you an see all the history (versions) of the file

first 'commit' was on Dec 12, 2018 and we can view all changes since...

ooking through them, regular changes till Jan 19, 2021

... then nothing till 6 months ago when a commit changes a bunch of the content and 'project status' from work in progress to 'use at your own risk'

Launch?

> what got deleted? 
Check my repo linked above
>
> GITHUB - OSINT

Final posts about OSINT - you could do on a code repository from the main viewing page on Github

- Watch / Fork / Stars : the more the better

- About: text

- tags: what the author thinks it is about

- Activity: overview of all file changes in repo

- Releases: important if you want to find the installers / packages / files to run a program. 

- Packages: similar to releases, depends if owners use it

- Contributors: Github profiles that committed code to repo (not necessarily employees)

- Languages: code used

Awesome - Github has a lot of data !

Yes... and there is more:

Issues - user submitted questions and requests
Pull requests (PR) - code changes proposed by people
Projects (also Wiki sometimes) - documentation

Also more to discover on 'branches' and tags

not today kitty
