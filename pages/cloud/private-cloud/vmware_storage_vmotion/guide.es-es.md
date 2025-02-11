---
title: VMware Storage VMotion
excerpt: Cómo migrar en caliente una máquina virtual a un host diferente
updated: 2020-07-10
---

**Última actualización: 30/06/2020**

## Objetivo

El **Storage vMotion** permite modificar la ubicación del almacenamiento de los archivos de la máquina virtual manteniendo la máquina virtual encendida. Es posible mover la máquina virtual por completo o disco por disco.

**Esta guía explica cómo realizar esta operación.**

## Procedimiento

### Migrar el disco de una máquina virtual

Para migrar los archivos de una máquina virtual hacia otro datastore, solo tendrá que hacer clic derecho en la máquina virtual encendida y seleccionar la opción `Migrate...`{.action}.

![Migrar disco](images/VmotionStorage1.png){.thumbnail}

### Seleccionar el tipo de vMotion

Puede elegir entre diversas opciones de **vMotion**. En nuestro ejemplo, solo queremos migrar la máquina virtual hacia otro banco de datos. Para ello, deberá seleccionar la opción `Change storage only`{.action}.

La opción `Change compute resource only`{.action} permite migrar la máquina virtual hacia otro host.  

Para más información sobre la operación **vMotion**, consulte nuestra [guía](/pages/cloud/private-cloud/vmware_vmotion_new).

![Selección de vMotion](images/VmotionStorage2.png){.thumbnail}

### Seleccionar el datastore

También puede elegir hacia qué almacenamiento desea migrar los datos.

Asimismo, es posible modificar la política de almacenamiento durante esta operación.

De este modo, si dispone de un [almacenamiento vSAN](/pages/cloud/private-cloud/vmware_vsan) o de la opción [VM encryption](/pages/cloud/private-cloud/vm_encrypt), podrá aplicar las políticas de almacenamiento creadas.

![Selección del datastore](images/VmotionStorage3.png){.thumbnail}

En caso de que disponga de varios discos virtuales en la misma máquina, podrá migrar un único disco utilizando el botón `Advanced`{.action}.

Aparecerá la siguiente interfaz:

![Datastore vMotion](images/VmotionStorage6.png){.thumbnail}

### Completar la operación vMotion

Haga clic en `Finish`{.action} para lanzar la migración.

![Completar la operación vMotion](images/VmotionStorage4.png){.thumbnail}

### Monitorizar la operación vMotion

Puede consultar el estado de la migración en su lista de tareas recientes. La duración de esta operación dependerá del tamaño de la MV, los accesos IO y el ancho de banda utilizado.

![Monitorizar la operación vMotion](images/VmotionStorage5.png){.thumbnail}

## Más información

Interactúe con nuestra comunidad de usuarios en <https://community.ovh.com/en/>.
