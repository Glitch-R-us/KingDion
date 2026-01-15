# Source Attribution

This document tracks the sources of code imported from upstream repositories.

## Directories Imported from gateio/proof-of-reserves

The following directories were imported from the upstream repository at https://github.com/gateio/proof-of-reserves:

### client/
Complete client command implementations for the CLI:
- `keygen.go` - ZK key generation command
- `prover.go` - ZK proof generation command  
- `tools.go` - Utility commands (status checking, asset queries, etc.)
- `user_proof.go` - User proof generation command
- `verify.go` - Verification commands (CEX and user)
- `witness.go` - Witness generation command

### utils/
Utility packages and helper functions:
- `account_tree.go` - Merkle tree account management
- `constants.go` - System constants (batch sizes, tree depth, asset counts)
- `error_codes.go` - Error code definitions
- `redis_lock.go` - Distributed locking with Redis
- `secret_manager.go` - AWS Secrets Manager integration
- `tools.go` - File and data processing utilities
- `types.go` - Core type definitions
- `utils.go` - General utility functions

### config/
Configuration files and management:
- `config.go` - Configuration loading logic
- `config.json` - Runtime configuration template
- `cex_config.json` - CEX verification configuration with asset information
- `user_config.json` - User verification configuration template
- `proof.csv` - Sample proof data
- `.DS_Store` - macOS metadata file (should be excluded via .gitignore)

### example_data/
Example datasets for testing:
- `PoR0612.csv` - Sample user asset data

## Import Path

All imports use the module path `gate-zkmerkle-proof` as defined in `go.mod`.

## License

All imported files are covered by the repository's GPLv3 license:
- Licensed under GPLv3 (see LICENSE file in repository root)
- Original upstream copyright: Copyright 2023 © Gate Technology Inc.

## Verification

The imported directories were verified to be byte-for-byte identical to the upstream repository as of the verification date (January 15, 2026).

Build verification:
```bash
go mod tidy    # ✅ Success
go build ./... # ✅ Success  
go test ./...  # ✅ All tests pass
```

## Upstream Repository

- Repository: https://github.com/gateio/proof-of-reserves
- Branch: master (default)
- License: GPLv3
