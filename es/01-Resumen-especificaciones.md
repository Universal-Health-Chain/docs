![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain**
Copyright © 2021 Fundación UNID. Reservados todos los derechos. 
<p>&nbsp  </p>

## **Historia clínica unificada y universal**

La [Fundación UNID](http://unid.es) y la empresa española Conéctate Soluciones y Aplicaciones SL ([ConnectHealth](https://connecthealth.info)), han desarrollado Universal Health Chain (UHC) como plataforma para la comunicación segura de datos de salud entre las personas y diferentes servicios de salud y de otros ámbitos.

[![](https://img.youtube.com/vi/LIEneYmrYRY/0.jpg)](https://www.youtube.com/watch?v=LIEneYmrYRY)

<sub>Vídeo de la plataforma UHC (clic para abrir Youtube)</sub>
<p>&nbsp  </p>

Las personas pueden unificar sus datos de salud de organizaciones públicas y privadas en su teléfono móvil, de manera segura, junto con su [Identificador Universal de Salud](https://patentscope.wipo.int/search/es/detail.jsf?docId=WO2020136289&tab=PCTBIBLIO). Universal Health Chain (UHC) utiliza los estándares internacionales [HL7 FHIR R4](http://hl7.org/fhir/R4), [International Patient Summary (IPS)](http://hl7.org/fhir/uv/ips), [Verifiable Credentials (VC)](https://www.w3.org/TR/vc-data-model/), entre otros, y permite además incluir archivos PDF, si bien PDF no es el formato internacional para el intercambio de datos médicos ni para atención sanitaria transfronteriza, como sí lo son HL7 FHIR e IPS.

IPS es un documento de FHIR con algunas secciones de la historia clínica obligatorias y otras opcionales, [definido por el Comité Europeo de Estandarización (CEN)](https://www.cen.eu/news/brief-news/Pages/NEWS-2021-009.aspx).
![](http://hl7.org/fhir/uv/ips/IPS_doc_library.png)
<sub>(imagen de <http://hl7.org/fhir/uv/ips>)</sub>
<p>&nbsp  </p>

La aplicación UHC-personal permite a la persona añadir datos de diferentes servicios de salud públicos y privados y de distintos territorios para unificar su historia clínica. También permite que los datos de salud puedan ser compartidos de forma segura desde el móvil de la persona con diferentes servicios de salud y también para otros fines como mostrar resultados de test de laboratorio o vacunación de COVID-19 a la hora de viajar, utilizando conexiones encriptadas que evitan que los datos puedan ser interceptados por personas no autorizadas.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Public_key_shared_secret.svg/536px-Public_key_shared_secret.svg.png)

<sub>(imagen de https://en.wikipedia.org/wiki/Diffie–Hellman_key_exchange)</sub>
<p>&nbsp  </p>

Los datos de la historia clínica del paciente o donante pueden ser recibidos o incorporados en la aplicación UHC-personal de dos formas diferentes:

1. La persona se descarga los datos desde los servicios de salud (públicos y privados) con un usuario y contraseña que le sean proporcionados y los incorpora en UHC-personal. Puede realizarlo añadiendo los archivos manualmente a la aplicación en formato PDF y FHIR JSON. También podrá conectar y descargar los datos de manera automática con los servicios de salud mediante Smart-On-FHIR.

2. El servicio de salud envía a la persona sus datos encriptados, directamente a la aplicación UHC-personal mediante una conexión segura que se crea a partir del Identificador Universal de Salud de la persona, de manera que solo la persona puede desencriptar los datos en su teléfono móvil. Los datos siempre viajan encriptados, por lo que ningún intermediario puede desencriptarlos.

[![](https://img.youtube.com/vi/5f0zP3O5B7c/0.jpg)](https://www.youtube.com/watch?v=5f0zP3O5B7c)

<sub>Vídeo de la aplicación UHC-personal (clic para abrir Youtube)</sub>
<p>&nbsp  </p>

## **Normativas de acceso y portabilidad de datos de salud y de atención sanitaria transfronteriza**

En EE.UU. la normativa USCDI hace obligatorio que los proveedores de servicios de salud proporcionen a sus clientes (pacientes) los datos de salud en el formato FHIR R4, mediante una API compatible con FHIR y con Oauth2, para que las personas puedan iniciar sesión en un servidor FHIR con un usuario y contraseña, visualizar sus datos y descargarlos en formato FHIR R4 o bien realizar esto mismo mediante una aplicación de terceros que se conecte al servidor FHIR con el usuario y contraseña del usuario para obtener un token de autenticación.

Esto, sin embargo, no impide los ataques del tipo Man-In-The-Middle, en el tráfico entre el servidor API del proveedor de salud y la aplicación o web del usuario, en el caso de que la red del usuario esté comprometida (por ejemplo una red WIFI mediante un ataque con DNS spoofing). UHC soluciona este problema mediante el servicio de mensajería con encriptación punto a punto y la aplicación UHC-personal.

En Europa la normativa especifica que los datos tienen que entregarse de manera digital a la persona en un formato electrónico común para la atención sanitaria transfronteriza. Este formato es [*International Patient Summary* (IPS), establecido por el Comité Europeo de Estandarización (CEN)](https://www.cen.eu/news/brief-news/Pages/NEWS-2021-009.aspx), que utiliza FHIR R4 y establece diferentes [secciones en el documento FHIR que contiene la historia clínica del paciente](http://hl7.org/fhir/uv/ips/ipsStructure.html).

UHC aporta la herramienta que permite cumplir con las difetentes normativas, ya que la persona podrá recibir sus datos de salud mediante el Identificador Universal de Salud, por ejemplo desde un laboratorio, y posteriormente podrá enviar o compartir determinados datos de salud como resultados de test de laboratorio o vacunaciones de COVID-19, entre otros datos posibles dentro de la historia clínica que la persona unifica y tiene encriptada de manera segura en la aplicación UHC-personal.
<p>&nbsp  </p>

## **Ciberseguridad y resiliencia en salud**

UHC es un sistema sistema resiliente ante virus y ataques informáticos (por ejemplo, Wannacry en 2017), terrorismo o catástrofes naturales. Permite que los sistemas de salud y las aplicaciones del los profesionales sanitarios puedan funcionar de forma autónoma incluso sin conexión a internet, ya que existe la posibilidad de compartir datos entre el móvil de la persona y un servicio de salud utilizando bluetooth en caso de caída de las redes o de los sistemas informáticos.

![](https://www.virtualsecurity.es/images/noticias/wannamapa.jpg)
<sub>(imagen de https://www.virtualsecurity.es/images/noticias/wannamapa.jpg)</sub>
<p>&nbsp  </p>

UHC se basa en la criptografía asimétrica de Curva Elíptica Diffie-Hellman (ECDH) en la que cada participante dispone de claves públicas y privadas para firma y encriptación de datos.
Mediante el Identificador Universal de Salud y la identidad digital de la Fundación UNID, cada usuario (paciente, profesional, organización) o dispositivo (servidor, dispositivo médico, etc.) tiene una identidad digital con unas claves privadas y públicas para firmar y encriptar información.
<p>&nbsp  </p>

## **Blockchain de la Fundación UNID**

Hyperledger Fabric es una red empresarial en la que pueden existir diferentes canales, de manera similar a las sub redes informáticas. Al ser una red permisionada, cada canal tiene establecidos qué *peer nodes* o nodos "iguales" (servidores de organizaciones) pueden pertenecer al mismo. En la blockchain de la Fundación UNID los canales serán distintos para "HealthCare" (certificación y verificación de datos para atención sanitaria y donaciones) que para "Biological Products" (certificación y trazabilidad de productos de origen biológico para fines medicinales).

![](https://www.serial-coder.com/img/posts/Demystifying-Hyperledger-Fabric/Fabric-Explained-4%20%28-sharp-2%29.png)
<sub>(imagen de https://www.serial-coder.com/post/demystifying-hyperledger-fabric-fabric-architecture)</sub>
<p>&nbsp  </p>

Cada organización puede tener uno o varios peer nodes, y cada peer node puede pertenecer a uno o varios canales. Por ejemplo, un mismo servidor puede pertenecer a HealthCare y Biological Products y la organización puede tener, uno o más servidores (peer nodes), por ejemplo en Europa, Norteamérica y Asia.

Un esquema se encuentra en la sección "[Peers and organizations](https://hyperledger-fabric.readthedocs.io/en/release-2.2/peers/peers.html)" en la documentación de Hyperledger Fabric:

![alt text](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/peers.diagram.8.png
 "Organizaciones y nodos")
  

Además de esto, Hyperledger Fabric permite que los peer nodes (o servidores) de una misma organización o de distintas organizaciones pueden utilizar [Private Data Collections o PDCs](https://hyperledger-fabric.readthedocs.io/en/release-2.2/private-data/private-data.html) para almacenar datos de forma privada, al margen de los canales públicos (ledgers), de manera temporal o permanente, cumpliendo con GDPR.

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-2.png)

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-3.png)
<p>&nbsp  </p>

De esta manera, una organización puede compartir información privada entre diferentes peer nodes de su organización, y también puede crear PDCs para compartir información privada con clientes o proveedores de su organización, o una administración pública de un territorio puede compartir datos con diferentes administraciones públicas de otros territorios o con otros tipos de organizaciones como laboratorios (por ejemplo para reporte de datos).

![](https://hyperledger-fabric.readthedocs.io/en/release-2.2/_images/PrivateDataConcept-1.png)

![](https://www.serial-coder.com/img/posts/Demystifying-Hyperledger-Fabric/Fabric-Explained-7%20%28-sharp-2%29.png)

<sub>(imagen de <https://www.serial-coder.com/post/demystifying-hyperledger-fabric-fabric-architecture>)</sub>
<p>&nbsp  </p>

Hyperledger Fabric es, por tanto, una red de redes que permite múltiples posibilidades. La característica principal de las PDCs es que para cada registro de datos que se guarda en una PDC, Hyperledger Fabric crea un valor *hash* o huella digital de ese registro de datos, y este hash es guardado en el ledger (público) del canal en el que se encuentre la PDC. De esta manera, cuando un cliente reciba los datos, podrá verificar que el hash o huella digital de los datos es cierto en el canal (público). Para hacer esto, el cliente genera el valor hash de los datos y lo compara con el el hash original guardado en el canal de la blockchain, mediante el ID del recurso almacenado en la PDC y el nombre de la PDC.

![](https://cdn.thenewstack.io/media/2020/08/e06c3bc6-image2.png)

<sub>(imagen de <https://thenewstack.io/using-private-data-collections-in-hyperledger-fabric>)</sub>
<p>&nbsp  </p>

De esta manera, Hyperledger Fabric puede ser utilizada como base de datos privada y distribuida con certificación de datos automática en el canal público, y que garantiza la confidencialidad de los datos mediante PDCs, cumplimiento con las normativas de protección de datos GDPR puesto que los datos en las PDCs son privados y pueden ser borrados (derecho al olvido).

![](https://miro.medium.com/max/700/0*TCU0KW7ZUJjpwGYH)

<sub>(imagen de <https://kctheservant.medium.com/private-data-implicit-data-collections-in-hyperledger-fabric-v2-0-f2ef41f0e99d>)</sub>
<p>&nbsp  </p>

![](https://miro.medium.com/max/2400/1*rP6Nz2xDsIXpgrXS6pyoWQ.png)

<sub>(imagen de <https://kctheservant.medium.com/private-data-and-transient-data-in-hyperledger-fabric-46b5258f391e>)</sub>
<p>&nbsp  </p>

La Fundación UNID, en colaboración con las empresas Conéctate Soluciones y Aplicaciones SL (España) y Connecting Solution & Applications Ltd. (Canadá), ha desarrollado smart-contracts en Hyperledger Fabric para la certificación y trazabilidad de procesos en la atención sanitaria y de productos biológicos para fines medicinales. La documentación se irá actualizando en la web de la Fundación (<http://unid.es>) y en Github (<https://github.com/Universal-Health-Chain/docs>)

La Fundación UNID está desarrollando en colaboración con Connecting Solution & Applications Ltd. los smart-contracts para la trazabilidad de productos biológicos (denominados chaincode en Hyperledger Fabric) en su versión 2.0:

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

Además, la Fundación UNID está desarrollando otros smart-contracts en colaboración con Conéctate Soluciones y Aplicaciones SL para registrar el hash de recursos FHIR y pruebas de firma digital ([Linked Data Proofs](https://w3c-ccg.github.io/ld-proofs/)) también en la versión 2.0 de Hyperledger Fabric.
<p>&nbsp  </p>

## **Estándares internacionales accesibles y sencillos para todos**

UHC permite que cualquier organización pueda crear y leer recursos de FHIR de una manera sencilla, tanto para atención sanitaria como para laboratorios, trazabilidad de productos biológicos y también para servicios y aplicaciones ajenos al ámbito de la salud. Cada organización podrá desplegar su propio servicio de manera gratuita o utilizar el servicio de ayuda alojado por la Fundación UNID, que está siendo desarrollado en colaboración con la empresa Conéctate Soluciones y Aplicaciones SL.

El envío de información de salud al usuario se realiza en UHC mediante mensajes, documentos y recursos FHIR R4, si bien UHC también admite Verifiable Credentials. Para organizaciones que todavía no hayan implantado FHIR, el sistema de UHC puede recibir solamente los códigos clínicos SNOMED LOINC y HL7 (entre otros) para construir los datos en formato FHIR y que estos sean enviados porteriormente a la persona, facilitando la transformación digital para ayudar a conseguir el cumplimiento de las normativas, uso de estándares internacionales y la atención sanitaria transfronteriza

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
<p>&nbsp  </p>

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
<p>&nbsp  </p>

## **Certificación de datos**

El servicio de ayuda de UHC permite obtener una huella digital de los datos. Las funciones hash generan una huella digital, y tienen la característica de que el valor hash generado es radicalmente distinto con un mínimo cambio que se produzca en los datos (con un solo bit modificado el valor hash es totalmente distinto). Por ejemplo, al aplicar la función hash SHA-256 (ampliamente utilizada), se obtiene un resultado o huella digital de este tipo:

*8100abc4946288bfcefab256cf7f8da14754e57645e87dcef172db6d4940b733*

Como el identificador UUID del recurso de FHIR (informe de laboratorio) es único y unívoco, el valor hash SHA-256 obtenido será también unívoco, es decir, no podrá obtenerse el mismo valor hash a partir de ningún otro recurso de FHIR, lo que asegura que los datos originales puedan ser verificados y que pueda conocerse si los datos que contiene el recurso de FHIR han sido alterados o modificados (el valor hash será totalmente distinto en tal caso).

De esta manera, una vez generado el recurso de FHIR y el valor hash asociado al identificador único del recurso de FHIR, la organización que crea los datos puede guardar el valor hash generado utilizando la red de blockchain de la Fundación UNID. El valor hash queda asociado en la red de blockchain con el identificador UUID del recurso de FHIR, de forma que un tercero podrá validar los datos originales siguiendo estos pasos:  

1. Generar el valor hash SHA-256 del recurso de FHIR que se quiere verificar, utilizando el servicio de ayuda de UHC u otras funciones que "canonicen" y "serialicen" el recurso de FHIR antes de generar el valor hash, para asegurar que se calcula siempre de la misma manera, de forma correcta y estandarizada.

2. Recuperar de la blockchain el hash original, utilizando el identificador universal UUID del recurso de FHIR.

3. Comparar el valor hash calculado con el valor hash almacenado en la blockchain.

4. En caso de que no coincidan, puede pedirse a la blockchain que recupere la historia del recurso de FHIR, para obtener los valores hash almacenados cada vez que se haya modificado el recurso de FHIR. De esta forma se puede comprobar si el valor hash calculado fue válido en algún estado anterior del recurso de FHIR (los datos recibidos están obsoletos) o si por el contrario los datos recibidos no han sido certificados en ningún momento en la red de blockchain.


Por tanto, cuando una aplicación recibe los datos del paciente, donante o cliente, tanto en el ámbito sanitario como en otros ámbitos, puede comprobar la huella digital de los datos para verificar la autenticidad de los mismos. Posteriormente, los datos FHIR pueden convertirse a un formato simplificado "hoja" (sheet) de UHC, a un formulario estandarizado JSON Schema Form y / o usar el código HTML correspondiente a estos datos, utilizando el servicio de ayuda de UHC u otras funciones.

La Fundación UNID está desarrollando, en colaboración con la empresa Conéctate Soluciones y Aplicaciones SL, una web de UHC para organizaciones y profesionales que permite realizar los procesos de una manera gráfica, de manera que cualquier profesional de una organización que colabore en el testeo de UHC con la fundación UNID, aunque no tenga conocimientos de programación y no sepa de terminología sanitaria, pueda ver cómo generar recursos de FHIR, generar la huella digital o *hash* de los datos, verificar la firma digital de los datos, etc. Esta web también puede ser utilizada para enviar datos médicos como la Historia Clínica de la persona en el formato internacional IPS (aprobado en Europa por el CEN) mediante conexiones encriptadas, directamente al móvil de la persona, de manera segura y evitando que las comunicaciones de los datos puedan ser interceptados por terceros malintencionados (hackers).
<p>&nbsp  </p>
  

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
<sub>*Esquema básico que muestra cómo un recurso de FHIR es introducido en una credencial verificable (VC) según el estándar de W3C*</sub>
<p>&nbsp  </p>

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
<sub>*Esquema básico que muestra cómo una "hoja" (sheet) de UHC es introducida en una credencial verificable (VC) según el estándar de W3C*</sub>
<p>&nbsp  </p>

La característica principal de las credenciales verificables es que pueden ser firmadas digitalmente en el formato estandarizado por W3C, generando un objeto "proof" en el formato Linked Data Proof (LD-Proof).

Los datos FHIR en una credencial verificable pueden ser firmados utilizando una credencial verificable o utilizando un recurso FHIR Provenance, que podría estar contenido dentro del recurso FHIR DiagnosticReport (utilizando el campo "contained" para ello) según las especificaciones de FHIR, o bien podría ser un recurso de FHIR adicional al recurso DiagnosticReport, tal y como está recogido en [United States Core Data for Interoperability (USCDI)](https://www.healthit.gov/isa/united-states-core-data-interoperability-uscdi). En este último caso, el campo "credentialSubject" de la credencial verificable contendría dos recursos de FHIR, uno con el informe de laboratorio (DiagnosticReport) y otro con la prueba de procedencia (Provenance).

El servicio de ayuda de UHC permitirá que puedan ser generadas y verificadas las firmas digitales tanto en el recurso FHIR Provenance como en el formato de Linked Data Proof definido por W3C.
<p>&nbsp  </p>  

## **Identificador Universal de Salud**

La Fundación UNID implementa en UHC la patente "[Protocolo Unificado de Identificación en Formación de Salud](https://patentscope.wipo.int/search/es/detail.jsf?docId=WO2020136289&tab=PCTBIBLIO)". De esta manera se consigue la identificación universal en la cadena de salud de pacientes, donantes, profesionales sanitarios, servicios de salud, organizaciones, productos biológicos y también de los procesos llevados a cabo en la atención sanitaria como encuentros médicos, resultados diagnósticos, procedimientos, intervenciones, prescripciones, etc.

En FHIR las referencias a Patient, Practitioner, Organization y a otros recursos como Immunization, DiagnosticReport, etc. se crean utilizando el nombre del recurso al que se refieren y añadiendo a continuación el identificador del recurso, separado con una barra diagonal, por ejemplo "Patient/identificador".

La Fundación UNID utiliza UUID v4 como identificador único que puede ser generado por cualquier organización para codificar recursos FHIR de forma universal, y que es compatible con International Patient Summary (IPS). De esta manera, la referencia en FHIR a un resultado de laboratorio sería "DiagnosticReport/uuid-v4" y la referencia de una vacunación sería "Immunization/uuid-v4".

Aplicando esto mismo a la identificación de personas, pacientes, profesionales, organizaciones y servicios de salud, la Fundación UNID proporciona un identificador universal a todas las partes relacionadas, de manera que pueda verificarse su autenticidad y su identidad.

Así, utilizando UUID v4 como base para la codificación de las identidades, compatible con FHIR, IPS y también con credenciales verificables (VC) y documentos DID, cada una de las partes que participan en la cadena de salud dispone de un Identificador Universal de Salud y de una identidad digital universal.

A modo de ejemplo, el Identificador Universal de la Fundación UNID se puede representar de las siguientes formas:

| Tipo                  | Descripción |
| ---                   | --- |
|*Paciente*                | *persona con un historial médico*|
|UNID URN               | urn:unid:patient:uuid:uuid-v4|
|UNID DID               | did:unid:patient:uuid:uuid-v4|
|UNID KEY ID (KID)      | did:unid:patient:uuid:uuid-v4#keyBase58|
|FHIR Reference         | Patient/uuid-v4|
|FHIR Identifier IETF   | urn:uuid:uuid-v4|
|IPS Full URN           | urn:uuid:uuid-v4|
|Compatible con Veres One    | did:v1:uuid:uuid-v4|

La Fundación UNID registra en la red de blockchain las identidades digitales junto con las claves criptográficas públicas asociadas a las mismas, que permiten la verificación de la firma digital de los datos y la encriptación de los mismos cuando se transmiten, utilizando conexiones seguras con encriptación de clave asimétrica.
<p>&nbsp  </p>

## **Identificador Universal de Productos de Origen Biológico**

Los productos de origen biológico como las vacunas o los hemoderivados son dispositivos médicos según las diferentes normativas y disponen de diferentes UDIs para cada legislación, por ejemplo en [Europa](https://ec.europa.eu/docsroom/documents/36664/attachments/1/translations/en/renditions/native), [EE.UU.](https://www.fda.gov/medical-devices/unique-device-identification-system-udi-system/udi-basics) y/o [Australia](https://www.mtaa.org.au/unique-device-identification-udi). Normalmente son implantados, inyectados o utilizados en un pacientes, tales como plasma en tratamientos estéticos ([PRP o plasma rico en plaquetas](https://es.wikipedia.org/wiki/Plasma_rico_en_plaquetas)), vacunas, concentrados de hematíes, medicamentos fabricados a partir de inmunoglobulinas y otro tipo de productos de origen biológico.

Los productos de origen biológico pueden estar codificados con diferentes sistemas tales como:

- [Health Industry Business Communications Council (HIBCC)](https://www.hibcc.org/)
- [International Council for Commonality in Blood Banking Automation (ICCBBA)](https://www.iccbba.org)
- [GS1](https://www.gs1.org/)

La tecnología de UHC permite verificar la trazabilidad de los productos biológicos a lo largo de toda la cadena de la salud y también por las personas y por otras organizaciones y profesionales ajenos a la salud, como en el caso de verificación de vacunación contra COVID-19.

A partir del código de barras de un producto de origen biológico, tanto los profesionales y servicios de salud como los pacientes que compran o reciben estos productos para ser utilizados en tratamientos médicos podrán obtener y verificar la información del producto, de manera unificada para productos de diferentes fabricantes, distintos sistemas de codificación y en diferentes normativas, mejorando la seguridad y la trazabilidad de estos productos y permitiendo a las personas conocer toda la información de los productos que les son suministrados o implantados.

A modo de ejemplo, el Identificador Universal de Productos Biológicos de la Fundación UNID se puede representar de las siguientes formas:

| Tipo                         	    | Descripción |
| ---				    | --- |
|*Dispositivos / productos médicos*   | *ejemplo: trazabilidad de una vacuna, hemoderivado, etc.*|
|FHIR Reference                     | Device/uuid-v4| 
|FHIR Identifier IETF               | urn:uuid:uuid-v4| 
|IPS Full URN                       | urn:uuid:uuid-v4| 
|UNID URN                           | urn:unid:device:uuid:uuid-v4| 
|UNID DID                           | did:unid:device:uuid:uuid-v4| 

UHC permite certificar y verificar la información de los productos biológicos fuera del ámbito de la salud, por ejemplo para verificar los datos de vacunación de COVID-19 en turismo, congresos, etc., de manera que puede verificarse en la red de blockchain de la Fundación UNID la autenticidad y la trazabilidad de una vacuna fabricada por la industria farmacéutica y administrada en un procedimiento de vacunación.

De esta manera, las organizaciones y profesionales sanitarios que crean datos de salud y de productos de origen biológico pueden registrar la huella digital de los mismos en la red de blockchain, de manera descentralizada, lo que permite que la autenticidad de los datos pueda ser verificada tanto por los pacientes que reciban estos datos como por otros profesionales y organizaciones con los que la persona comparta los datos posteriormente.
<p>&nbsp  </p>

## **Datos para investigación**

La Fundación UNID desarrolla smart-contracts en Hyperledger Fabric (chaincode) que utilizan las colecciones privadas (PDC) para anonimizar, deidentificar y generar datos para investigación.

De esta manera, cualquier organización podrá registrar datos para investigación de manera totalmente anónima y segura, enviando a la Fundación UNID los datos que quieren compartirse con la comunidad internacional.

A modo de ejemplo, el informe de laboratorio FHIR DiagnosticReport anteriomente mostrado es enviado al servicio de ayuda de UHC en este formato:

```json
{
	"region":"ESP",
	"fhirR4":"<FHIR DIAGNOSTIC REPORT>"
}
```

Este objeto de datos es anonimizado y deidentificado para generar un objeto UHC de tipo "research". Un ejemplo con el resultado del proceso se muestra a continuación:

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

Posteriormente, el objeto anonimizado y deidentificado se envía desde el servicio de salud a la Fundación UNID o a otra organización que haya sido aprobada por la Fundación como hub para recoger datos de investigación (por ejemplo, universidades).

Mediante un smart-contract privado en la blockchain de la Fundación UNID, se comprueba que los datos recibidos son válidos y se registra el objeto en el ledger público del canal mediante otro smart-contract, de manera que todos los *peer nodes* o servidores puedan consultar los datos que se hayan almacenado, de manera anónima, desde distintos hubs para realizar estadísticas o estudios de investigación, sin que pueda conocerse el servicio de salud origen de los datos en la blockchain.
<p>&nbsp  </p>

## **Sistemas Informáticos Hospitalarios (HIS) resilientes y atención sanitaria descentralizada**

Tras las crisis provocadas por el ataque de ransonware Wannacry en 2017 y por la pandemia de COVID-19 en 2020, la transformación digital en salud tiene que estar orientada a la descentralización de la atención sanitaria, para empoderar a los pacientes.

Hasta 2021, los sistemas hospitalarios se han basado en un modelo centralizado, en el que todas las terminales del personal sanitario se conectaban a un sistema central para poder leer y escribir datos en la historia clínica electrónica que tuviera esa persona en ese hospital. Además, las personas no tenían una forma sencilla de poder llevar la información de un sistema a otro y en cualquier idioma, por ejemplo en viajes de trabajo o de ocio. Por tanto, los profesionales sanitarios no podían tener una visión global de la persona, lo que provocaba una peor atención sanitaria y un mayor gasto sanitario (duplicación de pruebas diagnósticas, reingresos, etc.). Por otro lado, el profesional sanitario que atendía al paciente tampoco podía emitir un informe electrónico que fuera enviado de forma automática y segura al paciente. 

Utilizando FHIR, IPS, los identificadores UUID v4, el Identificador Universal de Salud y la identidad digital de la Fundación UNID, las personas se convierten en 2021 en el centro del ecosistema de la salud. Mediante UHC y el Identificador Universal de Salud, la persona puede unificar sus datos en el teléfono móvil, acudir a un servicio de salud habitual o a uno nuevo, mostrar su Identificador Universal de Salud y establecer una conexión encriptada con el profesional que le atiende para compartir datos de salud en los estándares internacionales.

Así mismo, utilizando el Identificador Universal de Salud, la identidad digital de la Fundación UNID, los identificadores UUID v4 y comunicación [DIDComm](https://github.com/decentralized-identity/didcomm-messaging), la aplicación del profesional sanitario puede:
1. Leer la información de la historia clínica que le envía la persona en formato FHIR / IPS.
2. Generar nuevos datos FHIR de forma descentralizada, identificando cada nuevo recurso de FHIR con un identificador UUID v4.
3. Firmar digitalmente los datos con las claves de firma accesibles de forma segura desde el dispositivo del profesional sanitario.
4. Enviar los nuevos datos médicos generados al paciente de forma segura, utilizando encriptación asimétrica para cifrar el mensaje.
5. Sincronizar los nuevos datos generados por la aplicación del profesional sanitario en el sistema hospitalario central y certificarlos en la red de blockchain, cuando se encuentren disponibles la conexión de red y el sistema hospitalario.
<p>&nbsp  </p>

## **FHIR: versatilidad y complejidad del estándar internacional**

FHIR es el estándar international para la atención sanitaria transfronteriza. Es un sistema muy versátil, pero su versatilidad se basa en complejas estructuras anidadas, lo que se traduce en mayor complejidad a la hora de realizar búsquedas, de convertir los datos desde o hacia otros formatos y de que pueda ser entendido y utilizado de una forma rápida y práctica por parte de cualquier aplicación y sistema informático.

UHC permite simplificar la adopción de FHIR y su utilización más allá del ámbito sanitario, por ejemplo para verificar resultados de laboratorio y vacunaciones de COVID-19 fuera del ámbito de la salud.

Como ejemplo, el código de la enfermedad objetivo de una vacunación (*targetDisease*) no está accesible directamente en el recurso FHIR Immunization, sino que los códigos están contenidos en una estructura anidada de varios niveles.

En este ejemplo, la enfermedad objetivo de la vacunación es COVID-19 y se codifica con dos sistemas diferentes: el código **U07.1** del sistema *ICD-10* y el código **840539006** del sistema *SNOMED*:

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
<sub>Ejemplo de recurso *FHIR Immunization* (vacunación) contra la enfermedad COVID-19 (enfermedad objetivo o *"targetDisease"*)</sub>
<p>&nbsp  </p>

UHC permite que este recurso de FHIR pueda ser creado y entendido de manera más sencilla por cualquier sistema informático mediante "hojas" (sheets) de UHC de esta manera:

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
<sub>Ejemplo de hoja de UHC ("sheet") correspondiente al recurso *FHIR Immunization* contra la enfermedad COVID-19</sub>
<p>&nbsp  </p>

Por otro lado, las referencias al paciente en el recurso *Immunization* pueden ampliarse de esta manera dentro según las especificaciones de FHIR:

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
<sub>Ejemplo del objeto de datos "patient" de un ciudadano español en un recurso FHIR Immunization</sub>
<p>&nbsp  </p>

De manera simplificada, el objeto "patient" anterior puede ser creado y convertido en la hoja ("sheet") *Immunization* de UHC de usando estos campos:

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
<sub>Campos correspondientes al identificador del paciente en una hoja ("sheet") UHC Immunization</sub>
<p>&nbsp  </p>


UHC permite simplificar y extender el uso de FHIR a cualquier sistema, tanto en el ámbito de la salud como fuera del ámbito de la salud, de manera que se puedan crear y entender las complejas estructuras anidadas de FHIR de una forma más simple y fácil de utilizar.
<p>&nbsp  </p>
