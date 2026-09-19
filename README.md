# Tesla (TeslaMate)

Your Tesla at a glance: battery level, charging power, range, odometer and inside/outside temperature, pushed from your own self-hosted [TeslaMate](https://github.com/teslamate-org/teslamate).

## Setup
1. Run TeslaMate.
2. Deploy the [TRMNL TeslaMate reporter](https://github.com/eden881/trmnl-teslamate-reporter) next to it.
3. Point the reporter at this plugin's webhook URL.

Your data stays on your own server until the reporter pushes it to TRMNL.

### Develop locally

Templates and settings live in [`src/`](src/), ready for [trmnlp](https://github.com/usetrmnl/trmnlp):

```sh
gem install trmnl_preview
trmnlp serve
```
