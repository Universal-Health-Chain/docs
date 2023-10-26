![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain (UHC) for Animal Health - version 3.0**
Copyright © FUNDACION UNID.

Copyright © CONECTATE SOLUCIONES Y APLICACIONES SL.

Copyright © CONNECTING SOLUTION & APPLICATIONS LTD.

All rights reserved.

<p>&nbsp</p>

[Previous: 01-Introduction](01-Introduction.md)

## **2. Universal, decentralized identity**

Providing a universal, digital and verifiable identity for each individual and organization (breeders, veterinary clinics and animal hospitals, laboratories, animal housing, insurance companies, etc.) is a key element, not only for staff (veterinary, administrative) but for animals (donors, patients) and related persons such as owners (legal guardians).

Organizations are legally registered in their countries and they contract professionals who can have qualifications and credentials. These professionals have roles in some departments based on their occupations as workers/employees with some professional qualifications. These workers can be associated with some concrete locations within the organization.

A public, decentralized and collision-free Unique Universal Identifier (UUID v4) for training and health can be generated for animals, other individuals and entities by using a software application, as defined in the Unified Identification Protocol for Training and Health.

In this way, the owners of an animal (holders) and other entities can generate both their own digital identities (including their own cryptographic keys) and the digital identity of the animal for veterinary data exchange by using a software application, as well as the relationship with the animal, which can be verified by staff from a government department as well as veterinary staff and others (airlines, etc.).

### **OpenID and Public Key Infraestructure (PKI) **

An OpenID Provider (OP) is an API service running in a physical or virtual server in some Information System (IS) and acts as the issuer of information (claims) for authentication and authorization of end-users (related persons, staff and electronic devices). It has the public cryptography keys available in a “jwks.json” file published in the URL of the service, as defined in the OpenID Connect Discovery specification for the JSON Web Key Set (JWKS).

Public Key Infrastructure (PKI) is used to create digital certificates and verifiable data such as SMART Health Cards (SHCs) and health certificates.

### **Public keys**

The status of the public keys generated in a decentralized way are blockchain certified and so are the identifiers of both individuals, organizations, departments, qualifications, contracts, consents, veterinary records, etc.

To comply with data privacy regulations such as GDPR (General Data Protection Regulation), the UNID Foundation's Hyperledger Fabric network is used. An organization can issue a batch of electronic and physical credentials for its employees and customers.

Both electronic and physical credentials issued by an organization can contain some data of the issuer such as the public cryptographic key used to sign the credential, where the ID of the public signature key (keyID or “kid”) is the thumbprint of the public key as per the IETF RFC 7638 specification (SHA-256 of the public JSON Web Key).

A cache memory with all the non-revoked keyIDs used by the federated organizations to generate electronic credentials can be stored in the software applications, used by end-users such as individuals (professionals, customers, related persons) but also by IOT devices. In this way, each time an electronic or physical credential is read, both the public key and its status and validity period can be known by the reader.
