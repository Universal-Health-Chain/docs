![](https://avatars.githubusercontent.com/u/57396025?s=200&v=4)
# **Universal Health Chain - versión 2.0** </br> *Cadena Universal de Salud*


Copyright © FUNDACION UNID.

Copyright © CONECTATE SOLUCIONES Y APLICACIONES SL.

Copyright © CONNECTING SOLUTION & APPLICATIONS LTD.

Reservados todos los derechos.

<p>&nbsp</p>

## **Resumen**

UHC es una **plataforma de comunicación descentralizada para el intercambio seguro de datos**.

UHC v2 utiliza la tecnología blockchain (cadena de bloques) *Hyperledger Fabric*, los estándares *OpenID*, el *Perfil de seguridad de grado financiero (FAPI)* y algoritmos de *Computación Post-Quántica (PQC)* para comunicaciones de datos seguras.

UHC es un sistema resistente diseñado para comunicar de forma segura a pacientes y personas autorizadas (tutores legales, cuidadores, etc.) con los servicios de salud y viceversa. Permite compartir documentos verificables e identidades digitales verificables a los servicios de salud, profesionales de la salud, pagadores, pacientes y personas autorizadas, utilizando Universal Health Identifiers (tecnología patentada) y HL7 FHIR como estándar internacional para el intercambio de datos ([USA](https://www.healthit.gov/isa/united-states-core-data-interoperability-uscdi), [EU](https://international-patient-summary.net/cen-and-iso-have-aligned-their-work/), [G7](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/1045267/G7-open-standards-final-report.pdf), [India](https://www.nrces.in/standards/hl7-international/hl7-fhir), [Argentina](https://www.argentina.gob.ar/salud/digital/estandares), etc.), convertiendo datos de otros formatos a FHIR y viceversa. También facilita estudios de investigación para obtener historias clínicas anonimizadas para investigación y estadística (gemelos digitales).

<p>&nbsp</p>

### **Cadena de bloques**

La tecnología blockchain es una herramienta utilizada en UHC para proporcionar una cadena de verdad, trazabilidad y para evitar accesos no autorizados o modificaciones tanto de identidades digitales, permisos y documentos generados.

La red blockchain de UNID se basa en Hyperledger Fabric: plataforma de registro distribuida, de código abierto, basada en permisos y de nivel corporativo, desarrollada por The Linux Foundation.

Tiene controles de privacidad avanzados y ha sido diseñado para la atención médica y la investigación (proveedores de atención médica, laboratorios, autoridades sanitarias, profesionales de la salud, investigadores) sin criptomonedas, donde todas las identidades de los miembros son conocidas y autenticadas, y donde los pacientes y profesionales pueden validar la autenticidad tanto de las identidades digitales de los diferentes actores de la cadena de salud como de los documentos generados en la atención médica, utilizando Identificadores Universales de Salud (tecnología patentada).

<p>&nbsp</p>

### **OpenID**

OpenID Connect (OIDC) es una capa de identidad que extiende el protocolo OAuth 2.0. Permite que los usuarios sean autenticados por sitios cooperantes (conocidos como partes de confianza o RP) utilizando un servicio de proveedor de identidad (IdP) de terceros.

<p>&nbsp</p>

### **API de grado financiero (FAPI)**

La API de grado financiero (FAPI) es una especificación liderada por la industria y desarrollada por OpenID Foundation. El perfil de seguridad FAPI 2.0 es una capa de seguridad de API basada en el marco de autorización de OAuth 2.0 (RFC6749) y en especificaciones adaptadas para proteger las API en escenarios de alto valor.

Si bien el perfil de seguridad FAPI 2.0 se desarrolló inicialmente con un enfoque en las aplicaciones financieras, está diseñado para ser aplicable de manera universal para proteger las API que exponen datos confidenciales y de alto valor (personales y de otro tipo), por ejemplo, en aplicaciones de salud digital y administración electrónica.

<p>&nbsp</p>

### **Criptografía poscuántica (PQC)**

Dentro de unos pocos años, las computadoras cuánticas romperán los algoritmos de criptográficos RSA (Rivest-Shamir-Adleman) y ECC (criptografía de curva elíptica) de los que dependen los sistemas digitales en la actualidad.

El objetivo de la criptografía post-cuántica (también llamada criptografía resistente a la computación cuántica) es desarrollar sistemas criptográficos que sean seguros frente a las computadoras cuánticas y a las clásicas, y que puedan interoperar con los protocolos y redes de comunicaciones existentes.

<p>&nbsp</p>

## **Servicios**

<Pendiente: describir los servicios>

- Servicio Local de Gestión de Identidades
- Servicio Local de Conexiones
- Servicio Local de Mensajería
- Servicio Local de Conversión de Datos
- Servicios de Sincronización de Datos
- Servicio de Directorio de UNID
- Servicio de Proxy de UNID