# NakoPay for Make

NakoPay modules for Make (formerly Integromat). Trigger automations on invoice
events, create invoices from scenarios, and pull payment data into your workflows.

[![Status](https://img.shields.io/badge/status-beta-blue)](https://nakopay.com/integrations)
[![License](https://img.shields.io/badge/license-MIT-green)](../LICENSE)

## Install

```
Connect from https://www.make.com/en/apps/nakopay
```

## Configure

1. Get an API key from <https://nakopay.com/dashboard/api-keys>.
2. In Make admin: Add NakoPay connection in scenario builder
3. Set the webhook URL shown in the plugin settings inside your NakoPay
   dashboard (Settings → Webhooks).

## Test mode

Use `sk_test_*` keys to run the full checkout against the NakoPay sandbox.
No real funds move. Flip to `sk_live_*` when you're ready for production.

## Supported features

- [x] Triggers: `invoice.paid`, `invoice.failed`, `refund.created`
- [x] Actions: create invoice, void invoice, look up customer
- [x] Polling + webhook subscriptions
- [x] Test mode

## Local development

See [`../CONTRIBUTING.md`](../CONTRIBUTING.md) for the full setup. Quick
start for YAML plugins:

- YAML stack: see CONTRIBUTING § "Local development per host".
- Run `bash ../scripts/check-no-internal-urls.sh .` before opening a PR.

## Release

Tag-driven from the monorepo:

```
plugins/scripts/release.sh make 0.1.0
```

The matching workflow at `.github/workflows/release-make.yml` handles the
upload to the marketplace. Full runbook in [`../PUBLISHING.md`](../PUBLISHING.md).

## Issues

File on <https://github.com/NakoPayHQ/plugin-make/issues>.

## About Make (formerly Integromat)

[Make (formerly Integromat)](https://www.make.com/) - visual automation platform for connecting apps and workflows. Visit their website to learn more about the platform and its features.

## License

MIT - see [`../LICENSE`](../LICENSE).
