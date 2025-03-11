Los equipos de red Huawei utilizan el sistema operativo VRP (Versatile Routing Platform).
Tomando como referencia el sistema operativo para equipos Cisco, IOS, se describirán los modos de operación en equipos VRP:

---
1. Modos de configuración

En ambos sistemas operativos, el modo de operación inicial de los equipos es **modo usuario**.
  - Cisco:
    - User EXEC mode: Indicado por el prompt `Device>`.
  - Huawei:
    - User mode: Indicado por el prompt `<Huawei>`.

En equipos Huawei el modo de configuración global, utilizado para realizar modificaciones a la configuración del dispositivo, es indicado con el prompt entre corchetes:
- `[Huawei]`

---
2. Configuración de interfaces

- Configurar direccionamiento IPv4:
  1. Ingresar a la interfaz.
  2. Ejecutar el comando `ip address` seguido de la dirección IPv4 y la máscara de red.
    - La máscara de red puede ser indicada por la máscara en notación decimal o utilizando el prefix-lenght
      - `ip address ipv4-address x.x.x.x`
      - `ip address ipv4-address [0-32]`

---
# Tabla de comandos básicos

| Tarea   | Comando Cisco | Comando Huawei      |
|----------|------|------------|
| Ingresar a modo de configuración global     | `configure terminal`   | `system-view`     |
| Ingresar a modo de configuración de interfaz    | `interface interface-id`  | `interface interface-id`  |
| Configurar direccionamiento IPv4 en interfaz   | `ip address ip-address mask`   | `ip address ip-address [mask/prefix-length]`   |
| Habilitar interfaz | `no shutdown` | `undo shutdown`  |
| Asignar nombre al dispositivo | `hostname nombre` | `sysname nombre` |
| Asignar Banner Motd a la consola | `banner motd texto` | `header shell information texto`  |
| Verificar todas las interfaces | `show ip interface brief`  | `display ip interface brief`   |
| Verificar Tabla de enrutamiento | `show ip route` | `display ip routing-table`   |
| Guardar la configuración actual | `copy running-config startup-config` | `save`  |
| Reiniciar el sistema | `reload` | `reboot`  |

