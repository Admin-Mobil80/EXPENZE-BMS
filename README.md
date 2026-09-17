# EXPENZE-BMS

The platform console, served at **bms.expenze.ai**.

Where Expenze is run *across* customers, as distinct from the customer-facing
portal: organisations, credits and pricing, the WhatsApp and intake channels,
and what the platform is doing.

| | |
|---|---|
| `index.html` | sign-in |
| `home.html` | the console |

## Part of Expenze

* **EXPENZE-PORTAL** — what customers use, at expenze.ai
* **EXPENZE-BMS** — this
* **EXPENZE-BACKEND** — the CDK app, the Lambdas, the policy engine, the tests

The backend deploys this one: its `app.py` points a CloudFront site stack at
`../BMS`, so the three check out as siblings under one folder.

## Deploying

From EXPENZE-BACKEND:

```bash
AWS_PROFILE=cloudmeter npx cdk deploy ExpenzeBms
```

Served from its own CloudFront distribution, separate from the portal's.
