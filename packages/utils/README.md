### Yieldmos Outpost Utils

This is a set of general utility functions to be used by the actual outpost contracts

Please note that this is still a pre-release version and breaking changes are expected to be frequent

## Example Compounding Prefs

```json
{
  "msg": {
    "compound": {
      "comp_prefs": {
        "relative": [
          {
            "destination": {
              "token_swap": {
                "target_denom": "uusdc"
              }
            },
            "amount": "250000000000000000"
          },
          {
            "destination": {
              "osmosis_staking": {
                "validator_address": "osmovaloper12345"
              }
            },
            "amount": "250000000000000000"
          },
          {
            "destination": {
              "red_bank_deposit": {
                "target_denom": "uatom"
              }
            },
            "amount": "250000000000000000"
          },
          {
            "destination": {
              "red_bank_lever_loop": {
                "denom": "uosmo"
              }
            },
            "amount": "250000000000000000"
          }
        ]
      },
      "delegator_address": "juno14r9pzdtdza6ma9cs2mznqrc4zqjwflsj3dl5tl"
    }
  },
  "funds": []
}
```
