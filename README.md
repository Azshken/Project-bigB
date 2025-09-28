# Project-bigB
This is a development log.

Bancor protocol had a good idea, bad execution. I lack the skill and experience to develop an AMM from scratch. I'll be buiilding and developing on the basis layed by Bancor.
It'll be slow. I'll learn by practising and understanding the Bancor V3 codebase.

### Main goals and changes:
- Simplify the code as much as possible, reduce overhead (compact and secure).
- Make the protocol sustainable with the least possible long term intervention.
- Make the protocol as decentralized as possible, non-reliant on admin.

#### Changes:
- No whitelisting
- No Governance token
- No migration
- No liquidity protection
    - Instant, simplified withdrawals
    - No withdrawal fee

#### Main benefits:
- Protocol token backed with real token equity
- Surplus revenue shared with LPs (IL mitigation, not protection)
- Stable LP gains
- Protocol token acts as a stablecoin following the ETH price

28/09/2025
- I'm refactoring the IPoolCollection.sol and PoolCollection.sol
- I've changed the withdrawalAmounts as it's tied to the IL protection. Left it in because of UX purposes. It's a view function. 

TO DO:
- DELETE renounceLiquidity -> it's for the admin to remove the surplus BNT token in the pool
- remove isPoolStable -> checks if the BNT in the pool is equal to poolFundingLimit
- minLiquidityForTrading - is it necessary?
