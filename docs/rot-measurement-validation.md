# XCENA RoT measurement validation

The RoT integration temporarily defers measurement validation while measurement
targets and TCB classification policy are defined. The sample configuration marks
the GET_MEASUREMENTS group as COMMON_TEST_ACTION_SKIP. The pinned responder
validator retains successful CHALLENGE and KEY_EXCHANGE tests without requesting
a measurement summary; it defers their TCB/ALL-summary variants.

Other configured groups remain enabled. The current RoT integration produces
1093 passed assertions, zero failed assertions, and an explicitly skipped
measurement group. This profile does not establish measurement/TCB correctness
and does not change responder firmware or capability advertisement.

To restore full coverage, update the validator to restore its two summary test
variants, enable the measurement group here, and revalidate the RoT runner's exact
expected assertion count. See SPDM-Responder-Validator/docs/deferred-measurement-validation.md.
