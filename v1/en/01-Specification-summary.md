![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain - v1**
Copyright © FUNDACION UNID.

Copyright © CONECTATE SOLUCIONES Y APLICACIONES SL.

All rights reserved. 
<p>&nbsp  </p>

## **Unified and universal medical history**

The [UNID Foundation](http://unid.es) and the spanish company Conéctate Soluciones y Aplicaciones SL ([ConnectHealth](https://connecthealth.info)), have developed Universal Health Chain (UHC) as a platform for the secure communication of health data between people and different health services and other type of services.

[![](https://img.youtube.com/vi/6Ans2_UPyXY/0.jpg)](https://www.youtube.com/watch?v=6Ans2_UPyXY)

<sub>*UHC platform video (click to open Youtube)*</sub>
<p>&nbsp  </p>

People can securely unify their health data from public and private organizations on their mobile phone, along with their [Universal Health Identifier] (https://patentscope.wipo.int/search/en/detail.jsf?docId=WO2020136289&tab=PCTBIBLIO). Universal Health Chain (UHC) uses the international standards [HL7 FHIR R4](http://hl7.org/fhir/R4), [International Patient Summary (IPS)](http://hl7.org/fhir/uv/ips), [Verifiable Credentials (VC)](https://www.w3.org/TR/vc-data-model/), among others. Although the
international format for the exchange of medical data for cross-border healthcare is
HL7 FHIR and IPS, UHC also allows adding PDF files.

IPS is a FHIR document with some mandatory and other optional medical history sections, [defined by the European Committee for Standardization (CEN)](https://www.cen.eu/news/brief-news/Pages/NEWS-2021-009.aspx).
![](http://hl7.org/fhir/uv/ips/IPS_doc_library.png)
<sub>*(image from <http://hl7.org/fhir/uv/ips>)*</sub>
<p>&nbsp  </p>

The UHC-personal application allows the person to add data from different public and private health services and from different territories to unify their medical history. It also allows health data to be securely shared from the person's mobile with different health services and also for other purposes such as showing laboratory test results or COVID-19 vaccinations when traveling, using encrypted connections to protect data.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Public_key_shared_secret.svg/536px-Public_key_shared_secret.svg.png)

<sub>*(image from https://en.wikipedia.org/wiki/Diffie–Hellman_key_exchange)*</sub>
<p>&nbsp  </p>



Patient or donor medical history data can be received or incorporated into the UHC-personal application in two different ways:

1.  The person downloads the data from different healthcare services (public and private) using a username and password on each system and incorporates the data into UHC-personal. This can be done by adding the files manually to the application in either PDF and FHIR JSON formats. Also will be possible to automatically connect and download data form healthcare services using Smart-On-FHIR.

2.  The healthcare service sends the data of the person to the UHC-personal application, securely shared via an encrypted connection that is created from the person's Universal Health Identifier, so that only the owner can decrypt the data on their mobile phone. This option prevents Man-In-The-Middle attacks, protecting the personal and medical data from hackers.

[![](https://img.youtube.com/vi/GtZTHiHmcZk/0.jpg)](https://www.youtube.com/watch?v=GtZTHiHmcZk)

<sub>*UHC-personal app video (click to open Youtube)*</sub>
<p>&nbsp  </p>

## **Regulations on access and portability of health data for cross-border healthcare**

In the US, the USCDI regulation makes it mandatory for healthcare services to provide their clients (patients) with health data in the FHIR R4 format, using an API compatible with FHIR and Oauth2, so that people can login into a FHIR server with a username and password, view their data and download the desired data in FHIR R4 format; also the same can be done through a third-party applications that connects to the FHIR server with the person's username and password to obtain an authentication token in order to automatically download the data into the application.

However, this does not prevent Man-In-The-Middle attacks on the traffic between the health provider's API server and the user's application or website, in case the user's network is compromised (for example, a WIFI network through DNS spoofing attack). UHC solves this problem by using the encrypted peer-to-peer messaging service and the UHC-personal app.

In Europe regulations specify that data has to be delivered digitally to the person in a common electronic format for cross-border healthcare. This format is [*International Patient Summary* (IPS), established by the European Committee for Standardization (CEN)](https://www.cen.eu/news/brief-news/Pages/NEWS-2021-009.aspx), that uses FHIR R4 and establishes different [sections in the FHIR document that contains the patient's medical history](http://hl7.org/fhir/uv/ips/ipsStructure.html).

UHC provides the tool that allows to comply with the different regulations, since people will be able to receive their health data through the Universal Health Identifier, for example from a laboratory, and later they will be able to send or share certain health data as test results of laboratory or COVID-19 vaccinations, among other possible data within the medical record that each person unifies and has securely encrypted in the UHC-personal application.
<p>&nbsp  </p>

## **Cybersecurity and resilience in health**

UHC is a resilient system against viruses and computer attacks (for example, Wannacry in 2017), terrorism or natural disasters. It allows health systems and applications of health professionals to function autonomously even without an internet connection, since there is the possibility of sharing data between the person's mobile phone and a health service using Bluetooth in case of networks or computer systems fall down.

![](https://frontera.net/wp-content/uploads/2017/05/WannaCry-e1494998398416.png)

<sub>*(image from https://frontera.net/news/global-macro/which-global-companies-were-hit-hardest-by-the-wannacry-attack/)*</sub>
<p>&nbsp  </p>

UHC is based on the asymmetric Elliptical Curve Diffie-Hellman (ECDH) cryptography in which each participant has public and private keys for signing and encrypting data.
Through the Universal Health Identifier and the digital identity in the UNID network, each user (patient, professional, organization) or device (server, medical device, etc.) has a digital identity with private and public keys to sign and encrypt information.
<p>&nbsp  </p>

## **UNID Foundation Blockchain**

Hyperledger Fabric is an enterprise network in which different channels can exist, similar to computer sub-networks. Being a permissioned network, each channel has established which peer nodes (organization servers) can belong to it. In the case of UHC there will be different channels, e.g. "HealthCare" (healthcare and donations) and "Biological Products" (registration and traceability of biological products for medicinal purposes).

![](https://www.serial-coder.com/img/posts/Demystifying-Hyperledger-Fabric/Fabric-Explained-4%20%28-sharp-2%29.png)

<sub>*(image from https://www.serial-coder.com/post/demystifying-hyperledger-fabric-fabric-architecture)*</sub>
<p>&nbsp  </p>

Each organization can have one or more peer nodes and each peer node can belong to one or more channels. For example, the same server can belong to HealthCare and Biological Products channels, and the organization can have one or more peer nodes, for example in Europe, North America, and Asia.

A schema of this comes in the "[Peers and organizations](https://hyperledger-fabric.readthedocs.io/en/release-2.2/peers/peers.html)" section in the Hyperledger Fabric documentation:

![alt text](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/peers.diagram.8.png
 "Organizaciones y nodos")
  

In addition, Hyperledger Fabric allows peer nodes (or servers) from the same organization or from different organizations to use [Private Data Collections (PDCs)](https://hyperledger-fabric.readthedocs.io/en/release-2.2/private-data/private-data.html) to store private data, outside of public channels (ledgers), temporarily or permanently, complying with GDPR.

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-2.png)

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-3.png)
<p>&nbsp  </p>

In this way, an organization can share private information between different peer nodes of its organization, and it can also create PDCs to share private information with clients or suppliers of its organization, or a public administration in a territory can share data with different public administrations of other territories or with other types of organizations such as laboratories (for example, for data reporting).

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-1.png)

![](https://www.serial-coder.com/img/posts/Demystifying-Hyperledger-Fabric/Fabric-Explained-7%20%28-sharp-2%29.png)

<sub>*(image from <https://www.serial-coder.com/post/demystifying-hyperledger-fabric-fabric-architecture>)*</sub>
<p>&nbsp  </p>

Hyperledger Fabric is therefore a network of networks that allows multiple possibilities. The main feature of PDCs is that Hyperledger  Fabric creates a  hash value (a digital fingerprint) of every data record stored on a PDC (asset), and this hash value is saved in the (public) ledger of the channel on which the PDC is located. This way, when clients receiving some data (e.g. a medical document), they can verify that the original hash value of the data is true on the public channel. To do this, the client generates the hash value of the data and compares it to the original hash saved on the blockchain channel, using the asset ID stored in the PDC and the name of the PDC.

![](https://cdn.thenewstack.io/media/2020/08/e06c3bc6-image2.png)

<sub>*(image from <https://thenewstack.io/using-private-data-collections-in-hyperledger-fabric>)*</sub>
<p>&nbsp  </p>

In this way, Hyperledger Fabric can be used as a private and distributed database with automatic data certification on the public channel; it guarantees the confidentiality of the data through PDCs and compliance with data protection regulations such as GDPR, since the data in the PDCs are private and data can be deleted (right to be forgotten).

![](https://miro.medium.com/max/700/0*TCU0KW7ZUJjpwGYH)

<sub>*(image from <https://kctheservant.medium.com/private-data-implicit-data-collections-in-hyperledger-fabric-v2-0-f2ef41f0e99d>)*</sub>
<p>&nbsp  </p>

![](https://miro.medium.com/max/2400/1*rP6Nz2xDsIXpgrXS6pyoWQ.png)

<sub>*(image from <https://kctheservant.medium.com/private-data-and-transient-data-in-hyperledger-fabric-46b5258f391e>)*</sub>
<p>&nbsp  </p>

The UNID Foundation, in collaboration with the companies Conéctate Soluciones y Aplicaciones SL (Spain) and Connecting Solution & Applications Ltd. (Canada), has developed smart contracts in Hyperledger Fabric (also known as chaincode) for the certification and traceability of processes in the health care and biological products for medicinal purposes. The documentation will be updated on the UNID Foundation's website (<http://unid.es>) and on Github (<https://github.com/Universal-Health-Chain/docs>)

The UNID Foundation is developing the 2.0 version of the smart-contracts for the traceability of biological products (called chaincode in Hyperledger Fabric) in collaboration with Connecting Solution & Applications Ltd.:

### **Product Management**

**PUT** /product

*creates a new product*

**GET** /product/{productId}

*gets a product*

**PUT** /product/{productId}

*updates a product*

**DELETE** /product/{productId}

*delete a product*

**POST** /product/{productId}​/split

*split a product into other products*

**POST** /product/merge

*merge a list of products into a new product*

**GET** /product/{productId}/trace

*get the full trace of a product*

**GET** /product/{query}

*get the requested products according to the query*

### **Event Management**

**PUT** /product/event

*creates a new event*

**GET** /product/event/{eventId}

*gets an event*

**GET** /product/event/{query}

*get the requested events according to the query*
<p>&nbsp  </p>

In addition, the UNID Foundation is developing other smart contracts in collaboration with Conéctate Soluciones y Aplicaciones SL to register the hash of FHIR resources and proof of digital signature ([Linked Data Proofs](https://w3c-ccg.github.io/ld-proofs/)) also in Hyperledger Fabric version 2.0.
<p>&nbsp  </p>

## **Accessible and simple international standards for everyone**

UHC allows any organization to create and read FHIR resources in a simple way, both for healthcare and laboratories, traceability of biological products and also for services and applications outside the healthcare sector. Each organization may deploy its own service for free or use the help desk hosted by the UNID Foundation, which is being developed in collaboration with the company Conéctate Soluciones y Aplicaciones SL.

Health information is sent through UHC to the user using FHIR R4 messages, documents, and resources, although UHC also supports Verifiable Credentials. For organizations that have not yet implemented FHIR, the UHC system can  receive only clinical codes (SNOMED, LOINC and HL7, among others) to build the data in FHIR format and to be sent to the person, facilitating the digital transformation and to help to achieve the compliance with regulations by using international standards for cross-border healthcare.

Specifically, the *UHC-FHIR-Helper service* enables the following:

1. Send some basic fields to generate the desired FHIR resource from these fields (laboratory test result, immunization, etc.), so that any organization will be able to adopt international standards such as HL7 FHIR and International Patient Summary (IPS).

2. Convert data in the FHIR international format to simple standardized forms, so that data can be read, verified and understood by any application and computer system in healthcare and also in other sector outside healthcare, to achieve interoperability not only between healthcare services but also outside healthcare: cinemas, theaters, museums, congresses, libraries, travel sector, etc.

As an example, a FHIR DiagnosticReport lab report can be generated by sending to the UHC Helper service a JSON data object containing international clinical terminology codes (widely recognized in both Europe and the US. and in other countries), such as LOINC, SNOMED and HL7 FHIR:

```javascript
{
	language: "es",
	categoryCodeFHIR: "LAB",
	conclusionCodeSNOMED: "260385009",
	conclusionCodeText: "Negativo",
	diagnosticReportCodeLOINC: "94762-2",
	effectiveDateTime: "2021-02-18",
	performerReferences: ["Organization/<universal-health-uuid>"],
	subjectReference: "Patient/<universal-health-uuid>"
}
```
<sub>*Example of a UHC "sheet" data object that simplifies the complex nested structure of FHIR*</sub>
<p>&nbsp  </p>

The UHC Helper Service converts those basic fields into the data structure of the corresponding FHIR resource (which in this case corresponds to a lab report or FHIR "DiagnosticReport") and also generates an unique UUID identifier (widely used internationally) to uniquely identify this FHIR resource globally and universally in any territory and organization:

``` json
{
	"category": [
		{
			"coding": [
				{
					"code": "LAB",
					"display": "Laboratory",
					"system": "http://terminology.hl7.org/CodeSystem/v2-0074"
				}
			],
			"text": "Laboratorio"
		}
	],
	"code": {
		"coding": [
			{
				"code": "94762-2",
				"display": "SARS-CoV-2 (COVID-19) Ab [Presence] in Serum or Plasma by Immunoassay",
				"system": "http://loinc.org"
			}
		],
		"text": "SARS-CoV-2 (COVID-19) Ab [Presencia] en suero o plasma por inmunoensayo"
	},
	"conclusionCode": [
		{
			"coding": [
				{
					"code": "260385009",
					"system": "http://snomed.info/sct"
				}
			],
			"text": "Negativo"
		}
	],
	"effectiveDateTime": "2020-02-18",
	"identifier": [
		{
			"system": "urn:ietf:rfc:3986",
			"value": "urn:uuid:<universal-health-diagnosticreport-uuid>"
		}
	],
	"language": "es",
	"performer": [
		{
			"reference": "Organization/<universal-health-uuid>"
		}
	],
	"resourceType": "DiagnosticReport",
	"subject": {
		"reference": "Patient/<universal-health-uuid>"
	}
}
```
<sub>*Example of FHIR Diagnostic Report resource generated from the previous UHC "sheet"*</sub>
<p>&nbsp  </p>

## **Data certification**

The UHC helper allows to get a digital fingerprint (hash value) of the data. Hash functions generate a thumbprint, and have the characteristic that the hash value generated is entirely different with minimal change to the data (with a single modified bit the hash value is completely different). For example, applying the SHA-256 hash function (widely used) results in a hash value of:

*8100abc4946288bfcefab256cf7f8da14754e57645e87dcef172db6d4940b733*

Because the UUID of the FHIR resource (lab report) is unique, the SHA-256 hash value obtained will also be unique, i.e. the same hash value cannot be obtained from any other FHIR resource, ensuring that the original data can be verified and that it can be known whether the data contained in the FHIR resource has been modified (the hash value will be completely different in such a case).

In this way, once the FHIR resource and the hash value associated with the unique identifier of the FHIR resource are generated, the organization that creates the data can save that hash value using the UNID Foundation blockchain network. The hash value is associated in the blockchain network with the UUID of the FHIR resource, so that a third party can validate the original data by following these steps:

1.  Generating the SHA-256 hash value of the FHIR resource to be verified, using the UHC Helper service or other functions that can "canonize" and "serialize" the FHIR resource before generating the hash value, to ensure that it is always generated in the same correct and standardized way.

2.  Retrieving the original hash from the blockchain, using the universal UUID of the FHIR resource.

3.  Comparing the calculated hash value with the hash value stored on the blockchain.

4.  If they do not match, the blockchain may be asked to retrieve the history of the FHIR resource, to get the hash values stored each time the FHIR resource has been modified. In this way, it is possible to check if the calculated hash value was valid in some previous state of the FHIR resource (the received data is obsolete) or if, on the contrary, the received data has never been certified at any time in the blockchain network.
<p>&nbsp  </p>

Therefore, when an application receives FHIR resources from a patient, donor, or customer, both in the healthcare sectors or in others, the digital fingerprint or hash value of the data can be used to verify the authenticity of the shared data. Subsequently, the FHIR data can be converted back to a simplified UHC “sheet” format, to a standardized JSON Schema Form and / or use the corresponding HTML code for this data, using the UHC helper service or other functions.
  
The UNID Foundation is developing a UHC testing website for organizations and professionals (in collaboration with the company Conéctate Soluciones y Aplicaciones SL) to carry out the processes in a graphical way, so that any professional of an organization that collaborates with the UNID foundation in the UHC testing will be able to see how to generate FHIR resources, data hash, verify the digital signature of the data, etc., even if they have no programming knowledge and does not know about medical terminology. This website can also be used to send medical data such as the person's Medical History in the international IPS format (approved in Europe by the CEN) through encrypted connections, directly to the person's mobile, securely and preventing the communications of the data from being intercepted by malicious third parties (hackers).
<p>&nbsp  </p>
  

## **Verifiable Credentials with FHIR**

The UNID Foundation has also developed a system that allows to convert FHIR data to verifiable credentials in the international format of the World Wide Web Consortium (W3C), in collaboration with the company Conéctate Soluciones y Aplicaciones SL. As an example, a FHIR verifiable credential or VC created from a diagnostic report such as the one above, can be created by simply adding the laboratory test result in the "credentialSubject" field (which containing the object or objects to which the verifiable credential refers) in this way:

```json
{
    "@context": ["https://www.w3.org/2018/credentials/v1"],
    "id": "<verifiable-credential-uuid>",
    "type": ["VerifiableCredential", "VC/FHIR/R4/DiagnosticReport"],
    "issuer": "<universal-health-identifier-organization-uuid>",
    "issuanceDate": "2021-02-18T13:30:00Z",
    "credentialSubject": "<FHIR DIAGNOSTIC REPORT>"
}
```  
<sub>*Basic example showing how a FHIR resource is entered into a verifiable credential (VC) according to the W3C standard*</sub>
<p>&nbsp  </p>

Similarly, UHC "sheet" formats can also be used within a verifiable credential, in which case the type of the credential will not start with "VC/FHIR/R4" but with "UHC/Sheet/1.0":
```json
{
    "@context": ["https://www.w3.org/2018/credentials/v1"],
    "id": "<verifiable-credential-uuid>",
    "type": ["VerifiableCredential", "UHC/Sheet/1.0/DiagnosticReport"],
    "issuer": "<universal-health-identifier-organization-uuid>",
    "issuanceDate": "2021-02-18T13:30:00Z",
    "credentialSubject": "<UHC-SHEET DIAGNOSTIC REPORT>"
}
```  
<sub>*Basic example showing how a UHC "sheet" is entered into a verifiable credential (VC) according to the W3C standard*</sub>
<p>&nbsp  </p>

The main characteristic of verifiable credentials is that they can be digitally signed in the W3C standardized format, generating a “proof” object using the Linked Data Proof format (LD-Proof).

The FHIR resource can be signed when contained into a Verifiable Credential or by using an FHIR Provenance resource, which could be contained within the FHIR DiagnosticReport resource (using the “contained” field for this) according to FHIR specifications, or it could be an additional FHIR resource to the DiagnosticReport resource, as listed in [United States Core Data for Interoperability (USCDI)](https://www.healthit.gov/isa/united-states-core-data-interoperability-uscdi). In this case, the "credentialSubject” field of the verifiable credential would contain two FHIR resources: one with the laboratory test result and another one with the signature proof.

The UHC helper service will allow digital signatures to be generated and verified in both the FHIR Provenance format and the verifiable credential format defined by W3C.
<p>&nbsp  </p>  

## **Universal Health Identifier**

The UNID Foundation implements in UHC the patent "[Unified Identification Protocol in Training and Health](https://patentscope.wipo.int/search/es/detail.jsf?docId=WO2020136289&tab=PCTBIBLIO)". In this way, universal identification of patients, donors, health professionals, health services, organizations, biological products and also of the processes carried out such as medical encounters, diagnostic results, procedures, interventions, prescriptions, etc.

*FHIR References* to Patient, Practitioner, Organization and other resources such as Immunization, DiagnosticReport, etc. are created using the name of the resource they refer to and then adding the identifier of the resource, separated by a forward slash, for example, *"Patient/identifier"*.

The UNID Foundation uses **UUID v4** as a unique identifier that can be generated by any organization to encode FHIR resources in a universal way, also compatible with International Patient Summary (IPS). Thus, the FHIR reference to a laboratory test result would be *"DiagnosticReport/uuid-v4"* and the reference to a vaccination would be *"Immunization/uuid-v4"*.

Applying the same thing to the identification of people, patients, professionals, organizations and healthcare services, the UNID Foundation provides a universal identifier to all related parties, so that their authenticity and identity can be verified.

Thus, using UUID v4 as a basis for the coding of identities, compatible with FHIR, IPS and also with verifiable credentials (VC) and DID documents, each of the parties that participate in the health chain has a Universal Health Identifier and a universal digital identity.

As an example, the Universal Identifier can be represented in the following ways:
| Type                  | Description |
| ---                   | --- |
|*Patient*                | *person with medical history*|
|UNID URN               | urn:unid:patient:uuid:uuid-v4|
|UNID DID               | did:unid:patient:uuid:uuid-v4|
|UNID KEY ID (KID)      | did:unid:patient:uuid:uuid-v4#keyBase58|
|FHIR Reference         | Patient/uuid-v4|
|FHIR Identifier IETF   | urn:uuid:uuid-v4|
|IPS Full URN           | urn:uuid:uuid-v4|
|Veres One compatible   | did:v1:uuid:uuid-v4|

The UNID Foundation registers in the blockchain network the digital identities together with the public cryptographic keys associated with them, which allow the verification of the digital signature of the data and the encryption of the same when they are transmitted, using secure encrypted connections with asymmetric keys.
<p>&nbsp  </p>

## **Universal Identifier of Biological Products for medicinal uses**

Products of biological origin such as vaccines or hemoderivatives are medical devices according to different regulations and have different UDIs for each legislation, for example, in [Europe](https://ec.europa.eu/docsroom/documents/36664/attachments/1/translations/en/renditions/native), [USA.](https://www.fda.gov/medical-devices/unique-device-identification-system-udi-system/udi-basics) and / or [Australia](https://www.mtaa.org.au/unique-device-identification-udi). They are normally implanted, injected or used in a patient, such as plasma in aesthetic treatments ([PRP or platelet rich plasma](https://en.wikipedia.org/wiki/Platelet-rich_plasma)), vaccines, packed red blood cells, medicines made from immunoglobulins and other types of products of biological origin.

Products of biological origin can be encoded with different systems such as:

- [Health Industry Business Communications Council (HIBCC)](https://www.hibcc.org/)
- [International Council for Commonality in Blood Banking Automation (ICCBBA)](https://www.iccbba.org)
- [GS1](https://www.gs1.org/)

UHC technology makes it possible to verify the traceability of biological products throughout the entire health chain and also by people and by other organizations and professionals outside health, as in the case of verification of vaccination against COVID-19 .

Both healthcare professionals / services and patients who buy or receive these products to be used in medical treatments will be able to obtain and verify product information from the barcode of a product of biological origin, in a unified way for products of different manufacturers, different coding systems and in different regulations, improving the security and traceability of these products and allowing people to know all the information about the products that are supplied or implanted to them.

As an example, the UNID Foundation's Universal Identifier for Biological Products can be represented in the following ways:

| Type                         	    | Description |
| ---				    | --- |
|*Biological products / medical devices*   | *example: traceability of a vaccine, hemoderivative, etc.*|
|FHIR Reference                     | Device/uuid-v4| 
|FHIR Identifier IETF               | urn:uuid:uuid-v4| 
|IPS Full URN                       | urn:uuid:uuid-v4| 
|UNID URN                           | urn:unid:device:uuid:uuid-v4| 
|UNID DID                           | did:unid:device:uuid:uuid-v4| 

UHC allows certifying and verifying the information of biological products outside the health sector, for example, to verify COVID-19 vaccination data in tourism, congresses, etc., so that the authenticity and traceability of a vaccine manufactured by the pharmaceutical industry and administered in a vaccination procedure can be verified in the blockchain network of the Fundación UNID.

In this way, organizations and health professionals that create health data or biological products data can register their hash in the blockchain network, in a decentralized way, which allows the authenticity of the data to be verified both by patients who receive this data and by other professionals and organizations with whom the person subsequently shares the data
<p>&nbsp  </p>

## **Data for reseach**

The UNID Foundation develops smart-contracts in Hyperledger Fabric (chaincode) that use private collections (PDC) to anonymize, deidentify and generate data for research.

In this way, any organization will be able to register data for research in a totally anonymous and secure way, sending the UNID Foundation the data that they want to share with the international community.

As an example, the FHIR DiagnosticReport laboratory test result shown above is sent to the UHC Helper service in this format:

```json
{
	"region":"ESP",
	"fhirR4":"<FHIR DIAGNOSTIC REPORT>"
}
```

This data object is anonymized and deidentified to generate a UHC object of type "research". An example, with the result of the process is shown below:

```json
{
	"codesHL7": ["LAB"],
	"codesLOINC": ["94762-2"],
	"codesSNOMED": ["260385009"],
	"dateTime": "2021-02-18",
	"resourceType": "DiagnosticReport",
	"region":"ESP"
}
```
Subsequently, the anonymized and deidentified object is sent from the health service to the UNID Foundation or to another organization approved by the Foundation as a hub for collecting research data (for example, universities).

Data received is verified through a private smart-contract on the UNID Foundation blockchain, then the object is registered in the channel's public ledger by means of another smart-contract, so that all the * peer nodes * or servers can consult data anonymously stored from different hubs,  without being able to know the healthcare service origin of the data in the blockchain, to carry out statistics or research studies.
<p>&nbsp  </p>

## **Resilient Hospital Information Systems (HIS) and decentralized healthcare**

Following the crises caused by the Wannacry ransonware attack in 2017 and the COVID-19 pandemic in 2020, the digital transformation in health has to be oriented towards the decentralization of healthcare, to empower patients.

Until 2021, hospital information systems have been based on a centralized model, in which all health personnel terminals were connected to a central system to be able to read and write data in the electronic medical record that that person had in that system. In addition, people did not have a simple way of being able to carry information from one system to another and in any language, for example, on business or vacation trips. Therefore, health professionals could not have a global vision of the person, which led to worse health care and higher health costs (duplication of diagnostic tests, readmissions, etc.). On the other hand, the healthcare professional attending the patient could not sent an electronic report automatically and securely to the patient.

In 2021 people become the center of the health ecosystem, thanks to FHIR and IPS standards, UUID v4 identifiers, the Universal Health Identifier and the digital identity in the UNID network. Through UHC and the Universal Health Identifier, the person can unify their data on the mobile phone, go to a regular health service or a new one, show their Universal Health Identifier and establish an encrypted connection with the professional who attends to them to share health data in international standards.

Likewise, using the Universal Health Identifier, the digital identity of the UNID Foundation, the UUID v4 identifiers and communication [DIDComm] (https://github.com/decentralized-identity/didcomm-messaging), the healthcare professional application can:
1. Read the information in the medical record that the person sends in FHIR / IPS format.
2. Generate new FHIR data in a decentralized way, identifying each new FHIR resource with a UUID v4 identifier.
3. Digitally sign the data with the signature keys securely accessible from the healthcare professional's device.
4. Send the new medical data generated to the patient in a secure way, using asymmetric encryption to encrypt the message.
5. Synchronize the new data generated by the healthcare professional application to the central hospital information system and certify them in the blockchain network, when the network connection and the hospital system are available.
<p>&nbsp  </p>

## **FHIR: versatility and complexity of the international standard**

FHIR is the international standard for cross-border healthcare. It is a very versatile system, but its versatility is based on complex nested structures, which translates into greater complexity when it comes to searching, converting data from or to other formats and allowing it to be understood and used in a way fast and practical by any application and computer system.

UHC simplifies the adoption of FHIR and its use beyond the healthcare setting, for example, to verify laboratory results and COVID-19 vaccinations outside the healthcare setting.

As an example, the code of the target disease for a vaccination (*targetDisease*) is not directly accessible in the FHIR Immunization resource, but rather the codes are contained in a nested multi-level structure.

In this example, the target disease for vaccination is COVID-19 and is coded using two different systems: the **U07.1** code from the *ICD-10* system and the **840539006** code from the *SNOMED* system:

```json
{
   "doseQuantity":{
      "code":"ml",
      "system":"http://unitsofmeasure.org",
      "value":0.3
   },
   "id":"universal-immunization-id",
   "lotNumber":"lot-1234",
   "manufacturer":{
      "display":"Pharmaceutical Laboratory",
      "identifier":{
         "type":{
            "coding":[
               {
                  "code":"PHL",
                  "system":"http://terminology.hl7.org/CodeSystem/MVX"
               }
            ]
         }
      }
   },
   "occurrenceDateTime":"2020-02-18",
   "patient":{
      "reference":"Patient/universal-health-id"
   },
   "protocolApplied":[
      {
         "doseNumberPositiveInt":1,
         "seriesDosesPositiveInt":2,
         "targetDisease":[
            {
               "coding":[
                  {
                     "code":"U07.1",
                     "system":"http://hl7.org/fhir/ValueSet/icd-10"
                  },
                  {
                     "code":"840539006",
                     "system":"http://snomed.info/sct"
                  }
               ]
            }
         ]
      }
   ],
   "resourceType":"Immunization",
   "status":"completed",
   "vaccineCode":{
      "coding":[
         {
            "code":"J07BX03",
            "system":"http://www.whocc.no/atc"
         },
         {
            "code":"207",
            "system":"http://hl7.org/fhir/sid/cvx"
         }
      ]
   }
}
```
<sub>Example of *FHIR Immunization* resource (vaccination) against disease COVID-19 (*"targetDisease"*)</sub>
<p>&nbsp  </p>

UHC allows this FHIR resource to be created and understood more easily by any computer system using UHC "sheets" in this way:

```javascript
{
    doseAmountCode: "ml",
    doseAmountValue: 0.3,
    id: "universal-immunization-id",
    lotNumber: "lot-1234", // Vaccine lot number.
    manufacturerReference: "Organization/universal-id",
    occurrenceDateTime: "2020-02-18", // Vaccine administration date.
    patientReference: "Patient/universal-health-id",
    protocolDoseAdministered: 1, // Number of the dose administered for immunity
    protocolTotalDosesRecommended: 2, // Recommended number of doses for immunity
    protocolTargetDiseasesCodesICD10: ["U07.1"], // Disease(s) being targetted: WHO ICD-10 code(s)
    protocolTargetDiseasesCodesSNOMED: ["840539006"], //Disease(s) being targetted: SNOMED code(s)
    status: "completed",
    vacineCodeATC: "J07BX03", // Vaccine administered: ATC code	
    vacineCodeCVX: "207", // Vaccine administered: HL7 CVX code	
}
```
<sub>Example of a UHC "sheet" corresponding to the *FHIR Immunization* resource against COVID-19 disease</sub>
<p>&nbsp  </p>

On the other hand, the references to the patient in the *Immunization* resource can be expanded in this way within according to the FHIR specifications:

```json
{
    "patient": {
        "identifier": {
            "assigner": {
                "display": "Ministerio del Interior - Gobierno de España"
            },
            "period": {
                "end": "2028-04-30",
                "start": "2018-04-30"
            },
            "system": "urn:oid:1.3.6.1.4.1.19126.3",
            "type": {
                "coding": [
                    {
                        "code": "NNESP",
                        "display": "National Person Identifier",
                        "system": "http://hl7.org/fhir/v2/0203/"
                    }
                ],
                "text": "Documento Nacional de Identidad"
            },
            "use": "official",
            "value": "DNI123456"
        },
        "reference": "Patient/universal-health-id",
        "type": "Patient"
    },
    "resourceType": "Immunization"
}
```
<sub>Example of the *"patient"* data object of a Spanish citizen in a FHIR Immunization resource</sub>
<p>&nbsp  </p>

In a simplified way, the above *"patient"* object can be created and converted to a *UHC Immunization sheet* using these fields:

```javascript
{
   patientIdentifierAssignerDisplay: "Ministerio del Interior - Gobierno de España",
   patientIdentifierCode: "NNESP", // HL7 type code: Spanish National Person Identifier
   patientIdentifierCodeCustomText: "Documento Nacional de Identidad",
   patientIdentifierCodeDisplay: "National Person Identifier",
   patientIdentifierCodeSystemUri: "http://hl7.org/fhir/v2/0203/", // HL7 Identifier Type system
   patientIdentifierPeriodEnd: "2028-04-30",
   patientIdentifierPeriodStart: "2018-04-30",
   patientIdentifierSystemUri: "urn:oid:1.3.6.1.4.1.19126.3", // Spanish's National Person Identifier System
   patientIdentifierUse: "official",
   patientIdentifierValue: "DNI123456", // The value of the Spanish National Person Identifier
}
```
<sub>Fields corresponding to the patient's identifier on a *UHC Immunization Sheet*</sub>
<p>&nbsp  </p>

UHC makes it possible to simplify and extend the use of FHIR to any system, both in the health sector and others, so that the complex nested structures of FHIR can be created, used and understood in a simpler and easier way.
<p>&nbsp  </p>
