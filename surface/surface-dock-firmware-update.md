---
title: 'Actualización del firmware Microsoft Surface Dock: información técnica para administradores de ti'
description: En este artículo se explica cómo usar la actualización de firmware Microsoft Surface Dock para actualizar el firmware de Surface Docking. Cuando se instale en tu dispositivo Surface, se actualizará cualquier muelle de superficie conectado al dispositivo Surface.
ms.localizationpriority: medium
ms.prod: w10
ms.mktglfcycl: manage
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
ms.topic: article
ms.reviewer: scottmca
manager: laurawi
ms.audience: itpro
ms.openlocfilehash: aab4c67a6a262b11cd5982ebe145afbddfeaa1c9
ms.sourcegitcommit: 109d1d7608ac4667564fa5369e8722e569b8ea36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/27/2020
ms.locfileid: "10834633"
---
# <span data-ttu-id="355a6-104">Actualización del firmware Microsoft Surface Dock: información técnica para administradores de ti</span><span class="sxs-lookup"><span data-stu-id="355a6-104">Microsoft Surface Dock Firmware Update: Technical information for IT administrators</span></span>

> [!IMPORTANT]
> <span data-ttu-id="355a6-105">Este artículo contiene instrucciones técnicas para los administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="355a6-105">This article contains technical instructions for IT administrators.</span></span> <span data-ttu-id="355a6-106">Si es un usuario doméstico, consulte [Cómo actualizar el firmware de Surface docking](https://support.microsoft.com/help/4023478/surface-update-your-surface-dock)   en el sitio de soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="355a6-106">If you are a home user, please see [How to update your Surface Dock Firmware](https://support.microsoft.com/help/4023478/surface-update-your-surface-dock) on the Microsoft Support site.</span></span> <span data-ttu-id="355a6-107">Las instrucciones del sitio de asistencia son las mismas que se describen a continuación, pero en este artículo encontrará información adicional para supervisar, comprobar e implementar la actualización en varios dispositivos en una red.</span><span class="sxs-lookup"><span data-stu-id="355a6-107">The instructions at the support site are the same as the general installation steps below, but this article has additional information for monitoring, verifying, and deploying the update to multiple devices on a network.</span></span>

<span data-ttu-id="355a6-108">En este artículo se explica cómo usar la actualización de firmware Microsoft Surface Dock para actualizar el firmware de Surface Docking.</span><span class="sxs-lookup"><span data-stu-id="355a6-108">This article explains how to use Microsoft Surface Dock Firmware Update to update Surface Dock firmware.</span></span> <span data-ttu-id="355a6-109">Cuando se instale en tu dispositivo Surface, se actualizará cualquier muelle de superficie conectado al dispositivo Surface.</span><span class="sxs-lookup"><span data-stu-id="355a6-109">When installed on your Surface device, it will update any Surface Dock attached to your Surface device.</span></span> 

<span data-ttu-id="355a6-110">Esta herramienta reemplaza la herramienta anterior de actualización de Microsoft Surface Dock, que anteriormente estaba disponible para descargar como parte de las herramientas de Surface.</span><span class="sxs-lookup"><span data-stu-id="355a6-110">This tool supersedes the earlier Microsoft Surface Dock Updater tool, previously available for download as part of Surface Tools for IT.</span></span> <span data-ttu-id="355a6-111">La herramienta anterior se denominaba Surface_Dock_Updater_vx.xx.xxx.x.msi (donde x indica el número de versión) y ya no se puede descargar y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="355a6-111">The earlier tool was named Surface_Dock_Updater_vx.xx.xxx.x.msi (where x indicates the version number) and is no longer available for download and should not be used.</span></span>

## <span data-ttu-id="355a6-112">Instalar la actualización del firmware de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-112">Install the Surface Dock Firmware Update</span></span>

<span data-ttu-id="355a6-113">En esta sección se describe cómo instalar manualmente la actualización del firmware.</span><span class="sxs-lookup"><span data-stu-id="355a6-113">This section describes how to manually install the firmware update.</span></span>

> [!NOTE]
> <span data-ttu-id="355a6-114">Microsoft lanza periódicamente nuevas versiones de la actualización del firmware Surface Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-114">Microsoft periodically releases new versions of Surface Dock Firmware Update.</span></span> <span data-ttu-id="355a6-115">El archivo MSI no se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="355a6-115">The MSI file is not self-updating.</span></span> <span data-ttu-id="355a6-116">Si ha implementado el MSI en dispositivos Surface y se publica una nueva versión del firmware, tendrá que implementar la nueva versión.</span><span class="sxs-lookup"><span data-stu-id="355a6-116">If you have deployed the MSI to Surface devices and a new version of the firmware is released, you will need to deploy the new version.</span></span>

1. <span data-ttu-id="355a6-117">Descargue e instale la [actualización de firmware Microsoft Surface Dock](https://www.microsoft.com/download/details.aspx?id=46703).</span><span class="sxs-lookup"><span data-stu-id="355a6-117">Download and install [Microsoft Surface Dock Firmware Update](https://www.microsoft.com/download/details.aspx?id=46703).</span></span>
    - <span data-ttu-id="355a6-118">La actualización requiere un dispositivo Surface que ejecute Windows 10, versión 1803 o posterior.</span><span class="sxs-lookup"><span data-stu-id="355a6-118">The update requires a Surface device running Windows 10, version 1803 or later.</span></span>
    - <span data-ttu-id="355a6-119">Si instalas el archivo MSI, es posible que se te pida que reinicies la superficie.</span><span class="sxs-lookup"><span data-stu-id="355a6-119">Installing the MSI file might prompt you to restart Surface.</span></span> <span data-ttu-id="355a6-120">Sin embargo, no es necesario reiniciar para realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="355a6-120">However, restarting is not required to perform the update.</span></span>

2. <span data-ttu-id="355a6-121">Desconecta el dispositivo Surface del muelle de superficie (con el adaptador de alimentación), espera ~ 5 segundos y, a continuación, vuelve a conectarte.</span><span class="sxs-lookup"><span data-stu-id="355a6-121">Disconnect your Surface device from the Surface Dock (using the power adapter), wait ~5 seconds, and then reconnect.</span></span> <span data-ttu-id="355a6-122">La actualización del firmware de Surface docking actualizará el Dock silenciosamente en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="355a6-122">The Surface Dock Firmware Update will update the dock silently in background.</span></span> <span data-ttu-id="355a6-123">El proceso puede demorar unos minutos en completarse y continuará aunque se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="355a6-123">The process can take a few minutes to complete and will continue even if interrupted.</span></span> 

## <span data-ttu-id="355a6-124">Supervisar la actualización del firmware de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-124">Monitor the Surface Dock Firmware Update</span></span>

<span data-ttu-id="355a6-125">Esta sección es opcional y proporciona información general sobre cómo supervisar la instalación de la actualización del firmware.</span><span class="sxs-lookup"><span data-stu-id="355a6-125">This section is optional and provides an overview of how to monitor installation of the firmware update.</span></span> 

<span data-ttu-id="355a6-126">Para supervisar la actualización:</span><span class="sxs-lookup"><span data-stu-id="355a6-126">To monitor the update:</span></span>

1. <span data-ttu-id="355a6-127">Abra el visor de eventos, vaya a **registros de Windows > aplicación**y, a continuación, en **acciones** , en el panel derecho, haga clic en **filtrar registro actual**, escriba **SurfaceDockFwUpdate** junto a **orígenes de eventos**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="355a6-127">Open Event Viewer, browse to **Windows Logs > Application**, and then under **Actions** in the right-hand pane click **Filter Current Log**, enter **SurfaceDockFwUpdate** next to **Event sources**, and then click **OK**.</span></span>

2. <span data-ttu-id="355a6-128">Escriba el comando siguiente en un símbolo del sistema con privilegios elevados:</span><span class="sxs-lookup"><span data-stu-id="355a6-128">Type the following command at an elevated command prompt:</span></span>

    ```cmd
    Reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\WUDF\Services\SurfaceDockFwUpdate\Parameters"
    ```
3. <span data-ttu-id="355a6-129">Instale la actualización como se describe en la [siguiente sección](#install-the-surface-dock-firmware-update) de este artículo.</span><span class="sxs-lookup"><span data-stu-id="355a6-129">Install the update as described in the [next section](#install-the-surface-dock-firmware-update) of this article.</span></span>
4. <span data-ttu-id="355a6-130">El evento 2007 con el siguiente texto indica una actualización correcta: **actualización del firmware finalizada. hr = 0 DriverTelementry EventCode = 2007**.</span><span class="sxs-lookup"><span data-stu-id="355a6-130">Event 2007 with the following text indicates a successful update: **Firmware update finished. hr=0 DriverTelementry EventCode = 2007**.</span></span> 
    - <span data-ttu-id="355a6-131">Si la actualización no se realiza correctamente, se mostrará el identificador de evento 2007 como un evento de **error** en lugar de la **información**.</span><span class="sxs-lookup"><span data-stu-id="355a6-131">If the update is not successful, then event ID 2007 will be displayed as an **Error** event rather than **Information**.</span></span> <span data-ttu-id="355a6-132">Además, la versión notificada en el registro de Windows no estará actualizada.</span><span class="sxs-lookup"><span data-stu-id="355a6-132">Additionally, the version reported in the Windows Registry will not be current.</span></span>
5. <span data-ttu-id="355a6-133">Una vez completada la actualización, los valores DWORD actualizados se mostrarán en el registro de Windows, que corresponde a la versión actual de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="355a6-133">When the update is complete, updated DWORD values will be displayed in the Windows Registry, corresponding to the current version of the tool.</span></span> <span data-ttu-id="355a6-134">Para obtener más información, consulte la sección [referencia de versiones](#versions-reference) en este artículo.</span><span class="sxs-lookup"><span data-stu-id="355a6-134">See the [Versions reference](#versions-reference) section in this article for details.</span></span> <span data-ttu-id="355a6-135">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="355a6-135">For example:</span></span>
    - <span data-ttu-id="355a6-136">Component10CurrentFwVersion 0x04ac3970 (78395760)</span><span class="sxs-lookup"><span data-stu-id="355a6-136">Component10CurrentFwVersion 0x04ac3970 (78395760)</span></span>
    - <span data-ttu-id="355a6-137">Component20CurrentFwVersion 0x04915a70 (76634736)</span><span class="sxs-lookup"><span data-stu-id="355a6-137">Component20CurrentFwVersion 0x04915a70 (76634736)</span></span>

>[!TIP]
><span data-ttu-id="355a6-138">Si ve "no se puede encontrar la descripción del identificador de evento xxxx del origen SurfaceDockFwUpdate" en el texto del evento, esto es lo que se espera y se puede ignorar.</span><span class="sxs-lookup"><span data-stu-id="355a6-138">If you see "The description for Event ID xxxx from source SurfaceDockFwUpdate cannot be found" in event text, this is expected and can be ignored.</span></span>

<span data-ttu-id="355a6-139">Consulte también las secciones siguientes de este artículo:</span><span class="sxs-lookup"><span data-stu-id="355a6-139">Also see the following sections in this article:</span></span> 
  - [<span data-ttu-id="355a6-140">Cómo comprobar la finalización de la actualización del firmware</span><span class="sxs-lookup"><span data-stu-id="355a6-140">How to verify completion of firmware update</span></span>](#how-to-verify-completion-of-the-firmware-update)
  - [<span data-ttu-id="355a6-141">Registro de eventos</span><span class="sxs-lookup"><span data-stu-id="355a6-141">Event logging</span></span>](#event-logging)
  - [<span data-ttu-id="355a6-142">Recomendaciones para la solución de problemas</span><span class="sxs-lookup"><span data-stu-id="355a6-142">Troubleshooting tips</span></span>](#troubleshooting-tips)
  - [<span data-ttu-id="355a6-143">Referencia de versiones</span><span class="sxs-lookup"><span data-stu-id="355a6-143">Versions reference</span></span>](#versions-reference)

## <span data-ttu-id="355a6-144">Implementación de red</span><span class="sxs-lookup"><span data-stu-id="355a6-144">Network deployment</span></span>

<span data-ttu-id="355a6-145">Puede usar los comandos de Windows Installer (Msiexec.exe) para implementar la actualización del firmware Surface Dock en varios dispositivos de la red.</span><span class="sxs-lookup"><span data-stu-id="355a6-145">You can use Windows Installer commands (Msiexec.exe) to deploy Surface Dock Firmware Update to multiple devices across your network.</span></span> <span data-ttu-id="355a6-146">Cuando use Microsoft Endpoint Configuration Manager u otra herramienta de implementación, escriba la siguiente sintaxis para asegurarse de que la instalación es silenciosa:</span><span class="sxs-lookup"><span data-stu-id="355a6-146">When using Microsoft Endpoint Configuration Manager or other deployment tool, enter the following syntax to ensure the installation is silent:</span></span>

- **<span data-ttu-id="355a6-147">Msiexec.exe/i \<path to msi file\> /Quiet/norestart</span><span class="sxs-lookup"><span data-stu-id="355a6-147">Msiexec.exe /i \<path to msi file\> /quiet /norestart</span></span>** 

  <span data-ttu-id="355a6-148">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="355a6-148">For example:</span></span>
  ```
  msiexec /i "\\share\folder\Surface_Dock_FwUpdate_1.42.139_Win10_17134_19.084.31680_0.msi" /quiet /norestart
  ```

  > [!NOTE]
  > <span data-ttu-id="355a6-149">No se crea un archivo de registro de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="355a6-149">A log file is not created by default.</span></span> <span data-ttu-id="355a6-150">Para crear un archivo de registro, tendrá que anexar "/l*v [rutaDeAcceso]". Por ejemplo: Msiexec.exe/i \<path to msi file\> /l*v%WINDIR%\logs\ SurfaceDockFWI. log "</span><span class="sxs-lookup"><span data-stu-id="355a6-150">In order to create a log file, you will need to append "/l*v [path]". For example: Msiexec.exe /i \<path to msi file\> /l*v %windir%\logs\ SurfaceDockFWI.log"</span></span>

  <span data-ttu-id="355a6-151">Para obtener más información, consulte la documentación de [Opciones de línea de comandos](https://docs.microsoft.com/windows/win32/msi/command-line-options) .</span><span class="sxs-lookup"><span data-stu-id="355a6-151">For more information, refer to [Command line options](https://docs.microsoft.com/windows/win32/msi/command-line-options) documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="355a6-152">Si desea mantener el Dock de Surface actualizado con cualquier otro método, consulte [actualizar su Dock de Surface](https://support.microsoft.com/help/4023478/surface-update-your-surface-dock) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="355a6-152">If you want to keep your Surface Dock updated using any other method, refer to [Update your Surface Dock](https://support.microsoft.com/help/4023478/surface-update-your-surface-dock) for details.</span></span>

## <span data-ttu-id="355a6-153">Implementación de Intune</span><span class="sxs-lookup"><span data-stu-id="355a6-153">Intune deployment</span></span>

<span data-ttu-id="355a6-154">Puede usar Intune para distribuir la actualización del firmware Surface Dock en sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="355a6-154">You can use Intune to distribute Surface Dock Firmware Update to your devices.</span></span> <span data-ttu-id="355a6-155">En primer lugar, tendrá que convertir el archivo MSI al formato. intunewin, como se describe en la siguiente documentación: [Intune administración de aplicaciones independiente-Win32](https://docs.microsoft.com/intune/apps/apps-win32-app-management).</span><span class="sxs-lookup"><span data-stu-id="355a6-155">First you will need to convert the MSI file to the .intunewin format, as described in the following documentation: [Intune Standalone - Win32 app management](https://docs.microsoft.com/intune/apps/apps-win32-app-management).</span></span>

<span data-ttu-id="355a6-156">Use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="355a6-156">Use the following command:</span></span>
  - **<span data-ttu-id="355a6-157">msiexec/i \<path to msi file\> /Quiet/q</span><span class="sxs-lookup"><span data-stu-id="355a6-157">msiexec /i \<path to msi file\> /quiet /q</span></span>**

## <span data-ttu-id="355a6-158">Cómo comprobar la finalización de la actualización del firmware</span><span class="sxs-lookup"><span data-stu-id="355a6-158">How to verify completion of the firmware update</span></span>

<span data-ttu-id="355a6-159">El firmware de Surface docking consta de dos componentes:</span><span class="sxs-lookup"><span data-stu-id="355a6-159">Surface dock firmware consists of two components:</span></span>

- <span data-ttu-id="355a6-160">**Component10:** Firmware de unidad Micro Controller (MCU)</span><span class="sxs-lookup"><span data-stu-id="355a6-160">**Component10:** Micro controller unit (MCU) firmware</span></span>
- <span data-ttu-id="355a6-161">**Component20:** Firmware del puerto de visualización (DP).</span><span class="sxs-lookup"><span data-stu-id="355a6-161">**Component20:** Display port (DP) firmware.</span></span>

<span data-ttu-id="355a6-162">La finalización satisfactoria de la actualización del firmware Surface docking genera nuevos valores de clave del registro para estos componentes de firmware.</span><span class="sxs-lookup"><span data-stu-id="355a6-162">Successful completion of Surface Dock Firmware Update results in new registry key values for these firmware components.</span></span>

**<span data-ttu-id="355a6-163">Para comprobar las actualizaciones:</span><span class="sxs-lookup"><span data-stu-id="355a6-163">To verify updates:</span></span>**

1. <span data-ttu-id="355a6-164">Abra Regedit y vaya a la siguiente ruta del registro:</span><span class="sxs-lookup"><span data-stu-id="355a6-164">Open Regedit and navigate to the following registry path:</span></span>

    - **<span data-ttu-id="355a6-165">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\Windows NT\CurrentVersion\WUDF\Services\SurfaceDockFwUpdate\Parameters</span><span class="sxs-lookup"><span data-stu-id="355a6-165">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\WUDF\Services\SurfaceDockFwUpdate\Parameters</span></span>**

2. <span data-ttu-id="355a6-166">Busque las claves del registro: **Component10CurrentFwVersion y Component20CurrentFwVersion**, que hacen referencia al firmware que se encuentra actualmente en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="355a6-166">Look for the registry keys: **Component10CurrentFwVersion and Component20CurrentFwVersion**, which refer to the firmware that is currently on the device.</span></span>

   ![Proceso de instalación de actualización de firmware Surface Dock](images/regeditDock.png)

3. <span data-ttu-id="355a6-168">Compruebe que los nuevos valores de la clave del registro coincidan con los valores de la clave del registro actualizadas que aparecen en la referencia de versiones al final de este documento.</span><span class="sxs-lookup"><span data-stu-id="355a6-168">Verify the new registry key values match the updated registry key values listed in the Versions reference at the end of this document.</span></span> <span data-ttu-id="355a6-169">Si los valores coinciden, el firmware se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="355a6-169">If the values match, the firmware was updated successfully.</span></span>

4. <span data-ttu-id="355a6-170">Si no puede comprobar, revise el registro de eventos y las sugerencias para la solución de problemas en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="355a6-170">If unable to verify, review Event logging and Troubleshooting tips in the next section.</span></span>

## <span data-ttu-id="355a6-171">Registro de eventos</span><span class="sxs-lookup"><span data-stu-id="355a6-171">Event logging</span></span>

**<span data-ttu-id="355a6-172">Tabla 1.</span><span class="sxs-lookup"><span data-stu-id="355a6-172">Table 1.</span></span> <span data-ttu-id="355a6-173">Archivos de registro de la actualización del firmware Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-173">Log files for Surface Dock Firmware Update</span></span>**

| <span data-ttu-id="355a6-174">Log</span><span class="sxs-lookup"><span data-stu-id="355a6-174">Log</span></span>                              | <span data-ttu-id="355a6-175">Ubicación</span><span class="sxs-lookup"><span data-stu-id="355a6-175">Location</span></span>                               | <span data-ttu-id="355a6-176">Notas</span><span class="sxs-lookup"><span data-stu-id="355a6-176">Notes</span></span>                                                                                                                                                                                                         |
| -------------------------------- | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="355a6-177">Registro de actualización de firmware de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-177">Surface Dock Firmware Update log</span></span> | <span data-ttu-id="355a6-178">Es necesario especificar la ruta de acceso (vea la nota)</span><span class="sxs-lookup"><span data-stu-id="355a6-178">Path needs to be specified (see note)</span></span> | <span data-ttu-id="355a6-179">Las versiones anteriores de esta herramienta escribían eventos a aplicaciones y servicios de la actualización de Logs\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="355a6-179">Earlier versions of this tool wrote events to Applications and Services Logs\Microsoft Surface Dock Updater.</span></span>                                                                                                  |
| <span data-ttu-id="355a6-180">Registro de instalación de dispositivo de Windows</span><span class="sxs-lookup"><span data-stu-id="355a6-180">Windows Device Install log</span></span>       | <span data-ttu-id="355a6-181">%windir%\inf\setupapi.dev.log</span><span class="sxs-lookup"><span data-stu-id="355a6-181">%windir%\inf\setupapi.dev.log</span></span>           | <span data-ttu-id="355a6-182">Para obtener más información sobre cómo usar el registro de instalación de dispositivos, consulte la documentación de [registro de SetupAPI](https://docs.microsoft.com/windows-hardware/drivers/install/setupapi-logging--windows-vista-and-later-) .</span><span class="sxs-lookup"><span data-stu-id="355a6-182">For more information about using Device Install Log, refer to [SetupAPI Logging](https://docs.microsoft.com/windows-hardware/drivers/install/setupapi-logging--windows-vista-and-later-) documentation.</span></span> |


**<span data-ttu-id="355a6-183">Tabla 2.</span><span class="sxs-lookup"><span data-stu-id="355a6-183">Table 2.</span></span> <span data-ttu-id="355a6-184">Identificadores de registro de eventos para la actualización de firmware Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-184">Event log IDs for Surface Dock Firmware Update</span></span>**<br>
<span data-ttu-id="355a6-185">Los eventos se registran en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="355a6-185">Events are logged in the Application Event Log.</span></span>  <span data-ttu-id="355a6-186">Nota: las versiones anteriores de esta herramienta escribieron eventos para las aplicaciones y servicios de la actualización del Dock Logs\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="355a6-186">Note:  Earlier versions of this tool wrote events to Applications and Services Logs\Microsoft Surface Dock Updater.</span></span>

| <span data-ttu-id="355a6-187">Id. de evento</span><span class="sxs-lookup"><span data-stu-id="355a6-187">Event ID</span></span> | <span data-ttu-id="355a6-188">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="355a6-188">Event type</span></span>                                                           |
| -------- | -------------------------------------------------------------------- |
| <span data-ttu-id="355a6-189">2001</span><span class="sxs-lookup"><span data-stu-id="355a6-189">2001</span></span>     | <span data-ttu-id="355a6-190">Se inició la actualización del firmware del Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-190">Dock firmware update has started.</span></span>                                    |
| <span data-ttu-id="355a6-191">2002</span><span class="sxs-lookup"><span data-stu-id="355a6-191">2002</span></span>     | <span data-ttu-id="355a6-192">Se ha omitido la actualización del firmware del Dock porque se sabe que Dock está actualizado.</span><span class="sxs-lookup"><span data-stu-id="355a6-192">Dock firmware update skipped because dock is known to be up to date.</span></span> |
| <span data-ttu-id="355a6-193">2003</span><span class="sxs-lookup"><span data-stu-id="355a6-193">2003</span></span>     | <span data-ttu-id="355a6-194">Error al descargar la versión del firmware en la actualización del firmware del Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-194">Dock firmware update failed to get firmware version.</span></span>                 |
| <span data-ttu-id="355a6-195">2004</span><span class="sxs-lookup"><span data-stu-id="355a6-195">2004</span></span>     | <span data-ttu-id="355a6-196">Consultando la versión de firmware.</span><span class="sxs-lookup"><span data-stu-id="355a6-196">Querying the firmware version.</span></span>                                       |
| <span data-ttu-id="355a6-197">2005</span><span class="sxs-lookup"><span data-stu-id="355a6-197">2005</span></span>     | <span data-ttu-id="355a6-198">El firmware del Dock no pudo iniciar la actualización.</span><span class="sxs-lookup"><span data-stu-id="355a6-198">Dock firmware failed to start update.</span></span>                                |
| <span data-ttu-id="355a6-199">2006</span><span class="sxs-lookup"><span data-stu-id="355a6-199">2006</span></span>     | <span data-ttu-id="355a6-200">No se pudieron enviar los pares de oferta o carga.</span><span class="sxs-lookup"><span data-stu-id="355a6-200">Failed to send offer/payload pairs.</span></span>                                  |
| <span data-ttu-id="355a6-201">2007</span><span class="sxs-lookup"><span data-stu-id="355a6-201">2007</span></span>     | <span data-ttu-id="355a6-202">Actualización de firmware finalizada.</span><span class="sxs-lookup"><span data-stu-id="355a6-202">Firmware update finished.</span></span>                                            |
| <span data-ttu-id="355a6-203">2008</span><span class="sxs-lookup"><span data-stu-id="355a6-203">2008</span></span>     | <span data-ttu-id="355a6-204">COMIENZA la telemetría de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="355a6-204">BEGIN dock telemetry.</span></span>                                                |
| <span data-ttu-id="355a6-205">2011</span><span class="sxs-lookup"><span data-stu-id="355a6-205">2011</span></span>     | <span data-ttu-id="355a6-206">FINALIZAR la telemetría del Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-206">END dock telemetry.</span></span>                                                  |

## <span data-ttu-id="355a6-207">Recomendaciones para la solución de problemas</span><span class="sxs-lookup"><span data-stu-id="355a6-207">Troubleshooting tips</span></span>

- <span data-ttu-id="355a6-208">Desconecta por completo la energía del muelle de superficie desde la alimentación de CA para restablecer el muelle de superficie.</span><span class="sxs-lookup"><span data-stu-id="355a6-208">Completely disconnect power for Surface dock from the AC power to reset the Surface Dock.</span></span>
- <span data-ttu-id="355a6-209">Desconecte todos los periféricos excepto el del Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-209">Disconnect all peripherals except for the Surface Dock.</span></span>
- <span data-ttu-id="355a6-210">Desinstale la actualización de firmware de Surface Dock actual y, a continuación, instale la última versión.</span><span class="sxs-lookup"><span data-stu-id="355a6-210">Uninstall any current Surface Dock Firmware Update and then install the latest version.</span></span>
- <span data-ttu-id="355a6-211">Asegúrese de que el muelle de superficie esté desconectado y deje el tiempo suficiente para que se complete la actualización mediante un LED en el puerto Ethernet del Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-211">Ensure that the Surface Dock is disconnected, and then allow enough time for the update to complete as monitored via an LED in the Ethernet port of the dock.</span></span> <span data-ttu-id="355a6-212">Espere hasta que el LED deje de parpadear antes de desconectar la superficie del Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-212">Wait until the LED stops blinking before you unplug Surface Dock from power.</span></span>
- <span data-ttu-id="355a6-213">Conecte el muelle de superficie a un dispositivo diferente para ver si es capaz de actualizar el Dock.</span><span class="sxs-lookup"><span data-stu-id="355a6-213">Connect the Surface Dock to a different device to see if it is able to update the dock.</span></span>

## <span data-ttu-id="355a6-214">Referencia de versiones</span><span class="sxs-lookup"><span data-stu-id="355a6-214">Versions reference</span></span>

>[!NOTE]
><span data-ttu-id="355a6-215">El archivo de instalación se publica con el siguiente formato de nombre: **Surface_Dock_FwUpdate_X.XX.XXX_Win10_XXXXX_XX.XXX.XXXXX_X.MSI** (por ejemplo: Surface_Dock_FwUpdate_1.42.139_Win10_17134_19.084.31680_0.msi) e instala de forma predeterminada en C:\Archivos de Files\SurfaceUpdate.</span><span class="sxs-lookup"><span data-stu-id="355a6-215">The installation file is released with the following naming format: **Surface_Dock_FwUpdate_X.XX.XXX_Win10_XXXXX_XX.XXX.XXXXX_X.MSI** (ex: Surface_Dock_FwUpdate_1.42.139_Win10_17134_19.084.31680_0.msi) and installs by default to C:\Program Files\SurfaceUpdate.</span></span>

### <span data-ttu-id="355a6-216">Versión 1.42.139</span><span class="sxs-lookup"><span data-stu-id="355a6-216">Version 1.42.139</span></span> 
*<span data-ttu-id="355a6-217">Fecha de lanzamiento: Septiembre 18 2019</span><span class="sxs-lookup"><span data-stu-id="355a6-217">Release Date: September 18 2019</span></span>*

<span data-ttu-id="355a6-218">Esta versión, que se encuentra en Surface_Dock_FwUpdate_1.42.139_Win10_17134_19.084.31680_0.MSI, actualiza el firmware en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="355a6-218">This version, contained in Surface_Dock_FwUpdate_1.42.139_Win10_17134_19.084.31680_0.MSI, updates firmware in the background.</span></span> 
**<span data-ttu-id="355a6-219">Valores de clave del registro actualizados:</span><span class="sxs-lookup"><span data-stu-id="355a6-219">Updated registry key values:</span></span>**<br>

- <span data-ttu-id="355a6-220">Component10CurrentFwVersion actualizado a **4ac3970**.</span><span class="sxs-lookup"><span data-stu-id="355a6-220">Component10CurrentFwVersion updated to **4ac3970**.</span></span>
- <span data-ttu-id="355a6-221">Component20CurrentFwVersion actualizado a **4a1d570**.</span><span class="sxs-lookup"><span data-stu-id="355a6-221">Component20CurrentFwVersion updated to **4a1d570**.</span></span>

<span data-ttu-id="355a6-222">Agrega compatibilidad para Surface Pro 7 y el portátil Surface 3.</span><span class="sxs-lookup"><span data-stu-id="355a6-222">It adds support for Surface Pro 7 and Surface Laptop 3.</span></span>

## <span data-ttu-id="355a6-223">Versiones heredadas</span><span class="sxs-lookup"><span data-stu-id="355a6-223">Legacy versions</span></span>

### <span data-ttu-id="355a6-224">Versión 2.23.139.0</span><span class="sxs-lookup"><span data-stu-id="355a6-224">Version 2.23.139.0</span></span>
*<span data-ttu-id="355a6-225">Fecha de lanzamiento: 10 de octubre de 2018</span><span class="sxs-lookup"><span data-stu-id="355a6-225">Release Date: 10 October 2018</span></span>*

<span data-ttu-id="355a6-226">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-226">This version of Surface Dock Updater adds support for the following:</span></span>

- <span data-ttu-id="355a6-227">Agregar compatibilidad con Surface Pro 6</span><span class="sxs-lookup"><span data-stu-id="355a6-227">Add support for Surface Pro 6</span></span>
- <span data-ttu-id="355a6-228">Agregar compatibilidad para Surface Laptop 2</span><span class="sxs-lookup"><span data-stu-id="355a6-228">Add support for Surface Laptop 2</span></span>


### <span data-ttu-id="355a6-229">Versión 2.22.139.0</span><span class="sxs-lookup"><span data-stu-id="355a6-229">Version 2.22.139.0</span></span>
*<span data-ttu-id="355a6-230">Fecha de lanzamiento: 26 de julio de 2018</span><span class="sxs-lookup"><span data-stu-id="355a6-230">Release Date: 26 July 2018</span></span>*

<span data-ttu-id="355a6-231">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-231">This version of Surface Dock Updater adds support for the following:</span></span>

- <span data-ttu-id="355a6-232">Aumentar la confiabilidad de la actualización</span><span class="sxs-lookup"><span data-stu-id="355a6-232">Increase update reliability</span></span>
- <span data-ttu-id="355a6-233">Agregar compatibilidad con Surface Go</span><span class="sxs-lookup"><span data-stu-id="355a6-233">Add support for Surface Go</span></span>

### <span data-ttu-id="355a6-234">Versión 2.12.136.0</span><span class="sxs-lookup"><span data-stu-id="355a6-234">Version 2.12.136.0</span></span>
*<span data-ttu-id="355a6-235">Fecha de lanzamiento: 29 de enero de 2018</span><span class="sxs-lookup"><span data-stu-id="355a6-235">Release Date: 29 January 2018</span></span>*

<span data-ttu-id="355a6-236">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-236">This version of Surface Dock Updater adds support for the following:</span></span>
* <span data-ttu-id="355a6-237">Actualización de firmware del conjunto de chips principal de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-237">Update for Surface Dock Main Chipset Firmware</span></span>
* <span data-ttu-id="355a6-238">Actualización de firmware de DisplayPort de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-238">Update for Surface Dock DisplayPort Firmware</span></span>
* <span data-ttu-id="355a6-239">Se ha mejorado la estabilidad de la pantalla para las pantallas externas cuando se usa con Surface Book o Surface Book 2</span><span class="sxs-lookup"><span data-stu-id="355a6-239">Improved display stability for external displays when used with Surface Book or Surface Book 2</span></span>

<span data-ttu-id="355a6-240">Además, en la instalación de esta versión de Surface Dock Updater en dispositivos Surface Book se incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-240">Additionally, installation of this version of Surface Dock Updater on Surface Book devices includes the following:</span></span>
* <span data-ttu-id="355a6-241">Actualización de firmware de la base de Surface Book</span><span class="sxs-lookup"><span data-stu-id="355a6-241">Update for Surface Book Base Firmware</span></span>
* <span data-ttu-id="355a6-242">Se ha agregado soporte para las actualizaciones de firmware de Surface Dock con mejoras destinadas a dispositivos de Surface Book</span><span class="sxs-lookup"><span data-stu-id="355a6-242">Added support for Surface Dock firmware updates with improvements targeted to Surface Book devices</span></span>


### <span data-ttu-id="355a6-243">Versión 2.9.136.0</span><span class="sxs-lookup"><span data-stu-id="355a6-243">Version 2.9.136.0</span></span>
*<span data-ttu-id="355a6-244">Fecha de lanzamiento: 3 de noviembre de 2017</span><span class="sxs-lookup"><span data-stu-id="355a6-244">Release date: November 3, 2017</span></span>*

<span data-ttu-id="355a6-245">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-245">This version of Surface Dock Updater adds support for the following:</span></span>

* <span data-ttu-id="355a6-246">Actualización de firmware de DisplayPort de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-246">Update for Surface Dock DisplayPort Firmware</span></span>
* <span data-ttu-id="355a6-247">Resuelve un problema con el audio en adaptadores de puerto de pantalla pasivos</span><span class="sxs-lookup"><span data-stu-id="355a6-247">Resolves an issue with audio over passive display port adapters</span></span>

### <span data-ttu-id="355a6-248">Versión 2.1.15.0</span><span class="sxs-lookup"><span data-stu-id="355a6-248">Version 2.1.15.0</span></span>
*<span data-ttu-id="355a6-249">Fecha de lanzamiento: 19 de junio de 2017</span><span class="sxs-lookup"><span data-stu-id="355a6-249">Release date: June 19, 2017</span></span>*

<span data-ttu-id="355a6-250">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-250">This version of Surface Dock Updater adds support for the following:</span></span>

* <span data-ttu-id="355a6-251">Surface Laptop</span><span class="sxs-lookup"><span data-stu-id="355a6-251">Surface Laptop</span></span>
* <span data-ttu-id="355a6-252">Surface Pro</span><span class="sxs-lookup"><span data-stu-id="355a6-252">Surface Pro</span></span>

### <span data-ttu-id="355a6-253">Versión 2.1.6.0</span><span class="sxs-lookup"><span data-stu-id="355a6-253">Version 2.1.6.0</span></span>
*<span data-ttu-id="355a6-254">Fecha de lanzamiento: 7 de abril de 2017</span><span class="sxs-lookup"><span data-stu-id="355a6-254">Release date: April 7, 2017</span></span>*

<span data-ttu-id="355a6-255">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-255">This version of Surface Dock Updater adds support for the following:</span></span>

* <span data-ttu-id="355a6-256">Actualización de firmware de DisplayPort de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-256">Update for Surface Dock DisplayPort firmware</span></span>
* <span data-ttu-id="355a6-257">Requiere Windows 10</span><span class="sxs-lookup"><span data-stu-id="355a6-257">Requires Windows 10</span></span>

### <span data-ttu-id="355a6-258">Versión 2.0.22.0</span><span class="sxs-lookup"><span data-stu-id="355a6-258">Version 2.0.22.0</span></span>
*<span data-ttu-id="355a6-259">Fecha de lanzamiento: 21 de octubre de 2016</span><span class="sxs-lookup"><span data-stu-id="355a6-259">Release date: October 21, 2016</span></span>*

<span data-ttu-id="355a6-260">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-260">This version of Surface Dock Updater adds support for the following:</span></span>

* <span data-ttu-id="355a6-261">Actualización de firmware de USB de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-261">Update for Surface Dock USB firmware</span></span>
* <span data-ttu-id="355a6-262">Fiabilidad mejorada de los puertos de audio, USB y Ethernet</span><span class="sxs-lookup"><span data-stu-id="355a6-262">Improved reliability of Ethernet, audio, and USB ports</span></span>

### <span data-ttu-id="355a6-263">Versión 1.0.8.0</span><span class="sxs-lookup"><span data-stu-id="355a6-263">Version 1.0.8.0</span></span>
*<span data-ttu-id="355a6-264">Fecha de lanzamiento: 26 de abril de 2016</span><span class="sxs-lookup"><span data-stu-id="355a6-264">Release date: April 26, 2016</span></span>*

<span data-ttu-id="355a6-265">Esta versión de Surface Dock Updater agrega compatibilidad con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="355a6-265">This version of Surface Dock Updater adds support for the following:</span></span>

* <span data-ttu-id="355a6-266">Actualización de firmware del conjunto de chips principal de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-266">Update for Surface Dock Main Chipset firmware</span></span>
* <span data-ttu-id="355a6-267">Actualización de firmware de DisplayPort de Surface Dock</span><span class="sxs-lookup"><span data-stu-id="355a6-267">Update for Surface Dock DisplayPort firmware</span></span>

