# Reporte Técnico de Inteligencia de Amenazas: AMID 
**Analista:** J
**Estado:** Fase Inicial - Análisis Estático Completado
A través del análisis estático del binario `payload_compromised.exe`, se aislaron los siguientes artefactos:
* **Dominio C2 (Red):** `http://malicious-c2-overlord.botnet`
* **Persistencia (Registro):** `HKCU\Software\Microsoft\Windows\CurrentVersion\Run\OverlordKey`
* **Mutex en Memoria:** `Global\AMID_Overlord_Mutex_v1.0`
* **API de Cifrado de Windows:** `Advapi32.dll` (`CryptEncrypt` / `CryptDecrypt`)
* **Extensiones Objetivo:** `.docx`, `.xlsx`, `.pdf`, `.jpg`El artefacto busca asegurar persistencia en el sistema operativo mediante el registro de Windows, evita la ejecución redundante utilizando un Mutex específico y cifra archivos críticos del usuario utilizando librerías nativas del sistema, para posteriormente reportar al servidor de Comando y Control (C2).
