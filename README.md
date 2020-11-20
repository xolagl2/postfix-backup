# postfix-backup

Este es un proyecto Ansible para realizar salvas de las configuraciones de 5 servidores de correo postfix remotos.

Los ficheros de configuracion de cada servidor se salvan dentro de carpeta con el nombre del hostname de cada servidor dentro de la carpeta "backups"

## Requerimientos:

- Se requiere tener ansible instalado y configurado, usuario "ansible" creado con sus respectivas llaves para conexion SSH en la PC de control.
- Se requiere que en cada servidor remoto este creado el usuario "ansible" con la respectiva llave ssh, copiada desde el equipo de control.
- Se debe modificar el fichero host segun los requerimientos existentes.
- Se debe modificar la definicion de la variable {{backupdir}} la ruta a la carpeta destino "backups".

## Metodo de ejecucion:

- Entrar al directorio del proyecto y ejecuta:
>  $ ansible-playbook postfix-backup.yml

