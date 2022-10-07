Troubleshooting quiere decir "Solución de problemas o Recursos para solucionar problemas", para  esta seccion lo aplicaremos para la perdida de paquetes de red. 

Cuando se administra un servidor o un equipo este puede llegar a tener problemas de red, los cuales van desde lo fisico a lo virtual(configuracion) en las distribuciones linux estas cuentan con herramientas para poder intuir el posible error que lo provoca.

---

## Comando ping

Este comando nos permite checar  si existe comunicación entre un equipo remoto y el nuestro.

```bash
#sintaxis para pedir ciertas veces si existe conexion en un equipo remoto
ping -c <numero de veces de consulta> <ip>
#ejemplo
ping -c 4 8.8.8.8
```

El resultado que nos da el comando anterior demuestra que existe conexion con el equipo remoto 8.8.8.8 ya que en los parametros de la parte inferior dice que de 4 paquetes tramitidos, estos fueron recividos en su totalidad en un tiempo de 300 ms.

```bash
[user@linux ~]$ ping -c 4 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=115 time=22.2 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=115 time=23.6 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=115 time=22.8 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=115 time=22.3 ms

--- 8.8.8.8 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3003ms
rtt min/avg/max/mdev = 22.192/22.735/23.645/0.580 ms
```

Para fines didacticos  se activo del firewall en modo panico  para simulara un fallo con la conexion el resultado que produce seria que los 4 paquetes que fueron enviados, todos estos no fueron recibidos tal y como se muestra a continuacion.

```bash
[user@linux ~]# ping -c 4 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.

--- 8.8.8.8 ping statistics ---
4 packets transmitted, 0 received, 100% packet loss, time 3085ms
```

existe ocasiones que de 4 paquete enviados 2 son recibidos y 2 son perdidos, lo cual se puede llegar a deducir que existe intermitencia en la conexion. 

---

## Comando mtr

Este comando nos permite ver los saltos(traceroute) que realiza el ordenador al host remoto al cual se desea comunicar por ejemplo.

```bash
            My traceroute [v0.95]
fedora (10.0.2.15) -> 8.8.8.8 (8.8.8.8)           2022-10-06T15:00:27-0500
keys: Help Display Mode    Restart statistics  order of fields quit
                                      Packets             Pings
Host                                 Loss%  Snt  Last Avg Best Wrst StDev
1. _gateway                            0.0% 439   0.7 0.6 0.2
2. 192.168.1.254                            0.0% 439   0.7 0.6 0.2
3. dns.google                            0.0% 439   0.7 0.6 0.2
```

Dentro de una red interna se veria  mejor el efecto ya que uno conoce aproximandamente que dispositivos existen dentro de la red.


