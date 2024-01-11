[Build Status SVG](https://travis-ci.org/KZen-networks/gotham-city.svg?branch=master)

[Build Status](https://travis-ci.org/KZen-networks/gotham-city)

...

### Server

...

List of supported Coin&#40;s&#41;:


 * BTC


**Extending the client to support more coin&#40;s&#41; is easy as long as the Elliptic Curve and signing scheme of the new blockchain are supported. In the case a blockchain is using secp256k1 together with ECDSA, the same keygen and signing code can be reused.**


|[OSINT/Github/gotham-city/gotham-city-demo.gif]|
|-----------------------------|


| Elements                                       | Gotham Server                                | Gotham Client                            |
| -------------------------------------------- | -------------------------------------------- |--------------------------------------------|
| Description | RESTful web service exposing APIs for two party ECDSA key generation and signing | Bitcoin minimalist decentralized wallet CLI app |
| Instructions | [View]&#40;gotham-server/README.md&#41; | [View]&#40;gotham-client/README.md&#41; |


...

### Project Description

...

### White paper overview
#### Abstract

We demonstrate a Bitcoin wallet that utilizes two party ECDSA &#40;2P-ECDSA&#41;. Our architecture relies on a simple client-server communication model. We show support for 2 party deterministic child derivation &#40;2P-HD&#41;, secret share rotation and verifiable recovery. We discuss the opportunities and challenges of using a multi-party wallet.

#### Background

For end-users, cryptocurrencies and blockchain-based assets are hard to store and manage. One of the reasons is the tradeoff between security and availability. Storing private keys safely requires dedicated hardware or extreme security measures which make using the coins) on a daily basis difficult. Threshold cryptography provides ways to distribute the private key and digital signing. This can potentially benefit security but at the same time reveal new challenges such as availability, ownership and recovery. Bitcoin is utilizing ECDSA as the signing scheme. There is an active line of research for practical and efficient multi-party ECDSA schemes.)

...


### Comperative Performance

The comparison was done on an Intel i9-8950HK &#40;2.9GHz&#41; using localhost for server &#40;no real network&#41;. The numbers are mean for 20 runs of 2P-ECDSA KeyGen and 50 runs for 2P-ECDSA Signing. Standard deviation is inconsistent but for both implementations it is order of magnitude smaller than mean value.

|        Implementation         |   Gotham city &#40;this repo&#41;    |    [Unbound]&#40;https://github.com/unbound-tech/blockchain-crypto-mpc&#41;       |
|-------------------------------|------------------------|------------------------|
| 2P-ECDSA KeyGen                      |        1.05 s            |      **0.813** s           |
|    2P-ECDSA Signing    |      **0.153** s        |      0.206 s     |

...
