# Science Project Smart Contract

## Overview

The ScienceProject smart contract is designed to manage a science project, tracking the number of scientists involved and ensuring certain criteria are met for project approval. The contract includes functions to handle the approval committee's decisions and check the eligibility of scientists.

## Features

### `approvalCommittee` Function

This function is used by the approval committee to approve or reject the science project. It takes two parameters:

- `_scientistsApproval`: The number of scientists approving the project.
- `_projectYear`: The year in which the project is being considered.

The function sets the `scientistsCount` variable to the provided approval count and ensures that the project year is 2010 or later. If the number of scientists approving the project is 15 or more, the function reverts with an error message, indicating that the project is considered an invention.

### `scientistEligibility` Function

This function is responsible for checking the eligibility of a scientist based on their age. It takes one parameter:

- `_scientistAge`: The age of the scientist.

The function uses a `require` statement to ensure that the scientist's age is 35 or older. If the age requirement is not met, the function reverts with an error message, stating that the individual is not considered a scientist.

## Usage

The contract can be deployed on a Ethereum-compatible blockchain. After deployment, the `approvalCommittee` function can be called to set the number of scientists approving the project and the project year. The `scientistEligibility` function can be used to verify the eligibility of individual scientists.


## License

This smart contract is released under the MIT License. See the [LICENSE](LICENSE) file for details.
