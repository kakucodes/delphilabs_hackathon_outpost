# Yieldmos Compounding Outposts

The purpose of this repo is to develop and release a set of asset management/compounding contracts predicated upon the functionality enabled by the CSDK Authz module.

## Protocol Usage

The expected flow should go as such:

1. The user should generate their own set of [compounding preferences](./packages/utils/src/osmosis_comp_prefs.rs) and have them stored wherever they expect to be broadcasting the compounding message (This could be with Yieldmos itself or in the dapp/browser or potentially on the user's own computer for use via the cli).
2. The comp prefs should be given to the outpost in the grants query with the outpost returning a list of the requisite grants that will be needed to fulfilled in order for the outpost be able to later compound for them according to their comp prefs.
3. The user should grant the previously noted Authz grants to the outpost contract's adress.
4. The outpost's compound message can now be called whenever the compounding of rewards should occur.

## Outposts Progress

| Chain ID    | Rewards                | Status                                              |
| ----------- | ---------------------- | --------------------------------------------------- |
| `osmosis-1` | `Osmosis Staking`      | [`in progress`](./contracts/osmosisstake/README.md) |
| `osmosis-1` | `Osmosis LPs`          | `not started`                                       |
| `osmosis-1` | `Mars Redbank Rewards` | `not started`                                       |

Testing and the grants query are still in progress on all fronts. These must be codified before the v1 release.

## Packages

| Package Name                                            | Description                                                   |
| ------------------------------------------------------- | ------------------------------------------------------------- |
| [utils](./packages/utils/README.md)                     | Base utilities for building outposts                          |
| [osmosis-helpers](./packages/osmosis-helpers/README.md) | Helpers for interacting with Osmosis DEX                      |
| red-bank-helpers                                        | Helpers for interacting with Mars Red Bank Outpost on Osmosis |

The companion chain code for the hackathon is available [here](https://github.com/Temporal-Network/temporal)
