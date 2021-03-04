![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain**
Copyright © 2021 Fundación UNID. Reservados todos los derechos. 
<p>&nbsp  <p>

## **Historia clínica unificada y universal**

La [Fundación UNID](http://unid.es) y la empresa española Conéctate Soluciones y Aplicaciones SL ([ConnectHealth](https://connecthealth.info)), han desarrollado Universal Health Chain (UHC) como plataforma para la comunicación segura de datos de salud entre las personas y diferentes servicios de salud y de otros ámbitos.

[![](https://img.youtube.com/vi/LIEneYmrYRY/0.jpg)](https://www.youtube.com/watch?v=LIEneYmrYRY)

Las personas pueden unificar sus datos de salud de organizaciones públicas y privadas en su teléfono móvil, de manera segura, junto con su [Identificador Universal de Salud](https://patentscope.wipo.int/search/es/detail.jsf?docId=WO2020136289&tab=PCTBIBLIO). Universal Health Chain (UHC) utiliza los estándares internacionales [HL7 FHIR R4](http://hl7.org/fhir/R4), [International Patient Summary (IPS)](http://hl7.org/fhir/uv/ips), [Verifiable Credentials (VC)](https://www.w3.org/TR/vc-data-model/), entre otros, y permite además incluir archivos PDF, si bien PDF no es el formato internacional para el intercambio de datos médicos ni para atención sanitaria transfronteriza, como sí lo son HL7 FHIR e IPS.

IPS es un documento de FHIR con algunas secciones de la historia clínica obligatorias y otras opcionales, [definido por el Comité Europeo de Estandarización (CEN)](https://www.cen.eu/news/brief-news/Pages/NEWS-2021-009.aspx).
![](http://hl7.org/fhir/uv/ips/IPS_doc_library.png)
<sub>(imagen de <http://hl7.org/fhir/uv/ips>)</sub>
<p>&nbsp  <p>

La aplicación UHC-personal permite a la persona añadir datos de diferentes servicios de salud públicos y privados y de distintos territorios para unificar su historia clínica. También permite que los datos de salud puedan ser compartidos de forma segura desde el móvil de la persona con diferentes servicios de salud y también para otros fines como mostrar resultados de test de laboratorio o vacunación de COVID-19 a la hora de viajar, utilizando conexiones encriptadas que evitan que los datos puedan ser interceptados por personas no autorizadas.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Public_key_shared_secret.svg/536px-Public_key_shared_secret.svg.png)

<sub>(imagen de https://en.wikipedia.org/wiki/Diffie–Hellman_key_exchange)</sub>
<p>&nbsp  <p>

Los datos de la historia clínica del paciente o donante pueden ser recibidos o incorporados en la aplicación UHC-personal de dos formas diferentes:

1. La persona se descarga los datos desde los servicios de salud (públicos y privados) con un usuario y contraseña que le sean proporcionados y los incorpora en UHC-personal. Puede realizarlo añadiendo los archivos manualmente a la aplicación en formato PDF y FHIR JSON. También podrá conectar y descargar los datos de manera automática con los servicios de salud mediante Smart-On-FHIR.

2. El servicio de salud envía a la persona sus datos encriptados, directamente a la aplicación UHC-personal mediante una conexión segura que se crea a partir del Identificador Universal de Salud de la persona, de manera que solo la persona puede desencriptar los datos en su teléfono móvil. Los datos siempre viajan encriptados, por lo que ningún intermediario puede desencriptarlos.

[![](https://img.youtube.com/vi/5f0zP3O5B7c/0.jpg)](https://www.youtube.com/watch?v=5f0zP3O5B7c)
<p>&nbsp  <p>

## **Normativas de acceso y portabilidad de datos de salud y de atención sanitaria transfronteriza**

En EE.UU. la normativa USCDI hace obligatorio que los proveedores de servicios de salud proporcionen a sus clientes (pacientes) los datos de salud en el formato FHIR R4, mediante una API compatible con FHIR y con Oauth2, para que las personas puedan iniciar sesión en un servidor FHIR con un usuario y contraseña, visualizar sus datos y descargarlos en formato FHIR R4 o bien realizar esto mismo mediante una aplicación de terceros que se conecte al servidor FHIR con el usuario y contraseña del usuario para obtener un token de autenticación.

Esto, sin embargo, no impide los ataques del tipo Man-In-The-Middle, en el tráfico entre el servidor API del proveedor de salud y la aplicación o web del usuario, en el caso de que la red del usuario esté comprometida (por ejemplo una red WIFI mediante un ataque con DNS spoofing). UHC soluciona este problema mediante el servicio de mensajería con encriptación punto a punto y la aplicación UHC-personal.

En Europa la normativa especifica que los datos tienen que entregarse de manera digital a la persona en un formato electrónico común para la atención sanitaria transfronteriza. Este formato es *International Patient Summary* o *IPS*, establecido por el Comité Europeo de Estandarización (CEN), que utiliza FHIR R4 y establece diferentes secciones en el documento FHIR que continene la historia clínica del pacicente.

UHC aporta la herramienta que permite cumplir con las difetentes normativas, ya que la persona podrá recibir sus datos de salud mediante el Identificador Universal de Salud, por ejemplo desde un laboratorio, y posteriormente podrá enviar o compartir determinados datos de salud como resultados de test de laboratorio o vacunaciones de COVID-19, entre otros datos posibles dentro de la historia clínica que la persona unifica y tiene encriptada de manera segura en la aplicación UHC-personal.
<p>&nbsp  <p>

## **Ciberseguridad y resiliencia en salud**

UHC es un sistema sistema resiliente ante virus y ataques informáticos (por ejemplo, Wannacry en 2017), terrorismo o catástrofes naturales. Permite que los sistemas de salud y las aplicaciones del los profesionales sanitarios puedan funcionar de forma autónoma incluso sin conexión a internet, ya que existe la posibilidad de compartir datos entre el móvil de la persona y un servicio de salud utilizando bluetooth en caso de caída de las redes o de los sistemas informáticos.

![](https://www.virtualsecurity.es/images/noticias/wannamapa.jpg)
<sub>(imagen de https://www.virtualsecurity.es/images/noticias/wannamapa.jpg)</sub>
<p>&nbsp  <p>

UHC se basa en la criptografía asimétrica de Curva Elíptica Diffie-Hellman (ECDH) en la que cada participante dispone de claves públicas y privadas para firma y encriptación de datos.
Mediante el Identificador Universal de Salud y la identidad digital de la Fundación UNID, cada usuario (paciente, profesional, organización) o dispositivo (servidor, dispositivo médico, etc.) tiene una identidad digital con unas claves privadas y públicas para firmar y encriptar información.
<p>&nbsp  <p>

## **Blockchain de la Fundación UNID**

Hyperledger Fabric es una red empresarial en la que pueden existir diferentes canales, de manera similar a las sub redes informáticas. Al ser una red permisionada, cada canal tiene establecidos qué *peer nodes* o nodos "iguales" (servidores de organizaciones) pueden pertenecer al mismo. En la blockchain de la Fundación UNID los canales serán distintos para "HealthCare" (certificación y verificación de datos para atención sanitaria y donaciones) que para "Biological Products" (certificación y trazabilidad de productos de origen biológico para fines medicinales).

![](https://www.serial-coder.com/img/posts/Demystifying-Hyperledger-Fabric/Fabric-Explained-4%20%28-sharp-2%29.png)
<sub>(imagen de https://www.serial-coder.com/post/demystifying-hyperledger-fabric-fabric-architecture)</sub>
<p>&nbsp  <p>

Cada organización puede tener uno o varios peer nodes, y cada peer node puede pertenecer a uno o varios canales. Por ejemplo, un mismo servidor puede pertenecer a HealthCare y Biological Products y la organización puede tener, uno o más servidores (peer nodes), por ejemplo en Europa, Norteamérica y Asia.

Un esquema se encuentra en la sección "[Peers and organizations](https://hyperledger-fabric.readthedocs.io/en/release-2.2/peers/peers.html)" en la documentación de Hyperledger Fabric:

![alt text](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/peers.diagram.8.png
 "Organizaciones y nodos")
  

Además de esto, Hyperledger Fabric permite que los peer nodes (o servidores) de una misma organización o de distintas organizaciones pueden utilizar [Private Data Collections o PDCs](https://hyperledger-fabric.readthedocs.io/en/release-2.2/private-data/private-data.html) para almacenar datos de forma privada, al margen de los canales públicos (ledgers), de manera temporal o permanente, cumpliendo con GDPR.

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-2.png)

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-3.png)
<p>&nbsp  <p>

De esta manera, una organización puede compartir información privada entre diferentes peer nodes de su organización, y también puede crear PDCs para compartir información privada con clientes o proveedores de su organización, o una administración pública de un territorio puede compartir datos con diferentes administraciones públicas de otros territorios o con otros tipos de organizaciones como laboratorios (por ejemplo para reporte de datos).

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-1.png)

![](https://www.serial-coder.com/img/posts/Demystifying-Hyperledger-Fabric/Fabric-Explained-7%20%28-sharp-2%29.png)

<sub>(imagen de <https://www.serial-coder.com/post/demystifying-hyperledger-fabric-fabric-architecture>)</sub>
<p>&nbsp  <p>

Hyperledger Fabric es, por tanto, una red de redes que permite múltiples posibilidades. La característica principal de las PDCs es que para cada registro de datos que se guarda en una PDC, Hyperledger Fabric crea un valor *hash* o huella digital de ese registro de datos, y este hash es guardado en el ledger (público) del canal en el que se encuentre la PDC. De esta manera, cuando un cliente reciba los datos, podrá verificar que el hash o huella digital de los datos es cierto en el canal (público). Para hacer esto, el cliente genera el valor hash de los datos y lo compara con el el hash original guardado en el canal de la blockchain, mediante el ID del recurso almacenado en la PDC y el nombre de la PDC.

![](https://cdn.thenewstack.io/media/2020/08/e06c3bc6-image2.png)

<sub>(imagen de <https://thenewstack.io/using-private-data-collections-in-hyperledger-fabric>)</sub>
<p>&nbsp  <p>

De esta manera, Hyperledger Fabric puede ser utilizada como base de datos privada y distribuida con certificación de datos automática en el canal público, y que garantiza la confidencialidad de los datos mediante PDCs, cumplimiento con las normativas de protección de datos GDPR puesto que los datos en las PDCs son privados y pueden ser borrados (derecho al olvido).

![](https://miro.medium.com/max/700/0*TCU0KW7ZUJjpwGYH)

<sub>(imagen de <https://kctheservant.medium.com/private-data-implicit-data-collections-in-hyperledger-fabric-v2-0-f2ef41f0e99d>)</sub>
<p>&nbsp  <p>

![](https://miro.medium.com/max/2400/1*rP6Nz2xDsIXpgrXS6pyoWQ.png)

<sub>(imagen de <https://kctheservant.medium.com/private-data-and-transient-data-in-hyperledger-fabric-46b5258f391e>)</sub>
<p>&nbsp  <p>

La Fundación UNID, en colaboración con las empresas Conéctate Soluciones y Aplicaciones SL (España) y Connecting Solution & Applications Ltd. (Canadá), ha desarrollado smart-contracts en Hyperledger Fabric para la certificación y trazabilidad de procesos en la atención sanitaria y de productos biológicos para fines medicinales. La documentación se irá actualizando en la web de la Fundación (<http://unid.es>) y en Github (<https://github.com/Universal-Health-Chain/docs>)

La Fundación UNID está desarrollando en colaboración con Connecting Solution & Applications Ltd. los smart-contracts para la trazabilidad de productos biológicos (denominados chaincode en Hyperledger Fabric) en su versión 2.0:

### **Product Management**

**PUT** /product
creates a new product

**GET** /product/{productId}
gets a product

**PUT** /product/{productId}
updates a product

**DELETE** /product/{productId}
delete a product

**POST** /product/{productId}​/split
split a product into other products

**POST** /product/merge
merge a list of products into a new product

**GET** /product/{productId}/trace
get the full trace of a product

**GET** /product/{query}
get the requested products according to the query

### **Event Management**

**PUT** /product/event
creates a new event

**GET** /product/event/{eventId}
gets an event

**GET** /product/event/{query}
get the requested events according to the query
<p>&nbsp  <p>

Además, la Fundación UNID está desarrollando otros smart-contracts en colaboración con Conéctate Soluciones y Aplicaciones SL para registrar el hash de recursos FHIR y pruebas de firma digital ([Linked Data Proofs](https://w3c-ccg.github.io/ld-proofs/)) también en la versión 2.0 de Hyperledger Fabric.
<p>&nbsp  <p>

## **Estándares internacionales accesibles y sencillos para todos**

UHC permite que cualquier organización pueda crear y leer recursos de FHIR de una manera sencilla, tanto para atención sanitaria como para laboratorios, trazabilidad de productos biológicos y también para servicios y aplicaciones ajenos al ámbito de la salud. Cada organización podrá desplegar su propio servicio de manera gratuita o utilizar el servicio de ayuda alojado por la Fundación UNID, que está siendo desarrollado en colaboración con la empresa Conéctate Soluciones y Aplicaciones SL.

El envío de información de salud al usuario se realiza en UHC mediante mensajes, documentos y recursos FHIR R4, si bien UHC también admite Verifiable Credentials. Para organizaciones que todavía no hayan implantado FHIR, el sistema de UHC puede recibir solamente los códigos clínicos SNOMED LOINC y HL7 (entre otros) para contruir los datos en formato FHIR y que estos sean enviados porteriormente a la persona, facilitando la transformación digital para ayudar a conseguir el cumplimiento de las normativas, uso de estándares internacionales y la atención sanitaria transfronteriza

En concreto, el servicio de ayuda de UHC permite lo siguiente:

1. Enviar unos campos básicos para generar el recurso de FHIR deseado a partir de estos campos (informe o test de laboratorio, vacunación, etc.), para que los estándares internacionales HL7 FHIR e International Patient Summary (IPS) sean de fácil adopción por parte de cualquier organización.

2. Convertir datos en el estándar internacional FHIR a formularios sencillos estandarizados, de manera que puedan ser leídos, verificados y entendidos por cualquier aplicación y sistema informático del ámbito de la salud y también de otros ámbitos ajenos al mundo sanitario, para lograr la interoperabilidad no solo entre los servicios de salud sino también de fuera del ámbito de la salud: cines, teatros, museos, congresos, bibliotecas, medios de transporte, etc.


A modo de ejemplo, un informe de laboratorio de FHIR (DiagnosticReport) puede ser generado enviando un objeto de datos JSON al servicio de ayuda de UHC (UHC-Helpers) que contenga los códigos de terminología clínica internacional (ampliamente reconocidos tanto en Europa como en EE.UU. y en otros países), como son principalmente LOINC, SNOMED y HL7 FHIR

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
<sub>*Ejemplo de objeto de datos "hoja" (sheet) de UHC que simplifica la compleja estructura anidada de FHIR*</sub>
<p>&nbsp  <p>

El servicio de ayuda de UHC convierte esos campos básicos (sheet) en la estructura de datos del recurso de FHIR correspondiente (que en este caso corresponde con un informe de laboratorio o FHIR "DiagnosticReport") y genera además un identificador único UUID (ampliamente utilizado internacionalmente) para identificar unívocamente este recurso de FHIR a nivel global y de manera universal en cualquier territorio y organización:

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
<sub>*Ejemplo de recurso FHIR Diagnostic Report generado a partir de la "hoja" (sheet) de UHC anterior*</sub>
<p>&nbsp  <p>

El servicio de ayuda de UHC permite obtener una huella digital de los datos. Las funciones hash generan una huella digital, y tienen la característica de que el valor hash generado es radicalmente distinto con un mínimo cambio que se produzca en los datos (con un solo bit modificado el valor hash es totalmente distinto). Por ejemplo, al aplicar la función hash SHA-256 (ampliamente utilizada), se obtiene un resultado o huella digital de este tipo:

*8100abc4946288bfcefab256cf7f8da14754e57645e87dcef172db6d4940b733*

Como el identificador UUID del recurso de FHIR (informe de laboratorio) es único y unívoco, el valor hash SHA-256 obtenido será también unívoco, es decir, no podrá obtenerse el mismo valor hash a partir de ningún otro recurso de FHIR, lo que asegura que los datos originales puedan ser verificados y que pueda conocerse si los datos que contiene el recurso de FHIR han sido alterado o modificados (el valor hash será totalmente distinto en tal caso).

De esta manera, una vez generado el recurso de FHIR y el valor hash asociado al identificador único del recurso de FHIR, la organización que crea los datos puede guardar el valor hash generado utilizando la red de blockchain de la Fundación UNID. El valor hash queda asociado en la red de blockchain con el identificador UUID del recurso de FHIR, de forma que un tercero podrá validar los datos originales siguiendo estos pasos:  

1. Generar el valor hash SHA-256 del recurso de FHIR que se quiere verificar, utilizando el servicio de ayuda de UHC u otras funciones que "canonicen" y "serialicen" el recurso de FHIR antes de generar el valor hash, para asegurar que se calcula siempre de la misma manera, de forma correcta y estandarizada.

2. Recuperar de la blockchain el hash original, utilizando el identificador universal UUID del recurso de FHIR.

3. Comparar el valor hash calculado con el valor hash almacenado en la blockchain.

4. En caso de que no coincidan, puede pedirse a la blockchain que recupere la historia del recurso de FHIR, para obtener los valores hash almacenados cada vez que se haya modificado el recurso de FHIR. De esta forma se puede comprobar si el valor hash calculado fue válido en algún estado anterior del recurso de FHIR (los datos recibidos están obsoletos) o si por el contrario los datos recibidos no han sido certificados en ningún momento en la red de blockchain.


Por tanto, cuando una aplicación recibe los datos en FHIR del paciente, donante o cliente, tanto en el ámbito sanitario como en otros ámbitos, puede comprobar la huella digital de los datos para verificar la autenticidad de los mismos. Posteriormente, los datos FHIR a un formato simplificado "plano" de UHC, a un formulario estandarizado JSON Schema Form y / o usar el código HTML correspondiente a estos datos, utilizando el servicio de ayuda de UHC u otras funciones.

La Fundación UNID está desarrollando, en colaboración con la empresa Conéctate Soluciones y Aplicaciones SL, una web de UHC para organizaciones y profesionales que permite realizar los procesos de una manera gráfica, de manera que cualquier profesional de una organización que colabore en el testeo de UHC con la fundación UNID, aunque no tenga conocimientos de programación y no sepa de terminología sanitaria, pueda ver cómo generar recursos de FHIR, generar la huella digital o *hash* de los datos, verificar la firma digital de los datos, etc. Esta web también puede ser utilizada para enviar datos médicos como la Historia Clínica de la persona en el formato internacional IPS (aprobado en Europa por el CEN) mediante conexiones encriptadas, directamente al móvil de la persona, de manera segura y evitando que las comunicaciones de los datos puedan ser interceptados por terceros malintencionados (hackers).
<p>&nbsp  <p>
  

## **Credenciales verificables con FHIR**

La Fundación UNID, en colaboración con Conéctate Soluciones y Aplicaciones SL, ha desarrollado también el sistema que permite convertir los datos de FHIR a credenciales verificables en formato internacional del World Wide Web Consortium (W3C). A modo de ejemplo, una credencial verificable o VC de FHIR, creada a partir de un informe diagnóstico como el anterior, puede ser creada simplemente añadiendo el informe de laboratorio en el campo "credentialSubject" (que contiene el objeto u objetos a los que se refiere la credencial verificable) de esta forma:

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
<sub>*Esquema básico que muestra cómo un resurso de FHIR es introducido en una credencial verificable (VC) según el estándar de W3C*</sub>
<p>&nbsp  <p>

De manera similar, también se pueden utilizar los formatos "sheet" de UHC dentro de una credencial verificable, en cuyo caso el tipo de la credencial no comenzará con "VC/FHIR/R4" sino con "UHC/Sheet/1.0":
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
<sub>*Esquema básico que muestra cómo un resurso de FHIR es introducido en una credencial verificable (VC) según el estándar de W3C*</sub>
<p>&nbsp  <p>

La característica principal de las credenciales verificables es que pueden ser firmadas digitalmente en el formato estandarizado por W3C, generado un objeto "proof" en el formato Linked Data Proof o LD-Proof.

Los datos FHIR en una credencial verificable pueden ser firmados utilizando una credencial verificable o utilizando un recurso FHIR Provenance, que podría estar contenido dentro del recurso FHIR DiagnosticReport (utilizando el campo "contained" para ello) según las especificaciones de FHIR, o bien podría ser un recurso de FHIR adicional al recurso DiagnosticReport, tal y como está recogido en [United States Core Data for Interoperability (USCDI)](https://www.healthit.gov/isa/united-states-core-data-interoperability-uscdi). En este último caso, el campo "credentialSubject" de la credencial verificable contendría dos recursos de FHIR, uno con el informe de laboratorio (DiagnosticReport) y otro con la prueba de procedencia (Provenance).

El servicio de ayuda de UHC permitirá que puedan ser generadas y verificadas las firmas digitales tanto en el recurso FHIR Provenance como en el formato de Linked Data Proof definido por W3C.
<p>&nbsp  <p>  

## **Identificador Universal de Salud**

La Fundación UNID implementa en UHC la patente "[Protocolo Unificado de Identificación en Formación de Salud](https://patentscope.wipo.int/search/es/detail.jsf?docId=WO2020136289&tab=PCTBIBLIO)". De esta manera se consigue la identificación universal en la cadena de salud de pacientes, donantes, profesionales sanitarios, servicios de salud, organizaciones, productos biológicos y también de los procesos llevados a cabo en la atención sanitaria como encuentros médicos, resultados diagnósticos, procedimientos, intervenciones, prescripciones, etc.

En FHIR las referencias a Patient, Practitioner, Organization y a otros recursos como Immunization, DiagnosticReport, etc. se crean utilizando el nombre del recurso al que se refieren y añadiendo a continuación el identificador del recurso, separado con una barra diagonal, por ejemplo "Patient/identificador".

La Fundación UNID utiliza UUID v4 como identificador único que puede ser generado por cualquier organización para codificar recursos FHIR de forma universal, y que es compatible con International Patient Summary (IPS). De esta manera, la referencia en FHIR a un resultado de laboratorio sería "DiagnosticReport/<uuid>" y la referencia de una vacunación sería "Immunization/<uuid>".

Aplicando esto mismo a la identificación de personas, pacientes, profesionales, organizaciones y servicios de salud, la Fundación UNID proporciona un identificador universal a todas las partes relacionadas, de manera que pueda verificarse su autenticidad y su identidad.

Así, utilizando UUID v4 como base para la codificación de las identidades, compatible con FHIR, IPS y también con credenciales verificables (VC) y documentos DID, cada una de las partes que participan en la cadena de salud dispone de un Identificador Universal de Salud y de una identidad digital universal.

A modo de ejemplo, el Identificador Universal de la Fundación UNID se puede representar de las siguientes formas:

| Type                  | Description |
| ---                   | --- |
|Patient                | a person with medical history|
|UNID URN               | urn:unid:patient:uuid:uuid-v4|
|UNID DID               | did:unid:patient:uuid:uuid-v4|
|UNID KEY ID (KID)      | did:unid:patient:uuid:uuid-v4#keyBase58|
|FHIR Reference         | Patient/uuid-v4|
|FHIR Identifier IETF   | urn:uuid:uuid-v4|
|IPS Full URN           | urn:uuid:uuid-v4|
|Veres One (v1) DID     | did:v1:uuid:uuid-v4|

La Fundación UNID registra en la red de blockchain las identidades digitales junto con las claves criptográficas públicas asociadas a las mismas, que permiten la verificación de la firma digital de los datos y la encriptación de los mismos cuando se transmiten, utilizando conexiones seguras con encriptación de clave asimétrica.
<p>&nbsp  <p>

## **Identificador Universal de Productos de Origen Biológico**

Los productos de origen biológico como las vacunas o los hemoderivados son dispositivos médicos según las diferentes normativas y disponen de diferentes UDIs para cada legislación, por ejemplo en [Europa](https://ec.europa.eu/docsroom/documents/36664/attachments/1/translations/en/renditions/native), [EE.UU.](https://www.fda.gov/medical-devices/unique-device-identification-system-udi-system/udi-basics) y/o [Australia](https://www.mtaa.org.au/unique-device-identification-udi). Normalmente son implantados, inyectados o utilizados en un pacientes, tales como plasma en tratamientos estéticos ([PRP o plasma rico en plaquetas](https://es.wikipedia.org/wiki/Plasma_rico_en_plaquetas)), vacunas, concentrados de hematíes, medicamentos fabricados a partir de inmunoglobulinas y otro tipo de productos de origen biológico.

Los productos de origen biológico pueden estar codificados con diferentes sistemas tales como:

- [Health Industry Business Communications Council (HIBCC)](https://www.hibcc.org/)
- [International Council for Commonality in Blood Banking Automation (ICCBBA)](https://www.iccbba.org)
- [GS1](https://www.gs1.org/)

La tecnología de UHC permite verificar la trazabilidad de los productos biológicos a lo largo de toda la cadena de la salud y también por las personas y por otras organizaciones y profesionales ajenos a la salud, como en el caso de verificación de vacunación contra COVID-19.

A partir del código de barras de un producto de origen biológico, tanto los profesionales y servicios de salud como los pacientes que compran o reciben estos productos para ser utilizados en tratamientos médicos podrán obtener y verificar la infomración del producto, de manera unificada para productos de diferentes fabricantes, distintos sistemas de codificación y en diferentes normativas, mejorando la seguridad y la trazabilidad de estos productos y permitiendo a las personas conocer toda la información de los productos que les son suministrados o implantados.

A modo de ejemplo, el Identificador Universal de Productos Biológicos de la Fundación UNID se puede representar de las siguientes formas:

| Type                         	    | Description |
| ---				    | --- |
|Dispositivos / productos médicos   | ejemplo.: trazabilidad de una vacuna, hemoderivado, etc.|
|FHIR Reference                     | Device/uuid-v4| 
|FHIR Identifier IETF               | urn:uuid:uuid-v4| 
|IPS Full URN                       | urn:uuid:uuid-v4| 
|UNID URN                           | urn:unid:device:uuid:uuid-v4| 
|UNID DID                           | did:unid:device:uuid:uuid-v4| 

UHC permite certificar y verificar la información de los productos biológicos fuera del ámbito de la salud, por ejemplo para verificar los datos de vacunación de COVID-19 en turismo, congresos, etc., de manera que puede verificarse en la red de blockchain de la Fundación UNID la autenticidad y la trazabilidad de una vacuna fabricada por la industria farmacéutica y administrada en un procedimiento de vacunación.

De esta manera, las organizaciones y profesionales sanitarios que crean datos de salud y de productos de origen biológico pueden registrar la huella digital de los datos generados en la red de blockchain, de manera descentralizada, lo que permite que la autenticidad de los datos pueda ser verificada tanto por los pacientes que reciban estos datos como por otros profesionales y organizaciones con los que la persona comparta los datos posteriormente.
