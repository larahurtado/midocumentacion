Su funcion es realizar informes de actividades del sistema, este proceso es activado por un crontab cada cierto tiempo para generar un informe.

## Instalación(SAR)

---

## Instalación(kSAR)

1. Verificar que tiene instalado java, para saber si esta instalado ejecutar el siguiente comando.

```bash
[user@linux ~]$ java --version
openjdk 17.0.4.1 2022-08-12
OpenJDK Runtime Environment (Red_Hat-17.0.4.1.1-1.fc36) (build 17.0.4.1+1)
OpenJDK 64-Bit Server VM (Red_Hat-17.0.4.1.1-1.fc36) (build 17.0.4.1+1, mixed mode, sharing)
```

**Nota:** si aparece lo anterior significa que tiene instalado java, en caso de no tener instalado java abra el siguiente enlace.

2. Descargar el archivo con terminacion **.jar** del siguiente enlace [Release v5.2.3 · vlsi/ksar · GitHub](https://github.com/vlsi/ksar/releases/tag/v5.2.3) , verificar que sea la version mas reciente
3. Una vez descargado solo ejecute el archivo **.jar** con el siguiente comando

```bash
#sintaxis
java -jar <archivo>.jar 

#ejemplo
java -jar ksar-5.2.4-b396_gf0680721-SNAPSHOT-all.jar 
```

---

## Graficar datos de sar con KSAR

Para poder graficar los archivos que genera el comando sar es 



---

## Graficar datos de sar con SARchart
