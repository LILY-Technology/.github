# Contributing

## Branches

`main` is the only long-lived branch. Everything else is short-lived and named
for what it is:

```
feature/<short-name>     a new capability
fix/<short-name>         a defect
hotfix/<short-name>      a defect that is hurting production right now
chore/<short-name>       dependencies, tooling, release mechanics
docs/<short-name>        documentation only
```

Never commit to `main` directly. On the production repositories the branch
rules will refuse it anyway, and that refusal is deliberate: a day when `main`
was red and nobody knew is what the rules exist to prevent.

## Commits

[Conventional Commits](https://www.conventionalcommits.org):
`feat:` `fix:` `chore:` `docs:` `test:` `refactor:` — with a scope where it
helps, e.g. `fix(wallet): …`.

**Write the message for whoever reads it in six months.** The subject says what
changed; the body says *why*, and what breaks without it. A commit that says
«fix bug» has thrown away the only record of the reasoning.

## Pull requests

Every change goes through a PR — including one-line changes, including yours.

A PR is ready when:

- [ ] the tests pass, and any new behaviour has a test that **fails without the
      change** — a test that passes either way is proving nothing;
- [ ] lint passes;
- [ ] no secret, key, keystore, service-account JSON or `.env` is in the diff;
- [ ] the description says what it does, how it was verified, and what it
      touches that handles money, authentication or customer data.

## Money, if you are touching it

Payments, the wallet, the ledger, payouts and pricing are held to a higher bar:

- a new money path needs a test asserting it agrees with the existing payout
  calculation — the ledger and the payout system disagreeing about what somebody
  is owed is the most expensive defect in this codebase;
- declare a payment rail in **one** place and let every other site derive it;
- never re-implement a commission, tier or rounding rule. Import the one that
  exists. A second copy will drift, and the drift will be invisible.

## Secrets

Secrets live in GitHub Actions secrets or the deployment platform's
environment — never in the repository, never in an `.env.example`, never in a
workflow file.

If you commit one by accident: say so immediately. **Rotate it**; deleting the
commit does not revoke it.
