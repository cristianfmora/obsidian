# Extender una partición

1. Escoger la partición para agregar el grupo
   ```
   # Agregar espacio al grupo
   pvcreate /dev/sdx
	```
2. Extender volumen lógico
	```
	 lvextend -L +tamaño /dev/[name-vg]/[name-lv]
	 # Ej: lvextend -L +10G /dev/mapper/datos-root
   ```
3.  Redimensionar archivos xfs
   ```
   xfs_growfs /punto/de/montaje
   ej: xfs_growfs /dev/mapper/datos-root
```