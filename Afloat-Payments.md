# W3F Grant Proposal

- **Project Name:** Afloat Open source payment integration
- **Team Name:** Afloat Inc.
- **Payment Address:** bc1q0aghk8qufzwpmrp5nfyu9r7dh3yynmphk7rhjj
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 2


## Overview

[Afloat](https://stayafloat.io/#/) is one of the first real-use cases of blockchain technology in the accounting industry. It enables the fractional buying and selling of tax credits that historically have been inefficient, opaque, and centralized. It has already processed tax credits ranging in orders from $2K -$70k USD.

Afloat has migrated to Polkadot, and is now looking to build an open source component needed to integrate with Dwolla, a low fee fiat on/off ramp focused on Traditional Banking integration, that provides account verification and KYC. This proposal would enable any substrate project to easily integrate with Dwolla. It also includes components that can be used with any payment integrator.

### Background

To drive mass adoption, bridges to the current banking system are needed. Afloat is a great use case that connects blockchain and government taxes. And like many other projects, need integration with the current banking system that facilitates compliance with US regulation.

The product explainer from the previous proposal can be found [here](https://github.com/Afloat-Inc/Grants-Program/blob/master/applications/Afloat.md#Product)


### Workflow

<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/7217054/160020369-b64ae31d-8cc5-49ce-8c4d-82dea85546cf.png">
</p>
<br />


## Ecosystem Fit

Afloat serves tax payers that want to buy and/or sell tax credits. These users will benefit from an easy to use, compliant Fiat on/off ramp which is also a common, top of mind, challenge for digital native projects and developers in the ecosystem. 


### Community

Developers from the Polkadot community will be able to leverage the Fiat integration for the products and send questions to the team.

#### Continuing Education for CPAs

Continuing the migration of Afloat’s, enables the founder and current CEO [Louise Reed](https://www.linkedin.com/in/louisewreed/) to continue her education efforts at a number of CPE conferences, where CPAs receive continuing education credits to maintain their licenses each year. Familiarizing her with Fiat integration with the Polkadot ecosystem will enable her to educate other CPAs about current, compliant and affordable solutions.

#### Crypto Clients

Working in a historically conservative industry, CPAs are starting to feel the push from blockchain/crypto clients to accept the new technology and are now being forced to help with risk mitigation (alongside lawyers).


#### Bridging Communities
Afloat would naturally bridge two opposing communities: accounting, the most trusted and conservative industries, and blockchain, one of the most innovative industries. By association with such a trusted industry, blockchain would receive credibility in the eyes of the general public while also modernizing accounting with new and better processes.

#### Natural Use Case

There is a huge educational and technological divide in the learning curve for accountants when it comes to blockchain, but Afloat adds an easy and natural way to learn.  Most people, including CPAs and businesses, tend to understand only what they can see and experience, and Afloat brings tangibility to an otherwise intangible industry.

#### Speaking arrangements - Check with Louise

Louise Reed is scheduled to speak at the following Certified Public Accountant Societies.

| Date of Talk | CPA Society | Location |
| -----------: | ----------- | -------- |
| 5/26/2022    | NC          | Greensboro |
| 8/24/2022    | GA          | Atlanta |
| 9/26/2022    | VA (+ VA Tech) | Roanoke |
| 11/17/2022   | VA (+ VA Tech) | Virginia Beach |


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

With a master's degree in physics from Duke University and a Master of Accounting from the University of North Carolina at Chapel Hill, Louise W. Reed has been a CPA for fifteen years and has grown a successful private practice that specializes in working with small businesses. In the spring of 2018, Louise conceptualized and founded Afloat to allow her clients to have the same tax opportunities traditionally found in only the largest of CPA firms. Under her leadership, Afloat built the current application (private ethereum clone) with an in-house team and successfully launched in 2021. [Awards](https://stayafloat.io/#/media)

Afloat is partnering with Hashed Systems DAO LLC, a substrate development team with years of experience building blockchain applications. They have worked on substrate and Polkadot since spring 2021. Additional relevant experience below:

[Proxy](https://prxyco.com/) manages $1B plus in assets from foreigh investors looking to benefit from the EB-5 visa program. It was built by real estate and EB5 attorneys, blockchain specialists and licensed investment advisors. It's plattform secures the chain of evidence and approvals between developers and funding sources of the projects leveraging the Polkadot ecosystem. The Hashed team built the entire application, deployed it and currently supports it.

[Hypha DAO](https://dho.hypha.earth/#/): Smart contracts and front end development that enables the creation of flexible roles, assignments and contributions with recurring payments. Design and implement a graph data layer to improve web application performance. Design and build a [Double Entry accounting](https://us02web.zoom.us/rec/share/eRqiBvq-dsV0L_hEjW5e8DWNYQlUn2bLhI8-86jkRVwdXiN3TiD5edym17ubCd9R.QhKQw_Byy0t5_8SW?startTime=1647371674000) (Passcode: .V$C#Br2) plattform that streams wallet activity, supports token price history, reporting and currency conversion.

[SEED](https://joinseeds.earth/): Smart contract and mobile development that capture the project's constitution, enable voting on proposals and basic identity management like reputation, vote history etc. Design and build a PWA token swaps app. Design and build a basic [Economic Simulator](https://seeds-sim.hypha.earth/dashboard) that enables voters to understand the economic impact of policy changes.


### Relevant profile links
- Louise Reed CPA website: https://louisereedcpa.com/
- Louise Reed LinkedIn: https://www.linkedin.com/in/louisewreed/
- Augusto on LinkedIn: https://www.linkedin.com/in/augustolara/
- Sebastian on GitHub: https://github.com/sebastianmontero 
*  Polkadot Blockchain Academy Graduate (Buenos Aires)
- Jose Maria on Github: https://github.com/jmgayosso and Gitlab: https://gitlab.com/jmgayosso
- Hashed website: https://hashed.io/
- Erick on GitHub: https://github.com/tlacloc


## Development Roadmap :nut_and_bolt:
### Overview
- **Total Estimated Duration:** 13 weeks
- **Full-Time Equivalent (FTE):**  2 FTE (across 5 contributors)
- **Total Costs:** 46,200 USD

#### Languages
- All pallets will be developed in Rust. 
- The custodial/persistence partner backend will be developed in Nodejs, with a slight possibility of porting it to Rust.
- The front end will be Angular, with a possibility that it will be migrated to Vuejs.

### Milestone 1 — User onboarding (set and verify identity with gatekeeper parameters) and slides.
- **Estimated duration:** 5 weeks
- **FTE:**  2
- **Costs:** 17,675 USD
(5 contributors)

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


### Milestone 2 — Originate and configure a tax credit and create sales order for tax credits.
- **Estimated duration:** 4 weeks
- **FTE:**  2
- **Costs:** 14,140 USD
(5 contributors)

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code and a basic **tutorial** of the modules delivered in this Milestone.|
| 0c. | Testing | Unit testing will be applied to ensure reliability. Documentation of tests and results will be provided |
| 0d. | Video | We will provide a video demonstration that will illustrate all of the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** in English and Spanish that explains what was built and how it can benefit other projects
| 1. | Originate Tax Credit | Web client for onboarding new tax credits as NFTs, appropriate metadata persisted using the Uniques and likely Statemint specifications. |
| 2. | Upload Confidential Documents | This feature allows for NFT originators to upload encrypted files attached to tax credits. The files will be accessible only by the user and the application administartor. | 
| 3. | Tax Credit verification | MVP Tax Credit pallet, compatible with the prebuilt Uniques pallet (and/or RMRK), will support data validation rules by jurisdiction and tax credit type. The user will be able to save a draft of their tax credit if they need to identify more IRL steps to fix discrepancies. It's like a 'tax credit compiler'. |
| 4. | List for Sale | Ability for Tax Credit (NFT) owners to assign a price and list it for sale.| 


### Milestone 3 — Sell the entire or a fraction of the tax credit to interested buyers using fruniques pallets.
- **Estimated duration:** 2 weeks
- **FTE:**  2
- **Costs:** 7,070 USD
(5 contributors)

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code and a basic **tutorial** of the modules delivered in this Milestone. |
| 0c. | Testing | Unit testing will be applied to ensure reliability. Documentation of tests and results will be provided |
| 0d. | Video | We will provide a video demonstration that will illustrate all of the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** in English and Spanish that explains what was built and how it can benefit other projects
| 1. | Order Part of an NFT | Web client and pallet support for fractionalizing a Tax Credit NFT. Users may specify the % and/or direct amount for the order. Rust and Angular/Vuejs | 
| 2. | Complete/Confirm Order | Sell the entire or a fraction of the tax credit to interested buyers using fruniques pallets. Rust and Angular/Vuejs | 
| 3. | Order Settlement | Ensure the marketplace correctly calculates appropriate commissions and fees. Calculations will be in Rust, displayed in application using Angular/Vuejs |

### Milestone 4 — Redeem the tax credit and confirm redemption and freeze/burn asset on-chain.
- **Estimated duration:** 2 weeks
- **FTE:**  2
- **Costs:** 7,070 USD
(5 contributors)

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code and a basic **tutorial** of the modules delivered in this Milestone.|
| 0c. | Testing | Unit testing will be applied to ensure reliability. Documentation of tests and results will be provided |
| 0d. | Video | We will provide a video demonstration that will illustrate all of the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** in English and Spanish that explains what was built and how it can benefit other projects
| 1. | Approve Redemption Specialists | Pallet and web client for onboarding and approving/enrolling Tax Credit Redemption Specialists. These are experts that know how to perform appropriate steps to migrate a tax credit IRL. Approval will be handled by marketplace administrator initially, by the community eventually. |
| 2. | Request Redemption | Pallet and web function/form for requesting redemption, optionally from a specific Redemption Specialist or system will choose. |
| 3. | View materials and Redeem | Pallet support and web client for Redemption Specialist to review the encrypted tax credit materials and confirm that off-chain IRL redemption has been completed. Redemption completion will be approved by owner and Redemption specialist. | 
| 4. | Asset Manager | Once part or all of a tax credit NFT is redeemed, the Tax Credit Asset Manager(s) will be able to lock, freeze, and/or burn the NFT. |
| 5. | Launch Materials | Launch materials, videos and speaking arrangements for Louise are already in queue.|  
 
## Future Plans
### Immediate Use
All Afloat users will be migrated to the substrate application and benefit from the identity and security enhancements. Afloat will gain access to the full substrate ecosystem and vice versa. 

### Next Phases
This proposal covers Afloat migration of the current functionality. Below are future phases that expand it:

#### Phase 2
User scenarios: 
- Registration/approval of new appraisers, 
- Request appraisal of NFT, 
- Appraise NFT, 
- Review and compensate appraiser

Web client for: 
- NFT creator to request judgment and grant access to Asset Grader(s)
- Asset Grader to review materials and provide judgment

#### Phase 3
User scenarios: 
- More advanced ordering and pricing models, 
- Candle auctions, 
- Improved compatibility with more jurisdictions.

#### Phase 4
- Provide API access and referral program for tax industry participants. (e.g. allow existing systems and networks to seamlessly integrate)

## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?** 
Raul Romanutti recommended the program on a call with Louise Reed, Max Gravitt and Augusto Lara on March 21st, 2022.

### Additional Context
#### State Tax Credit Breakdown
Currently, forty-one states offer tax credits designed to incentivize economically and socially desirable behavior, like historic structure rehabilitation, land preservation and film production.
- Linking a US bank account
<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/7217054/160020375-0e360e26-17f9-4856-8266-1e95b76efc7c.png">
</p>
<br />
Thirty-four of those states allow the producers of these credits to be incentivized even if they do not have enough state income to fully utilize the credits and/or need the cash flow to further expand the incentivized behavior.  
<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/7217054/160020372-8190f4aa-81aa-4b0e-ae1b-d92eb031df5b.png">
</p>
<br />

Blockchain Friendly State Breakdown
<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/7217054/160020643-84313880-4e0b-4942-8b1a-7278eb7aa219.png">
</p>
<br />
https://www.investopedia.com/news/majority-us-states-are-still-acknowledge-cryptocurrencies/
