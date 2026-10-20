# Validation and limits

| Item | Evidence |
|---|---|
| Baseline | Inspected specification v5.8; main source updated 14 August 2026 |
| Source comparison | Main engine, HUD and reporting match the local ATIS 1.0 working copy |
| Completeness | Development copy adds newer strategy-test revision and tracer; working copy supplies launcher |
| Offline command | `python -B -m unittest test_atis_strategy test_atis_reporting` |
| Baseline result | 45 tests passed on 20 October 2026 |
| Scope | Synthetic strategy/HUD tests and temporary SQLite reporting tests |
| Public contents | Documentation and two visually reviewed historical interface images |

An initial test attempt could not create SQLite files in the execution environment's
default temporary directory. Pointing temporary files at the writable workspace
resolved the environment issue; the rerun passed all 45 tests.

No connection diagnostic, historical tracer, live MT5 session or real SMTP send was
run for publication. The public repository includes no executable test suite and
does not claim that reviewers can reproduce the private tests here. Long-running
operation, clean-machine setup, production security and market profitability remain
outside this validation. Screenshots are interface evidence, not financial evidence.
