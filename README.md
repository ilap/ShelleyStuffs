# Diagrams

Click on the selected diagram to open it in [Draw.io](https://draw.io)


__Disclaimer__: These diagrams are not accurate, even they can be completely wrong, as Cardano Shelley's been under continuous and still ongoing development and/or I misunerstood the specs.


> Found some other Shelley related diagrams here:
https://github.com/deshawes/shelley-mud-maps/

## Shelley Signing Keys

[![SigningKeys](/images/SigningKeyTypes.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FEd25519%20Types.drawio)

## Network Communications
[![Network Communications](/images/Shelley_Network_Communications.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FNetwork_Communications.drawio)

## Transitions
[![TrasnitionsDetails](images/Transitions_details.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FTransitions_details.drawio)

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
- [Shelley CDDL](https://github.com/input-output-hk/cardano-ledger-specs/blob/c4aab5045977ab2bf45a27f5804cfcbe2509fc5e/shelley/chain-and-ledger/shelley-spec-ledger-test/cddl-files/shelley.cddl#L3)
- [Ledger Spec Page 70](https://hydra.iohk.io/job/Cardano/cardano-ledger-specs/shelleyLedgerSpec/latest-finished/download/1)
- [Current implementation](https://github.com/input-output-hk/cardano-ledger-specs/blob/master/shelley/chain-and-ledger/executable-spec/src/Shelley/Spec/Ledger/BlockChain.hs)


[![ShelleyBlock](images/ShelleyBlock.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FShelleyBlock.drawio)

## Shelley Keys and Addresses
[![ShelleyKeyAndAddresses](images/ShelleyKeyAndAddresses.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FShelleyKeyAndAddresses.drawio)

## Shelley Transaction (Simple)
[![TransactionSimple](images/Transaction_simple.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FTransaction_simple.drawio)

## CArdano Wallet Specification

[![WalletSpecification](images/Wallet_Specification.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FWallet_Specification.drawio)

## HD Wallets 

[![HD Wallets](images/HW_wallets.png)](https://app.diagrams.net/#Hilap%2FShelleyStuffs%2Fmaster%2Fdiagrams%2FHW_wallets.drawio)
