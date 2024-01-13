# Observations from commit history review of gotham-city from version 0.1.0 to 0.1.1 release

from Oct 27 2019 to Aug 10 2023 (code base remained pretty dormant between May 2021 to March 2023)

## v 0.1.0 - 0.1.2 (Oct 27 2019)
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c

### /gotham-city/gotham-client

/gotham-client/cargo.toml
Added Oded Leiba as a dev

Full deletion of gotham-client/src/api/mod.rs
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-6de529a72286321f5ea1b5c80ea0436e9ac039d2a00095c6cca4badf44cc05d6

Added a bunch of code to gotham-client/src/ecdsa/mod.rs + gotham-client/src/ecdsa/keygen.rs
(maybe replaces function of mod.rs that was deleted before or it might be used in /gotham-server)

Created a new file gotham-client/src/ecdsa/recover.rs

Created a new file gotham-client/src/ecdsa/types.rs

### Added EDDSA to code

Created a new file gotham-client/src/eddsa/keygen.rs

Created a new file gotham-client/src/eddsa/mod.rs

Created a new file gotham-client/src/eddsa/sign.rs

Created a new file gotham-client/src/eddsa/types.rs


### Updated gotham-client/src/lib.rs
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-97765514fc8eba2203b64cfe56a53b08d82e0dc064f582ba8ec32a0b7a9fa11b

### Added schnorr to code

Created new file gotham-client/src/schnorr/mod.rs
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-16cb5f5c00656cc24d51135df54cc3ed5ee880e7461219bb20d6bbfc982e200e


## /gotham-city/gotham-server


gotham-server/Cargo.toml - Updated authors + dependencies + libraries of server code
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-95671e3645aa6c715c8d394b29949dc8e365de22149662ad612cbc2fa8c380b8

ECDSA routes updated - several functions conslidated into 'db::MPCStruct'
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-53c451037d560804cc7de9d04fe4d735478ddc283e0a5a0acf54449fdc62a428

EDDSA routes created (new file)
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-b6df61f72831394d72d39987df89e1142e6cc63bd5143722e8616e33054c685a

Adding EDDSA and Schnorr to gotham-server/src/server.rs
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-af5c89ab03128c4ec906386c1741ee9b970cd79d5ef14052f90756abf8822082

AWS instruction code for Dynamo DB (does the AWS infrastructure handle user requests?)
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-922dd5eb42cb970855b43575f0c736995de01de01b45e0cf7a71b4c68bdeb203

Storage of user data simplified/abstracted (INVESTIGATE)
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-fb5ba30ae9724f780e857c9eb4c4322dff812c314beebb27f8e56be15e507bfa

New test functions added to integration-tests/src/test.rs
https://github.com/ZenGo-X/gotham-city/commit/a77e05fb266686db3bef06a07e04113b806be06c#diff-6110a5386b91d037255fd34bde990f401f5e98f1dd208fdb03f37c47d6af545f

## v 0.1.3 (May 10 2020)
https://github.com/ZenGo-X/gotham-city/commit/05469aabd7b2a127ff2dd8a3e8a6abeee18be198#diff-af5c89ab03128c4ec906386c1741ee9b970cd79d5ef14052f90756abf8822082

In commit message is writte 'alternate Lindell' - cryptography handeling updated

Deletions in gotham-client/src/ecdsa/keygen.rs
https://github.com/ZenGo-X/gotham-city/commit/05469aabd7b2a127ff2dd8a3e8a6abeee18be198#diff-d1865bbb070249fb137de04a3711383cb3d12537e60fd521d6ec628cfae1596f

Deletions in gotham-client/src/ecdsa/rotate.rs
https://github.com/ZenGo-X/gotham-city/commit/05469aabd7b2a127ff2dd8a3e8a6abeee18be198#diff-96813538c1be2740efcbf1ce4fa6719d789e253f448adb4552bea30dcb96eb9c

Deletion in gotham-server/src/routes/ecdsa.rs
https://github.com/ZenGo-X/gotham-city/commit/05469aabd7b2a127ff2dd8a3e8a6abeee18be198#diff-53c451037d560804cc7de9d04fe4d735478ddc283e0a5a0acf54449fdc62a428

Deletion of following from gotham-server/src/server.rs
< ecdsa::third_message, ecdsa::fourth_message, ecdsa::rotate_third, ecdsa::rotate_fourth

https://github.com/ZenGo-X/gotham-city/commit/05469aabd7b2a127ff2dd8a3e8a6abeee18be198#diff-af5c89ab03128c4ec906386c1741ee9b970cd79d5ef14052f90756abf8822082


## v 0.1.4 (May 13 2021)
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

change key rotation - kms / curve / paillier / lindell_2017 in gotham-client/src/ecdsa/rotate.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

Adding curv::elliptic::curves::ed25519::{FE, GE}; & use curv::BigInt; to gotham-client/src/eddsa/keygen.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

Changing curv in gotham-client/src/escrow/mod.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

Similar changes in gotham-client/src/wallet/mod.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

Similar changes in gotham-server/src/routes/ecdsa.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

Similar changes in gotham-server/src/routes/eddsa.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

Interesting deletions of '3rd/4th messages' within gotham-server/src/tests.rs
https://github.com/ZenGo-X/gotham-city/commit/58a6a765dc8c759bbb56288bea1c97f05ad3086e

After these code edits no other activity except for a bot that updates dependencies happened to the /gotham-city public repository between May 13 2021 and Mar 20 2023

### See next commit-observations document
