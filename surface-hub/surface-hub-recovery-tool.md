---
title: Uso de la herramienta de recuperación de Surface Hub
description: Cómo usar la Herramienta de recuperación de Surface Hub para volver a crear una imagen del SSD.
ms.assetid: FDB6182C-1211-4A92-A930-6C106BCD5DC1
ms.reviewer: ''
manager: laurawi
keywords: administrar Surface Hub
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 12/18/2020
ms.localizationpriority: medium
ms.openlocfilehash: 9df9de731ac5c8f8acb393db3d4b16e9d1c98a9e
ms.sourcegitcommit: 5cfac94c220c8a8d4620c6a7fa75ae2fae089c7f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312036"
---
# <span data-ttu-id="8d970-104">Uso de la herramienta de recuperación de Surface Hub</span><span class="sxs-lookup"><span data-stu-id="8d970-104">Using the Surface Hub Recovery Tool</span></span>

<span data-ttu-id="8d970-105">La Herramienta de recuperación de [Microsoft Surface Hub](https://www.microsoft.com/download/details.aspx?id=52210) te ayuda a volver a crear una imagen de la unidad de estado sólido (SSD) de Surface Hub con un dispositivo de escritorio Windows 10, sin llamar al soporte técnico ni reemplazar el SSD.</span><span class="sxs-lookup"><span data-stu-id="8d970-105">The [Microsoft Surface Hub Recovery Tool](https://www.microsoft.com/download/details.aspx?id=52210) helps you re-image your Surface Hub Solid State Drive (SSD) using a Windows 10 desktop device, without calling support or replacing the SSD.</span></span> <span data-ttu-id="8d970-106">Con esta herramienta, puedes volver a crear una imagen de un SSD que tenga una contraseña de administrador desconocida, errores de arranque, no haya podido completar una recuperación en la nube o para un dispositivo que tenga una versión anterior del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8d970-106">With this tool, you can reimage an SSD that has an unknown Administrator password, boot errors, was unable to complete a cloud recovery, or for a device that has an older version of the operating system.</span></span> <span data-ttu-id="8d970-107">La herramienta no corregirá los SSD físicamente dañados.</span><span class="sxs-lookup"><span data-stu-id="8d970-107">The tool will not fix physically damaged SSDs.</span></span>

<span data-ttu-id="8d970-108">Para volver a crear una imagen de la SSD de Surface Hub con la Herramienta de recuperación, tendrás que quitar el SSD de Surface Hub, conectar la unidad al cable USB a SATA y, a continuación, conectar el cable al equipo de escritorio en el que está instalada la herramienta de recuperación.</span><span class="sxs-lookup"><span data-stu-id="8d970-108">To re-image the Surface Hub SSD using the Recovery Tool, you'll need to remove the SSD from the Surface Hub, connect the drive to the USB-to-SATA cable, and then connect the cable to the desktop PC on which the Recovery Tool is installed.</span></span> <span data-ttu-id="8d970-109">Para obtener más información sobre cómo quitar la unidad existente de Surface Hub, consulta reemplazo de [SSD de Surface Hub.](surface-hub-ssd-replacement.md)</span><span class="sxs-lookup"><span data-stu-id="8d970-109">For more information on how to remove the existing drive from your Surface Hub, see [Surface Hub SSD replacement](surface-hub-ssd-replacement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d970-110">No deje que el dispositivo se ponga en modo de suspensión ni interrumpa la descarga del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="8d970-110">Do not let the device go to sleep or interrupt the download of the image file.</span></span>

<span data-ttu-id="8d970-111">Si la herramienta no consigue restablecer la unidad, ponte en contacto con el soporte [técnico de Surface Hub.](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support)</span><span class="sxs-lookup"><span data-stu-id="8d970-111">If the tool is unsuccessful in reimaging your drive, please contact [Surface Hub Support](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support).</span></span>

## <span data-ttu-id="8d970-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8d970-112">Prerequisites</span></span>

### <span data-ttu-id="8d970-113">Mandatory</span><span class="sxs-lookup"><span data-stu-id="8d970-113">Mandatory</span></span>

- <span data-ttu-id="8d970-114">Equipo host que ejecuta la versión de 64 bits de Windows 10, versión 1607 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8d970-114">Host PC running 64-bit version of Windows 10, version 1607 or higher.</span></span>
- <span data-ttu-id="8d970-115">Acceso a Internet</span><span class="sxs-lookup"><span data-stu-id="8d970-115">Internet access</span></span>
- <span data-ttu-id="8d970-116">Puerto USB 2.0 abierto o posterior</span><span class="sxs-lookup"><span data-stu-id="8d970-116">Open USB 2.0 or greater port</span></span>
- <span data-ttu-id="8d970-117">Cable USB a SATA</span><span class="sxs-lookup"><span data-stu-id="8d970-117">USB-to-SATA cable</span></span>
- <span data-ttu-id="8d970-118">10 GB de espacio libre en disco en el equipo host</span><span class="sxs-lookup"><span data-stu-id="8d970-118">10 GB of free disk space on the host computer</span></span>
- <span data-ttu-id="8d970-119">Ssd que se suministran con Surface Hub o un SSD proporcionado por el soporte técnico como reemplazo.</span><span class="sxs-lookup"><span data-stu-id="8d970-119">SSDs shipped with Surface Hub or a SSD provided by Support as a replacement.</span></span> <span data-ttu-id="8d970-120">Los SSD no proporcionados por Microsoft no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8d970-120">SSDs not supplied by Microsoft are not supported.</span></span>

### <span data-ttu-id="8d970-121">Recomendaciones</span><span class="sxs-lookup"><span data-stu-id="8d970-121">Recommended</span></span>

- <span data-ttu-id="8d970-122">Conexión a Internet de alta velocidad</span><span class="sxs-lookup"><span data-stu-id="8d970-122">High-speed Internet connection</span></span>
- <span data-ttu-id="8d970-123">Puerto USB 3.0 abierto</span><span class="sxs-lookup"><span data-stu-id="8d970-123">Open USB 3.0 port</span></span>
- <span data-ttu-id="8d970-124">Cable USB 3.0 o superior de USB a SATA</span><span class="sxs-lookup"><span data-stu-id="8d970-124">USB 3.0 or higher USB-to-SATA cable</span></span>
- <span data-ttu-id="8d970-125">La herramienta de creación de imágenes se probó con la siguiente creación y modelo de cables:</span><span class="sxs-lookup"><span data-stu-id="8d970-125">The imaging tool was tested with the following make and model of cables:</span></span>
    - <span data-ttu-id="8d970-126">Startech USB312SAT3CB</span><span class="sxs-lookup"><span data-stu-id="8d970-126">Startech USB312SAT3CB</span></span>
    - <span data-ttu-id="8d970-127">Rosawill RCUC16001</span><span class="sxs-lookup"><span data-stu-id="8d970-127">Rosewill RCUC16001</span></span>
    - <span data-ttu-id="8d970-128">Ugreen 20231</span><span class="sxs-lookup"><span data-stu-id="8d970-128">Ugreen 20231</span></span>

## <span data-ttu-id="8d970-129">Descargar la Herramienta de recuperación de Surface Hub</span><span class="sxs-lookup"><span data-stu-id="8d970-129">Download Surface Hub Recovery Tool</span></span>

<span data-ttu-id="8d970-130">La Herramienta de recuperación de Surface Hub está disponible para su descarga desde herramientas [de Surface Hub](https://www.microsoft.com/download/details.aspx?id=52210) para TI en el nombre de archivo \*\*SurfaceHub_Recovery_v2.0.139.0.msi. \*\*</span><span class="sxs-lookup"><span data-stu-id="8d970-130">Surface Hub Recovery Tool is available for download from [Surface Hub Tools for IT](https://www.microsoft.com/download/details.aspx?id=52210)  under the file name **SurfaceHub_Recovery_v2.0.139.0.msi**.</span></span>

<span data-ttu-id="8d970-131">Para iniciar la descarga, haga **clic en Descargar**, elija **SurfaceHub_Recovery_v2.0.139.0.msi** de la lista y haga clic en **Siguiente.**</span><span class="sxs-lookup"><span data-stu-id="8d970-131">To start the download, click **Download**, choose **SurfaceHub_Recovery_v2.0.139.0.msi** from the list, and click **Next**.</span></span> <span data-ttu-id="8d970-132">En la ventana emergente, elija una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8d970-132">From the pop-up, choose one of the following:</span></span>

- <span data-ttu-id="8d970-133">Haga **clic en Ejecutar** para iniciar la instalación inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8d970-133">Click **Run** to start the installation immediately.</span></span>
- <span data-ttu-id="8d970-134">Haga **clic en** Guardar para copiar la descarga en el equipo para su instalación posterior.</span><span class="sxs-lookup"><span data-stu-id="8d970-134">Click **Save** to copy the download to your computer for later installation.</span></span>

<span data-ttu-id="8d970-135">Instala la Herramienta de recuperación de Surface Hub en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="8d970-135">Install Surface Hub Recovery Tool on the host PC.</span></span>

## <span data-ttu-id="8d970-136">Ejecutar la herramienta de recuperación de Surface Hub</span><span class="sxs-lookup"><span data-stu-id="8d970-136">Run Surface Hub Recovery Tool</span></span>

1. <span data-ttu-id="8d970-137">En el equipo host, selecciona el botón Inicio, desplázate por la lista alfabética de la izquierda y selecciona el acceso directo de la herramienta de recuperación. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d970-137">On the host PC, select the **Start** button, scroll through the alphabetical list on the left, and select the recovery tool shortcut.</span></span>

    ![Acceso directo de la Herramienta de recuperación de Microsoft Surface Hub](images/shrt-shortcut.png)

2. <span data-ttu-id="8d970-139">Haz clic en **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="8d970-139">Click **Start**.</span></span>

    ![Botón Inicio de la herramienta de recuperación](images/shrt-start.png)


3. <span data-ttu-id="8d970-141">En la **ventana Guía,** haga clic **en Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="8d970-141">In the **Guidance** window, click **Next**.</span></span>

    ![No dejar que la máquina vaya a la guía de suspensión](images/shrt-guidance.png)

4. <span data-ttu-id="8d970-143">En la ventana Seleccionar imagen, haga clic en **RS2** o en su **sucesora 20H2,** seleccione Continuar **y,** a continuación, **seleccione Descargar imagen.**</span><span class="sxs-lookup"><span data-stu-id="8d970-143">In the Select image window, click either **RS2** or its successor **20H2**, select **Continue,** and then select **Download image.**</span></span>

     <span data-ttu-id="8d970-144">![Imagen de descarga de la herramienta de ](images/shrt-select-image.png) ![ recuperación de la herramienta de recuperación de la selección de la herramienta de recuperación de la](images/shrt-download-image.png)</span><span class="sxs-lookup"><span data-stu-id="8d970-144">![Recovery Tool Select image](images/shrt-select-image.png) ![Recovery Tool Download image](images/shrt-download-image.png)</span></span>

5. <span data-ttu-id="8d970-145">El tiempo para descargar la imagen de recuperación depende de las velocidades de conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="8d970-145">Time to download the recovery image is dependent on internet connection speeds.</span></span> <span data-ttu-id="8d970-146">En una conexión corporativa promedio, puede tardar hasta una hora descargar el archivo de imagen de 8 GB.</span><span class="sxs-lookup"><span data-stu-id="8d970-146">On an average corporate connection, it can take up to an hour to download the 8GB image file.</span></span>

    ![Descargar imagen](images/shrt-download.png)



5. <span data-ttu-id="8d970-148">Una vez completada la descarga, la herramienta te indica que conectes una unidad SSD.</span><span class="sxs-lookup"><span data-stu-id="8d970-148">When the download is complete, the tool instructs you to connect an SSD drive.</span></span> <span data-ttu-id="8d970-149">Si la herramienta no puede encontrar la unidad conectada, es muy posible que el cable que se usa no notifique el nombre del SSD a Windows.</span><span class="sxs-lookup"><span data-stu-id="8d970-149">If the tool is unable to locate the attached drive, there is a good chance that the cable being used is not reporting the name of the SSD to Windows.</span></span>  <span data-ttu-id="8d970-150">La herramienta de creación de imágenes debe encontrar el nombre de la unidad como "Dispositivo USB LITEON L CH-128V2S" para poder continuar.</span><span class="sxs-lookup"><span data-stu-id="8d970-150">The imaging tool must find the name of the drive as "LITEON L CH-128V2S USB Device" before it can continue.</span></span>  <span data-ttu-id="8d970-151">Para obtener más información sobre cómo quitar la unidad existente de Surface Hub, consulta reemplazo de [SSD de Surface Hub.](surface-hub-ssd-replacement.md)</span><span class="sxs-lookup"><span data-stu-id="8d970-151">For more information on how to remove the existing drive from your Surface Hub, see [Surface Hub SSD replacement](surface-hub-ssd-replacement.md).</span></span>

    ![Connect SSD](images/shrt-drive.png)

6. <span data-ttu-id="8d970-153">Cuando se reconozca la unidad, haz clic en **Inicio** para comenzar el proceso de creación de imágenes de nuevo.</span><span class="sxs-lookup"><span data-stu-id="8d970-153">When the drive is recognized, click **Start** to begin the re-imaging process.</span></span> <span data-ttu-id="8d970-154">En la advertencia de que se borrarán todos los datos de la unidad, haga clic en **Aceptar.**</span><span class="sxs-lookup"><span data-stu-id="8d970-154">On the warning that all data on the drive will be erased, click **OK**.</span></span>



    <span data-ttu-id="8d970-155">Antes de aplicar la imagen del sistema a la unidad, el SSD se vuelve a particionar y formatear.</span><span class="sxs-lookup"><span data-stu-id="8d970-155">Prior to applying the system image to the drive, the SSD is repartitioned and formatted.</span></span> <span data-ttu-id="8d970-156">La copia de los archivos binarios del sistema llevará aproximadamente 30 minutos, pero puede tardar más en función de la velocidad del bus USB, el cable que se usa o el software antivirus instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8d970-156">Copying the system binaries will take approximately 30 minutes, but can take longer depending on the speed of your USB bus, the cable being used, or antivirus software installed on your system.</span></span>



## <span data-ttu-id="8d970-157">Solución de problemas y problemas comunes</span><span class="sxs-lookup"><span data-stu-id="8d970-157">Troubleshooting and common problems</span></span>

<span data-ttu-id="8d970-158">Problema</span><span class="sxs-lookup"><span data-stu-id="8d970-158">Issue</span></span> | <span data-ttu-id="8d970-159">Notas</span><span class="sxs-lookup"><span data-stu-id="8d970-159">Notes</span></span>
--- | ---
<span data-ttu-id="8d970-160">La herramienta no puede crear una imagen del SSD</span><span class="sxs-lookup"><span data-stu-id="8d970-160">The tool fails to image the SSD</span></span> | <span data-ttu-id="8d970-161">Asegúrate de que estás usando un SSD suministrado por fábrica y uno de los cables probados.</span><span class="sxs-lookup"><span data-stu-id="8d970-161">Make sure you are using a factory-supplied SSD and one of the tested cables.</span></span>
<span data-ttu-id="8d970-162">The reimaging process appears halted/frozen</span><span class="sxs-lookup"><span data-stu-id="8d970-162">The reimaging process appears halted/frozen</span></span> | <span data-ttu-id="8d970-163">Es seguro cerrar y reiniciar la herramienta de recuperación de Surface Hub sin ningún efecto negativo en el SSD.</span><span class="sxs-lookup"><span data-stu-id="8d970-163">It is safe to close and restart the Surface Hub Recovery Tool with no ill effect to the SSD.</span></span>
<span data-ttu-id="8d970-164">La herramienta no reconoce la unidad</span><span class="sxs-lookup"><span data-stu-id="8d970-164">The drive isn’t recognized by the tool</span></span> | <span data-ttu-id="8d970-165">Comprueba que el SSD de Surface Hub se enumeró como una Lite-On, "LiteON L CH-128V2S USB Device".</span><span class="sxs-lookup"><span data-stu-id="8d970-165">Verify that the Surface Hub SSD is enumerated as a Lite-On drive, "LITEON L CH-128V2S USB Device".</span></span>  <span data-ttu-id="8d970-166">Si la unidad se reconoce como otro dispositivo con nombre, el cable actual no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8d970-166">If the drive is recognized as another named device, your current cable isn’t compatible.</span></span> <span data-ttu-id="8d970-167">Pruebe otro cable o uno de los cable probados enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8d970-167">Try another cable or one of the tested cable listed above.</span></span>
<span data-ttu-id="8d970-168">Error: -2147024809</span><span class="sxs-lookup"><span data-stu-id="8d970-168">Error: -2147024809</span></span> | <span data-ttu-id="8d970-169">Abre el Administrador de discos y quita las particiones de la unidad de Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="8d970-169">Open Disk Manager and remove the partitions on the Surface Hub drive.</span></span>  <span data-ttu-id="8d970-170">Desconecte y vuelva a conectar la unidad al equipo host.</span><span class="sxs-lookup"><span data-stu-id="8d970-170">Disconnect and reconnect the drive to the host machine.</span></span> <span data-ttu-id="8d970-171">Reinicia la herramienta de creación de imágenes de nuevo.</span><span class="sxs-lookup"><span data-stu-id="8d970-171">Restart the imaging tool again.</span></span>

<span data-ttu-id="8d970-172">Si la herramienta no consigue restablecer la unidad, ponte en contacto con el soporte [técnico de Surface Hub.](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support)</span><span class="sxs-lookup"><span data-stu-id="8d970-172">If the tool is unsuccessful in reimaging your drive, please contact [Surface Hub Support](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support).</span></span>

## <span data-ttu-id="8d970-173">Historial de versiones</span><span class="sxs-lookup"><span data-stu-id="8d970-173">Version history</span></span>

### <span data-ttu-id="8d970-174">Versión v2.0.139.0</span><span class="sxs-lookup"><span data-stu-id="8d970-174">Version v2.0.139.0</span></span>

*<span data-ttu-id="8d970-175">Fecha de lanzamiento: 18 de diciembre de 2020</span><span class="sxs-lookup"><span data-stu-id="8d970-175">Release date: December 18, 2020</span></span>*<br>
<span data-ttu-id="8d970-176">Esta versión de la Herramienta de recuperación de Surface Hub agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8d970-176">This version of Surface Hub Recovery Tool adds support for the following:</span></span>
- <span data-ttu-id="8d970-177">Actualización para admitir Windows 10 Team 2020 Update (20H2)</span><span class="sxs-lookup"><span data-stu-id="8d970-177">Update to support Windows 10 Team 2020 Update (20H2)</span></span>
- <span data-ttu-id="8d970-178">Mejoras en la experiencia del usuario</span><span class="sxs-lookup"><span data-stu-id="8d970-178">User experience improvements</span></span>
- <span data-ttu-id="8d970-179">Cambios en la arquitectura</span><span class="sxs-lookup"><span data-stu-id="8d970-179">Architectural changes</span></span>
- <span data-ttu-id="8d970-180">Adiciones de telemetría</span><span class="sxs-lookup"><span data-stu-id="8d970-180">Telemetry additions</span></span>

