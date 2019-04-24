WinPlay.io Fairness Verification
---

## WinPlay Reveal Steps

* Use the first EOS Block Hash starting every minute as seed, and sign with an pair of long term unchanged unchanged EOS private and public keys
* Perform sha256 hash on the signature result to get the reveal Hash
* Use the last 5 digits of the reveal Hash as lotto result
* Calc Formula: Reveal HASH = sha256(sign(BlockHash))

## Why Reveal Result Absolute Fairness

* Player CANNOT cheat: Players bet in previous minute, and BlockHash seed is the first block in coming minute.
* EOS BP CANNOT cheat: BP can predict block hash, but cannot predict signature hash, since block hash is NOT the final result, but only a seed.
* WinPlay team CANNOT cheat: Signature EOS public key is long term unchanged and pre-known by everybody, and the public key matches the one and the only private key. The most important point is WinPlay team cannot predict block hash which is controlled by BP nodes.

## Fairness Verification How-to

Take the reveal result as an example:

![Result](result.png)

Block Hash: 
`0340c044dc6743e9185686416de09b7f25df32b2787293c216ce988a5435d42e`

Signature of Block Hash:
`SIG_K1_KWQfPUoo13tPpbwxMQgv174H3Tt3euWSQ2YTAV2xzTqewHtFbuSVmbWM3z795riHWt3873ZDu6L3VktRgyc2jEyouNw4vM`

Signature Public Key (Long term unchanged):
`EOS6J5ePXXH4vgfA1XT72qBsKKeH7tJEW3ed7d1Hmwo1BqgeSWZfV`

### Signature of Block Hash Verification

Open a 3rd party EOS key tool: [https://bachvtuan.github.io/eos-key-tools/](https://bachvtuan.github.io/eos-key-tools/)

![Verify Signature](verify-sign.png)

### Reveal Hash Verification

Open a 3rd party sha 256 hash tool: [https://emn178.github.io/online-tools/sha256.html](https://emn178.github.io/online-tools/sha256.html)

![Verify sha256](verify-sha256.png)
