# surfpool

> Where you train before surfing Solana

<div align="center">
  <picture>
    <source srcset="https://raw.githubusercontent.com/txtx/surfpool/main/docs/assets/surfpool.png">
    <img alt="surfpool" style="max-width: 60%;">
  </picture>
</div>

`surfpool` is to solana what `anvil` is to ethereum: a blazing fast in-memory testnet that has the ability to point-fork Solana mainnet instantly.

## Specs


### Design

Instead of using  a full Solana test validator `solana-test-validator`, `surfpool` uses the low level `solana-svm` API through the excellent wrapper [LiteSVM](https://github.com/LiteSVM/litesvm).
This approach provides greater flexibility and significantly faster boot times.

`surfpool` is also available as a library on crates.io - facilitating its integration in other projects.

### Command line

```console
$ surfpool start
```

### Configurable

- [ ] Ability to pull configuration from a `Surfpool.toml` manifest file
- [ ] Ability to setup slot time (default to `400ms`)
- [ ] Ability to setup epoch duration (default to `432,000`)
- [ ] Ability to configure behavior:
    - [ ] genesis
    - [ ] point-fork mainnet
    - [ ] stream-fork mainnet
- [ ] Ability to configure the RPC node URL to default to.

### RPC Support

- [ ] Support `HTTP Methods`
    - Priority 1:
        - [x] getVersion
        - [x] getSlot
        - [x] getEpochInfo
        - [x] getLatestBlockhash
        - [x] sendTransaction
        - [ ] getAccountInfo
        - [ ] requestAirdrop
        - [ ] getMultipleAccounts
        - [ ] getFeeForMessage
        - [ ] getBalance
        - [ ] simulateTransaction
        - [ ] getTransaction
    - Priority 2:
        - [ ] getBlock
        - [ ] getBlockCommitment
        - [ ] getBlockHeight
        - [ ] getBlockProduction
        - [ ] getBlocks
        - [ ] getBlocksWithLimit
        - [ ] getBlockTime
        - [ ] getClusterNodes
        - [ ] getEpochSchedule
        - [ ] getFirstAvailableBlock
        - [ ] getGenesisHash
        - [x] getHealth
        - [ ] getHighestSnapshotSlot
        - [ ] getIdentity
        - [ ] getInflationGovernor
        - [ ] getInflationRate
        - [ ] getInflationReward
        - [ ] getLargestAccounts
        - [ ] getLeaderSchedule
        - [ ] getMaxRetransmitSlot
        - [ ] getMaxShredInsertSlot
        - [ ] getMinimumBalanceForRentExemption
        - [ ] getProgramAccounts
        - [ ] getRecentPerformanceSamples
        - [ ] getRecentPrioritizationFees
        - [ ] getSignaturesForAddress
        - [ ] getSignatureStatuses
        - [ ] getSlotLeader
        - [ ] getSlotLeaders
        - [ ] getStakeMinimumDelegation
        - [ ] getSupply
        - [ ] getTokenAccountBalance
        - [ ] getTokenAccountsByDelegate
        - [ ] getTokenAccountsByOwner
        - [ ] getTokenLargestAccounts
        - [ ] getTokenSupply
        - [ ] getTransactionCount
        - [ ] getVoteAccounts
        - [ ] isBlockhashValid
        - [ ] minimumLedgerSlot
- [ ] Support `Websocket Methods`

### Going Further
- [ ] Ability to watch and update fetched account
