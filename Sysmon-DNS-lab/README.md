# 🛡️ Sysmon DNS Threat Hunting Lab

Este proyecto demuestra la implementación de **Microsoft Sysmon** para el monitoreo avanzado de consultas DNS en entornos Windows, permitiendo la visibilidad de conexiones de red a nivel de proceso.

## 🚀 Contenido del Repositorio
- `dns-monitor-config.xml`: Configuración optimizada para capturar el Evento ID 22 (DNS), filtrando tráfico legítimo de navegadores y Steam.
- `Get-DnsAlerts.ps1`: Script de automatización en PowerShell para extraer alertas DNS en tiempo real.

## 📊 Evidencia de Funcionamiento
![Evidencia de Sysmon](./img/evidencia-sysmon.png)
*Captura: Monitoreo activo de procesos realizando consultas DNS (Evento 22).*

## 🧠 Conocimientos Aplicados
- Análisis de logs de seguridad (Windows Event Viewer).
- Configuración de filtros XML para SIEM/Sysmon.
- Diferenciación entre tráfico legítimo (CDNs de Qwilted/Steam) y posibles indicadores de compromiso.