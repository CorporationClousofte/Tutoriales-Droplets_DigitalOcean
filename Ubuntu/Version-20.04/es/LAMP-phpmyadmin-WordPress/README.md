# INSTALACCION LAMP PHPMYADMIN SSL & WORDPRESS

En este tutorial vamos a aprender como crear nuestro primer Droplet e igual instalar LAMP, phpmyadmin, ssl & WordPress de una manera facil.

Puede usar este cupon para obtener $100 en creditos que lo puedes usar para crear tu primer droplet para personalizado o practicar. (Solamente para nuevos miembros)

[![DigitalOcean Referral Badge](https://web-platforms.sfo2.cdn.digitaloceanspaces.com/WWW/Badge%201.svg)](https://www.digitalocean.com/?refcode=1f68e98f66e2&utm_campaign=Referral_Invite&utm_medium=Referral_Program&utm_source=badge)

<img src="../images/es/LAMP-phpmyadmin-WordPress/Tutorial_Instalar-Lamp-phpmyadmin-ssl-Wordpress-Ubuntu20.04_DigitalOcean.png" alt="Portada-Tutorial-Lamp-WordPress-Ubuntu20.04" height="600">

## Paso 1: Crearemos un nuevo Droplet en DIGITAL OCEAN

Ingresamos a nuestro panel de contro, abrimos la seccion "Create" y selecionamos "Droplets"

<img src=".../images/es/LAMP-phpmyadmin-WordPress/1.Crear-Droplet-Panel-DO.png" alt="Panel-Control-DO" height="400">

Vamos seleccionar la distribuccion con su version, en este tutorial vamos a usar Ubuntu 20.04 (LTS) x64

<img src="../images/es/LAMP-phpmyadmin-WordPress/2.Crear-Nuevo-Droplet-Ubuntu.png" alt="Distribuccion-Version-Droplet" height="400">

Elegirmos el plan que necesitamos para nuestro proyecto, en este caso seleciono la categoria "Basic" con el CPU "Premium AMD" y de acuerdo a nuestro presupuesto podemos elegir cualquier droplet pero para practicar vamos a seleccionar que dice $6mon RAM: 1GB SSD: 25GB Transferencia: 1000GB.
(Las categorias se encuentra en la parte final de tutorial)

<img src="../images/es/LAMP-phpmyadmin-WordPress/3.Selecionamos-el-Nivel-Droplet-DO.png" alt="Planes Droplets" height="400">

Si queremos mas almacenamientos podemos añadir volumen bloques que solamente cobra $0.10 x GB x Mes pero en este caso no vamos añadir nada de volumen porque es solamente practicar pero si tiene un proyecto puede añadirlo queda en su decision.

<img src="../images/es/LAMP-phpmyadmin-WordPress/4.Bloques-Almacenamiento-Droplets.png" alt="Volumens Droplets" height="400">

Vamos a elegir la ubicacion donde queremos que se encuentre nuestro Droplet, DO tiene varias regiones segun su disponiblidad, en este caso como vivo en Ecuador voy a selecionar la ubicacion San Francisco #3

<img src="../images/es/LAMP-phpmyadmin-WordPress/5.Regiones-Centro-Datos-DO.png" alt="Regiones Droplets DO" height="400">

En esta parte es muy importante ya que debemos elegir la seguridad de acceso de nuestro Droplet en este caso voy a seleccionar la parte "SSH" keys

<img src="../images/es/LAMP-phpmyadmin-WordPress/6.Autenticacion-SSH-DO.png" alt="Authenticacion SSH" height="400">

En esta seccion si queremos tener copia de seguridad seleccionamos pero es opcional, el resto si debemos seleccionar porque es el monitoreo de consumo de nuestro Droplet la IPv6 y el User Data

<img src="../images/es/LAMP-phpmyadmin-WordPress/7.Opciones-Droplet-DO.png" alt="Opciones Droplets DO" height="400">

En esta parte si queremos cambiar el hostname de nuestro Droplet y si no dejamos por defecto. Si esta todo podemos proceder a create droplet.

<img src="../images/es/LAMP-phpmyadmin-WordPress/8.Hostname-Droplet-DO.png" alt="Opciones Droplets DO" height="400">

Esperemos que se termine de crear el droplet, se toma unos segundos en terminar.

<img src="../images/es/LAMP-phpmyadmin-WordPress/9.Cargar-Droplet-DO.png" alt="Cargar Droplets DO" height="400">

Luego abrimo el panel de nuestro Droplet y podemos observar todas las caracteristicas como las ips las graficas los volumnes las copias de seguridad, etc.

<img src="../images/es/LAMP-phpmyadmin-WordPress/10.Info-Droplet-DO.png" alt="Info Droplets DO" height="400">
<img src="../images/es/LAMP-phpmyadmin-WordPress/11.Info2-Droplet-DO.png" alt="Info Droplets DO" height="400">


## Paso 2: Actualizar y Descargar Paquetes en nuestro Droplet

En este paso vamos a ingresar a nuestro droplet al talvez de panel de control de nuestra cuenta de DO. (Importante la key ssh debe estar agregada a Droplet)

<img src="../images/es/LAMP-phpmyadmin-WordPress/12.Acces-Root-Droplet-DO.png" alt="Acces Root Droplet" height="400">

Dentro de nuestro Droplet podemos observar la informacion importante que nos indicar el sistema Ubuntu

<img src="../images/es/LAMP-phpmyadmin-WordPress/13.InfoInterno-Droplet-DO.png" alt="Info Interno Droplet" height="400">

### Ahora viene la parte interesante comenzamos a usar los comandos para navegar por nuestro sistema y actualizado de manera correcta.

Vamos a explicar los comandos basicos que usaremos para que no solamente copie y pegue sino sepa que es lo que esta copiando o escribiendo :)

```
cd <NombreCaperta> -> cd home
cd .. -> Significa que estamos retrociendo la carpeta anterior que estamos
cd / : Significa que se mueve a la carpeta raiz de todo el sistema
pwd : Podemos saber en que carpeta estamos ubicado actualmente
ls : Nos muestra todas las carpetas que estamos ubicado.
```

Ahora vamos a nuestro terminal. 

```
sudo apt-get update && sudo apt-get upgrade
```

El comando anterior significa que queremos actualizar los paquetes y sistemas e igual descargar lo que necesite nuestro Droplet ya que viene por default




## Conceptos

- Un Droplet es una máquina virtual (VM) basada en Linux donde ese ejecutar sobre el hardware virtualizado. Es decir un Droplet es un servidor virtual VPS.
- Ubuntu es una distribuccion basada en Debian de sistema operativo Linux la madre de todos los software de medio mundo.

## Categorias Droplets DO
- Regular & Premium (Solamente Plan Basico): Puedes elegir tu CPU regular o premium, de cuale el premium viene con procesadores INTEL o ADM más modernas y SSD NVMe.
- Procesadores Intel: Las categorias General Purpose, CPU-Optimized, Memory-Optimized, Storage-Optimized viene con los mejores procesadores de Intel
- **Basic:** Esta opcion es recomendable para mayoria de los casos de uso, tanto si quieres alojar sitios web, entornos de pruebas o practicar el sistema operativo sin precouparte dañar tu PC.
- **General Purpose:** Esta maquina virtual de alto rendimiento es recomendable para aplicaciones de produccion, como alojamiento de aplicaciones web, sitios de comercio electronico, bases de datos de tamaño mediano y aplicaciones empresariales que requieren una mayor proporcion de memoria a CPU.
- **CPU-Optimized:** Esta maquina virtual optimizada cómputo con hyper-threads dedicados es recomendable para aplicaciones con uso intensivo de CPU, como CI/CD, codificación y transcodificación de vídeo, publicación de anuncios, aprendizaje automático, procesamiento por lotes y servidores front-end web y de aplicaciones activos.
- **Memory-Optimized:** Esta maquina virtual optimizada en memoria con 8 GB de RAM por vCPU e hyper-threads es recomendable para aplicaciones con uso intensivo de RAM, como bases de datos de alto rendimiento, cachés en memoria a escala web y procesamiento de big data en tiempo real.
- **Storage-Optimized:** Esta maquina virtual optimizada en almacenamiento es recomendable para grandes bases de datos NoSQL, MongoDB y Elasticsearch, bases de datos de series temporables y otros almacenes de datos.

--------------------------------------------------------------------------------------------------------------------------------------

Este conocimiento fundamental te ayudará para que puedas crear droplets tan facil sin tanto rodeos.

Curso Propedútico de LAMP PHPMYADMIN SSL WORDPRESS para Tutoriales Droplets DO - Corporation Clousofte.

Material desarrollado con base en los contenidos de Digital Ocean, traducción e implementación por: David Lucero Sigcho - Developer de Clousofte.

Redes:
* GitHub: [DavidLuceroSigcho](https://github.com/DavidLuceroSigcho)
* Twitter:
* Instagram: [DavidLuceroSigcho](https://www.instagram.com/DavidLuceroSigcho/)
* Linkedin: [DavidLuceroSigcho](https://www.linkedin.com/in/david-lucero-sigcho/)