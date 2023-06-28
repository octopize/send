# [![Send](./assets/icon-64x64.png)](https://gitlab.com/timvisee/send/) Send

Octopize fork of timvisee/send which is a fork of mozilla/send.

This fork is intended to allow customers to share their sensible data with us in a secure way.

Our change will mostly be cosmetics and to enforce some security settings.


## History


A fork of Mozilla's [Firefox Send][mozilla-send].
Mozilla discontinued Send, this fork is a community effort to keep the project
up-to-date and alive.

- Forked [at][fork-commit] Mozilla's last publicly hosted version
- _Mozilla_ & _Firefox_ branding [is][remove-branding-pr] removed so you can legally self-host
- Kept compatible with [`ffsend`][ffsend] (CLI for Send)
- Dependencies have been updated
- Mozilla's [changes][mozilla-patches] since the fork have been selectively [merged][mozilla-patches-pr]
- Mozilla's experimental report feature, download tokens, trust warnings and FxA changes are not included

Find an up-to-date Docker image here: [docs/docker.md](docs/docker.md)

The original project by Mozilla can be found [here][mozilla-send].

Thanks [Mozilla][mozilla] for building this amazing tool!

[donate]: https://timvisee.com/donate
[ffsend]: https://github.com/timvisee/ffsend
[fork-commit]: https://gitlab.com/timvisee/send/-/commit/3e9be676413a6e1baaf6a354c180e91899d10bec
[mozilla-patches-pr]: https://gitlab.com/timvisee/send/-/merge_requests/3
[mozilla-patches]: https://gitlab.com/timvisee/send/-/compare/3e9be676413a6e1baaf6a354c180e91899d10bec...mozilla-master
[mozilla-send]: https://github.com/mozilla/send
[mozilla]: https://mozilla.org/
[remove-branding-pr]: https://gitlab.com/timvisee/send/-/merge_requests/2

---

**Docs:** [FAQ](docs/faq.md), [Encryption](docs/encryption.md), [Build](docs/build.md), [Docker](docs/docker.md), [More](docs/)

---

## Table of Contents

* [What it does](#what-it-does)
* [Requirements](#requirements)
* [Development](#development)
* [Commands](#commands)
* [Configuration](#configuration)
* [Localization](#localization)
* [Contributing](#contributing)
* [Instances](#instances)
* [Deployment](#deployment)
* [Clients](#clients)
* [License](#license)

---

## What it does

A file sharing experiment which allows you to send encrypted files to other users.

---

## Requirements

- [Node.js 16.x](https://nodejs.org/)
- [Redis server](https://redis.io/) (optional for development)
- [AWS S3](https://aws.amazon.com/s3/) or compatible service (optional)

---

## Development

To start an ephemeral development server, run:

```sh
npm install
npm start
```

Then, browse to http://localhost:8080

---

## Commands

| Command          | Description |
|------------------|-------------|
| `npm run format` | Formats the frontend and server code using **prettier**.
| `npm run lint`   | Lints the CSS and JavaScript code.
| `npm test`       | Runs the suite of mocha tests.
| `npm start`      | Runs the server in development configuration.
| `npm run build`  | Builds the production assets.
| `npm run prod`   | Runs the server in production configuration.

---

## Configuration

The server is configured with environment variables. See [server/config.js](server/config.js) for all options and [docs/docker.md](docs/docker.md) for examples.

---

## Localization

See: [docs/localization.md](docs/localization.md)

---

## Contributing

Pull requests are always welcome! Feel free to check out the list of "good first issues" (to be implemented).

---

## Deployment

See: [docs/deployment.md](docs/deployment.md)

Docker quickstart: [docs/docker.md](docs/docker.md)

AWS example using Ubuntu Server `20.04`: [docs/AWS.md](docs/AWS.md)

---

## Clients

- Web: _this repository_
- Command-line: [`ffsend`](https://github.com/timvisee/ffsend)
- Thunderbird: [FileLink provider for Send](https://addons.thunderbird.net/thunderbird/addon/filelink-provider-for-send/)

---

## License

[Mozilla Public License Version 2.0](LICENSE)

[qrcode.js](https://github.com/kazuhikoarase/qrcode-generator) licensed under MIT

---
