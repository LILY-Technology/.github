## What this does

<!-- One or two sentences. Why it exists, not only what changed. -->

Closes #

## Changes

-
-

## How it was verified

<!--
Not "it should work". What did you run, and what did it say?
For a new behaviour: say that the test FAILS without this change — a test that
passes either way proves nothing.
-->

- [ ] tests pass locally
- [ ] lint passes
- [ ] a new test covers the new behaviour, and fails without it

## Does it touch money, authentication, or customer data?

<!--
Money = payments, wallet, ledger, payouts, commission, pricing, refunds.
If yes: say which figure moves, and what asserts it still agrees with the
existing payout calculation.
-->

- [ ] No
- [ ] Yes — explained above

## Deployment notes

<!--
New env var? A migration? An order these must go in?
On repos with deploy-on-push, merging IS deploying — say if anything must be
set BEFORE the merge.
-->

## Checklist

- [ ] no secret, key, keystore, service-account JSON or `.env` in the diff
- [ ] no commented-out or dead code left behind
- [ ] user-facing strings are in the right language
- [ ] `CLAUDE.md` / docs updated if this changes a rule somebody could trip over
