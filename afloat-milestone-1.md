# Milestone Delivery :mailbox:

**The [invoice form :pencil:](https://docs.google.com/forms/d/e/1FAIpQLSfmNYaoCgrxyhzgoKQ0ynQvnNRoTmgApz9NrMp-hd8mhIiO0A/viewform) has been filled out correctly for this milestone and the delivery is according to the official [milestone delivery guidelines](https://github.com/w3f/Grants-Program/blob/master/docs/milestone-deliverables-guidelines.md).**  

* **Application Document:** https://github.com/w3f/Grants-Program/blob/master/applications/native-bitcoin-vaults.md
* **Milestone Number:** 1

**Context** (optional)

We recorded a [video summary and demonstration](https://youtu.be/OYKvt-xir3E) for this milestone.

As mentioned in the proposal, we weren't sure if the `no_std` version of [Bitcoin Dev Kit](https://github.com/bitcoindevkit) would be ready, so we used an offchain worker in the meantime. The `no_std` versions of the dependencies (`rust-bitcoin` and `rust-miniscript`) have been developed but are not yet released. Once those are released, BDK will updated and we will integrate those changes into our solution. You can follow progress with this [open issue](https://github.com/bitcoindevkit/bdk/issues/205).

Also, instead of using Spectre Desktop or Caravan as the signer, we are using the mobile app [BlueWallet](https://github.com/BlueWallet). It is open source React Native and available on both app stores. This was a bit more difficult because it required the additional deliverable of encoding the payloads as QR codes. However, we believe it is an overall better fit, more secure, and improved UX over the other options.

We also originally intended to use the identity pallet `additional` mapping for storing the `xpub`. However, updating this field drops verification judgements from the identity, which of course would not be a desired effect. Instead, we save the `xpub` with our pallet. There is no impact to user experience.

**Deliverables**
| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code and a basic **tutorial** of the modules delivered in this Milestone.|
| 0c. | Testing | Unit testing will be applied to ensure reliability. Documentation of tests and results will be provided |
| 0d. | Video | We will provide a video demonstration that will illustrate all of the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** in English and Spanish that explains what was built and how it can benefit other projects |
| 1. | Set Profile and Upload KYC Materials | User onboarding web client for uploading identity details in a privacy preserving manner. Data will be encrypted and only accessible by 1) the user, 2) a pre-specified KYC administrator account, and 3) a persistence partner/custodian that the user or app administrator selects. |
| 2. | KYC Admin | KYC administrator screen for viewing and approving new user (market participant) requests. We plan to use the existing `registrar` process on the Identity pallet. UI is in Angular, with a small chance we may migrate it to Vuejs |
| 3. | Slides |1-3 additional presentation slides for Louise W. Reed, CPA’s currently scheduled talks at CPA conferences regarding blockchain, cryptocurrency, triple-entry accounting and transferring state tax credits.  The additional slides will be added to address why Afloat sees value in being supported by Polkadot’s ecosystem| 

**Repositories** 
(all MIT licensed)
| Component | Repo | Language |
| -----: | ----------- | ------- |
| Pallet | [Hashed Substrate](https://github.com/hashed-io/hashed-substrate/tree/main/pallets/nbv-storage) | Rust
| Bitcoin Services | [BDK Services](https://github.com/hashed-io/bdk-services) | Rust |
| Client | [Web App](https://github.com/hashed-io/native-bitcoin-vaults-UI) | Quasar/Vuejs |
| QR Codec | [QR Encoding Package](https://github.com/hashed-io/nbv-ur-codec) | Javascript |


**Additional Information**

We will create more extensive and polished end user documentation with the full product release (next milestone).
