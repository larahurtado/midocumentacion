## keytool

Es un comando que administra un almacen de claves(base de datos) de claves criptografica, cadena de certificados X.509 y certificados de confianza

* Generar un par de claves en almacen por defecto(~/.keystore)

```bash
keytool -genkeypair -keyalg <RSA|DSA|EC> -alias <aliaskey>
```
* Generar un par de claves en almacen definido en un path absoluto o relativo

```bash
keytool -genkeypair -keyalg <RSA|DSA|EC> -alias <aliaskey> -keystore <path/name|name>
```

* Ver todas las claves que tiene el almacen por defecto(~/.keystore)

```bash
keytool -genke-keystore 
```



---
## Key Store



---
## Referencias
+ [Tipos de claves, algoritmos y operaciones](https://learn.microsoft.com/es-es/azure/key-vault/keys/about-keys-details)
+ [keytool comand oracle](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/keytool.html)
+ [keystore GUI](https://keystore-explorer.org/downloads.html) 