Sysmon DNS Threat Hunting Project
Objetivo
Implementar un sistema de monitoreo de resolución de nombres (DNS) para detectar posibles balizas de malware (beacons) o exfiltración de datos en entornos Windows utilizando Microsoft Sysmon.

Implementación
    1. Configuración: Diseñé un archivo XML personalizado para filtrar el tráfico legítimo (CDN de Steam, navegadores, Windows Update) y resaltar consultas originadas por procesos sospechosos como PowerShell o ejecutables en rutas temporales.

    2. Análisis de Eventos: Utilicé el Evento ID 22 para trazar la relación entre un proceso (Image) y el dominio consultado (QueryName).

Hallazgo de Ejemplo (Caso Real)
    "Durante las pruebas, identifiqué que el proceso steam.exe generaba múltiples consultas a dominios de CDNs como qwilted-cds.cqloud.com. Gracias a Sysmon, pude verificar que el binario era legítimo y la conexión era esperada para la descarga de contenido, descartando un falso positivo."