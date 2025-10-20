# paseo-chain-specs

All chain specification files can be found at the following base URL:
[PASEO Chain Specs](https://zondax.ch/paseo)


Available chain specification files:

- [paseo-collectives.raw.json](https://paseo-r2.zondax.ch/chain-specs/paseo-collectives.raw.json)
- [paseo-asset-hub.json](https://paseo-r2.zondax.ch/chain-specs/paseo-asset-hub.json)
- [paseo-bridge-hub.raw.json](https://paseo-r2.zondax.ch/chain-specs/paseo-bridge-hub.raw.json)
- [paseo-coretime.raw.json](https://paseo-r2.zondax.ch/chain-specs/paseo-coretime.raw.json)
- [paseo-people.raw.json](https://paseo-r2.zondax.ch/chain-specs/paseo-people.raw.json)
- [paseo.raw.json](https://paseo-r2.zondax.ch/chain-specs/paseo.raw.json)

Use wget to download the needed file:

```bash
wget https://paseo-r2.zondax.ch/chain-specs/paseo.raw.json
```

## Chain Spec Types

This repository contains two types of chain specifications:

- **Regular specs** (e.g., `paseo.raw.json`): Standard chain specification files for most node operators
- **Light client friendly specs** (e.g., `paseo.raw.smol.json`): Optimized specifications for light clients

**Note on Asset Hub**: The Asset Hub specification is only available as `paseo-asset-hub.json` (light client friendly format) in this repository, as the full raw specification file is too large to handle easily on GitHub. If you need modifications to the full Asset Hub spec, please:
- Open an issue describing your requirements, or
- Submit a PR with bootnode additions to the `.smol` version, and we will sync both files

## Contributing

### Bootnode Contributions

We welcome bootnode contributions to improve network connectivity! To add your bootnode:

1. Fork this repository
2. Add your bootnode information to the appropriate chain spec file(s)
3. Submit a Pull Request

Your contributions help strengthen the Paseo testnet infrastructure.

