# Instalación de Windows Server 2019 – HPE DL360 Gen10

Documento con los pasos y problemas que encontré al instalar
Windows Server 2019 en un servidor físico HPE ProLiant DL360 Gen10.

## Contexto inicial
- El servidor llevaba más de un año apagado
- No había sistema operativo instalado
- Los discos no eran reconocidos durante la instalación

## Proceso de instalación
1. Encendido del servidor y acceso a BIOS / System Utilities
2. Intento de detección de discos desde Intelligent Provisioning
3. Durante la instalación de Windows Server, el instalador no mostraba ningún disco disponible

## Problema principal
Windows Server 2019 no detectaba los discos rígidos durante la instalación.
Esto se debía a la falta de drivers del controlador de almacenamiento.

## Solución
- Descarga de los drivers de almacenamiento correspondientes al modelo del servidor
- Carga manual del driver durante la instalación de Windows Server
- Una vez cargado el driver, los discos fueron reconocidos correctamente

## Estado actual
- Windows Server 2019 instalado correctamente
- Drivers instalados
- Pendiente: configuración de RAID y almacenamiento

## Notas
Este documento forma parte de un laboratorio personal para aprender
administración de servidores y resolución de problemas reales.
