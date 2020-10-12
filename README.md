# Grin Testing Plan

In this document we will setup a testing plan for the Grin Node & Wallet. The Grin Node and Wallet will be set up using the official Grin docs: https://docs.grin.mw .

## Progress Report

Here is where we fill in worked hours on QA for Grin (grin.mw) and explain what we have done and what is still to do.

| Date  | Name | Worked Hours | Work Done | Work Not Done | Problems |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 3.10.2020 | Warm Beer | 3 | Today I have spitted through the Grin documentation and worked through the setup process on Mac, Linux and Windows. During the setup I encountered minor issues and have documented them here along with some suggestions: https://github.com/mimblewimble/docs/issues/35 . I have also started a public Github repo: https://github.com/WarmBeer/GrinTesting where we can describe our testing plan for the Grin Wallet and Node. | The feature list on the GrinTesting repo is incomplete and needs to be complemented. | - |

## Configuration Options WIP

**grin-server.toml**

- [CO-GN1] Choose directory for grin blockchain
- [CO-GN2] Use TLS certificates 
- [CO-GN3] Choose listen address for services
- [CO-GN4] REST API authentication
- [CO-GN5] Foreign API authentication
- [CO-GN6] Select the chain type
- [CO-GN7] Change chain validation mode
- [CO-GN8] Run node in full archive mode
- [CO-GN9] Skip sync on startup
- [CO-GN10] Run ncurses TUI
- [CO-GN11] Run test miner

| CO-ID | Parameter | Description |
| --------- | ---------- | ---------- |
| CO-GN1 | db_root | the directory, relative to current, in which the grin blockchain is stored |
| CO-GN2 | tls_certificate_file | path of TLS certificate file, self-signed certificates are not supported |
| CO-GN2 | tls_certificate_key | private key for the TLS certificate |
| CO-GN3 | api_http_addr | the address on which services will listen, e.g. Transaction Pool |
| CO-GN4 | api_secret_path | path of the secret token used by the Rest API and v2 Owner API to authenticate the calls |
| CO-GN5 | foreign_api_secret_path | path of the secret token used by the Foreign API to authenticate the calls |
| CO-GN6 | chain_type | The chain type, which defines the genesis block and the set of cuckoo. Parameters used for mining as well as wallet output coinbase maturity. Can be: AutomatedTesting - For CI builds and instant blockchain creation. UserTesting - For regular user testing (cuckoo 16). Floonet - For the long term floonet test network. Mainnet - For mainnet |
| CO-GN7 | chain_validation_mode | the chain validation mode, defines how often (if at all) we want to run a full chain validation. Can be: "EveryBlock" - run full chain validation when processing each block (except during sync) "Disabled" - disable full chain validation (just run regular block validation) |
| CO-GN8 | archive_mode | run the node in "full archive" mode (default is fast-sync, pruned node) |
| CO-GN9 | skip_sync_wait | skip waiting for sync on startup, (optional param, mostly for testing) |
| CO-GN10 | run_tui | whether to run the ncurses TUI (Ncurses must be installed) |
| CO-GN11 | run_test_miner | Whether to run a test miner. This is only for developer testing (chaintype usertesting) at cuckoo 16, and will only mine into the default wallet port. real mining should use the standalone grin-miner |
| CO-GN11 | test_miner_wallet_url | test miner wallet URL (burns if this doesn't exist) |

## Use Cases WIP

List of features we want to test

**Grin (Node)**

- [GN1] Run a Grin node

**Grin Wallet**

- [GW1] Display commands for a certain feature
- [GW2] Initialize a Grin wallet
- [GW3] Create an account
- [GW4] Show account balance 
- [GW5] Receive Grin
- [GW6] Send Grin

## Test Cases

Here we describe the steps to test a certain feature and show the test results.

- **ID**: (GW for Grin Wallet | GN for Grin Node)X.Y Eg: "GW5.1" with X as the ID of the Use Case and Y as an incremental ID based on the number of Test Cases for a certain Use Case.
- **Test Case**: Describe what you are testing in a few words. Eg: "Receive Grin using ToR while connected to ext. Node"
- **Testing Steps**: Describe ALL the steps you need to take to conduct the test.
- **Expected Result**: What is the expected result after doing all the Testing Steps.
- **Status**: Waiting | Passed | Failed
- **Actual Result**: Empty if it's the same as Expected Result, else describe what happened.
- **Comments**: Optional. Can be used to describe the test environment.

| ID | Test Case | Testing Steps | Expected Result | Status | Actual Result | Comments |
| - | - | - | - | - | - | - |
