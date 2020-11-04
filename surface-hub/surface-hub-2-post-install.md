---
title: Configurar Windows 10 Pro o Enterprise en Surface Hub 2
description: En este artículo, se incluyen recomendaciones para garantizar la mejor experiencia al usar un equipo de lápiz y una pantalla grande personalizados.
keywords: Surface Hub, Windows 10, escritorio, instalar, configuración
ms.prod: surface-hub
ms.mktglfcycl: deploy
ms.localizationpriority: low
ms.sitesec: library
ms.pagetype: deploy
audience: admin
manager: laurawi
ms.audience: itpro
author: greg-lindsay
ms.author: greglin
ms.collection: M365-modern-desktop
ms.topic: article
ms.date: 11/03/2020
appliesto:
- Surface Hub 2S
ms.openlocfilehash: b86776b56e892c34ea8b5abbc55d5c48723a5f9e
ms.sourcegitcommit: 3ca1d1bc77452acca914d0af03e252ee260ebf1a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154132"
---
# Configurar Windows 10 Pro o Enterprise en Surface Hub 2

Después de completar el proceso de instalación de la migración a Windows 10 Pro o Enterprise, puede realizar los siguientes pasos para configurar las aplicaciones y la configuración de su Surface Hub 2. Estos pasos se recomiendan para garantizar la mejor experiencia de uso de este equipo de pantalla táctil y de lápiz de gran tamaño.

Al realizar estos pasos, es posible que le resulte útil usar un teclado y un mouse con cable o inalámbrico.

## Configurar las opciones del sistema

1. Inicie sesión con una cuenta que tenga privilegios de administrador local en el dispositivo.  

    - En los dispositivos Unidos a Azure AD, el usuario que realiza la combinación de Azure AD se agrega automáticamente al grupo de administradores local. Los administradores globales de Azure AD y los administradores de dispositivos Azure AD <a href="https://docs.microsoft.com/azure/active-directory/devices/assign-local-admin" target="_blank"> también son administradores locales </a> . 
    
    - Puede escribir **net localgroup Administrators** en un símbolo del sistema para enumerar las cuentas que tienen derechos de administrador local.
    
2. Cambie el nombre del dispositivo con un nombre descriptivo, por ejemplo: **nombre de usuario-SHub-escritorio**.

3. Seleccione **Start**  >  **Settings**  >  **accounts**  >  **Sync Your Settings** y desactiva la **configuración de sincronización** . 

    - La configuración que se usa aquí tiene el propósito de habilitar la mejor experiencia táctil de pantalla grande y, por lo tanto, es posible que no desee sincronizar otros dispositivos.
    
4. Reinicia el dispositivo.

## Habilitar el teclado táctil y el panel táctil

1. Puntee y mantenga presionado o haga clic con el botón derecho en la barra de tareas y seleccione Mostrar botón de **teclado táctil** y **Mostrar botón de panel táctil**. 

    - El teclado táctil es útil para la entrada directa por parte del usuario, y el panel táctil virtual ayuda a seleccionar con precisión, mantener la información en la pantalla o como alternativa para tocar y mantener el mouse. 
    
    - Consulta el ejemplo siguiente:

      ![Configuración táctil](images/touch.png)

2. Configure el teclado táctil en QWERTY y flotantes.

    1. Seleccione el icono de **teclado** en la barra de tareas para mostrar el teclado táctil.
    
    2. En el teclado táctil, seleccione el icono de teclado en la esquina superior izquierda para abrir la configuración del teclado.
    
    3. Seleccione el siguiente tipo de teclado en la fila superior para habilitar QWERTY y la última opción de la segunda fila para habilitar el flotante, que es muy útil en esta gran pantalla. Vea los ejemplos siguientes:

       ![Configuración del teclado](images/kbd.png)
 
3. Establecer la configuración de teclado de pantalla.

    1. Seleccione el icono de **configuración** en el teclado táctil o busque y Abra **configuración de escritura**.
    
       ![configuración de teclado de software](images/sh2-softkeyboard.png)

    1. Habilite todas las opciones de ortografía, escritura y teclado táctil.


En el ejemplo siguiente se muestra el panel táctil, que es útil para desplazarse y seleccionar las opciones. El teclado en pantalla se usa para buscar en Microsoft Store:

![Usar el panel táctil](images/store.png)

## Configurar el mouse y el teclado Bluetooth (opcional)

Conecte un teclado y un mouse si usa el dispositivo como dispositivo principal de Windows, o bien Utilícelo a menudo para trabajar con texto o con precisión.

Si el dispositivo Surface Hub está cerca de un PC, puedes usar el <a href="https://aka.ms/mm" target="_blank"> mouse sin bordes </a> para desplazarte sin problemas entre el Surface Hub y el equipo. Para obtener más información, vea <a href="https://blogs.microsoft.com/ai/microsoft-download-from-the-garage-mouse-without-borders/" target="_blank"> Descargar Microsoft del garaje: mouse sin bordes. </a>

## OneDrive para la Empresa

Use <a href="https://docs.microsoft.com/onedrive/onedrive" target="_blank"> OneDrive para </a> la empresa para compartir fácilmente herramientas, registros y otros archivos entre todos los dispositivos de su trabajo.

- OneDrive le permite compartir sus archivos de trabajo entre sus equipos portátiles, el escritorio Surface Hub y los dispositivos móviles administrados por Intune. Los archivos se pueden editar en cualquier dispositivo y todos los dispositivos conectados a la red se actualizarán con los cambios.

- Teniendo en cuenta el tamaño de la SSD del Surface Hub (128 GB), si configura OneDrive en su dispositivo de escritorio Surface Hub, asegúrese de que la configuración predeterminada es mantener los archivos en línea y descargar archivos a medida que los usa.

Para configurar OneDrive de modo que descargue los archivos solo cuando sea necesario, establezca la configuración **de archivos a petición** para **ahorrar espacio y descargar archivos a medida que los usa**. Para obtener más información, vea <a href="https://docs.microsoft.com/onedrive/files-on-demand-windows" target="_blank"> consultar y establecer los Estados a petición de los archivos en Windows </a> .

![Configuración de OneDrive](images/onedrive.png)

> [!NOTE]
> También puede repetir estos pasos para configurar un OneDrive personal, pero asegúrese de ahorrar espacio en disco y solo descargar archivos a medida que los necesite.

## SharePoint y Teams

Los archivos de canal de SharePoint y Teams también se pueden sincronizar localmente con los dispositivos de escritorio, como equipos portátiles y Surface Hub, con el motor de sincronización de OneDrive.

Para sincronizar los archivos corporativos internos con la unidad local con la aplicación de sincronización de OneDrive:

1. Vaya a un sitio de SharePoint y navegue hasta el directorio de documentos de nivel superior para ver los archivos que le interesa ver o editar desde el dispositivo local.

2. Seleccione el botón **sincronizar** en la parte superior de la cinta de opciones de SharePoint.

3. Seleccione al **abrir** en el elemento emergente **este sitio está intentando abrir Microsoft OneDrive**.

4. Compruebe que los archivos de SharePoint se sincronizan con su unidad local seleccionando en el icono de OneDrive en la parte inferior derecha de la barra de tareas.

5. Compruebe que la configuración esté configurada para mantener los archivos en línea y descargar los archivos solo a medida que los usa:

    1. Abra el explorador de archivos.
    
    2. Vaya al nombre de SharePoint y haga clic con el botón secundario. por ejemplo, **contoso \ \<SharePoint Document Folder Name\> **.
    
    3. Seleccione **liberar espacio**.
    
    4. La columna Estado mostrará el estado de archivos y carpetas. Para obtener más información, vea <a href="https://support.microsoft.com/office/sync-sharepoint-files-with-the-onedrive-sync-client-groove-exe-59b1de2b-519e-4d3a-8f45-51647cf291cd" target="_blank"> sincronizar archivos de SharePoint con el cliente de sincronización de OneDrive </a> .
    
6. Los archivos de canales de equipos se almacenan en sitios de SharePoint, con todas las mismas funciones de documento de SharePoint, incluido el historial de versiones y la sincronización con dispositivos de escritorio locales. Para sincronizar los archivos de canal:

    1. Navegue hasta el canal de interés de los equipos y seleccione la pestaña **archivos** en la parte superior. Después, seleccione **sincronizar**. Los archivos comenzarán a sincronizarse y se verán en el explorador de archivos en el **escritorio \ contoso \ \<name of the Teams Channel\> **.
    
    2. Use el mismo procedimiento que usó para sincronizar los sitios de SharePoint para mantener los archivos en la nube y descargarlos solo cuando los use, pulse y mantenga presionado o haga clic con el botón derecho en el explorador de archivos en el nombre de canal de Teams y, a continuación, seleccione **liberar espacio**.

## Configuración del lápiz de Surface Hub

**Emparejar el lápiz de Surface Hub de Bluetooth**

Emparejar el lápiz para mantener actualizado el firmware del lápiz y obtener la información de carga de la batería en la página de configuración del dispositivo Bluetooth o en la aplicación de Surface:

1. Seleccione **Start**  >  **Settings**  >  **Devices**.

2. Seleccione **Agregar Bluetooth u otro dispositivo**.

3. Elija **Bluetooth**.

4. Quite el botón cola de pluma y agite para desconectar la conexión de la batería.

5. Vuelva a colocar el tapón y mantenga presionado el tapón hasta que el LED de emparejamiento parpadee.

6. En la configuración de Bluetooth Surface Hub, seleccione **lápiz de Surface Hub 2**.

7. Complete la operación de emparejamiento. 

8. Si el emparejamiento no se realiza correctamente, puede intentar volver a emparejar el lápiz. Si esto no funciona, puede comprobar si la batería se cobra comprobando que el lápiz funciona en la aplicación de pizarra. En caso contrario, reemplace la batería y, a continuación, intente volver a emparejar la pluma. Si es necesario, reinicie el dispositivo e inténtelo de nuevo.

**Establecer accesos directos del lápiz** El lápiz del Surface Hub tiene un botón de método abreviado al que a veces se hace referencia como "hacer clic". Para configurar los accesos directos debe emparejar primero el lápiz, como se ha descrito anteriormente.

1. Busque el lápiz y seleccione **pluma & la configuración de Windows Ink**.

2. Cerca de la parte inferior de la página, seleccione los accesos directos del lápiz que abre el cuadro de diálogo, que se muestra aquí:

   ![Accesos directos de lápiz](images/sh2-pen-shortcuts.png)

## Configuración de la cámara

Puede montar la cámara en la parte superior o en cualquiera de los lados del dispositivo. Monte la cámara en una posición para optimizar el ángulo de la cámara si está usando el Hub con un soporte de escritorio en lugar de un carrito o está cerca del concentrador. La cámara no gira automáticamente, por lo que debe tener una clave hexadecimal 2mm para girar la cámara de forma manual. 

Para obtener más información sobre cómo montar la cámara y girar la cámara de forma manual, consulte <a href="https://support.microsoft.com/help/4509729/surface-hub-2s-camera-lens-orientation" target="_blank"> Surface Hub 2s orientación de lente de la cámara </a> .

## Configuración de Windows Hello

Surface Hub 2S si se ejecuta Windows 10 Enterprise, se permite el conjunto completo de aplicaciones de escritorio Win32, así como las opciones de Windows Hello biométricas. El accesorio de lector de huellas dactilares Surface Hub 2 se puede conectar a cualquier puerto USB-C del dispositivo. 

Para solicitar un lector de huellas dactilares Surface Hub 2 o para ver especificaciones técnicas, consulta (surface-hub-2-essential-add-ons.md "target =" _blank ">complementos esenciales para Windows 10 Pro y Enterprise en Surface Hub 2 </a> . 

Después de insertar el lector Fingerprint Reader, seleccione **Start**  >  **Settings**  >  **accounts**  >  **Sign-in Options**  >  **huellator de Windows Hello** para inscribir su huella dactilar.

Usar un dispositivo certificado de Windows Hello para un reconocimiento facial. La cámara Surface Hub 2S no admite el reconocimiento facial de Windows Hello.

## Habilitar un icono de método abreviado de pantalla de bloqueo en la barra de tareas

Para agregar un icono a la barra de tareas que permita un único toque de pantalla similar al método abreviado de teclado Windows-L: 

1.  Puntee y mantenga presionado o haga clic con el botón derecho en el escritorio, seleccione **nuevo**  >  **método abreviado**  >  **examinar**  >  **escritorio**  >  **Aceptar**  >  **Next**.

1.  Escriba un nombre para el acceso directo, como **bloquear mi PC**y, a continuación, seleccione **Finalizar**.

1.  Haga clic con el botón secundario del ratón o mantenga pulsado el acceso directo recién creado en el escritorio y seleccione **propiedades**. En la pestaña **acceso directo** , escriba lo siguiente en el campo de **destino** : **Rundll32.exe User32.dll, LockWorkStation**

1.  Seleccione el botón **Cambiar icono** y vaya a **C:\Windows\System32\imageres.dll** y seleccione el icono que quiera usar. 

    Observa el siguiente ejemplo:

    ![Elegir un icono](images/lock.png)
    
1.  Seleccione **Aceptar** para guardar el método abreviado.

1.  Haga clic con el botón derecho o mantenga presionado el acceso directo y seleccione **anclar a la barra de tareas**.

1. Una vez que haya anclado el acceso directo de bloqueo a la barra de tareas, puede eliminarlo del escritorio.

## Aplicaciones

### Actualizar las aplicaciones instaladas

Para actualizar todas las aplicaciones de la tienda instaladas:

1. Abra la aplicación Microsoft Store y seleccione **Ver más** puntos suspensivos en la esquina superior derecha.

2. Seleccione **Descargas y actualizaciones**.

2. Seleccione **Obtener actualizaciones**.

### Microsoft Whiteboard

Para instalar la pizarra de Microsoft:

 - Seleccione el icono **área de trabajo de Windows Ink** en la esquina inferior derecha de la barra de tareas y descargar **pizarra**.
 
   ![Área de trabajo de tinta](images/ink.png) 

Como alternativa, puede instalar whiteboard desde Microsoft Store:

1. Abra la aplicación Microsoft Store y busque **pizarra**.

2. Elija **no gracias** para iniciar sesión y usar en todos los dispositivos.

3. Anclar pizarra a la barra de tareas.

### Aplicación Surface

1. En Microsoft Store, busque **Surface**.

2. Establezca el filtro **disponible en en** **todos los dispositivos**.

3. Instala la aplicación **Surface** . Debe ser la primera aplicación de la lista. Es posible que necesites asociar tu MSA a la tienda para instalar la aplicación.

4. Ancla la aplicación de **Surface** a la barra de tareas.

### Recorte y anotación

1. Abra el **recorte &** aplicación de boceto y ancle la barra de tareas.

2. Seleccione los puntos suspensivos en la esquina superior derecha y, a continuación, seleccione **configuración**.

3. En **configuración**, Active **copiar automáticamente en el portapapeles**, **Guardar recortes**y **varias ventanas** (opcional).

### Microsoft Office

1. Abra el <a href="https://portal.office.com/account#installs" target="_blank"> portal de Office </a> e instale las aplicaciones que desee.

2. Anclar las aplicaciones de Office que desee a la barra de tareas.

3. Si Outlook está instalado, asegúrese de establecer el OST de Outlook para que solo se guarden las últimas dos semanas de caché. Esto disminuirá en gran medida el uso del disco y el tiempo de configuración.

    - Seleccione **File**  >  **configuración** de la cuenta de archivo y seleccione su cuenta.
    
    - Seleccione **cambiar** y el control deslizante para **usar el modo caché de Exchange** en 14 días.

### Microsoft Teams

1. Descargue e instale <a href="https://teams.microsoft.com/downloads" target="_blank"> Microsoft Teams </a> .

2. Establecer la configuración para la aplicación de inicio automático (opcional).

3. Anclar equipos a la barra de tareas.

4. Considere la posibilidad de reducir las notificaciones de Teams en el dispositivo para evitar distracciones (opcional).

   ![Notificaciones de Teams](images/teams.png)

### Conectar aplicación

> [!IMPORTANT]
> En Windows 10, versión 2004 y posteriores, la aplicación de conexión para proyección inalámbrica con Miracast no está instalada de forma predeterminada, pero está disponible como una característica opcional. Si ha instalado (o actualizado a) Windows versión 2004 o posterior, es posible que vea lo siguiente en la pantalla proyectar en este equipo en configuración:

![Proyectar a este equipo](images/sh2-project.png) 


1. Para instalar la aplicación desde la página de configuración "proyectar en este equipo", selecciona **características opcionales**  >  **agrega una característica** y luego instala la aplicación de **visualización inalámbrica** .

2. En **algunos dispositivos con Windows y Android puede proyectar en este equipo cuando lo digas correctamente**, elija:

    - **Disponible en todas partes** si el dispositivo no está en una red corporativa.
    - En caso contrario, elija **disponible en todas partes en redes seguras**.
    
3. En **preguntar al proyecto en este equipo**, seleccione **solo la primera vez**.

4. En **requerir PIN para el emparejamiento**, elija **nunca**.

5. Para iniciar la aplicación y anclarla en la barra de tareas, busque **Connect**.

6. Abra la aplicación. Mientras la aplicación está abierta, haga clic con el botón derecho en el icono de la aplicación conectar en la barra de tareas y seleccione **anclar a la barra de tareas**.

7. Después, cierre la aplicación Connect. Es posible que el **proyecto a este equipo** no funcione a menos que se haya ejecutado la aplicación al menos una vez.

Configuración recomendada cuando no se encuentra en la red corporativa:

![Configuración en casa](images/project1.png)

Configuración recomendada en la red corporativa:

![Configuración en el trabajo](images/project2.png)

### Tu Teléfono

La aplicación de **tu teléfono** se instala de forma predeterminada en Windows 10. Si no está presente, también puede instalarlo desde la tienda Windows.

Para obtener información sobre cómo configurar la aplicación, vea <a href="https://www.windowscentral.com/how-set-your-phone-windows-10" target="_blank"> Cómo configurar el teléfono en Windows 10 y cómo sincronizar datos entre su equipo y su teléfono </a> . Además, consulta <a href="https://www.windowscentral.com/how-fix-common-problems-your-phone-app-windows-10" target="_blank"> cómo solucionar problemas comunes con tu aplicación de teléfono en Windows 10 </a> .

### Zonas súper sofisticadas

Las **zonas súper sofisticadas** ayudan a los usuarios a organizar las ventanas para maximizar el espacio de la pantalla. Ahora se incluye en <a href="https://github.com/microsoft/PowerToys/releases" target="_blank"> PowerToys </a> en github.

### Explorador de cromo de cromo

Descarga e instala el nuevo <a href="https://www.microsoft.com/en-us/edge?form=MY01BL&OCID=MY01BL" target="_blank"> navegador Edge de cromo </a> .


### Herramienta de diagnóstico de hardware Surface Hub

La <a href="https://www.microsoft.com/p/surface-hub-hardware-diagnostic/9nblggh51f2g" target="_blank"> herramienta de diagnóstico de hardware de Surface Hub </a> está disponible gratuitamente en Microsoft Store. La herramienta está diseñada para ayudarte a asegurarte de que Surface Hub funcione de la mejor manera posible. Contiene pruebas para determinar si el firmware está actualizado y configurado correctamente. Las pruebas interactivas permiten confirmar que la funcionalidad esencial funciona según lo esperado. Si surgen problemas, los resultados se pueden guardar y compartir con el equipo de soporte técnico de SurfaceHub. Haga clic en el vínculo para instalarlo desde Microsoft Store y, a continuación, ancle la aplicación a la barra de tareas.

## Configuración adicional

### Cola de plumas Seleccione para iniciar pizarra

1. Busque el **lápiz** y seleccione **pluma & la configuración de Windows Ink**.

2. Cerca de la parte inferior de la página, en **accesos directos de lápiz** , **Seleccione una vez** para la **pizarra de Microsoft**. 

### Administración de energía

Hay varias opciones de configuración de energía disponibles para obtener la mejor experiencia con Windows 10 Pro o Enterprise en Surface Hub 2. Esto incluye tiempos de espera de pantalla y equipo y cómo interactúan con la detección de presencia humana integrada (Doppler), el protector de pantalla y la protección con contraseña y, si es adecuado, cómo pasar la configuración de energía de la Directiva de grupo para usuarios de equipos portátiles o de escritorio.

Windows 10 Pro o Enterprise en Surface Hub 2 evita que la pantalla pase de la pantalla a la entrada táctil, el mouse y el teclado, así como la detección de la ocupación de la ocupación integrada (Doppler). La detección de la ocupación de los seres humanos está habilitada de forma predeterminada, pero si se desea, se puede deshabilitar en UEFI al alternar la opción dispositivo en la herramienta de configuración de Surface UEFI, ya sea como parte de la migración inicial o mediante la creación y aplicación de un paquete de configuración UEFI posterior. 

**Administración de energía: configuración de suspensión de pantalla y PC**

1. Seleccione **Start**  >  **Settings**  >  **System**  >  **Power & Sleep**.

2. Configure el control deslizante de modo de energía para **obtener el mejor rendimiento**.

3. Configure valores de pantalla y de espera para su preferencia, así como para la detección de presencia de Doppler que reactiva el dispositivo cuando se detecta movimiento. Como práctica recomendada, se recomienda configurar la pantalla para que se apague **después de dos horas** y el equipo **apagado después de 4 horas.**

**Administración de energía: protector de pantalla**

1. Busque **pantalla de bloqueo** y Abra **configuración de pantalla de bloqueo**.

2. Configure la configuración del **protector de pantalla** y la **configuración del tiempo de espera de pantalla** para sus preferencias. Los valores predeterminados recomendados son:

   - Protector de pantalla a (ninguno) o un protector de pantalla de su elección.
   - Tiempo de espera de 15 minutos.
   - En reanudar, Mostrar la pantalla de inicio de sesión.


**Administración de energía: Directiva de grupo**

Antes de realizar el procedimiento siguiente, consulte con el Departamento de TI para obtener una aprobación para excluir un dispositivo Surface Hub 2S de la Directiva de administración global de energía. Algunas configuraciones de administración de energía pueden deshabilitar la función de detección de presencia.

1. Busque **software Center** y ábralo.

2. Seleccione **Opciones**.

3. Expanda la **Administración de energía**  y seleccione no aplicar la **configuración de energía de mi departamento de ti a este equipo**.

   ![Configuración de software](images/soft-cntr.png)

### Sensor de almacenamiento

Surface Hub 2 tiene un SSD de 128 GB para almacenamiento local, por lo que es necesario considerar el uso de las medidas de almacenamiento de almacenamiento durante el uso normal.  Para configurar el sensor de almacenamiento:

1.  Busque la **configuración de almacenamiento**, que se encuentra en **configuración del sistema**.

2.  En **configuración**, seleccione **Activar sensor de almacenamiento** para abrir la página Configuración de **almacenamiento** .

3.  Activar el sentido **de**almacenamiento.

4.  Seleccione **configurar sensor de almacenamiento o ejecutarlo ahora** y configure las opciones para mantener los archivos en línea todo lo posible (debido a un espacio en disco limitado).

Configuración recomendada:

- Ejecutar sensor de almacenamiento = todos los días.
- Elimine los archivos temporales que mis aplicaciones no usan = cada 14 días (al menos).
- Eliminar archivos de mi carpeta de descargas si ya lo han recibido durante más de = 30 días.
- OneDrive: el contenido se volverá a estar en línea si no se abre durante más de = 30 días.

### Modo tableta

Activa el modo tableta si así lo deseas.


### Configuración de sonido

1. Busque la **configuración de sonidos** y abra esta página.

2. Seleccione **Panel de control de sonido** a la derecha y seleccione la pestaña **sonidos** .

3. En **eventos de programa** , establezca **Conectar dispositivo** y **desconectar dispositivo** a **ninguno**.

### Notificaciones de silencio

1. Busque el **Asistente de concentración** y abra esta página.

2. Seleccione **solo alarmas**. Esto evitará controles flotantes de notificaciones constantes.

### Liberador de espacio en disco

1. Busque el **liberador de espacio en disco** y abra esta aplicación.

2. En **archivos para eliminar**, seleccione los archivos que desea eliminar. 

3. Seleccione **limpiar archivos de sistema**.

## Completar y comprobar

1. Busque e instale todas las actualizaciones de Windows.

2. Actualizar la Directiva de grupo

   1. En un símbolo del sistema con privilegios elevados, escriba **gpupdate/force/boot/wait: 0**.
   
3. Reinicia el dispositivo.

4. Comprobar las aplicaciones de la barra de tareas.

   - Conectar aplicación
   - Icono de candado
   - Recorte y anotación
   - Teams (si corresponde)
   - Aplicaciones de Office (si corresponde)
   - Aplicación Surface
   - Pizarra
    
5. Comprobar la detección de presencia.

   - La detección de presencia será un icono verde en la bandeja del sistema.
    
6. Comprobar que los proyectos se han habilitado con la aplicación Connect. Después de configurar  **Project en esta** configuración de equipo, ejecute la aplicación Connect al menos una vez. (Posteriormente, no es necesario que la aplicación Connect se esté ejecutando para proyectar en Surface hub).

7. Comprobar la configuración de energía y suspensión.

    - Protector de pantalla: 15 minutos, establecido en (ninguno), de formas o en blanco; Asegúrese de que la casilla requerir contraseña está seleccionada.
    - Pantalla: **apague después de 2 horas**.
    - PC:  **apagar después de 4 horas**.
    
8. Compruebe que Windows Hello está funcionando.

9. Comprobar la sincronización la configuración está deshabilitada.

10. Comprobar las aplicaciones de inicio.

> [!TIP]
> Después de instalar y configurar Windows 10, Surface Hub 2S se puede administrar como cualquier otro dispositivo de Windows 10.

## Temas relacionados

<a href="surface-hub-2s-migrate-os.md" target="_blank"> Migrar a Windows 10 Pro o Enterprise en Surface Hub 2</a>
