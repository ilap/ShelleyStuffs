# Diagrams

Click on the selected diagram to open it in [Draw.io](https://draw.io)


__Disclaimer__: These diagrams are not accurate, even they can be completely wrong, as Cardano Shelley's been under continuous and still ongoing development and/or I misunerstood the specs.


> Found some other Shelley related diagrams here:
https://github.com/deshawes/shelley-mud-maps/

## Min UTxO ADA calculation
[![ShelleyTransaction](https://github.com/ilap/ShelleyStuffs/blob/master/images/minUTXO.drawio.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FminUTXO.drawio)

### References
- [Alonzo UTxO Rules](https://github.com/input-output-hk/cardano-ledger-specs/blob/3d6edf3981a0f1b762e4dfeaecd7eecb755ea928/alonzo/impl/src/Cardano/Ledger/Alonzo/Rules/Utxo.hs#L100)
- [Min-UtxO](https://github.com/input-output-hk/cardano-ledger-specs/tree/master/doc/explanations/min-utxo.rst)


## Shelley Transaction Changes

__An Other Disclaimer__: This diagram is not accurate at all, so you all are welcome to contribute for correcting my mistakes.


Initial shelley **transaction** contains:
- **transactin body**, which hash is used for public key based witness
- **transaction witness set**, a set of different type of witnesses and
- **transaction metadata**, a placeholder for optional metadata.

The following iterative updates, by Hard Fork Combinator, had been or will be made to switch to the Goguen era:

[![ShelleyTransaction](https://github.com/ilap/ShelleyStuffs/blob/master/images/ShelleyTransactionChanges4Gougen.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FShelleyTransactionChanges4Gougen.drawio)

### References

- [MetaData](https://github.com/input-output-hk/cardano-node/blob/b82e6c780937a8e9570915248c3d825e8211ab3d/doc/reference/tx-metadata.md)
- [Simple Script](https://github.com/input-output-hk/cardano-node/blob/b82e6c780937a8e9570915248c3d825e8211ab3d/doc/reference/simple-scripts.md)
- [Multi Asset](https://github.com/input-output-hk/cardano-node/blob/b82e6c780937a8e9570915248c3d825e8211ab3d/doc/reference/multi-assets.md)
- [Alonzo Ledger Changes](https://hydra.iohk.io/job/Cardano/cardano-ledger-specs/specs.alonzo-ledger/latest/download/1/alonzo-changes.pdf)
- [Plutus Core Report](https://hydra.iohk.io/job/Cardano/plutus/darwin.docs.plutus-report/latest/download-by-type/doc-pdf/plutus)
- [Multi Asset (Gougen) CDDL](https://github.com/input-output-hk/cardano-ledger-specs/blob/master/shelley-ma/shelley-ma-test/cddl-files/shelley-ma.cddl)
- [Shelley CDDL](https://github.com/input-output-hk/cardano-ledger-specs/blob/c4aab5045977ab2bf45a27f5804cfcbe2509fc5e/shelley/chain-and-ledger/shelley-spec-ledger-test/cddl-files/shelley.cddl#L3)
- [Alonzo CDDL](https://github.com/input-output-hk/cardano-ledger-specs/blob/master/alonzo/test/cddl-files/alonzo.cddl)

### Cardano's Ledger Spec Multi-Aset (MA) explanations

- [Policies](https://github.com/input-output-hk/cardano-ledger-specs/tree/master/doc/explanations/policies.rst)
- [Token Bundles](https://github.com/input-output-hk/cardano-ledger-specs/tree/master/doc/explanations/token-bundles.rst)
- [Features](https://github.com/input-output-hk/cardano-ledger-specs/tree/master/doc/explanations/features.rst)
- [FAQ](https://github.com/input-output-hk/cardano-ledger-specs/tree/master/doc/explanations/faq.rst)
- [Glossary](https://github.com/input-output-hk/cardano-ledger-specs/tree/master/doc/explanations/glossary.rst)

### Certificates
#### Operational Certificate

- VKey_ev - operational hot key
- n - Certificate issue nuber (cold counter)
- c0 - start KES Period and
- Cold key Signature
- Cold verification key


#### Pool Certificate
It is based only on pool param structure
``` json
{
    "poolParams": {
        "publicKey": "a3bdfcc9630daa7d1da3c1efaa611bdd1f507e62bde8aca8936a070a",
        "vrf": "53cfce04b70accb948250f2c7b18d07ede4db525464612368f0d34327dafd415",
        "pledge": 250000000000,
        "cost": 340000000,
        "margin": 2.99e-2,
        "rewardAccount": {
            "network": "Testnet",
            "credential": {
                "key hash": "842dd0ee48839c992a9cd5f1a7b34b40a1fa3b12e6743e3adcf07dba"
            }
        },
        "owners": [
            "842dd0ee48839c992a9cd5f1a7b34b40a1fa3b12e6743e3adcf07dba"
        ],
        "relays": [
            {
                "single host name": {
                    "port": 8900,
                    "dnsName": "relays-alonzo.poolunder.com"
                }
            }
        ],
        "metadata": {
            "url": "https://www.poolunder.com/testnet_undr.json",
            "hash": "d808d07705e1e6a478edc6501f134bd9f5c916c6af0c5ca002dbc16ca380e7fa"
        }
    },
    "futurePoolParams": null,
    "retiring": null
}
```

## Shelley Signing Keys

[![SigningKeys](/images/SigningKeyTypes.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FEd25519%20Types.drawio)

References:
- [BIP32-ED25519 Presentation](https://datatracker.ietf.org/meeting/interim-2017-cfrg-01/materials/slides-interim-2017-cfrg-01-sessa-bip32-ed25519/)
- [BIP32-ED25519 Paper](https://drive.google.com/open?id=0ByMtMw2hul0EMFJuNnZORDR2NDA)
- [Key REcovery Attack on BIP32-ED2559](https://forum.w3f.community/t/key-recovery-attack-on-bip32-ed25519)

## Network Communications
[![Network Communications](/images/Shelley_Network_Communications.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FNetwork_Communications.drawio)

## Transitions
[![TrasnitionsDetails](images/Transitions_details.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FTransitions_details.drawio)

> It turned out that the stability window is _3k/f_ instead of _2k_

## Shelley Blocks

A shelley **block** contains:
- **block header**, which contains
    - **block header body** and the
    - **block header body signature** (cold key signature)
- and **block body** which is simply the **transactions** of the block.

Transactions contains
- **transaction body**
- **transaction witness set** and an optional
- **transaction metadata** 

See details in the picture below.

References: 
- [Multi Asset (Gougen) CDDL](https://github.com/input-output-hk/cardano-ledger-specs/blob/master/shelley-ma/shelley-ma-test/cddl-files/shelley-ma.cddl)
- [Shelley CDDL](https://github.com/input-output-hk/cardano-ledger-specs/blob/c4aab5045977ab2bf45a27f5804cfcbe2509fc5e/shelley/chain-and-ledger/shelley-spec-ledger-test/cddl-files/shelley.cddl#L3)
- [Ledger Spec Page 70](https://hydra.iohk.io/job/Cardano/cardano-ledger-specs/shelleyLedgerSpec/latest-finished/download/1)
- [Current implementation](https://github.com/input-output-hk/cardano-ledger-specs/blob/master/shelley/chain-and-ledger/executable-spec/src/Shelley/Spec/Ledger/BlockChain.hs)


[![ShelleyBlock](images/ShelleyBlock.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FShelleyBlock.drawio)

## Shelley Keys and Addresses
[![ShelleyKeyAndAddresses](images/ShelleyKeyAndAddresses.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FWallet_Specification.drawio)

## Shelley Transaction (Simple)
[![TransactionSimple](images/Transaction_simple.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2Fransaction_simple.drawio)

## Cardano Wallet Specification

[![WalletSpecification](images/Wallet_Specification.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FWallet_Specification.drawio)

## HD Wallets 

[![HD Wallets](images/HW_wallets.png)](https://app.diagrams.net/#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Filap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FHW_wallets.drawio)
