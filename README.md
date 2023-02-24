# zombienet

## [Sequester Grant 1](https://docs.google.com/document/d/1hfmXwe6Gli92YKr5J6BCffGWU9EmKUF-FkSbLs2w-OQ/edit#heading=h.v6is2ta0txr1)

### Milestone 1: Local XCM Transfer

To test the completion of the 1st Milestone and view local XCM transfer, you can run via zombienet.

Check out the 1st-milestone-11-22-22 release of [sequester-parachain-template](https://github.com/SequesterChain/sequester-parachain-template), [pallets/donations](https://github.com/SequesterChain/pallets), and [sequester-rococo](https://github.com/SequesterChain/sequester-rococo) in the SequesterChain repo.

Then, [install Zombienet](https://substrate.stackexchange.com/questions/4692/how-do-i-spin-up-a-testnet-with-zombienet) and run your platform equivalent of:

```
./zombienet-macos spawn milestone_1_config.toml -p native
```

Once you make enough transfers on the sequester-parachain-template chain (5-6+), the sequester-parachain-template will send an XCM containing the collected transaction fees to the sequester-rococo parachain.

### Milestone 2: Transfer on Rococo

We have enabled the functionality of sending tokens from one chain to another with different tokens on their chain. To complete the reserve-backed transfer using the donations pallet, you must first register the token from the sequester parachain template on the sequester rococo chain. This can be done with the following extrinsic:

0x1f0201010100a50f0100010100d43593c715fdd31c61141abd04a99fd6822c8558854ccde39a5684e7a56da27d010400010100a10f000700e876481700000000

You can then send transactions on the alternative chain implementing the donations pallet, which will deposit the reserve-backed transfer onto the rococo chain.
