
User Experience Guidelines

Version 3.

May 2025

### Legal Notice

Financial Data Exchange, Inc (FDX) is a standards body and adopts these User Experience Guidelines for general use among industry
stakeholders. Many of the terms, however, are subject to additional guidance under prevailing laws, industry norms, and/or
governmental regulations. While referencing certain laws that may be applicable, readers, users, members, or any other parties
should seek legal advice of counsel relating to their particular practices and applicable laws in the jurisdictions where they do
business. See FDX’s complete Legal Disclaimer located at [http://www.financialdataexchange.org](http://www.financialdataexchange.org) for other applicable disclaimers.
Copyright © 2025 - FDX - All Rights Reserved.

### Revision History

```
Document Version Notes Date
```
##### 3.

```
Describes CFPB Section 1033 requirements. Incorporates FDX
RFCs 0318, 0327. Added section numbering, streamlined
graphics and document flow.
```
```
May 2025
```
##### 2.

```
Incorporates FDX RFC 0240 to introduce a Money Movement
user journey and edits to the Data Clusters section. Reorders
Consent Dashboard subsections, removes the DAP Consent
Dashboard section, and determined must vs should language.
```
```
December 2022
```
##### 2.

```
Incorporates FDX RFC 0151 describing consent editing, as
well as changes to the Data Cluster section. May 2022^
```
##### 2.

```
Incorporates FDX RFCs 0150, 0159, and 0160 describing
consent management, Data Cluster requirements, and journey
notification.
```
```
October 2021
```
##### 1.

```
Initial Document Release
This document was created as a result of FDX RFC 0019 and
incorporates the full contents of the RFC for public release.
```
```
December 2020
```

## Contents


- 1 INTRODUCTION
   - 1.1 DOCUMENT PURPOSE AND INTENDED AUDIENCE
   - 1.2 SCOPE
   - 1.3 TERMINOLOGY AND CONCEPTS
   - 1.4 FDX REFERENCES
- 2 DATA SHARING
   - 2.1 PRINCIPLES GUIDING DATA SHARING EXPERIENCES
   - 2.2 DATA SHARING AND FLOW
      - 2.2.1 Types of Financial Data
      - 2.2.2 Parties Involved in Financial Data Sharing
      - 2.2.3 Flow of Financial Data
      - 2.2.4 The Consumer Financial Protection Bureau (CFPB) Required Rulemaking on Personal Financial Data Rights (CFPB Section 1033)
   - 2.3 CONSENT COMPONENTS
      - 2.3.1 Business Purpose
      - 2.3.2 Data Clusters
      - 2.3.3 Duration of Consent
      - 2.3.4 Account List
   - 2.4 LIFE CYCLE OF CONSENT
      - 2.4.1 Grant Consent
      - 2.4.2 Manage Consent
      - 2.4.3 Revoke Consent
      - 2.4.4 Reauthorize Consent
- 3 USER EXPERIENCE GUIDELINES
   - (DR-DAP-DP) 3.1 GRANT CONSENT JOURNEY: DATA RECIPIENT AUTHORIZATION USING A DATA ACCESS PLATFORM TO FACILITATE THE CONNECTION TO A DATA PROVIDER
      - 3.1.1 Initiate - Sample User Content
      - 3.1.2 Select Data Provider – Sample User Content
      - 3.1.3 Authorize – Sample User Content
      - 3.1.4 Authenticate – Sample User Content
      - 3.1.5 Confirm Authorization (Optional) – Sample User Content
      - 3.1.6 Select Accounts – Sample User Content
      - 3.1.7 Complete – Sample User Content
   - 3.2 CONSENT GRANT JOURNEY: DATA ACCESS PLATFORM AUTHORIZATION (DR-DAP-DP)
      - 3.2.1 Initiate - Sample User Content
      - 3.2.2 Select Data Provider - Sample User Content
      - 3.2.3 Authorize - Sample User Content
      - 3.2.4 Authenticate - Sample User Content
      - 3.2.5 Confirm Authorization (Optional) – Sample User Content
      - 3.2.6 Select Accounts – Sample User Content
      - 3.2.7 Complete – Sample User Content
   - 3.3 GRANT CONSENT JOURNEY: DATA RECIPIENT AUTHORIZATION USING A DATA ACCESS PLATFORM (DR-DAP-DP)
      - 3.3.1 Data Recipient Authorization - Sample User Content
- 4 POST CONSENT GRANT JOURNEY
   - 4.1 NOTIFICATION
      - 4.1.1 Notification - Sample User Content
   - 4.2 CONSENT MANAGEMENT AND DASHBOARDS
      - 4.2.1 Overview
      - 4.2.2 Consent Dashboard at the Data Provider (Optional)
      - 4.2.3 Consent Dashboard at the Data Access Platform
      - 4.2.4 Consent Dashboard at the Data Recipient
   - 4.3 ANNUAL REAUTHORIZATION
      - 4.3.1 Overview
      - 4.3.2 Direct Connection Data Recipient Reauthorization with Optional Data Provider Confirmation
      - 4.3.3 Data Access Platform Reauthorization with Optional Data Provider Confirmation
- APPENDIX A: GRANT CONSENT EXAMPLES
- SECTION 1033) APPENDIX B: CONSUMER FINANCIAL PROTECTION BUREAU (CFPB) REQUIRED RULEMAKING ON PERSONAL FINANCIAL DATA RIGHTS (CFPB


## 1 INTRODUCTION

### 1.1 DOCUMENT PURPOSE AND INTENDED AUDIENCE

This document provides non-binding user experience (UX) guidelines and best practices for designing user-permissioned data
sharing experiences within the FDX ecosystem. These guidelines are intended to support FDX implementers in creating intuitive,
transparent, and user-centric financial data-sharing interfaces.

Importantly, this document is not part of the FDX Consensus Standard Data Format (CSDF), which establishes technical
conformance requirements for Data Providers under a CFPB Section 1033 “consensus standard.” These UX Guidelines are not a
“consensus standard” and are purely advisory and do not impose any conformance obligations nor legal requirements. Implementers
may choose to follow these recommendations to enhance user experiences but are not required to do so for conformance with FDX
standards.

This guidance is geared to provide best practices for the user experience. Organizations should consult their compliance and/or
legal partners to determine what, if any, regulatory or legal requirements may apply.

**Intended Audience**

This document is intended for professionals involved in designing, building, and managing user-permissioned data-sharing
experiences, including:

- UX/UI designers
- Product managers
- Software engineers
- Compliance and risk management professionals

**Purpose and Approach**

The UX Guidelines aim to assist implementers in:

- Accelerating design decision-making during the development of data-sharing experiences;
- Providing clarity on best practices regarding how users access, understand, and control their shared financial data; and
- Encouraging alignment with industry best practices, while allowing flexibility for adaptation based on business needs and
    regulatory considerations.


These recommendations are based on consumer research, industry collaboration, and existing implementations within the financial
services ecosystem. Insights were drawn from FDX members and organizations engaged in financial data security, user protection,
and regulatory oversight. However, these guidelines do not constitute regulatory requirements, nor do they imply an endorsement by
any regulatory body.

**How These Guidelines Relate to Other FDX Publications**

While these UX Guidelines are independent of the FDX API Specification, CSDF, and FDX Security Models, they complement these
resources by providing practical recommendations on designing user interfaces and interactions. Implementers are encouraged to
review these guidelines alongside applicable FDX technical documents for a more holistic approach to user-permissioned data
sharing.

For additional references, see the References section below.

### 1.2 SCOPE

This document describes the concepts of financial data sharing, data flow, and Data Clusters, followed by specific guidelines for an
End User grant consent journey for financial data sharing.

### 1.3 TERMINOLOGY AND CONCEPTS

Section 3 of this document describes the UX Guidelines. Two concepts are applied during the presentation of the UX Guidelines. The
top level of a user experience is presented as a **Journey**. Each journey contains a set of **Processes**.

1. **Journeys** – These capture the end-to-end view of a consent management operation, such as granting consent, refreshing
    consent, or modifying/revoking the consent.
2. **Process** – Each journey is broken up into a process that maps to a specific user goal, for example, disclosure, authentication,
    authorization, etc. Processes contain steps and options for the user to complete each goal. Each process may involve one or
    more pages that the End User may navigate, based on the implementation of that process by the entity that owns it.

For example, granting consent is a larger Journey that the End User embarks upon. The Journey contains a few Processes, for
example authorize, which is a multi-step process. During the authorize Process, an End User will complete steps to select accounts
to include in authorization. Thus, granting consent is the Journey and the act of authorizing is a Process within that Journey.


### 1.4 FDX REFERENCES

Other FDX publications that are referenced in this document include:

```
 FDX API Documentation and YAML Data Structures
 FDX Security Control Considerations for Consumer Financial Account Aggregation Services
 FDX Financial-Grade API Security Specification
 FDX Consensus Standard Data Format (CSDF)
 FDX Data Minimization Guidelines
```

## 2 DATA SHARING

This section describes the principles that guide data sharing, the concepts of data sharing and flow, the consent components
involved, and the concept of consent by business purpose.

### 2.1 PRINCIPLES GUIDING DATA SHARING EXPERIENCES

The User Experience (UX) Guidelines described herein have been derived from a number of sources, including:

```
 FDX’s core principles: Control, Access, Transparency, Traceability and Security;
 FS-ISAC’s initial work on Durable Data API (DDA) user experiences; and
 research into permissions and consent performed by The Clearing House.
```

FDX’s core principles of data sharing are defined as:

**Control**

End users should be able to consent to share their financial data for services or applications.

**Access**

End users should have access to their data and the ability to determine which entities will have access to their data.

**Transparency**

End users using financial services should know how, when, and for what purpose their data is used and only data that is required to
provide such services should be shared with the organization providing the service.

**Traceability**

All data transfers should be traceable. End users should have a complete view of all entities that are involved in the data-sharing
flow.

**Security**

Entities need to ensure the safety and privacy of data during access and transport and when that data is at rest.

These core principles help build trust in financial data sharing by providing clear, efficient, and consistent experiences for user
interactions. Informed by user research, these guidelines streamline data sharing processes while prioritizing security and privacy.


### 2.2 DATA SHARING AND FLOW

Financial data sharing describes the process by which a consumer or business entity uses an application or service to access their
own financial data available at one of their financial service providers. This flow of data can enable people and businesses to
manage and interact with their financial data using their chosen applications, experiences and services.

#### 2.2.1 Types of Financial Data

Financial data can be categorized in three ways:

1. **Primary financial data** is data associated with actual financial accounts, including balances, holdings, and transactions
    directly reflecting monetary and financial actions. There are many types of primary financial data; the most commonly
    accessed include banking and investment account data, but may also include commerce data, tax data, employment data,
    credit score data, asset information, and business accounting data, depending on the account type and user.
2. **Customer identity data** is information that can be used to uniquely identify the End User, such as name, address, email, or
    telephone number.
3. **Derived financial data** consists of observations, analysis, or models developed with primary data as an input, such as a cash
    flow analysis. Derived data may be the result of both financial and non-financial inputs.

This document will focus on the first two categories - primary financial data and customer identity data that is often included or part
of primary financial data. These currently cover the majority of financial data access products and services. Derived or secondary
financial data is often considered proprietary information.

#### 2.2.2 Parties Involved in Financial Data Sharing

For the purposes of these guidelines, the following terms are defined as:

**Consumers** : a natural person acting in their personal capacity.

**End Users** : include Consumers, individuals acting in a business capacity, and entities, such as a business or other legal entity, who
are giving permission to share their data, which may include data sharing that is outside the scope of CFPB Section 1033.

**End User Delegates** : refers to delegated persons or entities, such as End Users’ CPAs, brokers, fiduciaries and other advisors, who
have been legally authorized by the End User or other legal entity (e.g., court of law) to grant permission to share and receive the End
Users’ Financial Account Information on the End Users’ behalf.


**Data Provider (DP)** : the entity that holds End Users’ Financial Account Information, including, without limitation to banks, credit
unions, digital wallet providers and brokerages.

**Data Recipient (DR)** : service company, application (financial app), financial institution, product or service where End Users (on their
own or through their End User Delegates) manage or act on their finances, whether actively managing their finances (such as moving
money or applying for credit) or passively doing so (such as garnering recommendations or insights).

**Data Access Platform (DAP)** : intermediary that facilitates financial data access, permissioning, transit, storage and/or consent on
behalf of Data Recipients or End Users, also commonly referred to as “Data Aggregators”. In some cases, Data Access Platforms do
not have a direct relationship with the End User. The data may be passed through without modification or may be normalized in line
with permitted objectives (e.g., parsed for readability or used to confirm other data). Data Access Platforms should not be
misidentified with parties who do not obtain End Users’ consent but gather data, sometimes referred to as Data Brokers or Data
Harvesters.

**Authorized Third Party** : an entity that collects authorization from an End User to share their financial data from their Data Provider to
either the Data Recipient or a Data Access Platform performing the role of a Data Recipient. Refer to CFPB Section 1033.401, if
applicable.

#### 2.2.3 Flow of Financial Data

Financial data flows from a Data Provider (source) to the Data Recipient (requester). Data Access Platforms/End User Delegates
may be involved in one or more aspects of facilitating this flow. The financial data flow process is as follows:

1. Data sharing is often initiated with a prompt by the Data Recipient to the End User to access their accounts.
2. The End User identifies the Data Provider where the End User’s account(s) is held.
3. The Data Provider inspects the request, evaluates applicable risk-based denial considerations and, if appropriate, confirms
    the sharing of the End User’s financial data.

With this permission recorded, the Data Provider and Data Recipient exchange access details to enable the flow of financial data. In
some cases, a Data Access Platform may help facilitate the access between the Data Recipient and the Data Provider. In this
instance, the access details are exchanged between the Data Provider and the Data Recipient via the Data Access Platform.

Different entities may take on different roles based on the flow of financial data, such as:

```
 Financial Institution (Data Provider) → App (Data Recipient)
```

```
Account transaction data flows to a budgeting app where it is used to track spending by category
```
```
 Financial Institution (Data Provider) → Service Provider (Data Recipient)
```
```
Account balance data flows to a loan-provider to determine the End User’s borrowing power
```
```
 Financial Institution (Data Provider) → Aggregator (Data Access Platform) → App (Data Recipient)
```
```
Investment holdings from across multiple brokerages flow through an aggregator, which normalizes the data, to an
app where it is used to give a 360° view of assets
```
```
 Payroll Provider (Data Provider) → App (Data Recipient)
```
```
Employment information such as payroll data and W-2s flowing to a payroll, tax or loan application
```
```
 App (Data Provider) → Financial Institution (Data Recipient)
```
```
Credit score information or personal/business financial information going to a financial institution to help deliver
tailored financial services to that consumer or business
```
```
 Service Provider (Data Provider) → Financial Institution (Data Recipient)
```
```
Product recommendations based on portfolio data from across multiple financial institutions flows to a bank that can
then offer financial products to its customer
```
#### 2.2.4 The Consumer Financial Protection Bureau (CFPB) Required Rulemaking on Personal Financial Data Rights (CFPB Section 1033)

In October 2024, the Consumer Financial Protection Bureau (CFPB) established the Required Rulemaking on Personal Financial Data
Rights (CFPB section 1033). The final rule requires banks, credit unions, and other financial services providers to make consumers’
data available upon request to consumers and authorized third parties in a secure and reliable manner; defines obligations for third
parties accessing consumers’ data, including important privacy protections; and promotes fair, open, and inclusive industry

### standards. See Appendix B for additional information.


### 2.3 CONSENT COMPONENTS

A flow wherein an End User consents to the sharing of financial data should clearly articulate:

1. What entities are sharing (Data Provider) and receiving the data (Data Recipient and/or Data Access Platform, as applicable)
2. A description of the requested product(s) or service(s)
3. What data will be shared
4. How long will the data be authorized to share to deliver the specific product or service
5. How to revoke consent
6. What accounts will be needed to provide the product or service

The **Data Recipient** should describe all consent components to the End User in a clear and prominent manner. The Data Recipient
may optionally use data services provided by a Data Access Platform to convey the consent components and to manage various
parts of the consent lifecycle. The Data Recipient, or the Data Access Platform on behalf of the Data Recipient, may provide the CFPB
Section 1033 required disclosures, however the Data Recipient remains ultimately responsible for compliance with the applicable
disclosure requirements.

This consent lifecycle should allow the End User to consent to the data sharing without providing the End User’s Data Provider log-in
credentials. The components of consent include Business Purpose, Data Clusters, Duration and Account List.

#### 2.3.1 Business Purpose

When capturing consent, Data Recipients should provide a clear description of the specific product(s) or service(s) (Business
Purpose) that it provides and for which the End User is authorizing data access.

2.3.1.1 Permitted Uses Under CFPB Section 1033.421 (if applicable)

Examples of permitted uses of covered data under this section include:

1. Servicing or processing the product or service the consumer requested,
2. Uses that are reasonably necessary to improve the product or service the consumer requested,
3. Uses that are reasonably necessary to protect against or prevent actual or potential fraud, unauthorized transactions, claims,
    or other liability, and
4. Uses that are specifically required under other provisions of law, including to comply with a properly authorized subpoena or
    summons or to respond to a judicial process or government regulatory authority.


2.3.1.2 Restricted Uses of Covered Data under CFPB Section 1033.421 (if applicable)

Data Recipients are prohibited from using consumer covered data for any purpose beyond what is reasonably necessary to provide
the consumer-required product or service, and those otherwise discussed in Section 2.3.1.1, unless a separate authorization is
obtained.

Examples of uses of covered data that are not permitted as part of, or reasonably necessary to provide any other product or service,
are:

1. Targeted advertising,
2. Cross-selling of other products or services, or
3. The sale of covered data.

Note that these use cases may be permitted if the Data Recipient obtains separate authorization.

2.3.1.3 Uses of Non-covered Data

Consistent with the FDX Data Minimization Guidelines, End Users should expect that Data Recipients and Data Access Platforms will
not use consumer financial data for any purposes beyond what is reasonably necessary to provide, develop, or improve the End User
requested product or service without a separate authorization or opt-in. However, some reasonable business purposes may include,
but not limited to:

1. Use of shared data to make product recommendations where the consent disclosure explicitly describes such
    recommendations as part of the requested product or service (e.g., as part of a personal financial management advisory
    service); or
2. Instances where the requested product or service explicitly and principally involves reporting the shared data to other third
    parties that have not received direct authorization to receive the data (e.g., consumer reporting agencies as part of a credit-
    building service).

#### 2.3.2 Data Clusters

**What is a Data Cluster?**

A Data Cluster is a term used to group a functional collection of data elements. As a fundamental part of the scope of consent, the
Data Cluster is used to define what data elements will be shared when consent is granted by an End User to share their account data
with a Data Recipient. For example, the Data Cluster named ACCOUNT_DETAILED provides data elements -- such as interest rate or


last activity date – associated with an account. Standardizing Data Clusters provides a consistent definition for all parties involved.
Specifically,

1. Data Clusters help Data Recipients communicate to the End User the specific data elements needed to deliver products or
    services effectively.
2. Data Clusters help Data Providers understand which data the End User has authorized to share
3. Data Clusters help both Data Recipients and Data Providers limit the amount of data shared to only what is authorized by the
    End User

Data Clusters can be used in combination to serve as modular “building blocks”. For example, a budgeting application might require
access to both the ACCOUNT_DETAILED cluster, which includes detailed account information, and the TRANSACTIONS cluster,
which covers historical and current account transactions.

It is up to the Data Recipient to determine what data it needs and collect authorization to access that data. Multiple products and
services offered by the same Data Recipient can utilize the same Data Clusters, as long as each product or service (or Business
Purpose) is explicitly authorized by the End User and the Data Provider is notified of each authorization. For example, a Data
Recipient offering both budgeting services and mortgage application support might rely on the same ACCOUNT_DETAILED cluster
for both purposes, provided the End User has authorized each service.

**Data Cluster Uses**

It is up to all entities to disclose clear and user-friendly labeling of data elements to the End User. Ideally, clear and standardized
terms are used in common among entities. However, the guidelines do not intend to prescribe the tone and specific verbiage that
each entity should use.

The Data Recipient should list all the Data Clusters they need to access, but when providing additional description of the Data
Cluster, may choose to only display the key elements that they will use to provide their product or service.

If a Data Provider chooses to confirm consent, the requested Data Clusters should generally describe the data elements. When
providing additional description for the Data Clusters, the Data Provider may not know which key elements the Data Recipient will
need and, as such, may list all of the key elements that are included.

**Data Cluster Terminology**


Data Clusters should be represented in a consistent way for the End User, across all involved parties and throughout all flows, much
like an industry taxonomy. This provides the following benefits:

- Streamlines representation of data to be shared across Data Recipients, Data Access Platforms and Data Providers
- Improves End User understanding of data sharing when language is consistent across data sharing parties
- Facilitates interoperability across data sharing parties
- Allows Data Recipients to capture data sharing scope programmatically
- Promotes consistent language across data sharing parties
- Enables clear, mutually understood backend communication between Data Recipient, Data Access Platform (where
    applicable) and Data Provider about the scope of authorized data

**Data Cluster Components**

The table below provides a list of FDX-standardized Data Clusters. The scope of data that the Data Recipient is entitled to access
depends on the End User's authorization.

- **Data Cluster** - the enumeration included either in the communicated scope of the consent object or pre-registered for the
    Data Recipient.
- **End User-facing Label** - the name of the Data Cluster. This name should be displayed to the End User in the grant consent
    journey by all parties disclosing the scope of data requested by the Data Recipient as well as in consent management
    experiences to ensure consistency and End User understanding.
- **Included Key Elements** - a list of key data elements which should be included, either in the flow or in a more detailed
    description, such as a tool tip. Data Recipients may choose to only document the elements that they use to support their
    product or service while the Data Provider may choose to show all the suggested elements for completeness. The entity may
    provide additional commentary as needed using any tone or style they choose, as long as the prescribed Data Cluster names
    and descriptions are used consistently.

The following terms are prescribed for use in all End User-facing interactions, applications, and experiences.

**Note** : These Data Clusters are suggested to be used as included herein.


**Table 1 Data Cluster Terminology**

```
Data Cluster Read/Write End User-facing Label Included Key Elements
```
```
ACCOUNT_BASIC Read Only Account identifying information
```
- Account display name
- Masked account number
- Account type and description

```
ACCOUNT_DETAILED Read Only^
Account summary
information
```
- Account display name
- Masked account number
- Account type and description
- Account balances
- Credit limits
- Due dates and interest rates

```
BALANCES Read Only^ Account balances^
```
- Account balance
- Available balance

```
BILLS Read Only Accountinformation billing • •^ Account bill dueUpcoming payment to account^
```
```
CUSTOMER_CONTACT Read Only Account contact details
```
- Your name, address, email and phone
- Name(s), address, email and phone of any account
    holders

```
CUSTOMER_PERSONAL Read Only Sensitive personal information
```
- Your name, address, email and phone
- Name(s), address, email and phone of any account
    holders
- Your date of birth
- Government ID
**IMAGES** Read Only Check images • Check images


Data Cluster Read/Write End User-facing Label Included Key Elements

**INVESTMENTS** Read Only Investment account holding details

- All individual holding details for investment accounts such
    as stocks, mutual funds, pensions and options
- Open orders, contributions, vesting and loans

**PAYMENT_SUPPORT** Read Only Account numbers •^ Full account and routing number^

- SWIFT or IBAN numbers

**REWARDS** Read Only^
Reward program
information

- Reward membership
- Total balance
- Rewards history

**SCHEDULED_PAYMENTS** Read Only Scheduled payment information • •^ Future-Payment historydated single and recurring payments

**SOCIAL_SECURITY_NUMBER** Read Only^ Social security number^ • Social security number

**STATEMENTS** Read Only Account statements • •^ Account PDF statements containing personal Account and transaction details information^

**TAX** Read Only^ Tax form data^

- Income reported
- Taxes withheld

**TERMS_AND_CONDITIONS** Read Only Account terms and conditions

- Interest rates
- Annual percentage rates
- Finance charges
- Credit limits

**TRANSACTIONS** Read Only Transaction data

- Pending and posted account transactions
- Transaction types, amounts
- Dates and descriptions

**TRANSFERS** Read/Write Transfer information •^ Transfer history^

- Scheduled transfers


#### 2.3.3 Duration of Consent

The CFPB Section 1033 rule adds a requirement, § 1033.411(b)(6), that the authorization disclosure include a brief description of the
expected duration of data collection and a statement that collection will not last longer than one year after the consumer’s most
recent reauthorization. In order to collect covered data beyond the one-year maximum period described in § 1033.421(b)(2), the
authorized third party will obtain a new authorization (see Section 4.3 Annual Reauthorization) from the consumer no later than the
anniversary of the most recent authorization from the consumer, as described in § 1033.421(b)(3).

A Data Recipient, or a Data Access Platform acting on its behalf, should disclose to the End User the duration of the consent as part
of the consent grant journey, and they should display the consent expiration date as part of the post consent grant journey where the
user can revoke consent.

The End User’s data may only be accessed in the specific context of the product or service for which the End User has agreed to
share data as part of the authorization associated with the product or service. Further, stored data should not be used by any party
for a purpose outside the scope of the original consent or as otherwise permitted by CFPB section 1033 without a new authorization
disclosure from the End User.

If consent expires or is revoked, the Data Recipient, and the Data Access Platform, if applicable, should delete the authorized data
except as allowed by CFPB Section 1033.

**Consent Not to Exceed One Year**

Under CFPB Section 1033, the maximum consent duration is no later than the anniversary of the most recent authorization from the
consumer. The duration of the consent provides the context defining how long the Data Recipient can collect the End User’s data.
The End User has the right to revoke (or withdraw) access at the Data Recipient at any time. The Data Recipient should provide a
method of revocation in a way that is at least as easy to access and operate as the initial authorization and is free from cost or
penalties.

_Sample Maximum One-Year Time-based Consent Language_

_Your consent is valid for one year and you may withdraw your consent at any time through [Data Provider, Data Recipient, or Data Access
Platform]._

_-OR-_

_Your consent is valid for one year and will expire on [date]. You may reauthorize or withdraw your consent at any time_.


**Time-based**

Time-based consent is granted when the service provided by the Data Recipient has a discrete window needed to complete a
specific task such as applying for a loan. The authorization disclosure presented to the End User includes the duration of the data
collection (e.g., 90 days), provides a clear explanation of how long access will be granted, and should be revoked at the end of the
specified time period by the Data Recipient. Access to data after that time will require the End User to re-consent with a new
authorization disclosure unless otherwise permitted by CFPB Section 1033. The post-consent journey should also disclose when
access expires.

_Sample Time-based Consent Language_

_Your consent is valid for 3 months and you may withdraw your consent at any time through [Data Provider, Data Recipient, or Data
Access Platform]._

**One-Time Use**

One-time consent is granted for a single, discrete, and short-lived interaction. One-time use consent is tied to an explicit End User-
action or application event that requires only a single retrieval of the covered data described in the authorization disclosure, such as
identity or account verification. The expectation is that once the data has been retrieved, the consent will be revoked, preventing it
from being used again in the future, unless otherwise permitted by CFPB Section 1033.

The End User’s data may only be accessed in the context of this interaction and, typically, the data will not be stored beyond the time
required for this specific interaction to be completed. There may be instances when the data may be used and/or stored for a longer
period in order to reasonably provide the End User’s previously requested product or service. In that case, the Data Recipient should
clearly disclose to the End User the data retention length and reason. Further, and subject to limited exceptions, the stored data
should not be used for a purpose outside the scope of the original authorization without a new authorization from the End User.
Additional data may not be accessed to contextualize the original data unless otherwise explicitly authorized by the End User or
otherwise permitted by law.

_Sample One-time Consent Language_

_[Data Recipient and, if applicable Data Access Platform] will have one-time access to your account verification information at [Data
Provider] not to exceed 24 hours. [Data Recipient] shall use and retain this information for no longer than needed to verify your account._


#### 2.3.4 Account List

The Data Recipient, or Data Access Platform on its behalf, is responsible for confirming the account(s) that the End User wants to
allow access. The Data Provider will share a list of selected accounts authorized through the grant consent journey.

Some Data Providers may choose to allow the End User the opportunity to pre-select a limited set of accounts to share with the Data
Recipient. In this case, only those selected accounts will be shared to the Data Access Platform, if involved, and Data Recipient.
However, the Data Recipient may present the accounts shared to the End User and, if available, provide an opportunity to further
restrict the list of authorized accounts.

If a Data Provider supports the ability to filter accounts based on the Data Recipient’s needs (i.e., checking accounts only), the Data
Recipient should leverage this capability to provide the most effective way to ensure that the accounts it needs will be permissioned.

The End User should have the ability to view which accounts they have authorized through the third-party application.


### 2.4 LIFE CYCLE OF CONSENT

FDX, consistent with applicable laws and regulations, requires that exchange or sharing of financial or other End User data must be
authorized by the End User. Ultimately, the End User has control over who is able to access that data, subject to certain legal and
regulatory exceptions. Generally, the End User whose data flows between Data Providers and Data Recipients or Data Access
Platforms acting on behalf of the Data Recipient must give express informed consent for the stated Business Purpose by obtaining
an authorization disclosure signed by the End User electronically or in writing.

Except under limited legal and regulatory exceptions, data sharing must be **explicitly** authorized by the End User. Changes to what
data is included in the authorization disclosure require completion of a new authorization disclosure by the End User.

While the authorization disclosure itself provides authorization for a maximum duration, the user experience of data sharing
generally takes place in three discrete phases:

```
 Grant Consent
 Manage Consent
 Revoke Consent
```
#### 2.4.1 Grant Consent

Granting consent is the process of **establishing the terms of data access** between a Data Provider (e.g., financial institution) and a
Data Recipient (e.g., financial application). A Data Access Platform, acting on behalf of either a Data Provider and/or a Data
Recipient, may also be involved. An authorization disclosure signed by an End User contains the terms of the consent granted by the
End User.

The process to grant consent is generally initiated from within the Data Recipient experience.

The Data Recipient is responsible for defining the types of data, or Data Clusters, needed to support the Business Purpose(s)
presented to the End User. A Data Access Platform may also be involved in defining the relevant terms, but the Data Recipient
remains ultimately responsible. If the End User wants to use the service offered by the Data Recipient, they must consent to making
available the data required to do so. Among other things, the Data Recipient should provide an authorization disclosure to the End
User that includes, clearly and conspicuously and segregated from other materials:

- All entities that will be accessing the data shared by this authorization (Data Provider, Data Recipient, Data Access Platform if
    applicable);


- a list of the product(s) and/or services(s) that requires access to the End User’s data;
- an explanation of the categories of data (Data Clusters) needed to provide the requested product(s) and/or service(s);
- a brief description of the expected duration of data collection;
- a description of the revocation method; and
- a statement that collection will not last longer than one year after the End User’s most recent authorization.

During the consent process, the End User directs the Data Provider what accounts to share with the Data Recipient and/or the Data
Access Platform acting on behalf of the Data Recipient.

During the consent process, the Data Provider has the option, but is not required, to confirm the authorization collected by the Data
Recipient, or Data Access Platform acting on the Data Recipient’s behalf, directly with the End User. CFPB Section 1033 requires the
Data Provider to make available covered data when it receives, among other things, information sufficient to document the Data
Recipient (or the Data Access Platform acting on the Data Recipient’s behalf) has followed the required authorization procedures. If
confirmation is done, the Data Provider MAY display (1) the categories of covered data the third party is requesting and (2) the
accounts to which the Data Recipient is seeking access. If this is done, the Data Provider MAY implement session-based account
type and cardinality filtering to align the End User’s account selection options with the use case of the Data Recipient.

Consent for financial or other data access is granted by one End User to a Data Recipient, for:

- a specific set of categories of covered data (e.g., Data Clusters),
- to provide the requested Business Purpose(s),
- for a specific list of accounts held by a Data Provider,
- for a specified period of time,
- and includes a certification statement.

#### 2.4.2 Manage Consent

**Managing consent** describes the process that allows the End User to **view and control** that consent through its lifecycle. Once the
Data Recipient obtains authorization to access covered data on the End User’s behalf, it should provide a copy of the authorization
disclosure to the End User or make it available in a location readily accessible to the End User. If in a readily accessible location, it
should be accessible until the Data Recipient’s access terminates.

CFPB Section 1033 requires that any changes, other than revocation, as discussed below, to the End User’s consent must be initiated
by the End User at the Data Recipient, or Data Access Platform, as applicable. Other than revocation, the Data Provider should not
permit changes to the scope of consent that was granted.


#### 2.4.3 Revoke Consent

**Revoking consent** is the process of **removing the access** between a Data Provider and a Data Recipient, and/or a Data Access
Platform acting on behalf of the Data Recipient, if applicable.

Access can be revoked from the Data Provider or the Data Recipient and/or the Data Access Platform acting on behalf of the Data
Recipient, if applicable. If consent is revoked from any party, then all parties involved must also stop accessing the data, as
applicable, and endeavor to synchronize their partners and Data Access Platforms that a consent has been revoked.

#### 2.4.4 Reauthorize Consent

**Reauthorize consent** is the process of **extending the expiration of an existing active consent** , which may also require re-
authentication with the Data Provider.

The End User initiates reauthorization through the Data Recipient, or a Data Access Platform acting on behalf of the Data Recipient.
Regardless of the process, the Data Recipient is responsible for compliance with the requirements of CFPB Section 1033. Based on
prearrangement with the Data Provider, the Data Recipient, or Data Access Platform acting on their behalf, is permitted to
communicate the new expiration date to the Data Provider or will redirect the End User to authenticate at the Data Provider to
complete the reauthorization process. The Data Provider may choose to confirm the reauthorization, or not, before returning to the
Data Recipient.


## 3 USER EXPERIENCE GUIDELINES

These guidelines provide recommendations for how manage the user experience that allows an End User to grant consent to share
their financial data from a Data Provider to a Data Recipient with or without the use of a Data Access Platform.

In the Financial Data-sharing ecosystem, there are three fundamental integrations involving the Data Recipient, Data Access Platform
and Data Provider:

1. **Data Recipient Authorization (DR-DP Direct)** in which the Data Recipient connect directly to the Data Provider without the use
    of a Data Access Platform. In this case, the Data Recipient collects the authorization from the End User.
2. **Data Access Platform Authorization (DR-DAP-DP)** in which the Data Recipient contracts with a Data Access Platform to
    collect and manage consent on its behalf, and
3. **Data Recipient Authorization using a Data Access Platform (DR-DAP-DP)** in which the Data Recipient collects the
    authorization from the End User but contracts with a Data Access Platform to provide a passthrough functionality to support
    Data Provider selection and integration.

While the basic steps of the Grant Consent Journey are the same for all three, the responsibility and order of the process steps varies
slightly based on the integration. The sections below describe the flows in more detail. The flow diagrams in each section illustrate
which role is responsible for each step and what each step should accomplish.

```
Note : The process steps shown in the flows below are high level and not intended to be equivalent to a “page” or intended to
require a certain number of screens shown to the End User in the flow. The sample screenshots and content are meant to
illustrate the concept, not to imply or suggest a solution.
```

### (DR-DAP-DP) 3.1 GRANT CONSENT JOURNEY: DATA RECIPIENT AUTHORIZATION USING A DATA ACCESS PLATFORM TO FACILITATE THE CONNECTION TO A DATA PROVIDER

### Access Platform to facilitate the connection to a Data Provider (DR-

### DAP-DP)

The journey shown below reflects the recommended End User experience when the Data Recipient connects to a Data Provider
directly without the use of a Data Access Platform. They are intended to illustrate who may be responsible for each step but is not
necessarily indicative of the number of pages required by either the Data Provider or the Data Recipient.

Refer to Table 1 Data Cluster Terminology on page 17 for FDX recommendations on Data Cluster terminology.

The consent journey may also include authorizations that are subject to CFPB Section 1033.

```
Note : The process steps shown in the flows below are high level and not intended to be equivalent to a “page” or intended to
require a certain number of screens shown to the End User in the flow. The sample screenshots and content are meant to
illustrate the concept, not to imply or suggest a solution.
```


#### 3.1.1 Initiate - Sample User Content

```
The Data Recipient should clearly indicate to the End User that a
process to authorize access to data from a Data Provider is being
initiated.
```
```
FDX recommendations:
```
- Explain how the process works
- Provide a path to learn more
- State that this connection is directly with their Data Provider
- Provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.1.2 Select Data Provider – Sample User Content

```
The Data Recipient should provide an easy to navigate selection
screen for all available Data Providers.
```
```
FDX recommendations:
```
- Provide a way for the user to search for their Data Provider
- Provide quick links to common Data Providers
- Provide an option to cancel the flow
- Clearly inform the End User that they are going to be redirected
    to the Data Provider

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.1.3 Authorize – Sample User Content

```
The Data Recipient should provide the End User with an authorization
disclosure that is clear, conspicuous, and segregated from other
material and contains the following elements. It should be provided
electronically (or in writing) and be signed by the customer
electronically (or in writing).
FDX recommendations:
```
- Provide a clear and conspicuous authorization disclosure.
- Include the name of the Data Recipient
- Include the name of the Data Provider
- Include a brief description of the product or service and a statement
    that the third party will collect, use, and retain the End User’s data
    only as reasonably necessary to provide that product or service
- Include the Data Clusters that will be accessed
- Include a certification to comply with applicable open banking
    requirements
- Include the duration for which data will be collected, not to exceed
    one year from the date of the most recent reauthorization
- Include a description of the method for a user to revoke access
- Obtain express informed consent that is electronically signed by the
    user
- Ensure that the authorization disclosure is in the same language as
    the language in which it was conveyed to the user. If the
    authorization disclosure is not in English, include a link to an
    English-language translation.

#### *Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences.


#### 3.1.4 Authenticate – Sample User Content

```
Provide a familiar and easy way for the user to
authenticate at the Data Provider.
FDX recommendations:
```
- The Data Provider should authenticate the End User
    using the same branding they would see on the
    Data Provider’s consumer data access portals
- The Data Provider should allow for biometric
    authentication, when available
- The Data Provider should provide a path to exit the
    flow without logging in

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.1.5 Confirm Authorization (Optional) – Sample User Content

```
The Data Provider is permitted to confirm the scope of
the authorization disclosure directly with the End User.
This includes:
```
- Allow the End User to select the accounts they want
    to share from an eligible account list. See Appendix
    on page 73 for additional details and sample user
    content
- Provide a clear summary of the Data Clusters that
    will be accessed with the ability to view more
    details
**FDX recommendations:**
- If known, state how long this consent will be active
- Provide a clear call to action (CTA)
- Do not permit alterations to the details of the
authorization
- Identify the name of the Data Recipient
- Inform the End User that, upon completion, they will
be logged out of the Data Provider and returned to
the Data Recipient
- Provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.1.6 Select Accounts – Sample User Content

```
The Data Recipient should display, at a minimum, the accounts which are
applicable to the use case and allow the End User to select which
accounts at the Data Provider to share.
FDX recommendations:
```
- Clearly indicate that the End User has returned to the Data Recipient
- Show the list of eligible accounts provided by the Data Provider
- Provide an easy way to select which accounts will or will not be shared
- Provide a quick way to select or deselect all accounts to be shared
- Provide a clear call to action
- Provide a path to cancel the flow without consent

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.1.7 Complete – Sample User Content

```
Give a clear indication that the data sharing consent has been
established and that the journey is complete.
FDX recommendations:
```
- Indicate success or reason for failure, if applicable
- Confirm the list of accounts that the End User has consented to
    share
- Provide an indication that consent can be updated or unlinked at
    any time by the End User (optional, best practice)
- Provide direction for next steps

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


### 3.2 CONSENT GRANT JOURNEY: DATA ACCESS PLATFORM AUTHORIZATION (DR-DAP-DP)

Data Recipients and/or Data Providers may elect to use Data Access Platforms to facilitate data sharing and perform the
authorization procedures on the Data Recipient’s behalf. The Data Recipient is responsible for compliance with CFPB Section 1033.
The prescribed journey shown below reflects the recommended information and functionality provided by the Data Recipient, Data
Access Platform, and Data Provider, respectively, when the Data Access Platform performs the authorization procedures. This
section is intended to show the various interactions, but not necessarily indicative of the number of pages needed to address the
various requirements of CFPB Section 1033.

This journey illustrates a consent journey in which the Data Access Platform performs the authorization procedures in lieu of the
Data Recipient. The authorization disclosure should be created, hosted, and managed by the Data Access Platform to ensure that the
Data Access Platform can fulfill its obligations to both Data Recipient and Data Provider and meet its own responsibilities under
CFPB Section 1033.

Refer to Section 3.3 for the journey in which the Data Recipient collects the authorization from the End User on the platform hosted
by the Data Access Platform.

Refer to Table 1 Data Cluster Terminology on page 17 for FDX recommendations on Data Cluster terminology.

The consent journey may also include authorizations that are subject to CFPB Section 1033.

```
Note : The process steps shown in the flows below are high level and not intended to be equivalent to a “page” or intended to
require a certain number of screens shown to the End User in the flow. The sample screenshots and content are meant to
illustrate the concept, not to imply or suggest a solution.
```


#### 3.2.1 Initiate - Sample User Content

```
The Data Recipient and/or Data Access Platform
should clearly indicate to the End User that a process
to authorize access to the End User’s data through
one of their service providers is being initiated, and
identify the parties involved.
```
```
FDX recommendations:
```
- Preview to the End User what they are going to do
- Identify the Data Recipient and Data Access
    Platform
- Provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.2.2 Select Data Provider - Sample User Content

```
The Data Access Platform should provide an easy to navigate selection
screen for all available Data Providers.
```
```
FDX recommendations:
```
- Provide a way for the End User to search for their Data Provider
- Provide quick links to common Data Providers
- Provide an option to cancel the flow
- The Data Access Platform should inform the user that they are going
    to be redirected to the Data Provider

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.2.3 Authorize - Sample User Content

```
The Data Access Platform should provide the End User with an
authorization disclosure that is clear, conspicuous, and segregated
from other material and contains the following elements. It should be
provided electronically (or in writing) and be signed by the customer
electronically (or in writing).
FDX recommendations:
```
- Include the name of the Data Recipient
- Include the name of the Data Access Platform
- Include the name of the Data Provider
- A brief description of the product or service and a statement that
    the third party will collect, use, and retain the End User’s data only
    as reasonably necessary to provide that product or service.
- Include the Data Clusters that will be accessed
- Include a certification that the Data Recipient will comply with
    applicable open banking law
- Include a certification that the Data Access Platform will comply
    with applicable open banking requirements
- Include the duration for which data will be collected, not to exceed
    one year from the date of the most recent reauthorization
- Include a description of the method for a user to revoke access
- Ensure that the authorization disclosure is in the same language as
    the language in which it was conveyed to the user. If the
    authorization disclosure is not in English, include a link to an
    English-language translation.

#### *Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences.


#### 3.2.4 Authenticate - Sample User Content

```
Provide a familiar and easy way for the End User to
authenticate at the Data Provider.
FDX recommendations:
```
- The Data Provider should authenticate the End User
    using the same branding they would see on the
    Data Provider’s consumer data access portals
- The Data Provider should allow for biometric
    authentication, when available
- The Data Provider should provide a path to exit the
    flow without logging in

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.2.5 Confirm Authorization (Optional) – Sample User Content

```
The Data Provider is permitted to confirm the scope of the authorization
disclosure directly with the End User. This includes:
```
- Allow the End User to select the accounts they want to share from an
    eligible account list. See Appendix A for additional details and sample
    user content
- Provide a clear summary of the Data Clusters that will be accessed
    with the ability to view more details
**FDX recommendations:**
- If known, state how long the consent will be active
- Provide a clear call to action (CTA)
- Do not permit alternations to the details of the authorization
- Identify the name of the Data Recipient
- Inform the End User that, upon completion, they will be logged out of
the Data Provider and returned to the Data Recipient
- Provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.2.6 Select Accounts – Sample User Content

```
The Data Access Platform should display, at a minimum, the accounts
which are applicable to the use case and allow the End User to select
which accounts from the Data Provider to share.
FDX recommendations:
```
- Clearly indicate that the End User has returned to the Data Access
    Platform
- Show the name of the Data Recipient who will be accessing the data
- Show the list of eligible accounts to share
- Provide an easy way to select which accounts will or will not be
    shared
- Provide a quick way to select or deselect all accounts to be shared
- Provide a clear call to action
- Provide a path to cancel the flow without consent

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 3.2.7 Complete – Sample User Content

```
The Data Recipient and/or Data Access Platform
should give a clear indication that the data sharing
consent has been established and that the journey is
complete.
FDX recommendations:
```
- Indicate success or reason for failure, if applicable
- Clearly indicate that they have returned to the Data
    Recipient, once redirected
- Provide an indication that consent can be managed
    by the user
- Provide direction for next steps

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


### 3.3 GRANT CONSENT JOURNEY: DATA RECIPIENT AUTHORIZATION USING A DATA ACCESS PLATFORM (DR-DAP-DP)

Data Recipients may utilize another third-party (such as a Data Access Platform) to facilitate the connection to the Data Provider but
maintain the responsibility of properly obtaining the required authorization disclosure from the End User. In this journey the Data
Recipient provides the authorization disclosure to the End User and includes a disclosure that a Data Access Platform is part of the
data exchange.

In the section 3.2 flow, the Data Recipient utilizes a Data Access Platform on the back end to manage the Authorization process in
addition to providing a connection to the Data Provider. In this section, the Data Access Platform provides the Data Recipient with a
list of Data Providers so that the Data Recipient can host the Data Provider selection and manage Authorization step directly. The
Data Recipient then uses basic Data Access Platform passthrough functionality to redirect to the Data Provider and the
corresponding response. The Data Recipient remains responsible for compliance with CFPB Section 1033, as applicable.

The Data Recipient should clearly disclose the authorization disclosure to obtain the End User’s express informed consent to access
data. The Data Recipient’s branding should be used on the authorization screen. The journey follows the same steps as shown in
section 3.2 Consent Grant Journey: Data Access Platform Authorization with the Data Recipient branding on the authorization
screen.

The Data Recipient also hosts the post-consent grant mechanisms for the End User to view and revoke consent through the Data
Recipient application.

Refer to Table 1 Data Cluster Terminology on page 17 for FDX recommendations on Data Cluster terminology.

The consent journey may also include authorizations that are subject to CFPB Section 1033.

```
Note : The process steps shown in the flows below are high level and not intended to be equivalent to a “page” or intended to
require a certain number of screens shown to the End User in the flow. The sample screenshots and content are meant to
illustrate the concept, not to imply or suggest a solution.
```


#### 3.3.1 Data Recipient Authorization - Sample User Content

When the Data Recipient provides the authorization disclosure to the End User, the Data Recipient branding will be used on the
authorization disclosure screen and should identify the Data Access Platform involved in the data exchange.

```
The Data Recipient should provide the End User with an authorization
disclosure that is clear, conspicuous, and segregated from other
material and contains the following required elements. It should be
provided electronically (or in writing) and be signed by the customer
electronically (or in writing).
```
```
FDX recommendations:
```
- Include the name of the Data Recipient
- Include the name of the Data Access Platform
- Include the name of the Data Provider
- A brief description of the product or service and a statement that
    the third party will collect, use, and retain the End User’s data only
    as reasonably necessary to provide that product or service.
- Include the Data Clusters that will be accessed
- Include a certification that the Data Recipient will comply with
    applicable open banking requirements
- Include a certification that the Data Access Platform will comply
    with applicable open banking requirements
- Include the duration for which data will be collected, not to
    exceed one year from the date of the most recent reauthorization
- Include a description of the method for a user to revoke access
- Ensure that the authorization disclosure is in the same language
    as the language in which it was conveyed to the user. If the
    authorization disclosure is not in English, include a link to an
    English-language translation.
_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


## 4 POST CONSENT GRANT JOURNEY

This section describes the requirement to provide the authorization disclosure to the End User and consent management
requirements.

### 4.1 NOTIFICATION

**Purpose – A Data Recipient (or Data Access Platform acting on behalf of a Data Recipient) is required to provide (or make
available) to the End User a copy of the signed authorization disclosure that reflects the date of the End User’s signature**

A Data Recipient may meet this requirement by sending a durable notification back to the End User via a previously established out-
of-band mechanism, such as email. This may provide additional assurance to the End User of completion of the authorization
process for data sharing and gives an opportunity for End Users to identify unauthorized or unintended access authorizations. The
notification also delivers a verification experience consistent with industry practices and other consumer services.

A Data Recipient may also meet this requirement by making a copy of the authorization disclosure signed by the End User, reflecting
the date of the End User’s signature, in a location that is readily accessible to the End User, such as the Data Recipient’s interface. If
the Data Recipient makes the authorization disclosure available in such a location, the Data Recipient should provide access to the
End User until the Data Recipient’s access to the covered data terminates.

**Various Recommended Notices and Options**

```
 Notify the End User when they have successfully revoked authorization to share data
 The Data Recipient (or Data Access Platform acting on behalf of a Data Recipient) may allow an option for the End User to
choose the method for providing the authorization disclosure to include:
o Email (available for delivery of the signed copy of the authorization disclosure or in a readily accessible location)
o Text message (available if the signed authorization disclosure is available in a readily accessible location)
o Push notification to their application (available if the signed authorization disclosure is available in a readily
accessible location)
 The Data Provider has the option to notify the End User that changing their password at the Data Provider will not revoke
previously provided data access authorization(s)
```
.


#### 4.1.1 Notification - Sample User Content

```
Sample Email
Sample Text Message
```

### 4.2 CONSENT MANAGEMENT AND DASHBOARDS

**Purpose – Once an End User has completed the authorization disclosure allowing the Data Recipient to access covered data from a
Data Provider (via the Data Recipient or the Data Access Platform on its behalf), the Data Recipient (and/or the Data Access
Platform on its behalf, as applicable) should provide a method for the End User to revoke the authorization that is as easy to
access and operate as the initial authorization.**

#### 4.2.1 Overview

CFPB Section 1033 requires the Data Recipient (and/or the Data Access Platform on behalf of the Data Recipient, as applicable) to
provide End Users with a method to revoke the Data Recipient’s authorization to access the End User’s covered data that is as easy
to access and operate as the initial authorization.

```
Note : Data Access Platforms who capture the authorization from the End User on behalf of the Data Recipient are included in
this requirement.
```
FDX refers to this interface as a Consent Dashboard. This section describes guidelines and requirements for the Consent Dashboard
of each entity.

**Use Case-based or Entity-based Consent Management**

The authorization provided by the End User can be managed by the Data Recipient (and/or the Data Access Platform on behalf of the
Data Recipient) for a specific product or service or at the Data Provider level. These constructs are independent from the access
token used in place of the digital credentials of the OAuth flow.

For a Data Recipient (and/or the Data Access Platform on behalf of the Data Recipient) Consent Dashboard, it is up to such entity to
determine the granularity to view and provide the End User the ability to revoke access via the Consent Dashboard.

Generally, FDX recommends that the Consent Dashboard include these details about the End User’s authorization on the Consent
Dashboard

```
o Entity Name(s) (Data Provider connected for the authorization and/or Data Access Platform, as applicable)
```
```
o List of the accounts from which data is collected
```
```
o Data Clusters used
```

```
o Authorization expiration date
```
```
o Product or service aligned to the data sharing
```
**Consent Revocation**

The Data Recipient (and/or the Data Access Platform on behalf of the Data Recipient) must provide the End User with the ability to
revoke consent. Once revoked, the Data Recipient (and/or the Data Access Platform on behalf of the Data Recipient) should notify
the Data Provider, any Data Access Platform, and other third parties that have been provided the End User’s covered data of the
revocation, as applicable. In a similar manner, if a Data Provider receives a request to revoke consent, it should notify the Data
Recipient (and/or the Data Access Platform on behalf of the Data Recipient) of such revocation. This allows the Data Provider, to
stop sharing the covered data and requires the other entities – the Data Recipient and, if applicable, the Data Access Platform, or any
other third parties to (1) no longer collect covered data and (2) no longer use or retain covered data previously collected, unless the
previously-collected data remains reasonably necessary to provide the product or service for which the data was collected.

If the user chooses to revoke consent via the Data Provider and the Data Provider provides an option to do so, the Data Provider may
provide a full revocation for all the data shared across all Data Recipients and/or Data Access Platforms (e.g., a master “kill switch”),
across all authorizations received from a specific Data Recipient and/or Data Access Platform, or as to all the data made available
for a specific authorization from a Data Recipient. The Data Provider, however, does not manage and cannot provide a revocation
method for individual Data Clusters used by the Data Recipient or Data Access Platform associated with a specific authorization or
authorizations.

The options for consent revocation at the Data Recipient or Data Access Platform include:

```
a) Use-case based revocation: the ability to revoke consent for a specific product or service (purpose) where covered data is
being used.
b) Entity-based full revocation: the ability to revoke all access whereby the end user access to the data provider, which may
result the access token being removed.
```

**Entity Notification of End User Revocation**

The entity capturing the revocation of the End User’s authorization to share covered data has obligations to notify other entities,
depending on the situation, and should implement a mechanism to notify other parties. If the End User revokes consent through the
Data Provider, the Data Provider should inform the Data Recipient in a timely manner but is not obligated to inform the Data Access
Platform of the End User’s revocation. The notified parties should act upon the notification and take any necessary actions to ensure
that the End User receives a consistent user experience, and that there is transparency and traceability of any change actions.

If changes originate from a Data Recipient, the End User may need to repeat steps of the original consent journey, for example to add
or update their accounts used in the product. However, the method used to revoke should be as easy to access and operate as the
initial consent. Data Recipients should redirect the End User to the appropriate place in the consent journey if they choose to make
changes to their previously authorized accounts from the Data Provider or Data Access Platform.


#### 4.2.2 Consent Dashboard at the Data Provider (Optional)

While CFPB Section 1033 does not require that the Data Provider have a Consent Dashboard, some Data Providers may wish to
present a list of all third parties that have access to the End User’s account data. FDX recommendations for a Data Provider Consent
Dashboard are included below.

4.2.2.1 View Consent from a Data Provider – Sample User Content

```
View Consent from a Data Provider
```
```
If the Data Provider chooses to present a Consent Dashboard, it should
include:
```
- The entities to which the data is being shared
- The Data Access Platform if involved in the consent; provide access to
    additional information about the Data Access Platform and its role,
    including links if possible
- The maximum duration of consent, which can be no more than on year
    after the End User’s most recent authorization, and the date that the
    current consent was granted. If the End User reauthorized the Data
    Recipient’s accessing covered data, then the new expiration date should
    be displayed
- The accounts authorized under the current authorization disclosure
- The Data Clusters that are being shared for the accounts authorized
    under the current authorization disclosure. Refer to Table 1 (Section
    2.3.2 Data Clusters) for how to best disclose the included Data Clusters
- The Consent Dashboard should be accessible at all times, excluding
    reasonable downtimes for maintenance
- As a best practice, prior authorizations, or a link to prior authorizations
    that have expired or have been revoked within a timeframe consistent
    with the Data Provider’s data retention policy may be displayed along
    with the date of expiration/revocation

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.2.2.2 Edit from a Data Provider

A Data Provider may only allow the End User to fully revoke an authorization (i.e., not permit modifications to the Data Clusters or
duration other than a full revocation). See section 4.2.4.2 Edit from a Data Recipient for more information about partial modification
of an existing authorization disclosure.

If the End User would like to modify portions of the authorization disclosure, FDX recommends that the Data Provider refer the End
User back to the Data Recipient and/or Data Access Platform to initiate any modifications to the authorization disclosure, as
applicable.

If an account, previously authorized by the End User to share covered data is no longer available to the End User at the Data Provider,
for whatever reason (e.g., closed accounts, accounts in bad legal status, etc.), the Data Provider should create a record
substantiating the basis for the denial and provide a response to the Data Recipient or Data Access Platform acting on behalf of the
Data Recipient the types of information denied, if applicable, and the reason(s) for denial.


4.2.2.3 Revocation from a Data Provider – Sample User Content

If the Data Provider provides a Consent Dashboard, FDX recommends that the Data Provider allow End Users have the following
revocation functionality.

```
Revocation from a Data Provider Consent Dashboard
```
```
End Users’ functionality from a Data Provider Consent
Dashboard could include:
```
- Immediate revocation of all authorizations for all Data
    Recipients and the Data Access Platforms that support
    them.
- Immediate revocation of one or more authorizations for a
    specific Data Recipient and the Data Access Platform that
    supports it, if applicable.
- If the Data Provider is aware of material impacts from the
    revocation, FDX recommends the Data Provider disclose to
    the End User those potential impacts prior to allowing
    revocation, as applicable.

#### *Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences.


#### 4.2.3 Consent Dashboard at the Data Access Platform

4.2.3.1 View Consent from a Data Access Platform Consent Dashboard – Sample User Content

```
View Consent from a Data Access
Platform Dashboard
```
```
FDX recommendations:
```
- The Consent Dashboard
    should be accessible at all
    times, subject to reasonable
    maintenance schedule
- The Data Recipients with
    which data is being shared
- The Data Providers from which
    data is being shared
- The accounts authorized
- The Data Clusters authorized
- The business purpose(s)
    included in the authorization
    disclosure that describes why
    the data is being shared with
    the Data Recipient
- Prior authorizations or a link to
    prior authorizations that have
    expired or have been revoked
    should be displayed, along
    with the date of expiration /
    revocation.
_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.2.3.2 Revocation from a Data Access Platform - Sample User Content

A Data Access Platform that includes the ability for an End User to revoke authorization from the Consent Dashboard, either on
behalf of a Data Recipient or for the Data Access Platform itself, should provide a method for revocation that is as easy to access
and operate as the initial authorization. If the Data Access Platform receives a revocation request from an End User, it should notify
the Data Provider, the Data Recipient, and any other third parties, if applicable.

```
Revocation from a Data Access Platform Dashboard
```
```
FDX recommendations:
```
- Provide a path for the End User to immediately
    revoke all access to their data and/or data for any
    Data Recipient for which access was facilitated by
    the Data Access Platform.
- As a best practice, any revocation of consent should
    be passed to any parties within the scope of the
    revocation.
- If the Data Access Platform is aware of material
    impacts from the revocation, FDX recommends the
    Data Access Platform disclose to the End User those
    potential impacts prior to allowing revocation, as
    applicable.

(^)
_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 4.2.4 Consent Dashboard at the Data Recipient

4.2.4.1 View Consent from a Data Recipient – Sample User Content

```
View Consent from Data Recipient Dashboard
End Users should be able to view the following from
a Data Recipient Consent Dashboard:
FDX recommendations:
```
- The Data Provider and what accounts have been
    authorized under an authorization disclosure
    from the End User
- The covered data (Data Clusters) that are being
    shared for the authorized accounts. Refer to
    Table 1 (Section 2.3.2 Data Clusters) for how to
    best disclose the included Data Clusters.
- Disclose if a Data Access Platform is involved.
    Provide access to additional information about
    the Data Access Platform and its role, including
    links if possible.
- Disclose the Business Purposes or name of the
    specific products and/or services provided in the
    authorization disclosure, such as budgeting or a
    mortgage application.
- Specify the exact date that the authorization will
    expire, which cannot exceed one year from the
    most recent authorization. If the End User has
    reauthorized, then the new expiration date should
    be displayed.
- Recommended: Provide a notification to the End
    User at least 30 days prior to authorization
    expiration to remind the End User to reauthorize
    access

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.2.4.2 Edit from a Data Recipient – Sample User Content

CFPB Section 1033 does not address the End User’s ability to edit the authorization, but does include a few rules related to
increasing covered data and the obligations of third parties (Data Recipients or Data Access Platforms managing consent on behalf
of a Data Recipient).

Any End User-initiated changes to the original consent should be treated as a new authorization or a re-authorization, depending on
the specific changes made. If the End User seeks to make a change, they should follow the consent grant journey to make scope
changes resulting in an increase or decrease in scope or addition of a new account(s) being authorized from the Data Provider. If a
Data Access Platform is managing authorizations on behalf of the Data Recipient, then the DAP may need to provide the ability for
the End User to make scope changes or add accounts to the authorization specific to a given Data Recipient.

**Examples of changes made by the End Users on the Data Recipient Dashboard**

- End User wants to authorize the Data Recipient to use their data for a new Business Purpose (use case) using **same Data**
    **Clusters** as the previously authorized use. The Data Recipient should collect a new authorization to use the same data for the
    new Business Purpose. This authorization should be communicated to the other entities involved.
- Data Recipient requires additional data ( **new or different Data Clusters** ) for the existing or new business purpose, the Data
    Recipient must provide a new authorization by sending the End User through the consent journey. This requires a new
    authorization disclosure from the End User. This would generate a new authorization expiration date, based on the expected
    duration identified in the authorization disclosure, and a Data Provider may require the End User to confirm the authorization
    prior to making the additional data available.
       - If the Data Provider presents the grant consent flow for an active authorization disclosure, the Data Provider may, but
          is not required to, indicate which accounts were previously selected and allow the End User to add and/or remove
          accounts as they choose.
- End User wants to authorize the Data Recipient to access additional account(s) not previously authorized. This generally
    requires the End User to go through the consent journey and provide a new authorization disclosure to include the additional
    account(s). This action may also update the authorization expiration date, if the authorization disclosure provided an updated
    duration statement. A Data Provider may require the End User to confirm the authorization prior to making the data
    associated the additional account(s) available.


Prior to the one-year authorization expiration, if the End User wants to extend the same authorization for the Data Recipient to
continue accessing their data, then the End User should be taken through the reauthorization journey. A Data Provider may require
the End User to confirm the authorization prior to making the additional data available. See section 0

- Annual Reauthorization.

```
Edit Consent from a Data Recipient
```
```
End Users should be able to take the following
actions from a Data Recipient Consent Dashboard.
```
```
FDX Recommendations:
```
- The ability to add or remove accounts; this should
    trigger an update through the Grant Consent flow
- Provide reauthorization beyond the maximum
    duration (one year from the End User’s most
    recent authorization); this should trigger an
    update through the Grant Consent flow
- Ability to revoke all access
- Ability to revoke consent to a specific Business
    Purpose (use case-based), e.g. PFM, Targeted
    Marketing, Tax Services; based on the scope of
    the authorization, this may require an updated
    authorization to the Data Provider via the grant
    consent journey

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.2.4.3 Revocation from a Data Recipient Consent Dashboard – Sample User Content

The method of revocation should be as easy to access and operate for the End User to stop sharing their data from a Data Provider
as the initial authorization to share data. If an End User revokes consent through the Data Recipient Consent Dashboard, the Data
Recipient should no longer collect data and notify the Data Provider, the Data Access Platform and any other third parties to whom
the Data Recipient has provided the End User’s covered data.

```
Revocation of Consent from a Data Recipient
Consent Dashboard
```
```
FDX Recommendations :
```
- Immediate revocation of all access to the End
    User’s data.
- If the Data Recipient is aware of material
    impacts from the revocation, FDX
    recommends the Data Recipient disclose to
    the End User those potential impacts prior to
    allowing revocation, as applicable.
- Optionally, provide use case-level
    authorization revocation capability. If the End
    User has consented to multiple Business
    Purposes, (e.g. PFM and Tax Services) then
    the Data Recipient should provide the ability
    to opt-out of each, without revocation of the
    entire authorization. This would be
    considered an Edit Consent. See section
    4.2.4.2 Edit from a Data Recipient

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


### 4.3 ANNUAL REAUTHORIZATION

#### 4.3.1 Overview

For a Data Recipient to collect data beyond the one-year maximum period, the Data Recipient (or a Data Access Platform acting on
behalf of a Data Recipient) must obtain a new authorization from the End User. The Data Recipient should communicate the new
authorization end date to the Data Provider with or without requiring reauthentication at the Data Provider, based on the bilateral
agreement between the Data Recipient, or the Data Access Platform on its behalf. This section includes FDX’s best practices for
reauthorization though a direct connection with the Data Recipient or an indirect connection via a Data Access Platform.


#### 4.3.2 Direct Connection Data Recipient Reauthorization with Optional Data Provider Confirmation

4.3.2.1 Initiate Reauthorize at Data Recipient- Sample User Content

```
The Data Recipient should allow the user to view their active Consents
and provide a path to initiate reauthorization.
```
```
FDX recommendations:
```
- Display the active Consents (Authorizations) per Section 4.2.4.1.
- Clearly identify the authorizations that need to be reauthorized
- Provide a path for the user to initiate the reauthorization journey

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.2.2 Reauthorize at the Data Recipient- Sample User Content

```
The Data Recipient should provide the End User with an authorization
disclosure that is clear, conspicuous, and segregated from other material
and contains the following required elements. It should be provided
electronically (or in writing) and be signed by the customer electronically
(or in writing).
FDX recommendations:
```
- Include the name of the Data Recipient
- Include the name of any Data Access Platform
- Include the name of the Data Provider
- Include a brief description of the product or service and a statement
    that the third party will collect, use, and retain the End User’s data
    only as reasonably necessary to provide that product or service
- Include the Data Clusters that will be accessed
- Include a certification to comply with applicable open banking law
- Include the duration for which data will be collected, not to exceed
    one year from the date of the most recent reauthorization
- Include a description of the path for a user to revoke access
- The authorization disclosure should be in the same language as the
    language in which it was conveyed to the user. If the authorization
    disclosure is not in English, it should include a link to an English-
    language translation.

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.2.3 Authenticate at the Data Provider (Optional) - Sample User Content

```
The Data Provider has the option to require
reauthentication as part of the reauthorization journey,
similar to the process used for the original
authorization, and should provide a familiar and easy
way for the End User to authenticate.
FDX recommendations:
```
- The Data Recipient should inform the End User that
    they are going to be redirected to the Data Provider
- The Data Provider should authenticate the End User
    using a familiar login page
- The Data Provider should allow for biometric
    authentication when available
- Both the Data Recipient and Data Provider should
    provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.2.4 Confirm Reauthorization at the Data Provider (Optional) - Sample User Content

```
The Data Provider may confirm the details of the reauthorization directly
with the End User.
FDX recommendations:
```
- Display the details of the authorization that was disclosed to the End
    User by the Data Recipient
- Do not alter or allow the user to edit the details of the authorization
- Provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.2.5 Reauthorization Complete - Sample User Content

```
The Data Recipient should give a clear indication that the
authorization disclosure has been signed by the End User and that
the journey is complete.
FDX recommendations:
```
- Indicate success or reason for failure, if applicable
- Clearly indicate that they have returned to the Data Recipient
- Provide an indication that consent can be revoked or
    reauthorized by the user
- Provide direction for next steps, including providing a copy of
    the signed reauthorization disclosure to the End User that
    reflects the date of the signature or make it available in a
    location that is readily accessible to the End User

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


#### 4.3.3 Data Access Platform Reauthorization with Optional Data Provider Confirmation

In some cases, the Data Provider may wish to ensure that the End User is initiating the reauthorization by requiring that the process
includes a reauthentication at the Data Provider. This example describes reauthorization confirmed by the Data Access Platform
with the option for the Data Provider to require reauthentication.


4.3.3.1 Initiate Reauthorize at the Data Recipient - Sample User Content

```
The Data Recipient should allow the user to view their active
authorizations and provide a path to initiate reauthorization.
FDX recommendations:
```
- Display the active authorizations per Section 4.2.4.1
- Clearly identify the authorizations that need to be reauthorized
- Provide a path for the user to initiate the reauthorization journey

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.3.2 Reauthorize at the Data Access Platform - Sample User Content

```
The Data Access Platform should provide the End User with an
authorization disclosure that is clear, conspicuous, and segregated from
other material and contains the following required elements. It should be
provided electronically (or in writing) and be signed by the customer
electronically (or in writing).
```
```
FDX recommendations:
```
- Include the name of the Data Recipient
- Include the name of the Data Access Platform
- Include the name of the Data Provider
- Include a brief description of the product or service and a statement
    that the third party will collect, use, and retain the End User’s data
    only as reasonably necessary to provide that product or service
- Include the Data Clusters that will be accessed
- Include a certification to comply with applicable open banking
    requirements
- Include the duration for which data will be collected, not to exceed
    one year from the date of the most recent reauthorization
- Include a description of the method for an End User to revoke access
- Ensure that the authorization disclosure should be in the same
    language as the language in which it was conveyed to the user. If the
    authorization disclosure is not in English, it should include a link to an
    English-language translation.

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.3.3 Authenticate at the Data Provider (Optional) - Sample User Content

```
The Data Provider has the option to require
reauthentication as part of the reauthorization journey
and should provide a familiar and easy way for the End
User to authenticate.
FDX recommendations:
```
- The Data Access Platform should inform the user
    that they are going to be redirected to the Data
    Provider
- The Data Provider should authenticate the user
    using a familiar login page
- The Data Provider should allow for biometric
    authentication when available
- Both the Data Access Platform and Data Provider
    should provide an option to cancel the flow.

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.3.4 Confirm Reauthorization (Optional) - Sample User Content

```
The Data Provider may confirm the details of the reauthorization directly
with the End User.
FDX recommendations:
```
- Display the details of the authorization that was disclosed to the user
    by the Data Access Platform
- Do not alter or allow the user to edit the details of the authorization
- Provide an option to cancel the flow

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


4.3.3.5 Reauthorization Complete - Sample User Content

```
The Data Recipient and/or Data Access Platform
should give a clear indication that the data sharing
consent has been established and that the journey is
complete.
FDX recommendations:
```
- Indicate success or reason for failure, if applicable
- Clearly indicate that they have returned to the Data
    Recipient
- Provide an indication that consent can be revoked
    or reauthorized by the End User
- Provide direction for next steps, including providing
    a copy of the signed reauthorization disclosure to
    the End User that reflects the date of the signature
    or make it available in a location that is readily
    accessible to the End User

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


## APPENDIX A: GRANT CONSENT EXAMPLES

This appendix provides extra and alternate examples for sample user consent journey displays.

```
Member Provided Example 1: Authorize
There may be some variation in how participants display various details
of these screens while following the UX Guidelines.
FDX recommendations:
```
- Include the name of the Data Recipient
- Include the name of the Data Access Platform
- Include the name of the Data Provider
- A brief description of the product or service and a statement that the
    third party will collect, use, and retain the End User’s data only as
    reasonably necessary to provide that product or service.
- Include the Data Clusters that will be accessed
- Include a certification that the Data Recipient will comply with
    applicable open banking law
- Include a certification that the Data Access Platform will comply with
    applicable open banking requirements
- Include the duration for which data will be collected, not to exceed
    one year from the date of the most recent reauthorization
- Include a description of the method for a user to revoke access
- Ensure that the authorization disclosure is in the same language as
    the language in which it was conveyed to the user. If the authorization
    disclosure is not in English, include a link to an English-language
    translation.

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


```
Member Provided Example 2: Authorize
There may be some variation in how participants
display various details of these screens while following
the UX Guidelines.
FDX recommendations:
```
- Include the name of the Data Recipient
- Include the name of the Data Access Platform
- Include the name of the Data Provider
- A brief description of the product or service and a
    statement that the third party will collect, use, and
    retain the End User’s data only as reasonably
    necessary to provide that product or service.
- Include the Data Clusters that will be accessed
- Include a certification that the Data Recipient will
    comply with applicable open banking law
- Include a certification that the Data Access
    Platform will comply with applicable open banking
    requirements
- Include the duration for which data will be
    collected, not to exceed one year from the date of
    the most recent reauthorization
- Include a description of the method for a user to
    revoke access
- Ensure that the authorization disclosure is in the
    same language as the language in which it was
    conveyed to the user. If the authorization disclosure
    is not in English, include a link to an English-
    language translation.
_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


```
Member Provided Example 3: Confirm Authorization:
```
```
There may be some variation in how participants
display various details of these screens while
following the UX Guidelines.
FDX recommendations:
```
- Optionally allow the user to select the accounts
    they want to share from an eligible account list.
- If this is done, the Data Provider should implement
    account type and cardinality filtering to ensure
    that the user understands which accounts are
    eligible for the use case
- In cases where the Data Provider includes
    account selection as part of the Confirm
    Authorization step, it is recommended that the
    Data Recipient does not show an additional
    account selection screen unless additional
    account scoping is necessary

_*Images are provided for guidance only. Please consult with legal counsel regarding the development of compliant user experiences._


## Appendix B: Consumer Financial Protection Bureau (CFPB)

## SECTION 1033) APPENDIX B: CONSUMER FINANCIAL PROTECTION BUREAU (CFPB) REQUIRED RULEMAKING ON PERSONAL FINANCIAL DATA RIGHTS (CFPB

## Section 1033)

As a standards-setting body for Open Banking, Financial Data Exchange (FDX) has a mandate to develop, improve and maintain a
common, interoperable standard for secure consumer and business access to financial records. To facilitate this, FDX provides the
User Experience Guidelines designed to promote a set of best practices and standardized interfaces that define the end-to-end
process for establishing and maintaining the consumers' authorization to share their financial data from their accounts held at Data
Providers to third parties.

Per CFPB Section 1033, there are specific requirements for parties involved in consumer authorization. This document will describe
how and where to best incorporate the following rules into the user experience for sharing financial data:

1. Ensure the authorization disclosure is clear, conspicuous, and segregated from other material (§ 1033.411(a)).
2. Include the name of the authorized third party in a readily understandable format (§ 1033.411(b)(1)).
3. Include the name of any data aggregator assisting the authorized third party in seeking authorization (§ 1033.431(b)).
4. Include the name of the Data Provider in a readily understandable format (§ 1033.411(b)(2))
5. Provide a brief description of the product or service the consumer has requested, along with a statement that the authorized
    third party will collect, use, and retain consumer data only as reasonably necessary (§ 1033.411(b)(3)).
6. Specify the categories of data that will be accessed, ensuring they are substantially similar to § 1033.211 (§ 1033.411(b)(4)).
7. Ensure the data aggregator certifies to the consumer that it agrees to the conditions for accessing consumer data (§
    1033.431(c)).
8. Include the required certification statement in the authorization disclosure to comply with the obligations outlined in §
    1033.421, ensuring compliance with § 1033.401(b) (§ 1033.411(b)(5)).
9. Describe the expected duration of data collection (not exceeding one year after the most recent reauthorization) and the
    revocation method required by § 1033.421(h)(1) (§ 1033.411(b)(6)-(7)).
10. Obtain the consumer’s express informed consent to access covered data on their behalf by providing an authorization
    disclosure that is signed electronically or in writing (§ 1033.401(c)).


11. Ensure the authorization disclosure is provided in the same language as the consumer communication, with an English-
    language translation link if applicable (§ 1033.411(c)).

These guidelines are intended as a resource to help drive interoperability in the financial ecosystem while also adhering to the FDX
fundamental principles discussed in Section 2.1 Principles Guiding Data Sharing Experiences.



