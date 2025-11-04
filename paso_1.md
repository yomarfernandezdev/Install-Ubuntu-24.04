
<a href="./requisitos.md">atrás</a> - Paso 1: Crear el Medio de Instalación y Arrancar - <a href="./paso_2.md">siguiente</a>

1. ## Descarga de Rufus

**Rufus** es una utilidad gratuita y de código abierto para Windows que te ayuda a formatear y crear medios USB de arranque.

  1.  Abre tu navegador web y ve al sitio oficial de Rufus: **`https://rufus.ie/es/`**
  2.  Desplázate hacia abajo hasta la sección de **"Descargar"**.
  3.  Haz clic en el enlace de la **versión ejecutable estándar** (por ejemplo, `rufus-4.x.exe`) o en la **versión Portable** (`rufus-4.x.p.exe`). **No requiere instalación**, solo tienes que ejecutar el archivo.
   
## Creación del USB de Arranque con Rufus
Asegúrate de tener la **imagen ISO de Ubuntu Server 24.04 LTS** descargada y una **unidad USB** (mínimo 8 GB, ten en cuenta que **todos los datos que contenga serán eliminados**).
   ### 1. Preparación

  1.  Conecta tu **unidad USB** a tu computadora.
  2.  Haz doble clic en el archivo **Rufus** que descargaste (`.exe`) para abrir la aplicación.

   ### 2. Configuración de Rufus

Una vez que Rufus esté abierto, sigue los siguientes pasos para configurar las opciones:

| Opción | Configuración | Notas |
| :--- | :--- | :--- |
| **Dispositivo** | Selecciona tu **USB** | **¡MUY IMPORTANTE!** Asegúrate de elegir la unidad USB correcta, ya que su contenido se borrará. |
| **Elección de arranque** | **Disco o imagen ISO** | Debe ser la opción por defecto. |
| **Botón SELECCIONAR** | Haz clic y busca el archivo **ISO de Ubuntu Server 24.04** | Navega hasta donde guardaste el archivo `.iso` y selecciónalo. |
| **Esquema de partición** | **GPT** o **MBR** | La elección de **GPT** (para sistemas más modernos con **UEFI**) o **MBR** (para sistemas más antiguos con **BIOS Legacy**) dependerá de la arquitectura del equipo donde vayas a instalar Ubuntu Server. **Generalmente, GPT es la recomendación actual**. |
| **Sistema de destino** | **UEFI (no CSM)** o **BIOS (o UEFI-CSM)** | Se ajustará automáticamente según el "Esquema de partición" elegido. |
| **Etiqueta de volumen** | Puedes dejar la etiqueta por defecto (Ej: `UBUNTU`) o ponerle un nombre que prefieras. | No es crítico. |
| **Sistema de archivos** | **FAT32** | Por lo general, se selecciona automáticamente el formato óptimo (como FAT32 o ISO9660) para la imagen ISO. |

> **Nota:** La mayoría de las configuraciones, como el **Tamaño de clúster**, se pueden dejar en sus valores por defecto.

   ### 3. Escritura de la Imagen ISO

  1.  Haz clic en el botón **EMPEZAR**.
  2.  Rufus te preguntará si deseas escribir la imagen en **modo Imagen ISO** (recomendado para la mayoría) o **modo Imagen DD**.
    * Para la mayoría de las ISO de Linux (como Ubuntu), selecciona la opción **"Escribir en modo Imagen ISO (Recomendado)"**.
    * Haz clic en **Aceptar**.
  3.  Aparecerá una **advertencia** de que **todos los datos en el USB serán destruidos**. Confirma haciendo clic en **Aceptar**.
  4.  Rufus comenzará el proceso de formateo de la unidad USB y luego la escritura de la imagen ISO. Esto puede tardar varios minutos.

  ### 4. Finalización

  1.  Una vez que el proceso se complete, la barra de estado se pondrá de color **verde** y dirá **"PREPARADO"**.
  2.  Haz clic en el botón **CERRAR**.
  3.  Tu **USB de Arranque de Ubuntu Server 24.04** está listo para usarse. Puedes extraer el USB de forma segura.

### 5.  Arranca desde el USB:
Conecta la unidad USB al servidor. Reinicia el servidor e ingresa al menú de arranque (generalmente presionando `F2`, `F10`, `F12` o `Supr`) para seleccionar la unidad USB como dispositivo de arranque.
### 6.  Selecciona el Instalador:
En el menú de inicio, selecciona la opción **"Install Ubuntu Server"**.


