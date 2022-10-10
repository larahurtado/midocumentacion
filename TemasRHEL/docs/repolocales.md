## Añadir Repositorio

Para agregar repositorios externos existen dos formas para hacerlo

1. Crear y editar un archivo **.repo**  en "/etc/yum.repos.d/" con la siguiente estructura:
   
   + Sintaxis basica de un archivo .repo
   
```bash
[etiqueta]
name=#nombre del servicio
baseurl=#url anydesk
gpgcheck=#
repo_gpgcheck=#
gpgkey=#
```

     

1. usando el comando:

```bash
dnf config-manager
```
