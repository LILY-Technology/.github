# Security Policy

## Reporting a vulnerability

**Do not open a public issue.** A public report tells an attacker before it tells us.

Use one of these instead:

1. **GitHub private vulnerability reporting** — the *Security* tab of the
   affected repository → *Report a vulnerability*. This is the preferred route:
   it keeps the report, our replies and the fix in one place, privately, until
   there is something safe to publish.
2. **<info@lilydelivery.com>** — if the repository is one you cannot see, or
   you would rather not use GitHub.

## What to include

Whatever you have. These help most:

- what the issue lets somebody do, in one sentence;
- the smallest reproduction you can manage — a request, a payload, a sequence;
- the affected repository, and a commit or version if you know it;
- whether you believe it has been exploited.

**Please do not test against production.** Lily Delivery carries real orders and
real money. If the only way to demonstrate something is against live systems,
tell us first and we will arrange it.

## What we will do

- **Acknowledge within 2 working days.** Khartoum hours; we are a small team and
  will say so rather than leave you guessing.
- **Tell you what we found**, including when we disagree that it is a
  vulnerability — with the reasoning, not a form reply.
- **Fix money and authentication issues first.** Those are the ones where an
  hour matters.
- **Credit you** if you want it, once a fix is released.

## Scope

In scope: anything in this organization's repositories, the Lily Delivery APIs,
the customer and driver apps, and our web properties.

Out of scope: reports generated only by an automated scanner with no shown
impact; missing hardening headers with no demonstrated consequence; denial of
service through sheer volume; social engineering of our staff or drivers.

## One thing we ask

If you find a credential — a key, a token, a password — in our code or history,
**tell us and do not use it**. We will rotate it. Removing a secret from Git does
not revoke it, and we would rather hear it from you than from our logs.
