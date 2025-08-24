# Pilares de la Ciberseguridad

## 1. Triada CIA (Confidencialidad, Integridad, Disponibilidad)

La Tríada CIA es un modelo fundamental en seguridad de la información que representa tres principios básicos:


### Confidencialidad

Definición: Proteger los datos del acceso no autorizado.

Objetivo: Asegurar que solo usuarios autorizados puedan acceder a la información.

Ejemplos de protección:

- Evitar el robo de contraseñas.

- Cifrado de bases de datos y comunicaciones.

- Control de acceso y autenticación multifactor (MFA).

Riesgos o ataques comunes:

- Filtración de datos (data breach).

- Phishing para robar credenciales.

- Ataques Man in the Middle (MITM).

- Robo de dispositivos o errores humanos.


### Integridad

Definición: Garantizar que los datos se mantengan precisos y fiables.

Objetivo: Evitar modificaciones no autorizadas de los datos.

Ejemplos de protección:

- Hashing de archivos para detectar cambios.

- Firmas digitales y certificados.

- Sumas de comprobación (checksums).

Riesgos o ataques comunes:

- Manipulación de registros financieros.

- Desfiguración de sitios web.

- Malware que modifica archivos sin autorización.

- Ataques de tipo supply chain (ej. SolarWinds).


### Disponibilidad

Definición: Garantizar que los sistemas, redes y datos sean accesibles cuando se necesiten.

Objetivo: Mantener el acceso continuo de los usuarios autorizados.

Ejemplos de protección:

- Redundancia de sistemas y servidores.

- Copias de seguridad periódicas.

- Planes de recuperación ante desastres (DRP).

Riesgos o ataques comunes:

- Ataques de Denegación de Servicio (DDoS).

- Ransomware que bloquea el acceso a archivos.

- Fallas técnicas o desastres naturales.

- Ejemplo real: ataque al Oleoducto Colonial.


### Conclusión de la Tríada CIA

La Tríada CIA proporciona un marco integral para proteger la información:

- Confidencialidad: mantener los secretos a salvo.

- Integridad: asegurar que los datos sean confiables.

- Disponibilidad: garantizar que los sistemas y datos estén accesibles.

---

## 2. Principios Extendidos de Seguridad

Además de la Tríada CIA, existen otros conceptos que fortalecen la seguridad:


### Autenticación

Definición: Verificar la identidad de un usuario, dispositivo o aplicación.

Ejemplos:

- Contraseña + nombre de usuario.

- Biometría: huella dactilar, reconocimiento facial.

- Tokens de seguridad, tarjetas inteligentes.

Importancia: Impide accesos no autorizados y permite la trazabilidad de usuarios. 


### Autorización

Definición: Determinar qué recursos y acciones puede realizar un usuario autenticado.

Ejemplo:

- Solo el personal de finanzas puede acceder a registros contables, aunque todos estén autenticados.

Formas comunes:

- Listas de control de acceso (ACL).

- Roles y políticas (RBAC, ABAC).

Importancia: Limita privilegios innecesarios y previene accesos indebidos.


### No Repudio

Definición: Garantiza que el emisor o receptor de una acción no pueda negar su participación.

Ejemplos de técnicas:

- Firmas digitales.

- Certificados digitales emitidos por autoridades confiables.

- Logs y registros auditables.

Ejemplo práctico:

- En una transacción bancaria, el cliente no puede negar haber autorizado la transferencia y el banco no puede negar haberla procesado.


### Conclusión de Principios Extendidos

La combinación de la Tríada CIA con la autenticación, autorización y no repudio proporciona un marco más completo para proteger la información y los sistemas en entornos digitales modernos.

- CIA: protege los datos de manera integral.

- Autenticación + Autorización: aseguran que solo quienes deben acceder, puedan hacerlo y solo a lo permitido.

- No Repudio: garantiza responsabilidad y trazabilidad de las acciones.