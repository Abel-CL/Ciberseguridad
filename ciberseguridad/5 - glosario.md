# 🌐 Glosario Extendido de Ciberseguridad (INCIBE)

---

## 🔹 Índice
1. [Fundamentos de seguridad](#fundamentos-de-seguridad)  
2. [Amenazas y ataques](#amenazas-y-ataques)  
3. [Malware](#malware)  
4. [Protección y monitoreo](#protección-y-monitoreo)  
5. [Identidad y acceso](#identidad-y-acceso)  
6. [Criptografía](#criptografía)  
7. [Web, redes y nube](#web-redes-y-nube)  
8. [Gestión, normas y respuesta](#gestión-normas-y-respuesta)  
9. [Seguridad móvil e IoT](#seguridad-móvil-e-iot)  
10. [Privacidad y normativa](#privacidad-y-normativa)  
11. [Herramientas y metodologías](#herramientas-y-metodologías)  

---

## 🔒 Fundamentos de seguridad
- **Activo**: recurso con valor (datos, sistemas, personas)  
- **Amenaza**: evento o actor que puede causar daño  
- **Vulnerabilidad**: debilidad que puede ser explotada  
- **Riesgo**: probabilidad × impacto de una amenaza sobre un activo  
- **Impacto**: consecuencia o daño que puede generar un incidente  
- **Confidencialidad**: proteger la información solo para usuarios autorizados  
- **Integridad**: asegurar que la información no sea alterada  
- **Disponibilidad**: garantizar acceso a sistemas y datos cuando se necesiten  
- **Incidente de seguridad**: evento que compromete confidencialidad, integridad o disponibilidad  
- **Brecha de seguridad**: exposición de datos no autorizada  

---

## ⚔️ Amenazas y ataques
- **Ataque**: acción para explotar vulnerabilidades y dañar activos  
- **Vector de ataque**: camino/técnica usada en un ataque  
- **Superficie de ataque**: todos los puntos posibles de entrada para un atacante  
- **APT (Advanced Persistent Threat)**: ataque avanzado, dirigido y prolongado  
- **0-day**: vulnerabilidad desconocida para el fabricante  
- **Exploit**: código o método que aprovecha una vulnerabilidad  

### 🧠 Ingeniería social
- **Phishing**: engaño para robar credenciales o dinero  
- **Spear phishing**: phishing dirigido a una persona o empresa específica  
- **Smishing**: phishing vía SMS/mensajería  
- **Vishing**: phishing por llamada de voz  
- **BEC (Business Email Compromise)**: fraude mediante correo corporativo  
- **Spoofing**: suplantación de identidad (correo, IP, teléfono)  

---

## 🐛 Malware
- **Malware**: software malicioso  
- **Virus**: se adjunta a archivos y se propaga al ejecutarse  
- **Gusano (Worm)**: se propaga automáticamente por la red  
- **Troyano**: se hace pasar por software legítimo  
- **Ransomware**: cifra datos y pide rescate  
- **Spyware**: recopila información sin consentimiento  
- **Adware**: muestra publicidad no deseada  
- **Rootkit**: oculta presencia de malware en el sistema  
- **Botnet**: red de equipos comprometidos controlados por un atacante  

---

## 🛡️ Protección y monitoreo
- **Firewall**: filtra tráfico de red según reglas  
- **IDS / IPS**: detección y prevención de intrusiones  
- **EDR / XDR**: detección y respuesta avanzada en endpoints / extendida  
- **SIEM**: centraliza y analiza logs para alertas  
- **DLP (Data Loss Prevention)**: evita fugas de información sensible  
- **Sandbox**: ejecución aislada para analizar archivos  
- **Honeypot**: señuelo para estudiar ataques  

---

## 👤 Identidad y acceso
- **Autenticación**: verificar quién eres  
- **Autorización**: permisos sobre qué puedes hacer  
- **MFA / 2FA**: múltiples factores de verificación  
- **IAM (Identity and Access Management)**: gestión de identidades y accesos  
- **RBAC (Role-Based Access Control)**: permisos basados en roles  
- **Principio de mínimo privilegio**: dar solo los accesos necesarios  
- **Segregación de funciones**: separar tareas críticas para evitar abusos  

---

## 🔑 Criptografía
- **Cifrado simétrico**: misma clave para cifrar y descifrar (AES)  
- **Cifrado asimétrico**: par de claves pública/privada (RSA, ECC)  
- **Hash**: huella única de datos (irreversible)  
- **Sal / Nonce**: valores aleatorios que fortalecen hashes/cifrados  
- **Firma digital**: garantiza integridad y no repudio  
- **PKI (Public Key Infrastructure)**: sistema de gestión de claves y certificados  
- **Certificado digital**: vincula clave pública con identidad  
- **TLS / HTTPS**: cifrado de comunicaciones en tránsito  
- **VPN**: túnel cifrado para proteger datos  

---

## 🌐 Web, redes y nube
- **WAF (Web Application Firewall)**: firewall de aplicaciones web  
- **XSS / CSRF / SQLi / SSRF**: vulnerabilidades web comunes  
- **DNS / DNSSEC**: resolución de nombres / validación de autenticidad  
- **NAT / Proxy / CDN**: traducción de direcciones / intermediario / distribución de contenido  
- **IaaS / PaaS / SaaS**: modelos de servicio en la nube  
- **Responsabilidad compartida**: reparto de seguridad entre proveedor y cliente  

---

## 📊 Gestión, normas y respuesta
- **CVE / CVSS / CWE**: vulnerabilidad / severidad / debilidades comunes  
- **Hardening**: asegurar un sistema con configuraciones seguras  
- **Baseline**: configuración estándar segura  
- **BIA / BCP / DRP**: análisis de impacto / continuidad / recuperación  
- **Copia 3-2-1**: 3 copias, 2 medios, 1 fuera de sitio  
- **IOC / IOA / TTP**: indicadores de compromiso / tácticas, técnicas y procedimientos  
- **MITRE ATT&CK**: marco de técnicas de adversarios  
- **Playbook / Runbook**: guías paso a paso para responder a incidentes  

---

## 📱 Seguridad móvil e IoT
- **Jailbreak / Rooting**: desbloqueo de dispositivos móviles  
- **Botnets IoT**: red de dispositivos IoT comprometidos  
- **Seguridad de firmware**: proteger el software básico de dispositivos  

---

## 🕵️ Privacidad y normativa
- **GDPR / LOPD / CCPA**: leyes de protección de datos  
- **Pseudonimización / anonimización**: técnicas para proteger identidad  
- **Consentimiento informado**: autorización explícita para usar datos  

---

## 🛠️ Herramientas y metodologías
- **Pentesting / Penetration Testing**: pruebas de seguridad simulando ataques  
- **Red Team / Blue Team / Purple Team**: ofensivo / defensivo / combinación  
- **Threat Intelligence**: información sobre amenazas actuales  
- **DevSecOps**: integración de seguridad en desarrollo y operaciones  
- **SDLC seguro**: ciclo de vida seguro del software  
- **OWASP Top 10**: lista de vulnerabilidades web críticas
