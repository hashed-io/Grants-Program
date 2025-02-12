# W3F Grant Proposal

- **Project Name:** Afloat Open source payment integration
- **Team Name:** Afloat Inc.
- **Payment Address:** bc1q0aghk8qufzwpmrp5nfyu9r7dh3yynmphk7rhjj
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 2


## Overview

[Afloat](https://stayafloat.io/#/) is one of the accounting industry's first real-use cases of blockchain technology. It enables the fractional buying and selling of tax credits that historically have been inefficient, opaque, and centralized. It has already processed tax credits ranging in orders from $2K -$70k USD.

Afloat has migrated to Polkadot, and is looking to build an open-source component needed to integrate with Dwolla, a low-fee fiat on/off ramp focused on Traditional Banking integration that provides account verification and KYC. This proposal would enable any substrate project to integrate with Dwolla easily. It also includes components that can be used with any payment integrator.

## Project Details

### Background

To drive mass adoption, bridges to the current banking system are needed. For example, afloat is a great use case that connects blockchain and government taxes. And like many other projects, it requires integration with the current banking system that facilitates compliance with US regulations.

The product explainer from the previous proposal can be found [here](https://github.com/Afloat-Inc/Grants-Program/blob/master/applications/Afloat.md#Product)

### Workflow

<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/7217054/226731648-04c7df9b-9774-4ced-8a30-9c7252c22b74.png">
</p>
<br />

Components details used in the Banking (Dwolla) Substrate integration. 

<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/7217054/227053993-fe3eff5b-e0ff-45df-a467-04c565d856df.png">
</p>
<br />


### Requirements

The full integration consists of two phases. This proposal covers the first phase. We've broken up the proposal to use the learnings from Phase 1 and n to estimate better Phase 2, which includes an Indexer.

#### Phase 1 - Create the API and Entrypoints for:

1. Creating a Dwolla account as a personally verified customer.

* Develop an API endpoint to enable users to create a Dwolla account as a personally verified customer.
* The endpoint should capture the user's details such as name, address, date of birth, social security number, and email address.
* The endpoint should validate the user's details against Dwolla's compliance requirements and create an account if the user passes.
* The endpoint should return a response indicating whether the account creation was successful.


2. Adding a bank account to a Dwolla account.

* Develop an API endpoint to enable users to add a bank account to their Dwolla account.
* The endpoint should capture the user's bank account details, such as routing and account numbers.
* The endpoint should validate the user's bank account against Dwolla's compliance requirements and add it to the user's account if it passes.
* The endpoint should return a response indicating whether the bank account addition was successful.


3. Verifying a bank account using microdeposits.

* Develop an API endpoint to enable users to verify their bank account using microdeposits.
* The endpoint should initiate the micro-deposit process by sending two small deposits to the user's bank account.
* The endpoint should require the user to verify the deposit amounts before the bank account is considered verified.
* The endpoint should return a response indicating whether the bank account verification was successful.


4. Depositing funds into a Dwolla balance.

* Develop an API endpoint to enable users to deposit funds into their Dwolla balance.
* The endpoint should capture the user's bank account details and the amount to be deposited.
* The endpoint should validate the user's bank account and initiate a transfer from the user's bank account to their Dwolla balance.
* The endpoint should return a response indicating whether the deposit was successful or not.


5. Transfer funds from a Dwolla balance to another user.

* Develop an API endpoint to enable users to transfer funds from their Dwolla balance to another user's Dwolla balance.
* The endpoint should capture the recipient's Dwolla account ID and the transfer amount.
* The endpoint should validate the user's balance and initiate a transfer to the recipient's Dwolla balance.
* The endpoint should return a response indicating whether the transfer was successful or not.


6. Withdrawing funds from a Dwolla balance.

* Develop an API endpoint to enable users to withdraw funds from their Dwolla balance.
* The endpoint should capture the user's bank account details and the amount to be withdrawn.
* The endpoint should validate the user's balance and initiate a transfer from the Dwolla balance to the user's bank account.
* The endpoint should return a response indicating whether the withdrawal was successful or not.


7. Webhook endpoints to handle events generated by Dwolla.

* Develop webhook endpoints to handle events generated by Dwolla.
* The endpoints should capture event data such as transaction status updates, bank account verification status, and balance updates.
* The endpoints should update the user's account based on the event data received.
* The endpoints should return a response indicating whether the update was successful or not.


8. Minting tokens when a user makes a deposit.

* Develop an API endpoint to enable users to mint tokens when they make a deposit.
* The endpoint should capture the user's deposit amount and issue a corresponding amount of tokens.
* The endpoint should interact with the Mapped Assets Pallet to mint the tokens and add them to the user's account.
* The endpoint should return a response indicating whether the minting process was successful or not.


## Ecosystem Fit

Help us locate your project in the Polkadot/Substrate/Kusama landscape and what problems it tries to solve by answering each of these questions:

Where and how does your project fit into the ecosystem?
Our target audiences are developers and entrepeneurs looking to launch products that require US-compliant Fiat integration. 
Are there any other projects similar to yours in the Substrate / Polkadot / Kusama ecosystem?
If so, how is your project different?
If not, are there similar projects in related ecosystems?

Developers in the substrate ecosystem looking to enable fiat on/off ramps with US banks while ensuring KYC compliance will be able to use open-source code and documentation to integrate their products.

Taxpayers using the Afloat platform, now part of the Polkadot ecosystem, will benefit from a compliant onboarding banking process and a faster buy/sell cycle.s

As far as we know, no other traditional banking integrations are KYC-compliant and open source.

#### Continuing Education for CPAs

Continuing the migration of Afloat's, enables the founder and current CEO [Louise Reed](https://www.linkedin.com/in/louisewreed/) to continue her education efforts at several CPE conferences, where CPAs receive continuing education credits to maintain their licenses each year. In addition, familiarizing her with Fiat integration with the Polkadot ecosystem will enable her to educate other CPAs about current, compliant, and affordable solutions.

#### Crypto Clients

Working in a historically conservative industry, CPAs are starting to feel the push from blockchain/crypto clients to accept the new technology and are now being forced to help with risk mitigation (alongside lawyers).


#### Bridging Communities
Afloat would naturally bridge two opposing communities: accounting, the most trusted and conservative industry, and blockchain, one of the most innovative industries. By association with such a trusted industry, blockchain would receive credibility in the eyes of the general public while also modernizing accounting with new and better processes.

#### Natural Use Case

There is a substantial educational and technological divide in the learning curve for accountants regarding blockchain, but Afloat adds an easy and natural way to learn. Most people, including CPAs and businesses, tend to understand only what they can see and experience, and Afloat brings tangibility to an otherwise intangible industry.



## Team :busts_in_silhouette:

### Team members

- Louise Reed - CEO and founder
- Sebastian Montero - Architect
- Augusto Lara - Project Manager
- Erick Casanova - Backend Developer
- Didier Mis May - Substrate Developer


### Contact

- **Contact Name:** Louise Reed
- **Contact Email:** louise@stayafloat.io
- **Website:** https://stayafloat.io/#/

### Legal Structure

- **Registered Address:** 6118 Saint Andrews Lane, Richmond, VA 23226
- **Registered Legal Entity:** Afloat, Inc.

### Team's experience

With a master's degree in physics from Duke University and a Master of Accounting from the University of North Carolina at Chapel Hill, Louise W. Reed has been a CPA for fifteen years and has grown a successful private practice that specializes in working with small businesses. In the spring of 2018, Louise conceptualized and founded Afloat to allow her clients to have the same tax opportunities traditionally found in only the largest of CPA firms. Under her leadership, Afloat built the current application (private Ethereum clone) with an in-house team and successfully launched in 2021. [Awards](https://stayafloat.io/#/media)

Afloat is partnering with Hashed Systems DAO LLC, a substrate development team with years of experience building blockchain applications. They have worked on substrate and Polkadot since the spring 2021. Additional relevant experience below:

[Proxy](https://prxyco.com/): Pallets, front-end, and back-end development that powers $1B plus in assets from foreign investors looking to benefit from the EB-5 visa program. Built by real estate and EB5 attorneys and licensed investment advisors. It secures the chain of evidence and approvals between developers and funding sources of the projects leveraging Polkadot security. 

[Hypha DAO](https://dho.hypha.earth/#/): Smart contracts and front-end development that enable the creation of flexible roles, assignments, and contributions with recurring payments. Design and implement a graph data layer to improve web application performance. Design and build a [Double Entry accounting](https://us02web.zoom.us/rec/share/eRqiBvq-dsV0L_hEjW5e8DWNYQlUn2bLhI8-86jkRVwdXiN3TiD5edym17ubCd9R.QhKQw_Byy0t5_8SW?startTime=1647371674000) (Passcode: .V$C#Br2) platform that streams wallet activity, supports token price history, reporting, and currency conversion.

[SEED](https://joinseeds.earth/): Smart contract and mobile development that captures the project's constitution, enable voting on proposals, and essential identity management like reputation, vote history etc. Design and build a PWA token swaps app. Design and build a basic [Economic Simulator](https://seeds-sim.hypha.earth/dashboard) that enables voters to understand the economic impact of policy changes.


### Relevant profile links
- Louise Reed CPA website: https://louisereedcpa.com/
- Louise Reed LinkedIn: https://www.linkedin.com/in/louisewreed/
- Sebastian on GitHub: https://github.com/sebastianmontero (Polkadot Blockchain Academy Graduate - Buenos Aires)
- Jose Maria on Github: https://github.com/jmgayosso and Gitlab: https://gitlab.com/jmgayosso
- Erick on GitHub: https://github.com/tlacloc
Hashed website: https://hashed.io/


## Development Roadmap :nut_and_bolt:
### Overview
- **Total Estimated Duration:** 13 weeks
- **Full-Time Equivalent (FTE):**  1 FTE (across 4 contributors)
- **Total Costs:** 37,300 USD

#### Languages
- All pallets will be developed in Rust. 
- Dwolla API will be writen in Javascript using NodeJS

### Milestone 1 — Create and verify accounts and move funds, including web hooks and token creation.
- **Estimated duration:** 13 weeks
- **FTE:**  1
- **Costs:** 37,300 USD
(4 contributors)


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code and a basic **tutorial** of the modules delivered in this Milestone.|
| 0c. | Testing | Unit testing will be applied to ensure reliability. Documentation of tests and results will be provided |
| 0d. | Video | We will provide a video demonstration to illustrate the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** in English and Spanish that explains what was built and how it can benefit other projects |
| 1. | Create account | 1. Develop an API endpoint to enable users to create a Dwolla account as a personally verified customer. 2. The endpoint should capture the user's details such as name, address, date of birth, social security number, and email address. 3. The endpoint should validate the user's details against Dwolla's compliance requirements and create an account if the user passes. 4. The endpoint should return a response indicating whether the account creation was successful or not. |
| 2. | Add bank account | 1. Develop an API endpoint to enable users to add a bank account to their Dwolla account. 2. The endpoint should capture the user's bank account details, such as routing and account numbers. 3. The endpoint should validate the user's bank account against Dwolla's compliance requirements and add it to the user's account if it passes. 4. The endpoint should return a response indicating whether the bank account addition was successful or not. |
| 3. | Verify account | 1. Develop an API endpoint to enable users to verify their bank account using microdeposits. 2. The endpoint should initiate the micro-deposit process by sending two small deposits to the user's bank account. 3. The endpoint should require the user to verify the deposit amounts before the bank account is considered verified. 4. The endpoint should return a response indicating whether the bank account verification was successful or not. | 
| 4. | Deposit funds | 1. Develop an API endpoint to enable users to deposit funds into their Dwolla balance. 2. The endpoint should capture the user's bank account details and the amount to be deposited. 3. The endpoint should validate the user's bank account and initiate a transfer from their bank account to their Dwolla balance. 4. The endpoint should return a response indicating whether the deposit was successful or not. |
| 5. | Transfer funds | 1. Develop an API endpoint to enable users to transfer funds from their Dwolla balance to another user's Dwolla balance. 2. The endpoint should capture the recipient's Dwolla account ID and the amount to be transferred. 3. The endpoint should validate the user's balance and initiate a transfer to the recipient's Dwolla balance. 4. The endpoint should return a response indicating whether the transfer was successful or not. |
| 6. | Withdrawing funds | 1. Develop an API endpoint to enable users to withdraw funds from their Dwolla balance. 2. The endpoint should capture the user's bank account details and the amount to be withdrawn. 3. The endpoint should validate the user's balance and initiate a transfer from the Dwolla balance to the user's bank account. 4. The endpoint should return a response indicating whether the withdrawal was successful or not. |
| 7. | Webhook endpoints | 1. Develop webhook endpoints to handle events generated by Dwolla. 2. The endpoints should capture event data such as transaction status updates, bank account verification status, and balance updates. 3. The endpoints should update the user's account based on the event data received. 4. The endpoints should return a response indicating whether the update was successful or not. |
| 8. | Minting tokens | 1. Develop an API endpoint to enable users to mint tokens when they deposit. 2. The endpoint should capture the user's deposit amount and issue a corresponding token amount. 3. The endpoint should interact with the Mapped Assets Pallet to mint the tokens and add them to the user's account. 4. The endpoint should return a response indicating whether the minting process was successful or not. |


## Future Plans
### Immediate Use
This proposal is one of two phases that will enable Afloat users to fund their accounts, transfer, buy and sell tax credits using their traditional bank accounts without worrying about compliance or KYC requirements.

### Next Phases

#### Phase 2
* Burning tokens when a user makes a withdrawal.

Requirements:
Develop an API endpoint to enable users to burn tokens when they withdraw.
The endpoint should capture the user's withdrawal amount and burn a corresponding token amount.
The endpoint should interact with the Mapped Assets Pallet to burn the tokens from the user's account.
The endpoint should return a response indicating whether the burning process was successful or not.

* Set up Indexer service
* Enable the mapped assets pallet indexing process to transfer funds between users when a transfer of tokens is made on the pallet.

Requirements:
Develop a service to enable the mapped assets pallet indexing process to transfer funds between users when tokens are transferred on the pallet.
The service should enable the server to receive notification of the transfer of tokens and transfer funds accordingly.
The service should ensure that the transfer of funds is only made between verified accounts and that sufficient funds are in the sender's account to cover the transfer.


## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?** 
Raul Romanutti recommended the program on a call with Louise Reed, Max Gravitt and Augusto Lara on March 21st, 2022.

