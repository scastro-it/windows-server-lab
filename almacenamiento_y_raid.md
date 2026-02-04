# Almacenamiento y RAID – HPE DL360 Gen10

Documento sobre las pruebas y decisiones relacionadas al almacenamiento
y RAID en el servidor HPE ProLiant DL360 Gen10.

## Hardware
- Servidor: HPE DL360 Gen10
- Cantidad de discos: 2 discos rígidos SATA

## Situación inicial
- Los discos no aparecían en Smart Array
- No fue posible crear RAID por hardware desde BIOS / Smart Storage
- Se detectaron limitaciones del controlador de almacenamiento

## Análisis
El modelo y la configuración del servidor no permiten RAID por hardware
sin un controlador Smart Array dedicado.

Por este motivo:
- No se pudo crear RAID desde BIOS
- Windows Server no detectaba discos sin drivers adecuados

## Alternativas evaluadas
1. RAID por hardware (no disponible en esta configuración)
2. RAID por software desde Windows Server
3. Uso de discos independientes (sin RAID)

## Decisión
Se optó por continuar con Windows Server instalado correctamente
y evaluar RAID por software como siguiente paso del laboratorio.

## Pendientes
- Configurar espejo (RAID 1) por software desde Windows Server
- Evaluar impacto y diferencias frente a RAID por hardware
