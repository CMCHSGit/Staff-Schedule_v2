# Staff Schedule v2

Rebuild of the CMCHS staff schedule (successor to
[`cmchs-staff-schedule`](https://github.com/CMCHSGit/cmchs-staff-schedule)), designed against the
Connected Healthcare Systems design system.

## What is in here

| Path | What it is |
| --- | --- |
| `Staff Schedule.dc.html` | The screen itself — week, day, leave-calendar and on-call views, desktop and mobile. The design to implement. |
| `Schedule Overview.dc.html` | Canvas that lays the screen out at four mobile sizes plus desktop. Imports `Staff Schedule`; start here to see the whole thing. |
| `assets/` | CHS logo (full colour and mark). |
| `uploads/` | Reference images pasted into the design session. |
| `_ds/connected-healthcare-systems-design-syst-914962cd-.../` | The CHS design system — tokens, component bundle, manifest and readme. Vendored, not hand-edited. |
| `support.js` | The Claude Design Component runtime (`dc-runtime`). Generated; do not edit. |

`_ds/.../readme.md` is the reference for brand voice, colour, type and the component inventory
(Button, Card, Badge, Field, Tabs, Alert, Dialog and the rest). Read it before adding UI.

## Design source

The screens come from the Claude Design project
[Staff Schedule](https://claude.ai/design/p/6e3db676-c402-4c31-8c31-b6775fcce92b).

Open `Schedule Overview.dc.html` first — it frames `Staff Schedule.dc.html` in the four mobile
views (`week`, `day`, `month`, `oncall`) and the 1440×900 desktop view, which is the fastest way to
see what each view is meant to do. `Staff Schedule.dc.html` takes `force-mobile` and `initial-view`
attributes; that is how the overview drives it.

## Conventions

- Design system files are vendored verbatim. Upgrade by re-exporting the whole `_ds/` directory.
- `.dc.html` files are design components, not shipping code: they are the spec the app is built
  from. They load `support.js` plus the `_ds` tokens and bundle via a `<helmet>` block.
- A4, not Letter, for anything printable. NZ English throughout. No emoji in product UI.
