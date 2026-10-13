# clone-lin-gmx-v2-borrow-fps

Experimental LIN clone of GMX V2 `getBorrowingFactorPerSecond` (uint64-scale, FLOAT' = 1e6).

- **Upstream:** [gmx-io/gmx-synthetics](https://github.com/gmx-io/gmx-synthetics) `contracts/market/MarketUtils.sol` commit `a85ea3491c19c93bb4b5a002d9b358fb769b7849` (GPL-2.0-or-later after BUSL Change Date 2026-08-31).
- **LIN kernel:** [`src/lin_gmx_v2_borrow_fps.lin`](src/lin_gmx_v2_borrow_fps.lin)
- **Proofs (lin-open only):** [kbelludoo/lin-open](https://github.com/kbelludoo/lin-open) `examples/gmx_v2_borrow_fps/` and `python3 test/prove_gmx_v2_borrow_fps_external.py`
- **Class:** EXPERIMENTAL. Not Arbitrum GMX V2 uint256 / FLOAT=1e30. Not a production replacement.

Named goldens (uint64-scale): linear fps **10**; skip-smaller long **0** / short **10** / equal **10**; kink below **8** vs linear **20**; kink above **64** vs applyFactor extra **40**; rfactor **100** vs ignore **10**; V2 delta **36000** vs applyFactor **0** vs V1 interval **10**; 128-bit wrap **14000000000000** vs naive i64 **-4446744073709**.
