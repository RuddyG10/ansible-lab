# Repositorio de Playbooks Ansible para Dispositivos de Red Cisco

Este repositorio contiene diversos **playbooks de Ansible** que permiten gestionar y configurar dispositivos de red Cisco de forma automatizada. Los playbooks incluyen tareas como la configuración de interfaces, la recolección de datos de los dispositivos y la configuración de servicios como SNMP y NTP.

## Inventario de Dispositivos

El archivo `inventory.ini` organiza los dispositivos en grupos según el sistema operativo de red. A continuación, se muestra un ejemplo de su estructura:

```ini
[iosxe]
devnetsandboxiosxe.cisco.com ansible_user=admin ansible_password=C1sco12345 ansible_network_os=cisco.ios.ios

[iosxr]
sandbox-iosxr-1.cisco.com ansible_user=admin ansible_password=C1sco12345 ansible_network_os=iosxr
## Requisitos

Para ejecutar estos playbooks de Ansible, asegúrate de cumplir con los siguientes requisitos:

1. **Ansible**: 
   - Debes tener Ansible instalado en tu sistema. Puedes instalarlo mediante `pip`:
     ```bash
     pip install ansible
     ```
   - **Versión recomendada**: Ansible 2.9 o superior.


2. **Archivo de Inventario**:
   - Define tus dispositivos en un archivo de inventario (`inventory.ini`) con la siguiente estructura de ejemplo:
     ```ini
     [iosxe]
     devnetsandboxiosxe.cisco.com ansible_user=admin ansible_password=C1sco12345 ansible_network_os=cisco.ios.ios

     [iosxr]
     sandbox-iosxr-1.cisco.com ansible_user=admin ansible_password=C1sco12345 ansible_network_os=iosxr
     ```
   - Personaliza los valores de `ansible_user`, `ansible_password`, y `ansible_network_os` según las credenciales y el sistema operativo de tus dispositivos.

3. **Conexión de Red**:
   - Verifica que tienes conectividad de red entre el servidor Ansible y los dispositivos de red Cisco.

4. **Permisos de Ejecución**:
   - Ejecuta Ansible desde una cuenta con los permisos necesarios para gestionar configuraciones en los dispositivos de red especificados.

---

Una vez cumplidos estos requisitos, estarás listo para ejecutar los playbooks y automatizar la configuración de los dispositivos Cisco.
