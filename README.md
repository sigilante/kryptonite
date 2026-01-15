# Kryptonite

_An experiment in Bitcoin on Nock ISA-based systems._

![](./img/hero.png)

Kryptonite aggregates and updates Bitcoin libraries for use on Nock ISA-based systems, such as [Urbit](https://github.com/urbit/urbit) and [NockApp](https://github.com/nockchain/nockchain).

Structure:

```
.
├── crate/
│   ├── btc-driver/      # Crypto driver (secp256k1 signing, etc.)
│   ├── btc-nockapp/     # NockApp kernel binary
│   └── jets/            # Jet implementations (if custom beyond driver)
├── hoon/
│   ├── app/
│   │   ├── gall/        # %btc-light Gall agent
│   │   └── nockapp/     # NockApp kernel entry
│   ├── lib/
│   │   ├── btc.hoon
│   │   ├── btc-addr.hoon
│   │   └── bip/
│   │       ├── b32.hoon
│   │       ├── b39.hoon
│   │       ├── b84.hoon
│   │       └── b174.hoon
│   ├── sur/
│   │   ├── btc.hoon
│   │   └── btc-wallet.hoon
│   ├── ted/             # Test threads (Urbit convention)
│   │   ├── test-b32.hoon
│   │   ├── test-b39.hoon
│   │   ├── test-bech32.hoon
│   │   └── test-psbt.hoon
│   └── gen/             # Generators (useful for manual testing)
├── test-data/           # Test vectors (JSON, consumable by both)
│   ├── bip32.json
│   ├── bip39.json
│   ├── bech32.json
│   └── psbt.json
└── vere/
```