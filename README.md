# phimac-support.github.io

This repository exists solely to serve the **MTA-STS policy** for `phimac.be` via GitHub Pages.

## What is MTA-STS?

MTA-STS (Mail Transfer Agent Strict Transport Security) is an email security standard defined in [RFC 8461](https://datatracker.ietf.org/doc/html/rfc8461). It allows mail servers to declare that they support TLS encryption and that sending mail servers should refuse to deliver mail if a secure connection cannot be established.

## How it works

GitHub Pages serves the MTA-STS policy file at the required URL:

```
https://mta-sts.phimac.be/.well-known/mta-sts.txt
```

The custom domain `mta-sts.phimac.be` points to this GitHub Pages site, making the policy accessible to external mail servers.

## Repository contents

- [`.well-known/mta-sts.txt`](.well-known/mta-sts.txt) — the MTA-STS policy file
- [`CNAME`](CNAME) — contains the custom domain (`mta-sts.phimac.be`) used by GitHub Pages; rename to `CNAME` (no extension) to activate it
- [`_config.yml`](_config.yml) — Jekyll config to ensure the `.well-known` directory is included

## Do not modify

This repository should not be used for anything other than hosting the MTA-STS policy. Changes to the policy file may affect email delivery for `phimac.be`.
