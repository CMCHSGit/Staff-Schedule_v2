# Staff Schedule v2

Rebuild of the CMCHS staff schedule (successor to
[`cmchs-staff-schedule`](https://github.com/CMCHSGit/cmchs-staff-schedule)), designed against the
Connected Healthcare Systems design system.

## What is in here

| Path | What it is |
| --- | --- |
| `_ds/connected-healthcare-systems-design-syst-914962cd-.../` | The CHS design system — tokens, component bundle, manifest and readme. Vendored, not hand-edited. |
| `support.js` | The Claude Design Component runtime (`dc-runtime`). Generated; do not edit. |

`_ds/.../readme.md` is the reference for brand voice, colour, type and the component inventory
(Button, Card, Badge, Field, Tabs, Alert, Dialog and the rest). Read it before adding UI.

## Design source

The screens come from the Claude Design project
[Staff Schedule](https://claude.ai/design/p/6e3db676-c402-4c31-8c31-b6775fcce92b).

`Schedule Overview.dc.html` is the first screen to be implemented. It is **not yet in this repo** —
pulling it needs an authorised Claude Design session (`/design-login` in Claude Code, then the
`claude_design` MCP can read the project).

## Conventions

- Design system files are vendored verbatim. Upgrade by re-exporting the whole `_ds/` directory.
- `.dc.html` files are design components, not shipping code: they are the spec the app is built
  from. They load `support.js` plus the `_ds` tokens and bundle via a `<helmet>` block.
- A4, not Letter, for anything printable. NZ English throughout. No emoji in product UI.
