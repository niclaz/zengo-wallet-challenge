# Observations from reviewing commit history of /gotham-city

Version: Alpha to 0.10

Start of gotham-city/gotham-client code
https://github.com/ZenGo-X/gotham-city/commit/c76e62a9304759ec7799b552703a1878807726e9

Implementation of ecdsa signing in /gotham-server
https://github.com/ZenGo-X/gotham-city/commit/c76e62a9304759ec7799b552703a1878807726e9

wallet.data added in /gotham-client code (incl keygen.rs)
https://github.com/ZenGo-X/gotham-city/commit/995f77cf28b56770186b3dc0ab0d9677f2573a86

Added Bitcoin to the system
https://github.com/ZenGo-X/gotham-city/commit/60af19830233751d4fdf297f1615beacfed04d52

Added electrumx_client
https://github.com/ZenGo-X/gotham-city/commit/60af19830233751d4fdf297f1615beacfed04d52

electrumx / wallet 'GetBalance'
https://github.com/ZenGo-X/gotham-city/commit/90481228189b83ecfcadfa4854fe7a11ccaa3136

/gotham-client backup escrow function + sample backup with pk and sk 
https://github.com/ZenGo-X/gotham-city/commit/238bf102bbfb0dea17f6d0a02ad299faa56c462e

more advanced Bitcoin actions
https://github.com/ZenGo-X/gotham-city/commit/d61c28bef081f1b5e64bad1542782cbaa72c6564

/gotham-client gets a full README.md + cli.yml script
several changes from println! functions > where are they stored???
/src/mod.rs >> interesting code change:

> println!("(wallet id: {}) Backup wallet with escrow", self.id);

> debug!("(wallet id: {}) Backup wallet with escrow", self.id);

https://github.com/ZenGo-X/gotham-city/commit/0e54d01bf4aa3b2b6be104c0edfbfa0f4033ca72

bitcoin sign_hast transactaction and signature code added + cfg test scripts
https://github.com/ZenGo-X/gotham-city/commit/2c4abb941a8281492978c059a5f9ad2249e7002d

deleted a bunch of println! sections
https://github.com/ZenGo-X/gotham-city/commit/f20c2fa056444317e4fa331458d054af3839e9bc

Added centipede dependency + 2 backup categories Private share backup and recovery + big change to client.backup and pk.json and sk.json + pub fn recover_and_save_shares
https://github.com/ZenGo-X/gotham-city/commit/561779911e963fdfa33a7bbf79d18abdf87ed16e

two domains to check up on (ELECTRUM_HOST)
https://github.com/ZenGo-X/gotham-city/commit/7ac7b17ceee4619da5176934ab741c4f40683544

gotham-client/cli.yml > share rotation code
https://github.com/ZenGo-X/gotham-city/commit/826d87b7617503dc1d47a1eade99a9f49755b30e

gotham-client (-e flag taken out of docs... but is it out of the code?)
https://github.com/ZenGo-X/gotham-city/commit/d9b1206afb23cbbb301566fb1cb953c587558ceb
+
https://github.com/ZenGo-X/gotham-city/commit/7b57dd0eee1f667f029194d5b2b8e4ed110f74d0

Escrow edits - crypto and shares + verify recovery code
https://github.com/ZenGo-X/gotham-city/commit/3398e446d9d3038b9124f5df030499c53593f92d

Big changes in gothan-server on signing and keygen
https://github.com/ZenGo-X/gotham-city/commit/23573f129a61751ea307abbfa391a1e1fc3e4ff0

gotham-utilities/server/buildspec.yml code - interesting specifications for server creation script
https://github.com/ZenGo-X/gotham-city/commit/6180fcdca1dfdc41b1589aedb4df94ba4d44134e

gotham-client/wallet/backup.data deleted
https://github.com/ZenGo-X/gotham-city/commit/1e54477398de0cc05c9d90e98006f409584d3a02

gotham-client/src/api/mod.rs - API rust code added  
+ fn sign code deleted
+ gotham-server/src/auth/cognito.rs code added 
+ gotham-server/src/auth/jwt.rs code added
+ gotham-server/src/auth/mod.rs
+ gotham-server/src/auth/passthrough.rs
+ gotham-server/src/storage/aws/dynamodb.rs
+ gotham-server/src/storage/aws/error.rs
+ gotham-server/src/storage/aws/mod.rs
+ gotham-server/src/storage/db.rs
+ gotham-utilities/server/cognito/jwt-to-pems.js
+ gotham-utilities/server/cognito/package-lock.json
+ gotham-utilities/server/cognito/package.json
+ cryptography changes
https://github.com/ZenGo-X/gotham-city/commit/2f26ea7ccc70b6c729ff7e57961b515129e46a60

rotation_party_one_second_message changed to alpha (term for first handshake)
https://github.com/ZenGo-X/gotham-city/commit/8ef41e825ee19bb29750da06fc105ebb4c21f4e9

More Alpha and BigInt (big integer for numbers)
https://github.com/ZenGo-X/gotham-city/commit/16996e95692214e80de7dba75776a1e0da36f196
