Los equipos de red Huawei utilizan el sistema operativo VRP (Versatile Routing Platform).
Tomando como referencia el sistema operativo para equipos Cisco, IOS, se describirán los modos de operación en equipos VRP:
1. Modos de configuración
---
En ambos sistemas operativos, el modo de operación inicial de los equipos es **modo usuario**.
  - Cisco:
    - User EXEC mode: Indicado por el prompt `Device>`.
  - Huawei:
    - User mode: Indicado por el prompt `<Huawei>`.

En equipos Huawei el modo de configuración global, utilizado para realizar modificaciones a la configuración del dispositivo, es indicado con el prompt entre corchetes:
- `[Huawei]`



| Tarea   | Comando Cisco | Comando Huawei      |
|----------|------|------------|
| Ingresar a modo de configuración global     | `configure terminal`   | `system-view`     |
| Ingresar a modo de configuración de interfaz    | `interface interface-id`  | `interface interface-id`  |
| Carlos   | 28   | Valencia   |
