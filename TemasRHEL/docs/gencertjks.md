## keytool

Es un comando que administra un almacen de claves(base de datos) de claves criptografica, cadena de certificados X.509 y certificados de confianza

* Generar un par de claves en almacen por defecto(~/.keystore)

```bash
keytool -genkeypair -keyalg <RSA|DSA|EC> -alias <aliaskey>
```
* Generar un par de claves en almacen definido en un path absoluto o relativo

```bash
keytool -genkeypair -keyalg <RSA|DSA|EC> -alias <aliaskey> -keystore <path/name|name>.<jks|keystore>
```

* Ver todas las claves que tiene el almacen por defecto(~/.keystore)

```bash
keytool -list 
```

* Ver todas las claves que tiene el almacen definido en un path absoluto o relativo


```bash
keytool -list -keystore <path/name|name>.<jks|keystore>
```

* Ver cierta clave que tiene el almacen por defecto(~/.keystore) detallada.

```bash
keytool -list -alias <aliaskey> -v 
```

* Ver cierta clave que tiene el almacen definido en un path absoluto o relativo detallada.


```bash
keytool -list -keystore <path/name|name>.<jks|keystore> -alias <aliaskey> -v
```


* Ver todas las claves que tiene el almacen por defecto(~/.keystore) detallada.

```bash
keytool -list -v
```

* Ver todas las claves que tiene el almacen definido en un path absoluto o relativo detallada.


```bash
keytool -list -keystore <path/name|name>.<jks|keystore> -v
```


* Ver todas las claves que tiene el almacen por defecto(~/.keystore) con estilo rfc.

```bash
keytool -list -rfc
```

* Ver todas las claves que tiene el almacen definido en un path absoluto o relativo con estilo rfc.


```bash
keytool -list -keystore <path/name|name>.<jks|keystore> -rfc
```



---
## Key Store

Es una interfaz grafica para la herramienta keytool


---
## Referencias
+ [Tipos de claves, algoritmos y operaciones](https://learn.microsoft.com/es-es/azure/key-vault/keys/about-keys-details)
+ [keytool comand oracle](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/keytool.html)
+ [keystore GUI](https://keystore-explorer.org/downloads.html) 