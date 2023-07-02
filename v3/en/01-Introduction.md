![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain (UHC) - version 3.0**
Copyright © FUNDACION UNID.

Copyright © CONECTATE SOLUCIONES Y APLICACIONES SL.

Copyright © CONNECTING SOLUTION & APPLICATIONS LTD.

All rights reserved.

<p>&nbsp</p>

## **1. Introduction**

People are the owners of their health data and professionals who attend them are the creators and verifiers of the data, while the information systems (IS) in the different organizations are the guarantors of the data and have the custody of the information.

HL7 FHIR has been approved by [G7](https://www.gov.uk/government/publications/g7-health-track-digital-health-final-reports) and other countries as the standard for data exchange between Information Systems (IS), clinicians and patients or donors. [SMART-On-FHIR](http://hl7.org/fhir/smart-app-launch/index.html) uses [OpenID Connect (OIDC)](https://openid.net/connect/) for the authorization and identification of both workers, customers (patients, donors) and medical devices of an organization in a FHIR server and standardizes the way of exchanging health data by using the [FHIR API](http://hl7.org/fhir/exchange-module.html). Additionally, the [Consumer Data Standards]() have been developed to make it easier for people to access their information and can be applied sector by sector, starting with banking, energy and telecommunications but for any other sector such as healthcare and for digital identity.

An interoperable and resilient Information System (IS) requires a platform agnostic method for data exchange and for data verification with post-quantum computing resistance. In this way, messages can be exchanged over any transport protocol such as TCP/IP (e.g.: Internet) and Bluetooth. It enables clinicians and other workers in different organizations to receive and send data even if the connection with the Information System (IS) is down.

UHC is a **decentralized communication platform for secure data exchange** which utilizes both *Selective Disclosure of information*, *Hyperledger Fabric* blockchain technology, *OpenID* standards, the *Financial-grade (FAPI) Security Profile* specification, *DIDComm messages* and *Post Quantum Computing (PQC)* algorithms for secure data exchange.

An OpenID Provider (OP) is an API service running in a physical or virtual server in the Information System (IS) of an organization and acts as the issuer of information (claims) for authentication and authorization of end-users (workers, customers and related persons, medical electronic devices, etc.). It has the public cryptography keys available in a “jwks.json” file published in the URL of the service, as defined in the OpenID Connect Discovery specification for the JSON Web Key Set (JWKS). But it is required of all the actors in the health chain to have its own universal, cross-border digital identity.

Providing a universal, digital and verifiable identity for each organization, department, office and practitioner is a key element in the security of the health sector. Public Key Infrastructure (PKI) is used to create digital certificates and verifiable data such as SMART Health Cards (SHCs) and health certificates, for example the EU Digital COVID Certificates (EUDCC) project, previously known as the EU Digital Green Certificates (DGC). It is also used by the ePassport (ICAO Doc9303), mDL (ISO Mobile Driver License) and eID (European ID) specifications.

Organizations (hospitals, diagnostic laboratories, nursing homes, insurance companies, etc.) are legally registered in their countries and they contract professionals who can have qualifications and credentials (medical doctor license, registered nurse, etc.). These professionals have roles in some departments based on their occupations as workers/employees with some professional qualifications. These workers can be associated with some concrete locations within the organization such as a doctor office in a healthcare service (department).

All of the information stored in Information Systems about organizations, departments, locations, as well as the information about the individuals such as workers (professional qualifications and licenses), customers (patients, donors), related persons (legal guardians, family members, etc.), can be issued (signed) by the Information System (IS), which is the issuer.

JSON Web Token (JWT) is a secure format that allows an issuer to express claims about a "subject" (person or other entity) to one or more audiences (intended recipients), such as the owner (holder of the information) and legal guardians. In addition, the[W3C Verifiable Credential (VC) specification](https://www.w3.org/TR/vc-data-model-2.0/) can be used for the issuance of the claims of the subject (the credential's subject) by using a JWT (JWT-VC) but also with Selective Disclosure of information (JWT-SD), to allow the holder (person) to disclose only certain specific information to a verifier, leaving other private information for the owner.

UHC enable secure data communications in a network infrastructure of federated organizations with PQC resistance, in order to improve the security and resilience of the healthcare ecosystem to provide cross-border healthcare to people, as well as interoperable claims and URIs for data verification.


[Next: 2. Universal, decentralized identity](./02-Universal-decentralized-identity.md)
