## Sistema de archivos XFS



## Sistema de archivos Ext4

Es una extension escalable del sistemas de archivos ext3, este sistema esta diseñado para soportar hasta 16 TB en su sistema de archivos, ademas que retira el límite de subdirectorio de 32000 presente en ext3.

**Nota:** Se recomienda que para sistemas de archivos superiores a 16  TB , se se el Sistema de archivos XFS.

Aunque este sistema de archivos sea optimo para la mayoria de cargas de trabajo,    puede surgir que su rendimiento sea afectado por lo cual existen diferentes opciones de ajustes para tratarlo.

+ Inicializacion de tabla de inodo

+ Conducta de Auto-fsync

+ Prioridad de E / S de diario

para obtener mas informacion de estos ajustes, selecionar el enlace 1 del apartado de referencias.

## fsck



## Referencias

1. [Sistemas de archivo Ext4, redhat.](https://access.redhat.com/documentation/es-es/red_hat_enterprise_linux/6/html/performance_tuning_guide/s-storage-fs)

2. [Sistemas de archivos XFS, redhat.]([7.3.2. Sistema de archivos XFS Red Hat Enterprise Linux 6 | Red Hat Customer Portal](https://access.redhat.com/documentation/es-es/red_hat_enterprise_linux/6/html/performance_tuning_guide/s-storage-xfs))

