Los equipos de red Huawei utilizan el sistema operativo VRP (Versatile Routing Platform).
Tomando como referencia el sistema operativo para equipos Cisco, IOS, se describirán los modos de operación en equipos VRP:

---
# Tabla de comandos básicos

| Tarea   | Comando Cisco | Comando Huawei      |
|----------|------|------------|
| [Ingresar a modo de configuración global](#modos-de-configuración)     | `configure terminal`   | `system-view`     |
| [Ingresar a modo de configuración de interfaz](#modos-de-configuración)    | `interface interface-id`  | `interface interface-id`  |
| [Configurar direccionamiento IPv4 en interfaz](#configurar-direccionamiento-ipv4)   | `ip address ip-address mask`   | `ip address ip-address [mask/prefix-length]`   |
| Habilitar interfaz | `no shutdown` | `undo shutdown`  |
| Asignar nombre al dispositivo | `hostname nombre` | `sysname nombre` |
| Asignar Banner Motd a la consola | `banner motd texto` | `header shell information texto`  |
| [Configurar contraseña de acceso](#configurar-contraseña-de-acceso) | `enable password contraseña` | `authentication-mode password`|
| Configurar hora y fecha | `clock set hh:mm:ss yyyy:mm:dd` | `clock datetime hh:mm:ss yyyy:mm:dd` |
| Crear una VLAN | `vlan vlan-id` | `vlan vlan-id` |
| Verificar la versión del sistema | `show version` | `display version`  |
| Verificar todas las interfaces | `show ip interface brief`  | `display ip interface brief`   |
| Verificar Tabla de enrutamiento | `show ip route` | `display ip routing-table`   |
| Verificar tiempo del dispositivo | `show clock` | `display clock`  |
| Guardar la configuración actual | `copy running-config startup-config` | `save`  |
| Reiniciar el sistema | `reload` | `reboot`  |

---
## Modos de configuración

En ambos sistemas operativos, el modo de operación inicial de los equipos es **modo usuario**.
  - Cisco:
    - User EXEC mode: Indicado por el prompt `Device>`.
  - Huawei:
    - User mode: Indicado por el prompt `<Huawei>`.

En equipos Huawei el modo de configuración global, utilizado para realizar modificaciones a la configuración del dispositivo, es indicado con el prompt entre corchetes:
- `[Huawei]`

Ciertos comandos (por ejemplo, el comando `save`) solo funcionan en la vista de usuario, por lo que fue incluida una combinación de teclas para cambiar a dicha vista de forma rápida: `Ctrl-z`.
Si deseas volver a la vista anterior puedes utilizar el comando `quit`.

### Eliminar la configuración
Una configuración puede ser descartada debido a varios motivos. En equipos Cisco se antepone la palabra "no" antes de un comando para eliminar la configuración.
- **En equipos Huawei**, se antepone la palabra *undo* para eliminar la configuración de un comando, por ejemplo: `undo ip address`.

---
## Configurar contraseña de acceso
1. Ingresar a la línea consola, por medio del comando `user-interface console 0`
2. Ejecutar comando `authentication-mode password`
3. Ejecutar comando `set authentication password cipher contraseña`


## Configuración de interfaces

### Configurar direccionamiento IPv4:
  1. Ingresar a la interfaz.
  2. Ejecutar el comando `ip address` seguido de la dirección IPv4 y la máscara de red.
    - La máscara de red puede ser indicada por la máscara en notación decimal o utilizando el prefix-lenght
      - `ip address ipv4-address x.x.x.x`
      - `ip address ipv4-address [0-32]`
    
## VLANs

### Creación de VLANs
En configuración global, crea una VLAN ejecutando el comando `vlan vlan-id`. Además, puedes crear múltiples VLANs ejecutando el comando `vlan batch vlan1, vlan2, ...`.
Puedes verificar las VLANs creadas con el comando `display vlan`.

---
# Referencias
- https://forum.huawei.com/enterprise/intl/en/thread/Basic-Operations-on-Huawei-VRP-CLI/667269526292676608?blogId=667269526292676608
- 
