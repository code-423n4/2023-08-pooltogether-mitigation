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
- [H-06: More shares can be minted than underlying assets available, rendering Vault.sol undercollateralized as a result](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/190)
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

## Overview of changes

- Twab Controller now checks query timestamps for safety. When requesting a twab, timestamps:
    1. are required to be finalized; i.e. cannot occur during an overwrite period
    2. are aligned to period boundaries.
- Tier adjustment algorithm
    1. The canary tier has been simplified, so that the prize size is adjusted instead of the number of prizes. Now the unified claim count across normal + canary tiers is used to determine the next number of tiers.
- Vault exchange rate
    1. The Vault now assumes shares are 1:1 with underlying assets, unless the vault is undercollateralized. No exchange rate is stored.

## Mitigations to be reviewed

### Branch

[pt-v5-prize-pool](https://github.com/GenerationSoftware/pt-v5-prize-pool)
[pt-v5-twab-controller](https://github.com/GenerationSoftware/pt-v5-twab-controller)
[pt-v5-vault](https://github.com/GenerationSoftware/pt-v5-vault)
[pt-v5-claimer](https://github.com/GenerationSoftware/pt-v5-claimer)

(all PRs have been merged into main)

### Individual PRs

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| [VAULT-PR-13](https://github.com/GenerationSoftware/pt-v5-vault/pull/13) | [H-01](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/443) | The issue turned out not to be the case; the exchange rate is always <= 1 (yield is liquidated). However, comments were added to clarify the behaviour |
| [VAULT-PR-9](https://github.com/GenerationSoftware/pt-v5-vault/pull/9) | [H-02](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/439) | Added SafeCast |
| [VAULT-PR-6](https://github.com/GenerationSoftware/pt-v5-vault/pull/6) | [H-03](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/427) | Fixed conversion and naming of field |
| [VAULT-PR-7](https://github.com/GenerationSoftware/pt-v5-vault/pull/7)| [H-04](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/396) | Removed recipient param |
| [VAULT-PR-19](https://github.com/GenerationSoftware/pt-v5-vault/pull/19) | [H-05](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/351) | Removed recipient param |
| [VAULT-PR-13](https://github.com/GenerationSoftware/pt-v5-vault/pull/13) | [H-06](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/190) | Fixed check for partial collateralization |
| [TWAB-PR-7](https://github.com/GenerationSoftware/pt-v5-twab-controller/pull/7) | [H-07](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/206) | Added check for zero address |
| [PRIZE-PR-18](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/18) | [H-08](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/147) | Fixed reserve accounting |
| [VAULT-PR-27](https://github.com/GenerationSoftware/pt-v5-vault/pull/27) | [H-09](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/79) | Fixed undercollateralized redemption while providing an exit |
| [VAULT-PR-21](https://github.com/GenerationSoftware/pt-v5-vault/pull/21) | [M-01](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/465) | Added hook gas limits and error handling |
| [TWAB-PR-5](https://github.com/GenerationSoftware/pt-v5-twab-controller/pull/5) | [M-02](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/464) | Ensure search timestamps are on or at period end timestamps |
| [VAULT-PR-11](https://github.com/GenerationSoftware/pt-v5-vault/pull/11) | [M-03](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/458) | Fixed 4626 compliance |
| [TWAB-PR-6](https://github.com/GenerationSoftware/pt-v5-twab-controller/pull/6) | [M-04](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/452) | Reject transfers to the sponsorship address |
| [PRIZE-PR-31](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/31) | [M-05](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/431) | Record deployer and permission draw manager |
| [VAULT-PR-25](https://github.com/GenerationSoftware/pt-v5-vault/pull/25) | [M-06](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/416) | Used CREATE2 for VaultFactory |
| [CLAIMER-PR-7](https://github.com/GenerationSoftware/pt-v5-claimer/pull/7) | [M-07](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/415) | Made max fee a function of the tier's prize size, not the smallest prize size |
| [PRIZE-PR-16](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/16) | [M-08](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/399) | Improved handling of prize size overflow |
| [PRIZE-COMMIT-ba56ea8b](https://github.com/GenerationSoftware/pt-v5-prize-pool/commit/ba56ea8bac3bce06f1e08ae071a19954dd720b1f) | [M-09](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/395) | Upgrade PRBMath to v4 and Solidity to 0.8.19 |
| [VAULT-PR-15](https://github.com/GenerationSoftware/pt-v5-vault/pull/15) | [M-10](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/384) | Removed `mintWithPermit` |
| [PRIZE-PR-24](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/24) | [M-11](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/352) | Recomputed Tier odds, reduced number of tiers, made grand prize period draws configurable |
| [TWAB-PR-5](https://github.com/GenerationSoftware/pt-v5-twab-controller/pull/5) | [M-12](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/334) | Aligned twab queries on period boundaries |
| [PRIZE-PR-17](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/17) | [M-13](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/332) | Superseceded by the simplification of tier expansion logic |
| [PRIZE-PR-17](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/17) | [M-14](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/331) | Improved tier shrinking, retention, and expansion logic |
| [PRIZE-PR-17](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/17) | [M-15](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/314) | Simplified tier expansion logic |
| [VAULT-PR-27](https://github.com/GenerationSoftware/pt-v5-vault/pull/27) | [M-17](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/256) | Redeemed underlying liquidity using shares, not assets directly. This socializes losses, if any. |
| [PRIZE-PR-22](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/22) | [M-19](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/243) | Added SafeCast |
| [VAULT-PR-17](https://github.com/GenerationSoftware/pt-v5-vault/pull/18) | [M-20](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/180) | Vault shares are now 1:1 with underlying asset, and the exchange logic has been simplified |
| [PRIZE-PR-10](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/10) | [M-21](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/150) | Draw query ends on closed draw |
| [VAULT-PR-18](https://github.com/GenerationSoftware/pt-v5-vault/pull/18) | [M-22](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/143) | Improved vault share / asset calculation |
| [VAULT-PR-11](https://github.com/GenerationSoftware/pt-v5-vault/pull/11) | [M-23](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/129) | Fixed compliance with 4626 |
| [CLAIMER-PR-8](https://github.com/GenerationSoftware/pt-v5-claimer/pull/8) [VAULT-PR-22](https://github.com/GenerationSoftware/pt-v5-vault/pull/22) [PRIZE-PR-23](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/23) | [M-24](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/115) | Added minVrgdaFee and allowed silent failure of claims |
| [VAULT-PR-20](https://github.com/GenerationSoftware/pt-v5-vault/pull/20) | [M-25](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/113) | Fixed permit implementations |
| [VAULT-PR-9](https://github.com/GenerationSoftware/pt-v5-vault/pull/9) | [M-26](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/91) | Added SafeCast |
| [PRIZE-PR-17](https://github.com/GenerationSoftware/pt-v5-prize-pool/pull/17) | [M-27](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/61) | Unified standard and canary tier |

## Out of Scope

| Issue | Reason |
| ----- | ------ |
| [M-16](https://github.com/code-423n4/2023-07-pooltogether-findings/issues/300) | Permissionless nature of vaults means that anyone can create custom vaults. |
