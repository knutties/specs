# Finternet - a functional system overview

This document will capture the following details about the Finternet system.

1. Tenets (aka) Guiding principles
1. Functional Architecture diagram that powers the Finternet
1. Glossary of key terms
1. Tracks

## Tenets (aka Guiding principles)

The architectural and technological choices that are used to design the systems
powering the Finternet should adhere to the following tenets or guiding
principles.  These principles are detailed in the [vision](http://bit.ly/finternet-vision) 
and [technology vision](http://bit.ly/finternet-tech) documents.

1. Users at the centre
1. Interoperability
1. Evolvability
1. Modularity
1. Scalability
1. Division of labour and competition
1. Inclusiveness and accessibility
1. Security and privacy (might want to add integrity and verifiability to this)
1. Resiliency (this is an additional one)

## Functional architecture diagram

![Functional Architecture](images/finternet.drawio.png?raw=true "Funtional Architecture")

### Entity

This section will detail out the entities that are involved in typical Finternet
flows.

* *Unified Ledger*
* *Legal Person* - Representation of individuals, businesses, or
  entities on the unified ledger. This entity can in turn create one of more
  sub-entities - token manager, credential manager or accounts. These
  sub-entities can initiate transactions, issue assets, or perform activities on
  the unified ledger, with identity verified through secure credentials and are
  detailed below.
* *Account* - Representation of an entity that can hold assets, credentials and
  perform transactions.
* *Token Manager* - An entity (service provider) responsible for issuing,
  managing, and governing tokens on the ledger. Token managers maintain
  oversight over asset issuance, transfers, and compliance with asset-specific
  rules and regulations.
* *Asset Class* - A broad category or type of asset that can exist on the
  ledger, such as financial securities, real estate, digital collectibles, or
  other tokenized items. Each class defines the shared characteristics and rules
  applicable to that group of assets.
* *Asset Instance* - A specific representation of an individual asset within a
  class, uniquely identifiable on the ledger. For example, one unit of a
  security, a particular piece of property, or a single digital collectible
  would each be considered an instance.
* *Asset Rule Set / Policies* - Policies/Workflows that token managers attach to
  asset classes to be executed on specific actions.
* *Credential Manager* - An entity or service provider responsible for issuing,
  managing, and governing credentials on the ledger.
* *Credential Class* - A broad category or type of credential that serves as a
  irrepudiable proof.
* *Credential Instance* - A representation of a credential within a class.  A
  digitally signed proof, issued by a trusted authority, that verifies
  qualifications, achievements, or attributes of an individual or entity. These
  credentials are cryptographically secure and can be used to authenticate
  participants in Finternet transactions.
* *Transfer Manager / Interop Manager* - An entity which facilitates transfer of
  assets between any two systems that adhere to the Inter Ledger Protocol.
* *Transaction* - A structured data entity representing an asset/thing-related
  action within Finternet. It contains all necessary information, such as
  participants, asset details, and verifiable credentials, required to execute a
  transaction. The transaction object ensures standardization, traceability, and
  compliance across different ledger systems, enabling seamless interoperability
  and validation within the platform.
* *Wallet* - A secure digital wallet that stores cryptographic keys, allowing
  users to authenticate and sign transactions across the Finternet. It provides
  application agnostic access to a user’s assets, ensuring consistent and secure
  authorization across different platforms and services.

## Working Groups

1. Core Architecture Working Group
1. Inter Ledger Protocol
1. Immutable Proof Store
1. UL Txn Ledger / Smart Contract Infra
    1. Solana track
    1. ETH track
    1. Ledger Adapter
1. User (Legal Person) Management (key/signing/PII) - Jay / Gautam
1. ULI API Services
    1. Management services
    1. Transaction services
