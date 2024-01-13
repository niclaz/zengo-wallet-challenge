# Observations from commit history review of gotham-city from version v 1.0.0 release (new gotham)

After v 0.1.4 in May 13 2021 for almost 2 years no code updates until release of 1.0.0

## v 1.0.0 (Jul 31 2023)

https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-95671e3645aa6c715c8d394b29949dc8e365de22149662ad612cbc2fa8c380b8

## /gotham-city

building out a config for circleci (.circleci/config.yml) and preparing release
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-78a8a19706dbd2a4425dd72bdab0502ed7a2cef16365ab7030a5a0588927bf47

Creation of cargo.toml for all of /gotham-city
With 3 workspace members and the workspace dependencies for Rust
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-2e9d962a08321605940b5a657135052fbcef87b5e360662bb527c96d9a615542

Change of software license from GPL 3.0 to Copyright by ZenGo Ltd.
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-2e9d962a08321605940b5a657135052fbcef87b5e360662bb527c96d9a615542

Adding electrum-address to /gotham-client/cli.yml
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-1bfae3a3b37c410356e26fe96bcfc47cbf86502cd89b39cc866458cb7a21fdc3

Created a bunch of Docker related files for deployment on there
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-af002f846119457004eaa9af400be1ffe29f893095897d197d26001f260121bd

Changes in gotham-client/src/ecdsa/keygen.rs (no more multi-party-ecdsa + Android related bindings + 'CString::new(private_share_json).unwrap().into_raw()'
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-d1865bbb070249fb137de04a3711383cb3d12537e60fd521d6ec628cfae1596f

Changes to ecdsa crypto - rotate function removed + recover.rs changes +
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-1919e06bd3113f4e3543beabf537026963d9a9b18599c4750fcac96529800ef8

Changes to signing process in gotham-client/src/ecdsa/sign.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-9dd4744708afdc9939b2299a72bdc98fa9ca8f5340ed50850bbb8b7d1a9dbebe

Deletion of EDDSA code (abandoing use?) in gotham-client/src/eddsa/keygen.rs + gotham-client/src/eddsa/mod.rs + gotham-client/src/eddsa/sign.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-9dd4744708afdc9939b2299a72bdc98fa9ca8f5340ed50850bbb8b7d1a9dbebe

Edits to gotham-client/src/lib.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-97765514fc8eba2203b64cfe56a53b08d82e0dc064f582ba8ec32a0b7a9fa11b

Deletion of lots of /gotham-client code in gotham-client/src/main.rs + gotham-client/src/schnorr/mod.rs + gotham-client/src/tests.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-502de56f9d62fa96cdad3e75d1e9e95f4e0949bcc684d2ea23503c562aa12bab

Lots of changes to gotham-client/src/wallet/mod.rs (INVESTIGATE)
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-bd02f85559c73570ec10fbd15a4f2d49ccd53b8a0b6fda749904c5ed913edb04  

## /gotham-city/gotham-server

Changes to gotham-server/Cargo.toml - updating dependencies and crates of use in workspace 
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-95671e3645aa6c715c8d394b29949dc8e365de22149662ad612cbc2fa8c380b8

Added almost 3000 lines of code about Rust dependencies in gotham-server/Cargo.lock
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-2680ca50f95f7e7f370cac7c2c6f03ec11c8f98c0c87ad2e3a16118b440d10e8

Changes to authentication process and error returns of code in gotham-server/src/auth/cognito.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-18510c3eef6684cd6aca5796d5df38c3166626e5381442faa95c733c0a97f445

jwt replaced by jsonwebtoken code gotham-server/src/auth/jwt.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-f84305991a27a0b4fe4d4b2c5570ee419b426ba7d99aed98043e365f27d5169a

deletion of lots of Rust crates from gotham-server/src/lib.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-4f6df16b3f3121bb2c1eff73d12e9dc9b9ae91f9a27139654f924a7368752f42

Additional conditions to server startup in gotham-server/src/main.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-604734e2e9c18a58c8049837225fbc9f6f0594e0db92663e85496db87e58b5ac

Changes to ecdsa routes
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-53c451037d560804cc7de9d04fe4d735478ddc283e0a5a0acf54449fdc62a428

changes to eddsa routes
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-b6df61f72831394d72d39987df89e1142e6cc63bd5143722e8616e33054c685a

Deletion of schnorr as a route option in gotham-server/src/routes/mod.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-d6bb649dde9f8c4ac83d2c4ed6ab88bc9abf2ebaf30abdcc9369df4c3934f0eb

Deletion of all of schnorr code in gotham-server/src/routes/schnorr.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-c4c4b93a595d8a7dadf16ca92b2704644f0657e7a9d2f3d14772ecb9bfbee507

More route changes upstream in gotham-server/src/server.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-af5c89ab03128c4ec906386c1741ee9b970cd79d5ef14052f90756abf8822082

Changes to gotham-server/src/storage/aws/dynamodb.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-922dd5eb42cb970855b43575f0c736995de01de01b45e0cf7a71b4c68bdeb203

Deletion of gotham-server/src/storage/aws/error.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-60532011a328c65bcb1577d66cdac99829116a9e1f137e21f24506094c4dcec0

Changes to gotham-server/src/storage/db.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-fb5ba30ae9724f780e857c9eb4c4322dff812c314beebb27f8e56be15e507bfa

Updating of test scripts from integration-tests/src/test.rs to integration-tests/tests/ecdsa.rs
https://github.com/ZenGo-X/gotham-city/commit/07d1ca18d5b80346b8621c4980fbe86f88ca4544#diff-6110a5386b91d037255fd34bde990f401f5e98f1dd208fdb03f37c47d6af545f

## updating README.md for v 1.0.0 (Aug 2 2023)
https://github.com/ZenGo-X/gotham-city/commit/81f246369bae511cdd26d87c8c51d04334e241f2

Main README.md
https://github.com/ZenGo-X/gotham-city/commit/81f246369bae511cdd26d87c8c51d04334e241f2#diff-b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5

/gotham-client/README.md
https://github.com/ZenGo-X/gotham-city/commit/81f246369bae511cdd26d87c8c51d04334e241f2#diff-d14214146fdf865784e8660bb80c78439b95e947c09d882008069ee62c49fcc5

Things noted:
+ Gotham server is a ECDSA agnostic signing machine
+ Deletion of lots of libraries used and adding [two-party-ecdsa](https://github.com/KZen-networks/two-party-ecdsa) a Rust implelemtation of Lindell's Crypto17 paper: [Fast Secure Two-Party ECDSA Signing](https://eprint.iacr.org/2017/552)
+ Changing of license from GPL 3.0 to Copyright
+ Commenting out the code found in research for OSINT - search (uncommented)README.md in this repository

## Cleaning up the code (INVESTIGATE)
https://github.com/ZenGo-X/gotham-city/commit/dbcff83c3628d98f2517da34ebad1c61499c532e

.circleci/config.yml
gotham-utilities/server/buildspec.yml
gotham-utilities/server/cognito/.gitignore
gotham-utilities/server/cognito/jwt-to-pems.js
gotham-utilities/server/cognito/package-lock.json
gotham-utilities/server/cognito/package.json
gotham-utilities/server/docker-build-img/Dockerfile
iclient.sh

## more cleaning (INVESTIGATE)
https://github.com/ZenGo-X/gotham-city/commit/c76974634abbddc2acb72049ab93a0028767d24d

gotham-client/docker_images/android/Dockerfile
gotham-client/docker_images/android/build_and_extract.sh
gotham-client/docker_images/ios/build_ios.sh
gotham-client/escrow/.gitkeep
gotham-client/escrow/git.keep

## demo-wallet added (Sept 26 2023)
https://github.com/ZenGo-X/gotham-city/commit/1b785a9dc55bd075dc9030f60ac373ddc41d5712

Full deletion of gotham-client/cli.yml
https://github.com/ZenGo-X/gotham-city/commit/1b785a9dc55bd075dc9030f60ac373ddc41d5712#diff-1bfae3a3b37c410356e26fe96bcfc47cbf86502cd89b39cc866458cb7a21fdc3

## Commit to bringing wallet to version 1.2.0
https://github.com/ZenGo-X/gotham-city/commit/0f057f45134a39eeb617403806c19cf0b77bc46a

Very few changes from version 1.1.0
