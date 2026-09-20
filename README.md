# Orbi Cloud documentation

中文版见 [/zh](https://github.com/orbi-build/orbi-cloud-docs/tree/main/zh)。

User documentation for [Orbi Cloud](https://orbi.build/cloud/?ref=cloud-docs-readme) — the hosted runner that turns a labelled GitHub Issue into a tested, independently reviewed, merged pull request.

These pages cover the whole path a user walks: signing in, installing the GitHub App, connecting a repository, provisioning, dispatching an Issue, reading the status page, cutting a release, and recovering when something goes wrong.

The open-source delivery engine lives in [orbi-build/orbi](https://github.com/orbi-build/orbi), and its documentation is at [docs.orbi.build](https://docs.orbi.build).

## Contents

| Page | Covers |
|---|---|
| `index.mdx` | What Orbi Cloud is, the delivery loop, what it costs |
| `quickstart.mdx` | Sign-in to first merged pull request, in five steps |
| `sign-in.mdx` | GitHub OAuth, language, sessions, personal vs organization |
| `install-app.mdx` | The GitHub App, what each permission is for, revoking |
| `connect-repository.mdx` | Choosing the repository and base branch, branch protection, rebinding |
| `provisioning.mdx` | What provisioning does, and the four failure classes |
| `model-configuration.mdx` | The included quota, BYOK, the supported providers |
| `billing.mdx` | Subscribing, the plan, the billing portal, cancelling |
| `first-issue.mdx` | Dispatching work, and how to write an Issue that succeeds |
| `delivery-lifecycle.mdx` | The `ai-*` label state machine and the independent review |
| `status-page.mdx` | How to read every card on the status page |
| `releases.mdx` | Cutting a release and the gates it passes |
| `limits-and-quotas.mdx` | The free allowance and the monthly token quota |
| `troubleshooting.mdx` | Every failure state and how to recover |
| `security.mdx` | Access boundaries, key storage, isolation, what CI guarantees |
| `faq.mdx` | Short answers with links to the detail |

## Local preview

Requires Node 22+.

```bash
npx mint@4.2.890 dev
```

Validate the build the same way CI does — it exits non-zero on any warning:

```bash
npx mint@4.2.890 validate
```

## Screenshots

The images in `images/` are captured from the application, not mocked up. They are produced against a local instance seeded with fixture tenants, so no real customer data appears in any of them.

Re-capture them after a user-visible UI change, so the documentation does not drift from the product.

## Contributing

Corrections are welcome — open an issue or a pull request.

If a page and the product disagree, that is worth reporting either way: it may be a documentation bug or a product bug, and which one it is should be decided deliberately rather than by quietly editing the prose to match.

## License

The documentation content is licensed under [CC BY 4.0](LICENSE).
