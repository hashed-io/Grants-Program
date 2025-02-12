# Milestone Delivery :mailbox:

**The [invoice form :pencil:](https://docs.google.com/forms/d/e/1FAIpQLSfmNYaoCgrxyhzgoKQ0ynQvnNRoTmgApz9NrMp-hd8mhIiO0A/viewform) has been filled out correctly for this milestone and the delivery is according to the official [milestone delivery guidelines](https://github.com/w3f/Grants-Program/blob/master/docs/milestone-deliverables-guidelines.md).**  

* **Application Document:** https://github.com/w3f/Grants-Program/blob/master/applications/native-bitcoin-vaults.md
* **Milestone Number:** 2

**Context** (optional)

We recorded a [video demonstration](https://us02web.zoom.us/rec/share/E4aqWkYK7n_f9tbmf5BNTqGMPW7NECOmkcY18iK5ZttHfWNLZeZ0JlAN3S-zpFOB.0QgU4C_WrzCEUS9Z?startTime=1665605589000) for this milestone.

As mentioned in the proposal, we weren't sure if the `no_std` version of [Bitcoin Dev Kit](https://github.com/bitcoindevkit) would be ready, so we used an offchain worker in the meantime. The `no_std` versions of the dependencies (`rust-bitcoin` and `rust-miniscript`) have been developed but are not yet released. Once those are released, BDK will updated and we will integrate those changes into our solution. You can follow progress with this [open issue](https://github.com/bitcoindevkit/bdk/issues/205).

Also, instead of using Spectre Desktop or Caravan as the signer, we are using the mobile app [BlueWallet](https://github.com/BlueWallet). It is open source React Native and available on both app stores. This was a bit more difficult because it required the additional deliverable of encoding the payloads as QR codes. However, we believe it is an overall better fit, more secure, and improved UX over the other options.

We also originally intended to use the identity pallet `additional` mapping for storing the `xpub`. However, updating this field drops verification judgements from the identity, which of course would not be a desired effect. Instead, we save the `xpub` with our pallet. There is no impact to user experience.

**Deliverables**
| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License | https://github.com/hashed-io/hashed-substrate/blob/main/LICENSE  | MIT |
| 0b. | Documentation | [Technical](https://github.com/hashed-io/hashed-substrate/tree/main/pallets/nbv-storage) Documentation and a step by step [Tutorial](https://github.com/hashed-io/hashed-network-portal-ui/blob/dev/docs/tutorials/native_bitcoin_vault_user_guide.md) on how to use NBV| The code has inline documentation and each repository has a detailed README with build, run, and test instructions. |
| 0c. | Testing Guide | https://github.com/hashed-io/bdk-services/blob/master/src/hbdk/mod.rs#L457, https://github.com/hashed-io/hashed-substrate/blob/main/pallets/nbv-storage/src/tests.rs  | Tests are build directly into Rust projects, integration tests shown in video described below |
| 0d. | Docker | https://github.com/hashed-io/bdk-services/blob/master/Dockerfile | Dockerfile for `bdk_services` is used to deploy to Kubernetes |
| 0e. | Video & Article | Videos in [Spanish](https://drive.google.com/file/d/1Tg0Bz09Zfoo8yhQP88bG5yepjtlyh_be/view) and [English](https://us02web.zoom.us/rec/share/E4aqWkYK7n_f9tbmf5BNTqGMPW7NECOmkcY18iK5ZttHfWNLZeZ0JlAN3S-zpFOB.0QgU4C_WrzCEUS9Z?startTime=1665605589000) and the articles in [Spanish](https://docs.google.com/document/d/1bJhRX4NXBJSH4MnMUBkkhlMQn8CKtsukLMCL4Zx1XUk/edit?usp=sharing) and [English](https://docs.google.com/document/d/1rAPWY7Mz015UUJhgYCdQ2F5pZPXJLnY0ZPgap9Q4Oqs/edit?usp=sharing) | NA |
| 1. | PSBT Signing	 | https://github.com/hashed-io/bdk-services | Users will be able to sign transactions using blue wallet, instead of Spectre Desktop. <br /><br />(Max or Erick - This was in the original proposal "Users will be able to sign transactions using our customized signer (Spectre Desktop) **and save the output to the Substrate node.**" Does it still make sense?) save the output to the Substrate node. |  
| 2. | Transaction Broadcast | https://github.com/hashed-io/hashed-substrate/tree/main/pallets/bitcoin-vaults | When the threshold of signatures has been reached, the status of the proposal changes and any co-signer can finalize and boradcast the transaction. <br /> <br />(Max or Erick - This was in the original proposal " the node will broadcast the transaction to the Bitcoin network (via integrated Bitcoin core node)" Does it still make sense?)  |  
| 4. | Hosted Instances	 | https://github.com/hashed-io/bdk-services/blob/master/README.md#generate-output-descriptors | Testnet and Mainet addresses: |  
| 5. | EZ-Try	| https://github.com/hashed-io/bdk-services/blob/master/README.md#generate-new-address | Max? |  
| 6. | Support & Maintenance |  | NA  |  

**Repositories** 
(all MIT licensed)
| Component | Repo | Language |
| -----: | ----------- | ------- |
| Pallet | [Hashed Substrate](https://github.com/hashed-io/hashed-substrate/tree/main/pallets/bitcoin-vaults) | Rust
| Bitcoin Services | [BDK Services](https://github.com/hashed-io/bdk-services) | Rust |
| Client | [Web App](https://github.com/hashed-io/native-bitcoin-vaults-UI) | Quasar/Vuejs |
| QR Codec | [QR Encoding Package](https://github.com/hashed-io/nbv-ur-codec) | Javascript |


**Additional Information**


