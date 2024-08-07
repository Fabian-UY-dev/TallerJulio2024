## Obligatorio Taller de Servidores Linux

Este documento describe como utilizar los playbooks de ansible para configurar una aplicacion Java con tomcat 9 en servidor CentOS  Stream 9 y una base de datos MariaDB en Ubuntu 24.04

## Instalación ansible core

pipx install ansible-core

Se necesitan instalar las siguientes colleciones para los playbooks

  - ansible.posix
  - community.general
  - community.mysql

Para instalarla se debe revisar la documentación de ansible y remplazar los terminos mynamespace y mycollection

ansible-galaxy collection install my_namespace.my_collection
## Requermientos (POST-ENTREGA)



## Verificación de playbooks

Para verificar que la sintaxis de los playbooks sea correcta se debe ejecutar el siguiente comando

ansible-playbook -i inventario --check nombre_playbook.yml

## Ejecución de Playbooks

Para utilizar los playbooks se debe ir a la carpeta donde se descargaron los archivos y ejectuar el siguiente comando

ansible-playbook -i invetory/servidores.toml nombre_playbook.yml--ask-become-pass

El archivo inventory contiene los host.

## License

[GPL-3.0](https://choosealicense.com/licenses/gpl-3.0/)