# Advanced Malware Intelligence & Defenses-AMID

Este proyecto forma parte de mi portafolio de ciberseguridad, en este escenario, se simula el aislamiento y análisis estático de un artefacto de compromiso (`payload_compromised.exe`) combinando Inteligencia de Amenazas y Threat Hunting Operativo.

## Estructura del Proyecto
*   **Malware_Analysis/**: Documentación y pautas del análisis estático del binario.
*   **Hunting_Rules/**: Reglas de detección proactiva (Regla YARA para memoria/disco y Regla Sigma para SIEM).
*   **Intel_Report/**: Reporte técnico formal en Markdown con la clasificación de Indicadores de Compromiso (IoCs).

## Tecnologías y Disciplinas Aplicadas
*   **Ingeniería Inversa (Análisis Estático)**: Extracción de strings, identificación de APIs críticas de Windows (`Advapi32.dll`) y firmas de Mutex.
*   **Threat Hunting**: Desarrollo de firmas YARA para escaneo de endpoints.
*   **Detección SIEM**: Diseño de reglas Sigma en formato YAML para la monitorización de logs de eventos de Windows (Event ID 4657).
