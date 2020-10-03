# Grin Testing Plan

In this document we will setup a testing plan for the Grin Node & Wallet. The Grin Node and Wallet will be set up using the official Grin docs: https://docs.grin.mw .

## Progress Report

Here is where we fill in worked hours on QA for Grin (grin.mw) and explain what we have done and what is still to do.

| Date  | Name | Worked Hours | Work Done | Work Not Done | Problems |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 3.10.2020 | Warm Beer | 3 | Today I have spitted through the Grin documentation and worked through the setup process on Mac, Linux and Windows. During the setup I encountered minor issues and have documented them here along with some suggestions: https://github.com/mimblewimble/docs/issues/35 . I have also started a public Github repo: https://github.com/WarmBeer/GrinTesting where we can describe our testing plan for the Grin Wallet and Node. | The feature list on the GrinTesting repo is incomplete and needs to be complemented. | - |

## Use Cases

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
