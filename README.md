# Orbi Cloud documentation

中文版见 [/zh](https://github.com/orbi-build/orbi-cloud-docs/tree/main/zh)。

User documentation for [Orbi Cloud](https://orbi.build/cloud/?ref=cloud-docs-readme) — the hosted runner that turns a labelled GitHub Issue into a tested, independently reviewed, merged pull request.

These pages cover the whole path a user walks: signing in, installing the GitHub App, connecting a repository, provisioning, dispatching an Issue, reading the status page, cutting a release, and recovering when something goes wrong.

The open-source delivery engine lives in [orbi-build/orbi](https://github.com/orbi-build/orbi), and its documentation is at [docs.orbi.build](https://docs.orbi.build).

## Contents

| Page | Covers |
|---|---|
| `index.mdx` | What Orbi Cloud is, the delivery loop, what it costs |
| `quickstart.mdx` | Sign-in to first merged pull request, following the status page's setup steps |
| `sign-in.mdx` | GitHub OAuth, the account menu, language, sessions, personal vs organization |
| `install-app.mdx` | The GitHub App, what each permission is for, revoking |
| `connect-repository.mdx` | Choosing the repository and base branch, branch protection, several repositories, deactivating |
| `provisioning.mdx` | What provisioning does, and how failures are classified |
| `model-configuration.mdx` | The included quota, BYOK, the supported providers |
| `billing.mdx` | The Free, Solo and Pro plans, subscribing, the billing portal, cancelling |
| `first-issue.mdx` | Dispatching work, and how to write an Issue that succeeds |
| `delivery-lifecycle.mdx` | The `ai-*` label state machine, the independent review, sharing a delivery |
| `status-page.mdx` | How to read the status page, top to bottom |
| `releases.mdx` | Versions, the delivery scope, cutting a release and the gates it passes |
| `limits-and-quotas.mdx` | The free allowance, the monthly token allowance and the repository limit |
| `troubleshooting.mdx` | Every failure state and how to recover |
| `security.mdx` | Access boundaries, key storage, isolation, what CI guarantees |
| `faq.mdx` | Short answers with links to the detail |

## Hand-written content — do not regenerate

Two things in this repository are written by hand and will be destroyed by a
full-site generation pass. Read this before pointing any documentation
generator — including the Mintlify GitHub App's authoring bot — at this repo.

- **The Chinese pages under `zh/`.** These are translations maintained against
  the English pages, not machine output regenerated on demand. A generator that
  only knows about the English pages deletes all sixteen of them.
- **The `mermaid` diagrams.** Four pages carry flow diagrams —
  `index.mdx` (the end-to-end path and the delivery loop), `delivery-lifecycle.mdx`,
  and their `zh/` counterparts. They encode the actual label state machine.
  A generator that rewrites prose replaces them with generic cards.

Beyond those two, the prose itself is specific on purpose: the error tables
(what the page says / what happened / what to do), the exact permission
rationale, the `?ref=` tracking parameters on outbound links, and the deep
links with anchors are all load-bearing. A regeneration pass that "improves
readability" trades them for longer text that says less.

This already happened once, on 2026-09-20: two bot commits deleted every `zh/`
page, dropped three of the four diagrams, and replaced the error tables with
card groups. Both were reverted in full — no salvageable content was found in
either. If a generation pass is ever wanted here, run it on a branch and read
the diff against `main` page by page before merging.

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

Re-capture them after a user-visible UI change, so the documentation does not drift from the product. English pages use `images/`, Chinese pages use `images/zh/`, captured with the product's own Chinese interface. The last full re-capture was on 2026-09-26, after the status page redesign (top bar with account menu, **Next** card, delivery history, folded **Settings and reference**).

## Contributing

Corrections are welcome — open an issue or a pull request.

If a page and the product disagree, that is worth reporting either way: it may be a documentation bug or a product bug, and which one it is should be decided deliberately rather than by quietly editing the prose to match.

## License

The documentation content is licensed under [CC BY 4.0](LICENSE).
