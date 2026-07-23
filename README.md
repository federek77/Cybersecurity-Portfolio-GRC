# Portfolio Profesional: Gestión de Vulnerabilidades y Cumplimiento Técnico (GRC)

Bienvenido a mi espacio de laboratorios prácticos y auditorías de infraestructura. Soy Federico Fijtman, Técnico Superior en Programación y Analista de Ciberseguridad certificado. Este repositorio reúne la documentación formal, reportes ejecutivos y matrices de riesgo derivadas de mis simulaciones en entornos controlados, orientados estrictamente al rol de **Analista de Vulnerabilidades / GRC**.

---

## 🛠️ Tecnologías y Entornos Utilizados

* **Motor de Auditoría:** Tenable Nessus Essentials v10.x (Firmas de amenazas y plugins actualizados).
* **Virtualización:** Oracle VirtualBox (Gestión de arquitecturas de red aisladas y entornos segmentados).
* **Sistemas Operativos:** Microsoft Windows 11 Enterprise (Anfitrión) y Linux Ubuntu/Debian (Sistemas objetivos).
* **Marcos de Trabajo y Estándares:** Mitre ATT&CK, Common Vulnerability Scoring System (CVSS), OWASP Top 10 y bases de datos globales CVE.

---

## 📂 Laboratorios y Reportes Disponibles

### 🔹 1. Hardening e Inventario de Activos (Windows 11)
* **Archivo:** `Informe_Vulnerabilidades_Windows_FedericoFijtman.pdf`
* **Metodología:** Escaneo perimetral interno de tipo *Basic Network Scan* sin credenciales sobre la IP anfitriona `192.168.100.148` para mapear la superficie de exposición inicial.
* **Resultado del Triage:** Diagnóstico de riesgo mínimo con un 100% de hallazgos en categoría informativa (INFO). Verificación y documentación de los protocolos críticos de compartición de archivos y llamadas remotas locales corporativas (SMB en Puerto 445, HTTPS y servicios protegidos por capas TLS/SSL).

### 🔹 2. Análisis de Riesgos Críticos y Remediación (Metasploitable 2)
* **Archivo:** `Informe_Analis_Riesgos_Metasploitable2_FedericoFijtman.pdf`
* **Metodología:** Configuración de arquitectura de red aislada mediante el segmento *Host-Only* (`192.168.56.0/24`), garantizando un entorno controlado y seguro para mitigar riesgos de exposición en la red local física. Auditoría profunda sobre un servidor Linux vulnerable a propósito (`192.168.56.101`).
* **Resultado del Triage:** Identificación de un vector masivo de exposición perimetral. Documentación y desarrollo de planes de mitigación estratégica para vulnerabilidades de impacto máximo (CVSS 10.0), incluyendo la credencial por defecto en el servicio virtual remoto (VNC Server 'password') y la detección de puertas traseras activas en servicios de comunicación (*Bind Shell* y *UnrealRCD Backdoors*).

### 🔹 3. Verificación de Evidencias y Explotación Manual (vsftpd 2.3.4)
* **Archivo:** `Informe_Explotacion_Manual_vsftpd_FedericoFijtman.pdf`
* **Metodología:** Análisis activo de la superficie de ataque perimetral mediante la utilidad **Netcat** y herramientas de enumeración sobre el segmento aislado. Simulación manual del disparador (*trigger*) de inyección en el servicio de transferencia de archivos (Puerto 21) para forzar la apertura del canal secundario de administración.
* **Resultado de la Prueba de Concepto (PoC):** Conexión exitosa y toma de control directa sobre el puerto oculto `6200`. Verificación de compromiso perimetral absoluto al obtener una consola remota interactiva con máximos privilegios de sistema (`root`), documentando la remediación técnica y el análisis de riesgo asociado a la vulnerabilidad global **CVE-2011-2523**.

### 🔹 4. Auditoría de Exposición Automatizada y Conexión Reversa (Metasploit)
* **Archivo:** `Informe_Explotacion_Automatizada_Metasploit_FedericoFijtman.pdf`
* **Metodología:** Inicialización y verificación del motor PostgreSQL nativo e indexación global del vector CVE-2011-2523 en **Metasploit Framework (MSFv6)**. Despliegue de una carga útil (*payload*) avanzada de conexión reversa (*Reverse Shell*) con **Meterpreter** para analizar la evasión de políticas y el comportamiento de los controles perimetrales.
* **Resultado del Triage:** Obtención exitosa de una sesión interactiva permanente y persistente directamente en la memoria RAM del servidor objetivo (`192.168.56.101`), validando el compromiso absoluto del activo con privilegios máximos de administrador (`root`) y evaluando el impacto operativo de la falta de segmentación interna.

### 🔹 5. Auditoría de Inyección Comandos y Restricción de Código Fuente (OWASP Top 10)
* **Archivo:** `Informe_Inyeccion_Comandos_OWASP_FedericoFijtman.pdf`
* **Metodología:** Análisis activo sobre el backend de una aplicación web corporativa (DVWA) bajo el estándar internacional **OWASP Top 10 (A03:2021-Injection)**. Inspección de código fuente PHP para diagnosticar la ejecución insegura de la función nativa `shell_exec()` acoplada por concatenación directa a variables de entrada de usuario sin controles de sanitización ni validación (*input validation*).
* **Resultado del Triage:** Explotación exitosa de la lógica defectuosa del formulario web mediante vectores con operadores separadores de instrucciones. Extracción del inventario completo de cuentas del sistema operativo (`/etc/passwd`) y despliegue de una carga útil para forzar una consola remota interactiva (*Reverse Shell*) vía Netcat bajo los privilegios del usuario de servicios web `www-data`.

---

## 🎯 Objetivo Profesional

Mi meta a corto plazo (3 a 6 meses) es proyectar mi carrera en el mercado IT como **Analista de Vulnerabilidades Junior / GRC** en esquemas de horarios de oficina tradicionales, aportando mi madurez analítica, responsabilidad corporativa y rigurosidad de procesos como activos de estabilidad. A largo plazo, proyecto mi desarrollo técnico hacia el campo del *Pentesting* y la seguridad ofensiva.

---
*Este repositorio se actualiza de forma manual y periódica a medida que se completen nuevos ciclos de auditoría e infraestructura en el laboratorio.*
