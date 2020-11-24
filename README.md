# postfix-backup

Proyecto Ansible para realizar salvas de las configuraciones de 5 servidores de correo postfix remotos.

Los ficheros de configuración de cada servidor se salvan dentro de la carpeta "backups", separados en carpetas con el nombre del hostname de cada servidor.

## Requerimientos:

- Se requiere tener ansible instalado y configurado en PC de Control.
- Usuario "ansible" creado con sus respectivas llaves para conexión SSH en la PC de control.
- Usuario "ansible" creado en cada servidor remoto a controlar.
- Llave ssh publica del usuario "ansible" copiada desde la PC de control, a los servidores remotos.
- Se debe modificar el fichero host segun las direcciones de los servidores remotos a controlar.
- Se debe modificar la variable {{backupdir}} con la ruta a la carpeta destino "backups".

## Metodo de ejecución básico:

- Entrar al directorio del proyecto y ejecutar:
>  $ ansible-playbook postfix-backup.yml

