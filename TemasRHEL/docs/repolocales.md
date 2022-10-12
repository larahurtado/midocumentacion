## Añadir Repositorio

Para agregar repositorios externos existen dos formas para hacerlo

1. Crear y editar un archivo **.repo**  en "/etc/yum.repos.d/" con la siguiente estructura:
   
   + Sintaxis basica de un archivo .repo

```bash
#nombre que recibira el repo
[etiqueta]
#nombre del repo
name= Fedora
#url anydesk.com/fedora/x86_64 or http:127.0.0.1/fedora/x86_64
baseurl= http://127.0.0.1/repositorio/fedora/x86_64/
# valor logico 1= verdadero 0 = falso, este parametro sirve para habilitar el reposito cuando se ejecute dnf update
enabled=1
# valor logico 1= verdadero 0 = falso, este parametro indica que si es necesario usar un gpgkey si es falso no es necesario porner 
gpgcheck=0
# url donde se ubica el gpgkey
gpgkey=
```

     

2. usando el comando:

```bash
dnf config-manager --ad-repo <urlrepo>
```

Cuando agregue uno o varios repositorios nuevo es necesario hacer lo siguiente:

1. Actualizar las listas de repositorios:
   
   ```bash
   dnf update --refresh
   ```
   
   + (OPCIONAL)si requiere eliminar los packequetes que fueron descargado anterior mente.
   
   ```bash
   dnf clean all
   ```

2. Instale el paquete que se encuentra en el repositorio agregado:
   
   ```bash
   dnf install <Nombredelpaquete>
   ```

---

## Crear un servidor de repositorios

### Requisitos

Tener instalado los siguiente paquetes

+ apache
  
  ```bash
  sudo dnf install httpd
  ```

+ createrepo
  
  ```bash
  sudo dnf install createrepo
  ```

### Procedimiento

1. Crear un directorio en **/var/www/html** donde guardaremos nuestros Packages  y repodata, tomar en cuenta que este deve tener una estructura como **/var/www/html/repositorio/<SO>/<arquitectura>**
   
   ```bash
   mkdir /var/www/html/repositorio/fedora/x86_64
   ```

2. Dentro de la anterior ruta crear el directorio **Packages**
   
   ```bash
   mkdir /var/www/html/repositorio/fedora/x86_64/Packages
   ```
   
   En este directorio guardaras todos los .rpm que deseas agregar a tu servidor.

3. Ahora generaremos los metadatos xml:
   
   ```bash
   createrepo /var/www/html/repositorio/fedora/x86_64
   ```
   
   El comando anterior generara un diretorio con nombre **repodata** el cual su contenido son los metadatos  xml, este comando se debe de ejecutar cuando su carpeta Package fue modificada(elimino o agrego un rpm).

4. Apartir de ahora ya tiene su servidor de paquetes listo, solo tiene que añadir el repositorio tal y como aparace en esta pagina en el apartado **Añadir repositorio**



## Enlaces de RPM app

+ [Anydesk](https://anydesk.com/es/downloads/thank-you?dv=centos8_64)

+ [TeamViewer](https://download.teamviewer.com/download/linux/teamviewer.x86_64.rpm)

+ [Opera](https://rpm.opera.com/rpm/opera_stable-91.0.4516.65-linux-release-x64-signed.rpm)
