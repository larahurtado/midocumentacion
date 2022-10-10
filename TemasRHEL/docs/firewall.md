## Modo Panico

En ocasiones es necesario cortar la comunicación de nuestro equipo esto principalmente se hace cuando nuestro equipo esta comprometido con algun atacante.

+ Para activar el trafico de red(activar el modo panico):

```bash
firewall-cmd --panic-on
```

+ Para desactivar el trafico de red(desactivar el modo panico):

```bash
firewall-cmd --panic-off
```

+ Para ver si el modo panico esta activo o desactivado:

```bash
firewall-cmd --query-panic
```
