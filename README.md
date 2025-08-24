# Ciberseguridad y Criptografía


## 1. Ciberseguridad Básica / Fundamentos
<details>
<summary>Ver detalles</summary>

📌 Descripción: Introducción a los conceptos esenciales de ciberseguridad, amenazas y vulnerabilidades.

Introducción a la sección

¿Qué es la ciberseguridad?

Pilares de la Ciberseguridad

- Confidencialidad

- Integridad

- Disponibilidad

Amenaza, Ataque y Vulnerabilidad

Glosarios y términos básicos

</details>

## 2. Seguridad de Redes y Comunicaciones
<details>
<summary>Ver detalles</summary>

📌 Descripción: Protección de redes y comunicaciones, firewalls, VPNs y control de acceso.

Introducción a la sección

Seguridad de las comunicaciones

¿Qué es una red informática?

¿Qué es un protocolo de red?

Modelo OSI

Caso práctico: Sniffers, direcciones MAC/IP, puertos

Conceptos básicos: MAC, IP, puertos

Modelo IPS / TCP-IP

Captura de tráfico de red: pasiva y activa

Protocolo ARP / DHCP

Protocolos seguros

- SSL/TLS y ECDH

- Funcionamiento SSL/TLS

- Caso práctico: HTTP y HTTPS

- HSTS

Segmentación y control

- Segmentación de red, Subred y VLAN

- Microsegmentación

- CIDR y Máscara de red/subred

Infraestructura

- Introducción a AWS y despliegue de apps y bases de datos

- Firewalls, DMZ, Balanceadores de carga, WAF

- Anti-DoS / Anti-DDoS

- IDS/IPS, Security Onion

- Proxy, Tipos de Proxy, SquidProxy

- VPN, Protocolos (IPSec, PPTP, OpenVPN)

</details>

## 3. SOC y Operaciones de Seguridad
<details>
<summary>Ver detalles</summary>

📌 Descripción: Operación de seguridad, monitorización, SIEM, respuesta a incidentes y Threat Hunting.

Introducción a la sección

Qué es un SOC

Capacidades/Servicios de un SOC

SIEM Intelligence & Alerting

Caso práctico: Splunk

Indicadores de compromiso (IoC) y MISP

Monitorización & Triage

Ticketing y gestión de incidentes - TheHive

Integración Splunk + TheHive + Cortex

Respuesta a incidentes

NIST SP 800-61

Uso de SOAR

Threat Hunting

Sandboxing - Cuckoo Sandbox

Gestión de vulnerabilidades - Nessus

Lectura: CVE, CVSS, CPE

- Honeypot

</details>

## 4. Endpoint Security / Hardening de Sistemas
<details>
<summary>Ver detalles</summary>

📌 Descripción: Protección de sistemas finales, hardening y monitorización.

Introducción a la sección

Ciberseguridad de sistemas operativos

Hardening del SO (CIS Benchmark)

Evaluación automática de Hardening

Antivirus (AV)

EDR y XDR

HIDS/HIPS

Monitorización del endpoint (beats, osquery, syslog)

Control de ejecución de aplicaciones (Applocker)

</details>

## 5. Firma Digital y PKI
<details>
<summary>Ver detalles</summary>

📌 Descripción: Firma digital, certificados y gestión de clave pública.

Introducción a la sección

Firma digital

Firma digital con recuperación de mensaje

Confidencialidad y firma digital

Firma digital con cifrado

Caso práctico: Firma digital con OpenSSL

Public Key Infrastructure (PKI)

Certificado de clave pública

Caso práctico: Creación de certificado con OpenSSL

Autoridad de Certificación (CA)

Certificado digital vs certificado de clave pública

Modelo de gestión de certificados

Modelo conectado y web

</details>

## 6. Gestión de Identidades, Riesgos y Amenazas
<details>
<summary>Ver detalles</summary>

📌 Descripción: Control de acceso, IAM, autenticación y gestión de riesgos.

Introducción a la sección

Gestión de Identidades y control de acceso (IAM)

IAM vs Active Directory

Caso práctico: IAM en AWS

Autenticación y Autorización: SAML, OAUTH, 2FA

Gestión y análisis de riesgos de ciberseguridad

Modelos de gestión y análisis de riesgos

Modelado de amenazas: MITRE ATT&CK, STRIDE

</details>

## 7. Criptografía Básica
<details> <summary>Ver detalles</summary>

📌 Descripción: Conceptos iniciales de criptografía y cifrados históricos.

Introducción a la sección

¿Qué es la criptografía?

- Lectura: Términos relevantes y componentes de un criptosistema

Asunciones de seguridad

Cifrados históricos y clásicos

- Cifrado César

- Cifrado César en la práctica

- Clasificación de los criptosistemas

Ataques a criptosistemas

- Ataques a un criptosistema

- Romper/Hackear un criptosistema

- Fuerza Bruta y otras técnicas de ataque

- Caso práctico: Rompiendo el cifrado César

- Resolución del caso práctico

Sustitución y análisis

- Cifrado simple por sustitución

- Espacio de claves del cifrado simple por sustitución

- Ataques estadísticos: Análisis de frecuencias

- Caso práctico: Rompiendo el cifrado simple por sustitución

- Resolución del caso práctico

Comparaciones

- Codificación vs Criptografía

- Esteganografía vs Criptografía

Otros cifrados

- Cifrado Playfair

- Caso práctico: Rompiendo el cifrado Playfair

- Cifrado Vigenere

- Seguridad del cifrado Vigenere

- Rompiendo el cifrado Vigenere

Seguridad absoluta

- Perfect Secrecy

- One-time pads

¿Cuándo utilizar One-time pads?

</details>

## 8. Criptografía Moderna
<details>
<summary>Ver detalles</summary>

📌 Descripción: Criptografía avanzada y sistemas actuales de cifrado simétrico y asimétrico.

Introducción a la sección

Criptosistemas simétricos modernos

- Stream Ciphers

- Propiedades de los Stream Ciphers

- Stream Ciphers populares

- RC4

- RC4 en la práctica

- ChaCha20

- Funcionamiento de ChaCha20

Block Ciphers

- Propiedades de los Block Ciphers

- Block Ciphers populares

- DES (Data Encryption Standard)

- Triple DES

- AES

- Modos de operación: ECB, CBC, CFB, OFB, CTR

Criptosistemas asimétricos (clave pública)

- Diffie-Hellman: Intercambio de claves

- RSA

Caso práctico: Generando un par de claves RSA con OpenSSL

Lectura: Curvas elípticas (Opcional)

Lectura: Computación cuántica (Opcional)

</details>

## 9. Seguridad de los Datos
<details>
<summary>Ver detalles</summary>

📌 Descripción: Protección, integridad y disponibilidad de la información, incluyendo funciones hash y backups.

Introducción a la sección

Seguridad de los datos

Cyber Security Framework (CSF)

Integridad de los datos

Funciones Hash

- Funciones Hash

- Aplicaciones de las funciones Hash

- Funciones Hash modernas

- Hashing de contraseñas en BBDD

Lectura: Ataques a funciones Hash (Rainbow tables)

Verificación de datos

- Checksums

- Checksums en la práctica

- Error Correcting Codes (ECC)

Autenticación de mensajes

- Message Authentication Code (MAC)

- CBC-MAC

Confidencialidad e integridad

- Confidencialidad

- integridad

- autenticación

Lectura: Modo de operación GCM

Protección de los datos

- Clasificación de la información: GDPR, PCI-DSS, HIPAA

Lectura: ISO 27001 y 27002

- Data Loss Prevention (DLP)

- Caso práctico: DLP Profesional/Empresarial

- Information Rights Management (IRM)

- Caso práctico: IRM Profesional/Empresarial

- Full Disk Encryption

- Caso práctico: Full Disk Encryption con Bitlocker

- Tokenización

Disponibilidad y resiliencia

Disponibilidad y Ciberresiliencia

Backups: Tipos y consideraciones

Caso práctico: Backup Profesional/Empresarial

Inventariado de activos: CMDB

Almacenamiento de claves: TPM y HSM

</details>
