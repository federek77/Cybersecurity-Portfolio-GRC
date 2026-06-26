# Portfolio Profesional: Gestión de Vulnerabilidades y Cumplimiento Técnico (GRC)

Bienvenido a mi espacio de laboratorios prácticos y auditorías de infraestructura. Soy Federico Fijtman, Técnico Superior en Programación y Analista de Ciberseguridad certificado. Este repositorio reúne la documentación formal, reportes ejecutivos y matrices de riesgo derivados de mis simulaciones en entornos controlados, orientados estrictamente al rol de **Analista de Vulnerabilidades / GRC**.

---

## 🛠️ Tecnologías y Entornos Utilizados
* **Motor de Auditoría:** Tenable Nessus Essentials v10.x (Firmas de amenazas y plugins actualizados).
* **Virtualización:** Oracle VirtualBox (Gestión de arquitecturas de red aisladas y entornos segmentados).
* **Sistemas Operativos:** Microsoft Windows 11 Enterprise (Anfitrión) y Linux Ubuntu/Debian (Sistemas objetivos).
* **Marcos de Trabajo y Estándares:** Mitre ATT&CK, Common Vulnerability Scoring System (CVSS) y base de datos global CVE.

---

## 📂 Laboratorios y Reportes Disponibles

### 🔹 1. Hardening e Inventario de Activos (Windows 11)
* **Archivo:** `Informe_Vulnerabilidades_Windows_FedericoFijtman.pdf`
* **Metodología:** Escaneo perimetral interno de tipo *Basic Network Scan* sin credenciales sobre la IP anfitriona `192.168.100.148` para mapear la superficie de exposición inicial.
* **Resultado del Triage:** Diagnóstico de riesgo mínimo con un 100% de hallazgos en categoría informativa (INFO). Verificación y documentación de los protocolos críticos de compartición de archivos y llamadas remotas locales corporativas (SMB en Puerto 445, HTTP y capas TLS/SSL).

### 🔹 2. Análisis de Riesgos Críticos y Remediación (Metasploitable 2)
* **Archivo:** `Informe_Analisis_Riesgos_Metasploitable2_FedericoFijtman.pdf`
* **Metodología:** Configuración de arquitectura de red aislada en modo *Adaptador Solo-Anfitrión* (`192.168.56.0/24`) para evadir el aislamiento perimetral de routers hogareños. Auditoría profunda sobre un servidor Linux vulnerable a propósito (`192.168.56.101`).
* **Resultado del Triage:** Identificación de un vector masivo de exposición perimetral. Documentación y desarrollo de planes de mitigación estratégica para vulnerabilidades de impacto máximo (CVSS 10.0), incluyendo la credencial por defecto en el servidor visual remoto (VNC Server 'password') y la detección de puertas traseras activas en servicios de comunicación (Bind Shell y UnrealIRCd Backdoors).

### 🔹 3. Verificación de Evidencias y Explotación Manual (vsftpd 2.3.4)
* **Archivo:** `Informe_Explotacion_Manual_vsftpd_FedericoFijtman.pdf`
* **Metodología:** Análisis activo perimetral mediante el framework avanzado *Netcat* sobre el segmento aislado solo-anfitrión. Simulación manual del trigger de inyección en el servicio de transferencia de archivos (Puerto 21) para forzar la apertura del canal secundario de administración.
* **Resultado de la Prueba de Concepto (PoC):** Conexión exitosa y toma de control directa sobre el puerto oculto `6200`. Verificación de compromiso perimetral absoluto al obtener una consola remota interactiva con identificador de privilegios de Administrador Supremo del sistema operativo (`uid=0(root)`), documentando la remediación de la vulnerabilidad crítica global CVE-2011-2523.

---

## 🎯 Objetivo Profesional
Mi meta a corto plazo (3 a 6 meses) es insertarme en el mercado IT como Analista de Vulnerabilidades Junior / GRC en esquemas de horarios de oficina tradicionales, aportando mi madurez analítica, responsabilidad corporativa y rigurosidad de procesos como activos de estabilidad. A largo plazo, proyecto mi desarrollo técnico hacia el campo del Pentesting y la seguridad ofensiva.

---
*Este repositorio se actualiza de forma manual y periódica a medida que se completan nuevos ciclos de auditoría e infraestructura en el laboratorio.*
