# paseo-chain-specs

All chain specification files are hosted **directly in this repository**. Download them from the
`main` branch via the raw URLs below (they are no longer served from external storage).

Available chain specification files:

- [`paseo.raw.json`](./paseo.raw.json) — **current** Paseo relay (substitute relay, new genesis), full spec for node operators
- [`paseo.raw.smol.json`](./paseo.raw.smol.json) — light-client friendly checkpoint spec for the current relay

> **Substitute-relay relaunch:** Paseo has been relaunched from block 0 with a new genesis
> (`Paseo`, protocol-id `pad`, ss58 `42`). The previous chain specs — the original relay
> (`Paseo Testnet`, protocol-id `pas`, ss58 `0`) and all system-chain specs — are archived under
> [`paseo-legacy/`](./paseo-legacy) for historical reference. System-chain specs for the new
> network will be added here as those chains are onboarded.

Use wget/curl to download the needed file, e.g.:

```bash
wget https://raw.githubusercontent.com/paseo-network/paseo-chain-specs/main/paseo.raw.json
```

## Chain Spec Types

This repository contains two types of chain specifications:

- **Regular specs** (e.g., `paseo.raw.json`): Standard chain specification files with the full raw
  genesis, for most node operators.
- **Light client friendly specs** (e.g., `paseo.raw.smol.json`): Checkpoint specs (genesis state
  root + a warp-sync `lightSyncState`) optimized for light clients such as smoldot.

## Contributing

### Bootnode Contributions

We welcome bootnode contributions to improve network connectivity! To add your bootnode:

1. Fork this repository
2. Add your bootnode multiaddr to the `bootNodes` array of the appropriate chain spec file(s) —
   for the relay, add it to **both** `paseo.raw.json` and `paseo.raw.smol.json` so the two stay in sync
3. Submit a Pull Request

Your contributions help strengthen the Paseo testnet infrastructure.
