# W3F Grant Proposal
- **Project Name:** Social Recovery Wallet
- **Team Name:** Hypha DAO Wallet Team
- **Payment Address:** <address> (BTC)
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 2

## Overview
Proposal for the RFP titled [Social Recovery Wallet](https://github.com/w3f/Grants-Program/blob/master/rfps/social-recovery-wallet.md).

### Background
We develop Flutter wallets. We have experience developing social recovery wallets in Flutter. We develop the [SEEDS Flutter wallet](https://github.com/JoinSEEDS/seeds_light_wallet), found at the [Android store](https://play.google.com/store/apps/details?id=com.joinseeds.seedswallet) and the [iOS store](https://apps.apple.com/us/app/seeds-light-wallet/id1507143650). 

We have implemented social recovery in that Flutter wallet. It operates on [Telos](https://telos.net). 

There is an existing Flutter wallet, [Polkawallet](https://github.com/polkawallet-io/app), that we will use as a reference model for the Polkadot integration. 

We will use the existing social recovery screens in the Seeds Light Wallet for polkadot recovery. 

### Recovery Screens

These screens include:
- Select your guardians
- Request to become a guardian [option to accept / reject]
- Finalize guardians (set social recovery accounts)
- Recover lost key (Request link to send to guardians)
- Wait before recover - to prevent malicious actors taking over an account
- Cancel recovery - prevent maliciuous actors

### Recovery Link
To make recovery easy for a user, we provide a link with a recovery transaction (vouch) to their guardians.

To make recovery more difficult to attack, we require the user to send this link manually to their guardians, using methods other than the wallet. Meaning they have to use email, messaging apps, etc, to request recovery and can't just do it in-app. This makes social attacks more difficult, at minimal inconvenience for user. 

The guardians can just click on the recovery link. 

They are then presented with a screen where they can accept or reject the recovery, with a small disclaimer on the risks. 


### Limitations
Features will be limited to those offered by default by the social recovery pallet. Funds from an account can be recovered. Support for dApps compatible with the recovery pallet can be added later. 

### Sign and Broadcast (Extended Goal)
In addition to social recovery, we will also migrate our Sign and Broadcast feature. It scans the QR code provided by polkadot.{js}, signs it, and broadcasts it to the network. 

Sign and Broadcast also establishes a trusted link between the browser and the device. The transaction results are reported on both the device and the browser. This feature uses the Flutter implementation of [Anchor Link](https://github.com/greymass/eosio-signing-request).

### Parity Signer (Extended Goal)
Parity Signer scans QR codes that are produced by polkadot.{js}. Parity Signer is a fully airgapped wallet, so the payload is signed on the device and the signed QR code is scanned back into browser plugin to be broadcast. 

Our wallet will scan the same QR codes, but broadcast it to skip the step of having to scan the QR back in. Scanning QR codes from mobile back into a webcam is an extra step. It is the most time consuming part because you have to align the phone over the webcam correctly, and it always takes another second or two to focus on the QR code. 

With social recovery fully implemented, wallet users can be more confident leaving their mobile wallets online.

## Scoping
- **_Features_** - All steps of the [Social recovery on Substrate](https://www.parity.io/blog/social-recovery-on-substrate/) article will be implemented. 
- **_Deployment_** - We will deploy the wallet to iOS and Android application stores. 
- **_Maintenance_** - We will maintain the components on the mainline releases of Substrate for no less than 2 years

### Project Team members
- Nikolaus Heger - Flutter Developer
- Jason Doh - Project Lead
- Gerardo Guijarro  - Flutter Developer
- Gabriel Guijarro - Flutter Developer
- Raul Urtecho - Flutter Developer
- Sky Blu - Technical QA
- Other team members as needed

We have already been learning Substrate and we are partnering with the [Hashed Network](https://github.com/hashed-io). Many of our users are already planned to migrate over. 

### Contact
- **Contact Name:** Nikolaus Heger
- **Contact Email:** nheger@gmail.com
- **Website:** https://hypha.earth

### Legal Structure
- **Registered Address:** 30 N. Gould St, Ste R, Sheridan, Wyoming
- **Registered Legal Entity:** Hypha DAO LLC

## Development Roadmap :nut_and_bolt:
### Overview
- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):**  2.5 FTE 
- **Total Costs:** 50,000 USD

#### Languages
- All deliverables will be written in Flutter/Dart. 

## Milestones
For each milestone, we will deliver documentation and a video.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code. |
| 0c. | Video | We will record and publish a video explainer and demonstration of all features. |

### Milestone 1 — Screen Designs and Configure Recovery
- **Estimated duration:** 4 weeks
- **FTE:**  2.5
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Screen Designs | We will work with our designer to design the screens for all of the steps required. |  
| 2. | Configure Recovery | Screens for a user to add recovery configuration to their account. Identify a list of existing accounts to serve as friends, and select threshold |  

### Milestone 2 — Initiate Social Recovery, Vouch, Claim, and Recover
- **Estimated duration:** 6 weeks
- **FTE:**  2.5
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Recovery Lookup | The ability to add friends and an indicator whether that friend has a an active recovery.  |  
| 2. | Vouch | The ability to vouch for user that has an active recovery requesting signature from the account in the wallet.  |  
| 3. | Claim and Recover | When threshold is met, user will have the ability to claim and recover their tokens.  |  

### Milestone 3 — Scan QR code, Sign, and Broadcast
- **Estimated Duration:** 6 weeks
- **FTE:**  2.5
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | QR Code Format | Flutter library for scanning polkadot.{js} QR codes |  
| 2. | Node Selector | User can configure which network they are connecting |  
| 3. | Sign and Broadcast | Integrate ESR and Anchor-link for Flutter |  
| 4. | Deployment | Wallet deployed to iOS and Android app stores |  

## Future Plans
We plan to continue enhancing the wallet. Many of our users are migrating to Hashed Network and will require Flutter modules for custom pallets. 

## Additional Information :heavy_plus_sign:
**How did you hear about the Grants Program?** 
Referral - Max Gravitt
