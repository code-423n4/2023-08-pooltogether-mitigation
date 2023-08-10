# PoolTogether - Mitigation Review details
- Total Prize Pool: $27,150 USDC 
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2023-08-pooltogether-mitigation/submit)
- Starts August 21, 2023 20:00 UTC 
- Ends August 25, 2023 20:00 UTC 

## Important note 

Each warden must submit a mitigation review for *every High and Medium finding* from the parent audit that is listed as in-scope for the mitigation review. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

Mitigations of all High and Medium issues will be considered in-scope and listed here.

- [H-01: The _currentExchangeRate of the Vault contract can't increase, and always be lower than or equal to _assetUnit](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/443)
- [H-02: Malicious user can steal other user's deposits from Vault.sol](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/439)
- [H-03: _amountOut is representing assets and shares at the same time in the liquidate function](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/427)
- [H-04: Vault.mintYieldFee FUNCTION CAN BE CALLED BY ANYONE TO MINT Vault Shares TO ANY RECIPIENT ADDRESS](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/396)
- [H-05: Delegated amounts can be forcefully removed from anyone in the TwabController](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/351)
- [H-06: More shares can be minted than underlying assets available, rendering Vault.sol undercollateralized as a result](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/307)
- [H-07: Resetting delegation will result in user funds being lost forever](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/206)
- [H-08: Increasing reserves breaks PrizePool accounting](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/147)
- [H-09: Vault is not compatible with some erc4626 vaults](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/79)
- [M-01: Unintended or Malicious Use of Prize Winners' Hooks](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/465)
- [M-02: TwabLib::getTwabBetween can return innacurate balances if _startTime and _endTime aren't safely bounded](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/464)
- [M-03: deposit function does not check for the maxMint amount.](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/458)
- [M-04: Balance invariant between individual and total twabs can be broken](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/452)
- [M-05: drawManager CAN BE SET TO A MALICIOUS ADDRESS](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/431)
- [M-06: Attacker can frontrun deployVault to deploy at the same address](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/416)
- [M-07: High Prizes might not be claimed](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/415)
- [M-08: PrizePool -> Winners wouldn't be able to claim prize correctly in claimPrize function](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/399)
- [M-09: PRBMATH pow() function can return inconsistent values which is root of computation for the Area under curvec(d) = −t ∗ ln(α)∗α ^ d *](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/395)
- [M-10: Vault.mintWithPermit() can be DOSed](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/384)
- [M-11: Tier odds in TieredLiquidityDistributor are incorrect](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/352)
- [M-12: Users can manipulate observation creation](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/334)
- [M-13: Number of prize tiers always increases if just 1 canary prize is claimed](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/332)
- [M-14: Tiers can be mantained active to give unfair advantage to user through DoS](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/331)
- [M-15: Threshold check for adding of new tiers is skipped when _nextNumberOfTiers is at the maximum](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/314)
- [M-16: VaultFactory allows deployment of vaults with non-authentic TwabController and PrizePool](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/300)
- [M-17: Exchange Rate Change in Case of Lossy Strategy will cause the Vault to Undercollateralized for generic ERC4626 Yield Vaults](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/256)
- [M-18: In Vault.sol, Math rounding is not ERC4626-complicant: _convertToAssets() should round up and _convertToShares should round down. maxWithdraw and maxRedeem does not completely adhere to EIP-4626](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/250)
- [M-19: Silent overflow could alter computation when calculating the vaultPortion in the PrizePool contract](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/243)
- [M-20: Improper handling of cases when withdrawable assets = 0](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/180)
- [M-21: Vault contribution calculations wrongly include the current round when claiming prizes](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/150)
- [M-22: Loss of precision leads to undercollateralized](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/143)
- [M-23: Vault does not conform to ERC4626](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/129)
- [M-24: Claimer.claimPrizes can be frontrunned in order to make losses for the claim bot](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/115)
- [M-25: depositWithPermit and mintWithPermit are allowed to be called by permit creator only](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/113)
- [M-26: Transfer of Vault tokens can cause accounting errors in other contracts](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/91)
- [M-27: Inconsistent behavior for canary claims in claimer](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/61)


[ ⭐️ SPONSORS ADD INFO HERE ]

## Overview of changes

Please provide context about the mitigations that were applied if applicable and identify any areas of specific concern.

## Mitigations to be reviewed

### Branch
[ ⭐️ SPONSORS ADD A LINK TO THE BRANCH IN YOUR REPO CONTAINING ALL PRS ]

### Individual PRs
[ ⭐️ SPONSORS ADD ALL RELEVANT PRs TO THE TABLE BELOW:]

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/your-repo/sample-contracts/pull/XXX | H-01 | This mitigation does XYZ | 

## Out of Scope

Please list any High and Medium issues that were judged as valid but you have chosen not to fix.
