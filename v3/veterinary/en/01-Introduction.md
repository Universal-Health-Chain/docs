![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain (UHC) for Animal Health - version 3.0**
Copyright © FUNDACION UNID.

Copyright © CONECTATE SOLUCIONES Y APLICACIONES SL.

Copyright © CONNECTING SOLUTION & APPLICATIONS LTD.

All rights reserved.

<p>&nbsp</p>

## **1. Introduction**

Animal owners (breeders, buyers) are also owners of their animal data; both the staff of veterinary clinics that care for the animals and some government departments are the creators and verifiers of the data, while the information systems (IS) in these organizations are the guarantors of the data and have custody of the information.

HL7 FHIR has been approved by [G7](https://www.gov.uk/government/publications/g7-health-track-digital-health-final-reports) as the standard for data exchange for cross-border eHealth but can also be used for data exchange in animal health between Information Systems (IS), veterinay staff, government staff and owners (breeders, buyers).

[SMART-On-FHIR](http://hl7.org/fhir/smart-app-launch/index.html) uses [OpenID Connect (OIDC)](https://openid.net/connect/) for the authorization and identification of both staff, customers (breeders, buyers) and standardizes the way of exchanging animal health data by using the [FHIR API](http://hl7.org/fhir/exchange-module.html). Additionally, the [Consumer Data Standards]() have been developed in Australia to make it easier for customers to access information in different sectors (started with banking, energy, telecommunications) and can be applied to any other sector such as animal health.

An interoperable and resilient Information System (IS) requires a platform agnostic method for data exchange and for data verification with post-quantum computing resistance. In this way, messages can be exchanged over any transport protocol such as TCP/IP (e.g.: Internet) and Bluetooth. It enables clinicians and other workers in different organizations to receive and send data even if the connection with the Information System (IS) is down.

UHC is a **decentralized communication platform for secure data exchange** which utilizes both *Selective Disclosure of information*, *Hyperledger Fabric* blockchain technology, *OpenID* standards, the *Financial-grade (FAPI) Security Profile* specification, *DIDComm messages* and *Post Quantum Computing (PQC)* algorithms for secure data exchange.

All of the information stored in an Information System (IS) about organizations, departments, locations, as well as the information about individuals such as workers (professional qualifications and licenses), animals (patients and donors) and legal guardians, can be issued (signed) by the IS, which is the issuer.

JSON Web Token (JWT) is a secure format that allows an issuer to express claims about a "subject" (animal or other entity) to one or more intended recipients, such as the owner of the animal (holder of the information). In addition, the [W3C Verifiable Credential (VC) specification](https://www.w3.org/TR/vc-data-model-2.0/) can be used for the issuance of the claims of the subject (the credential's subject) by using a JWT (JWT-VC) but also with Selective Disclosure of information (JWT-SD), to allow the holder (owner) to disclose only certain specific information to a verifier, leaving other private information for the owner.

Universal Health Chain (UHC) is developed by ConnectHealth (Conéctate Soluciones y Aplicaciones SL, Connecting Solution and Applications Ltd.) and managed by the UNID Foundation (Fundación UNID) to enable universal multipurpose identifiers for animals, related persons and entities, and secure data communications in a network infrastructure of federated organizations in order to provide cross-border animal health, as well as interoperable claims and URIs for data verification.


[Next: 2. Universal, decentralized identity](./02-Universal-decentralized-identity.md)
