---
title: Migrar a Windows 10 Pro o Enterprise en Surface Hub 2
description: En este artículo se describe el proceso de migración de equipo de Windows 10 en Surface Hub 2 a Windows 10 Pro o Windows 10 Enterprise.
keywords: separar valores con comas
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 09/03/2020
ms.localizationpriority: Medium
ms.openlocfilehash: a114a9200a58a848f2480de965f268cee71cebae
ms.sourcegitcommit: c74835239cf4e304af59465fb6fc785de4a0c5cc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/03/2020
ms.locfileid: "10994606"
---
# <span data-ttu-id="b061b-104">Migrar a Windows 10 Pro o Enterprise en Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-104">Migrate to Windows 10 Pro or Enterprise on Surface Hub 2</span></span>

## <span data-ttu-id="b061b-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="b061b-105">Introduction</span></span>

<span data-ttu-id="b061b-106">Surface Hub 2S viene preinstalado con el equipo con Windows 10, una edición personalizada de Windows 10 diseñada para facilitar la colaboración en entornos de reuniones.</span><span class="sxs-lookup"><span data-stu-id="b061b-106">Surface Hub 2S comes pre-installed with Windows 10 Team, a customized edition of Windows 10 designed to facilitate easy collaboration in meeting room environments.</span></span> <span data-ttu-id="b061b-107">Ahora tienes la opción de ejecutar Windows 10 Pro o Enterprise para usar Surface Hub 2 de manera similar a cualquier otro equipo.</span><span class="sxs-lookup"><span data-stu-id="b061b-107">Now you have the option of running Windows 10 Pro or Enterprise to use Surface Hub 2S much like any other PC.</span></span> 

> [!IMPORTANT]
><span data-ttu-id="b061b-108">A diferencia de una actualización o migración típica, este proceso requiere que siga un procedimiento prescriptivo, como se describe en esta página.</span><span class="sxs-lookup"><span data-stu-id="b061b-108">Unlike a typical upgrade or migration, this process requires you to follow a prescriptive procedure, as described on this page.</span></span> <span data-ttu-id="b061b-109">Revise los [componentes](#solution-components) de la solución y el [flujo de trabajo de migración](#migration-workflow-summary) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="b061b-109">Review the [Solution components](#solution-components) and [Migration workflow](#migration-workflow-summary) before proceeding.</span></span>

<span data-ttu-id="b061b-110">Para iniciar la migración desde el equipo de Windows 10, use un equipo independiente y una herramienta descargable, **Surface UEFI** , para crear un paquete que contenga una nueva configuración de UEFI que aplique a Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="b061b-110">You start the migration from Windows 10 Team using a separate PC and downloadable tool -- **Surface UEFI Configurator** --  to create a package containing a new UEFI setting that you apply to Surface Hub 2S.</span></span>  <span data-ttu-id="b061b-111">El configurador de Surface UEFI funciona como una interfaz en el modo Surface de administración de la empresa (SEMM), diseñado para facilitar la administración centralizada de la configuración del firmware en dispositivos Surface en un entorno corporativo.</span><span class="sxs-lookup"><span data-stu-id="b061b-111">Surface UEFI Configurator functions as an interface into Surface Enterprise Management Mode (SEMM), designed to facilitate centralized management of firmware settings on Surface devices in a corporate environment.</span></span> <span data-ttu-id="b061b-112">Para obtener más información sobre SEMM, consulte la [documentación del modo de administración de Microsoft Surface Enterprise](https://docs.microsoft.com/surface/surface-enterprise-management-mode).</span><span class="sxs-lookup"><span data-stu-id="b061b-112">To learn more about SEMM, see [Microsoft Surface Enterprise Management Mode documentation](https://docs.microsoft.com/surface/surface-enterprise-management-mode).</span></span>
 

## <span data-ttu-id="b061b-113">Componentes de la solución</span><span class="sxs-lookup"><span data-stu-id="b061b-113">Solution Components</span></span>

- <span data-ttu-id="b061b-114">Dispositivo Surface Hub 2S que ejecuta el sistema operativo Windows 10 Teams</span><span class="sxs-lookup"><span data-stu-id="b061b-114">Surface Hub 2S device running Windows 10 Team operating system</span></span>
- <span data-ttu-id="b061b-115">Dispositivo independiente que ejecuta Windows 10</span><span class="sxs-lookup"><span data-stu-id="b061b-115">Separate device running Windows 10</span></span>
- <span data-ttu-id="b061b-116">Herramienta configurador UEFI de Surface</span><span class="sxs-lookup"><span data-stu-id="b061b-116">Surface UEFI Configurator tool</span></span>
- <span data-ttu-id="b061b-117">Imagen del sistema operativo Windows 10 Pro o Enterprise, versión 1903 o superior</span><span class="sxs-lookup"><span data-stu-id="b061b-117">Windows 10 Pro or Enterprise OS image, version 1903 or greater</span></span>
- <span data-ttu-id="b061b-118">Dos unidades USB con 16 GB de almacenamiento, formato FAT32</span><span class="sxs-lookup"><span data-stu-id="b061b-118">Two USB drives with 16GB of storage, FAT32 format</span></span>
- <span data-ttu-id="b061b-119">Drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2, Windows Installer. Archivo MSI</span><span class="sxs-lookup"><span data-stu-id="b061b-119">Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2, Windows Installer .MSI file</span></span>
- <span data-ttu-id="b061b-120">Conexión a Internet</span><span class="sxs-lookup"><span data-stu-id="b061b-120">Internet connection</span></span>
- <span data-ttu-id="b061b-121">Solución de creación de imágenes (opcional)</span><span class="sxs-lookup"><span data-stu-id="b061b-121">Imaging solution (optional)</span></span>

 
## <span data-ttu-id="b061b-122">Resumen de flujo de trabajo de migración</span><span class="sxs-lookup"><span data-stu-id="b061b-122">Migration workflow summary</span></span>

| <span data-ttu-id="b061b-123">Paso</span><span class="sxs-lookup"><span data-stu-id="b061b-123">Step</span></span>  | <span data-ttu-id="b061b-124">Acción</span><span class="sxs-lookup"><span data-stu-id="b061b-124">Action</span></span>                                                                                                 | <span data-ttu-id="b061b-125">Resumen</span><span class="sxs-lookup"><span data-stu-id="b061b-125">Summary</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| - | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="b061b-126">uno</span><span class="sxs-lookup"><span data-stu-id="b061b-126">1</span></span> | [<span data-ttu-id="b061b-127">Comprobar si la versión de Surface Hub cumple con los requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="b061b-127">Verify UEFI version on Surface Hub 2S meets minimum requirements</span></span>](#verify-uefi-version-on-surface-hub-2s-meets-minimum-requirements)                                  | <span data-ttu-id="b061b-128">Asegúrese de que la versión de UEFI sea 694.2938.768.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b061b-128">Ensure the UEFI version is 694.2938.768.0 or later.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b061b-129">1</span><span class="sxs-lookup"><span data-stu-id="b061b-129">2</span></span> | [<span data-ttu-id="b061b-130">Descargar el configurador de Surface UEFI y los drivers y firmware de Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-130">Download Surface UEFI Configurator and Surface Hub 2 Drivers and Firmware</span></span>](#download-surface-uefi-configurator-and-surface-hub-2-drivers-and-firmware)                             | <span data-ttu-id="b061b-131">Descarga el [configurador de Surface UEFI](https://www.microsoft.com/download/details.aspx?id=46703) desde herramientas de Surface para ti e instálelo en un PC independiente.</span><span class="sxs-lookup"><span data-stu-id="b061b-131">Download [Surface UEFI Configurator](https://www.microsoft.com/download/details.aspx?id=46703) from Surface Tools for IT and install it on a separate PC.</span></span> <span data-ttu-id="b061b-132">Descargar [drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2. MSI](https://www.microsoft.com/download/details.aspx?id=101974) y guárdelo para usarlo en el paso 5.</span><span class="sxs-lookup"><span data-stu-id="b061b-132">Download [Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 .MSI file](https://www.microsoft.com/download/details.aspx?id=101974) and save it for use in Step 5.</span></span> |
| <span data-ttu-id="b061b-133">2</span><span class="sxs-lookup"><span data-stu-id="b061b-133">3</span></span> | [<span data-ttu-id="b061b-134">Preparar certificado SEMM</span><span class="sxs-lookup"><span data-stu-id="b061b-134">Prepare SEMM certificate</span></span>](#prepare-semm-certificate)                                                                          | <span data-ttu-id="b061b-135">Prepara el certificado necesario para ejecutar el configurador de Surface UEFI o usa tu certificado actual.</span><span class="sxs-lookup"><span data-stu-id="b061b-135">Prepare required certificate for running Surface UEFI Configurator or use your current certificate.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b061b-136">cuatro</span><span class="sxs-lookup"><span data-stu-id="b061b-136">4</span></span> | [<span data-ttu-id="b061b-137">Crear paquete SEMM</span><span class="sxs-lookup"><span data-stu-id="b061b-137">Create SEMM package</span></span>](#create-semm-package)                                                                               | <span data-ttu-id="b061b-138">Inicie Surface configurador UEFI para crear un paquete SEMM en una unidad USB que contenga los archivos de configuración necesarios para aplicar en Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="b061b-138">Launch Surface UEFI Configurator to create a SEMM package on a USB drive which will contain the required configuration files to apply on Surface Hub 2S.</span></span> <span data-ttu-id="b061b-139">Copie estos archivos de paquete de SEMM en una carpeta de su equipo.</span><span class="sxs-lookup"><span data-stu-id="b061b-139">Copy these SEMM package  files to a folder on your PC.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="b061b-140">4</span><span class="sxs-lookup"><span data-stu-id="b061b-140">5</span></span> | [<span data-ttu-id="b061b-141">Preparar una unidad flash USB que contenga una imagen de Windows 10, un paquete SEMM y drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-141">Prepare USB flash drive containing Windows 10 image, SEMM package, and Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2</span></span>](#prepare-usb-flash-drive-containing-windows-10-image-semm-package-and-surface-hub-2-drivers-and-firmware) | <span data-ttu-id="b061b-142">Cree una única unidad USB (denominada **BOOTME** en este ejemplo) que contenga una imagen de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b061b-142">Create a single USB drive (named **BOOTME** in this example) containing a Windows 10 image.</span></span> <span data-ttu-id="b061b-143">Agregue sus drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2 (paso 2) y archivos de paquete SEMM (paso 4) a la unidad de **BOOTME** .</span><span class="sxs-lookup"><span data-stu-id="b061b-143">Add your Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 (Step 2) and SEMM package files (Step 4) to the **BOOTME** drive.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="b061b-144">6</span><span class="sxs-lookup"><span data-stu-id="b061b-144">6</span></span> | [<span data-ttu-id="b061b-145">Actualice UEFI en Surface Hub 2S para habilitar la migración del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b061b-145">Update UEFI on Surface Hub 2S to enable OS migration</span></span>](#update-uefi-on-surface-hub-2s-to-enable-os-migration)                                              | <span data-ttu-id="b061b-146">Use la unidad **BOOTME** para arrancar Surface Hub 2s en el menú UEFI e instale SEMM paquete.</span><span class="sxs-lookup"><span data-stu-id="b061b-146">Use the **BOOTME** drive to boot Surface Hub 2S to the UEFI menu and install SEMM package.</span></span>|
| <span data-ttu-id="b061b-147">siete</span><span class="sxs-lookup"><span data-stu-id="b061b-147">7</span></span> | [<span data-ttu-id="b061b-148">Instalar Windows 10 Pro o la versión Enterprise 1903 o posterior</span><span class="sxs-lookup"><span data-stu-id="b061b-148">Install Windows 10 Pro or Enterprise version 1903 or later</span></span>](#install-windows-10-pro-or-enterprise)                                        | <span data-ttu-id="b061b-149">Use la unidad **BOOTME** para instalar **Windows 10 Pro o Enterprise** versión 1903 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b061b-149">Use the **BOOTME** drive to Install **Windows 10 Pro or Enterprise** version 1903 or later.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b061b-150">4,8</span><span class="sxs-lookup"><span data-stu-id="b061b-150">8</span></span> | [<span data-ttu-id="b061b-151">Instalar drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-151">Install Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2</span></span>](#install-surface-hub-2-drivers-and-firmware)                                        | <span data-ttu-id="b061b-152">Para asegurarse de que el dispositivo tiene todas las actualizaciones y drivers más recientes, instale los [drivers y el firmware para Windows 10 Pro y Enterprise en Surface Hub 2. Archivo MSI](https://www.microsoft.com/download/details.aspx?id=101974)</span><span class="sxs-lookup"><span data-stu-id="b061b-152">To ensure your device has all the latest updates and drivers, install [Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 .MSI file](https://www.microsoft.com/download/details.aspx?id=101974)</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b061b-153">99,999</span><span class="sxs-lookup"><span data-stu-id="b061b-153">9</span></span> | [<span data-ttu-id="b061b-154">Configurar completamente Surface Hub 2S como dispositivo de productividad personal</span><span class="sxs-lookup"><span data-stu-id="b061b-154">Fully configure Surface Hub 2S as a personal productivity device</span></span>](#next-steps)                                        |  <span data-ttu-id="b061b-155">Habilite el conjunto de opciones y aplicaciones recomendadas para optimizar el uso de Surface Hub 2S como dispositivo de productividad personal.</span><span class="sxs-lookup"><span data-stu-id="b061b-155">Enable the set of recommended settings and applications to optimize use of Surface Hub 2S as a personal productivity device.</span></span>                                                                                                                                                                                                                                                                    |

### <span data-ttu-id="b061b-156">Comprobar si la versión de Surface Hub cumple con los requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="b061b-156">Verify UEFI version on Surface Hub 2S meets minimum requirements</span></span>

<span data-ttu-id="b061b-157">La versión mínima de UEFI requerida antes de migrar Surface Hub de Windows 10 Team a Windows 10 escritorio es **694.2938.768.0**.</span><span class="sxs-lookup"><span data-stu-id="b061b-157">The minimum UEFI version required prior to migrating the Surface Hub from Windows 10 Team to Windows 10 Desktop is **694.2938.768.0**.</span></span>
 
**<span data-ttu-id="b061b-158">Para comprobar la versión de UEFI actual en su sistema:</span><span class="sxs-lookup"><span data-stu-id="b061b-158">To verify the current UEFI version on your system:</span></span>**

1. <span data-ttu-id="b061b-159">En la pantalla principal de Surface Hub 2S, seleccione **Inicio** y abra el **SurfaceApp** (toda la superficie de**aplicaciones**  >  **Surface**).</span><span class="sxs-lookup"><span data-stu-id="b061b-159">On Surface Hub 2S home screen, select **Start** and open the **SurfaceApp** (**All Apps** > **Surface**).</span></span>

1. <span data-ttu-id="b061b-160">Seleccione **la superficie** para mostrar información sobre el Surface Hub, incluida la versión actual de UEFI en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b061b-160">Select **Your Surface** to display information about the Surface Hub, including the current version of the UEFI on the device.</span></span> <span data-ttu-id="b061b-161">Si la versión de UEFI es **694.2938.768.0** o posterior, como se muestra a continuación, UEFI cumple con los requisitos para crear el paquete de SEMM para habilitar la migración del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b061b-161">If the UEFI version is **694.2938.768.0** or later as shown below, the UEFI is eligible for you to create the SEMM package to enable OS migration.</span></span>

   <span data-ttu-id="b061b-162">! [Abierto sur</span><span class="sxs-lookup"><span data-stu-id="b061b-162">![Open Sur</span></span>
1. <span data-ttu-id="b061b-163">Si la versión UEFI es anterior a la versión 6face de la aplicación & selecciona su Surface] (images/shm-fig1.png) 94.2938.768.0, tendrá que obtener una versión actual con Windows Update.</span><span class="sxs-lookup"><span data-stu-id="b061b-163">If the UEFI version is earlier than version 6face App & select Your Surface](images/shm-fig1.png) 94.2938.768.0, you will need to obtain a current version using Windows Update.</span></span>

**<span data-ttu-id="b061b-164">Para actualizar UEFI desde Windows Update:</span><span class="sxs-lookup"><span data-stu-id="b061b-164">To update UEFI from Windows Update:</span></span>**
1. <span data-ttu-id="b061b-165">En su Surface Hub 2S, inicie sesión como **Administrador**, vaya a configuración de **todas las aplicaciones**  >  **Settings** >  **actualizar y seguridad**  >  **Windows Update** e instale todas las actualizaciones y, a continuación, reinicie el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b061b-165">On your Surface Hub 2S, sign in as an **Admin**, go to **All apps** > **Settings**> **Update and Security** > **Windows Update** and install all updates, then restart the device.</span></span> <span data-ttu-id="b061b-166">Verifica la versión de UEFI con la aplicación Surface.</span><span class="sxs-lookup"><span data-stu-id="b061b-166">Verify the UEFI version using the Surface App.</span></span> <span data-ttu-id="b061b-167">Nota: Si no conoce el nombre de usuario o la contraseña de administrador, tendrá que restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b061b-167">Note: If you do not know your username or admin password, you will need to reset the device.</span></span> <span data-ttu-id="b061b-168">Para obtener más información, consulta [restablecer y recuperar en Surface Hub 2s](https://docs.microsoft.com/surface-hub/surface-hub-2s-recover-reset).</span><span class="sxs-lookup"><span data-stu-id="b061b-168">To learn more, see [Reset and recovery for Surface Hub 2S](https://docs.microsoft.com/surface-hub/surface-hub-2s-recover-reset).</span></span>

2. <span data-ttu-id="b061b-169">Repita estos pasos hasta que la versión de UEFI sea **694.2938.768.0** o posterior.</span><span class="sxs-lookup"><span data-stu-id="b061b-169">Repeat these steps until the UEFI version is **694.2938.768.0** or later.</span></span>

3. <span data-ttu-id="b061b-170">Si sigue sin ver el UEFI actualizado después de varios intentos, consulte el **historial de actualizaciones** y busque las instancias de errores de instalación de firmware.</span><span class="sxs-lookup"><span data-stu-id="b061b-170">If you still do not see the updated UEFI after multiple attempts, check **Update History** and look for any instances of failed firmware installations.</span></span> <span data-ttu-id="b061b-171">Es posible que tenga que restablecer el dispositivo (actualización de**configuración**  >  **&**  >  **dispositivo de restablecimiento**de seguridad).</span><span class="sxs-lookup"><span data-stu-id="b061b-171">You may need to reset your device (**Settings** > **Update & security** > **Reset device**).</span></span>

### <span data-ttu-id="b061b-172">Descargar el configurador de Surface UEFI y los drivers y firmware de Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-172">Download Surface UEFI Configurator and Surface Hub 2 Drivers and Firmware</span></span>

<span data-ttu-id="b061b-173">En un PC diferente:</span><span class="sxs-lookup"><span data-stu-id="b061b-173">On a separate PC:</span></span>

- <span data-ttu-id="b061b-174">Descarga e instala el [configurador Microsoft Surface UEFI](https://www.microsoft.com/download/details.aspx?id=46703) desde herramientas de Surface para ti.</span><span class="sxs-lookup"><span data-stu-id="b061b-174">Download and install Microsoft [Surface UEFI Configurator](https://www.microsoft.com/download/details.aspx?id=46703) from Surface Tools for IT.</span></span> <span data-ttu-id="b061b-175">El configurador de Surface UEFI no se puede ejecutar en Surface Hub 2S, mientras esté instalado el equipo con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b061b-175">Surface UEFI Configurator cannot be run on Surface Hub 2S, while Windows 10 Team is installed.</span></span>

- <span data-ttu-id="b061b-176">Descarga [los drivers y el instalador de Windows de Surface Hub 2. Archivo MSI](https://www.microsoft.com/download/details.aspx?id=101974) que se debe aplicar al instalar el nuevo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b061b-176">Download [Surface Hub 2 Drivers and Firmware Windows Installer .MSI file](https://www.microsoft.com/download/details.aspx?id=101974) to be applied when installing the new operating system.</span></span>

### <span data-ttu-id="b061b-177">Preparar certificado SEMM</span><span class="sxs-lookup"><span data-stu-id="b061b-177">Prepare SEMM certificate</span></span>

<span data-ttu-id="b061b-178">Si esta es la primera vez que usa el configurador de Surface UEFI, tendrá que preparar un certificado.</span><span class="sxs-lookup"><span data-stu-id="b061b-178">If this is your first time using Surface UEFI Configurator, you’ll need to prepare a certificate.</span></span> <span data-ttu-id="b061b-179">Este certificado garantiza que después de que un dispositivo se haya inscrito en SEMM, solo se podrán usar los paquetes creados con el certificado aprobado para modificar la configuración de UEFI.</span><span class="sxs-lookup"><span data-stu-id="b061b-179">This certificate ensures that after a device is enrolled in SEMM, only packages created with the approved certificate can be used to modify UEFI settings.</span></span> <span data-ttu-id="b061b-180">La forma de adquirir un certificado puede variar según el tamaño o la complejidad de su organización:</span><span class="sxs-lookup"><span data-stu-id="b061b-180">How you acquire a certificate may vary depending on the size or complexity of your organization:</span></span>

- <span data-ttu-id="b061b-181">Las organizaciones empresariales de gran tamaño suelen mantener su propia infraestructura de certificados para generar certificados por prácticas de seguridad estándar.</span><span class="sxs-lookup"><span data-stu-id="b061b-181">Large enterprise organizations typically maintain their own certificate infrastructure to generate certificates per standard security practices.</span></span>

- <span data-ttu-id="b061b-182">Las empresas medianas y otras pueden optar por obtener un certificado de proveedores de terceros.</span><span class="sxs-lookup"><span data-stu-id="b061b-182">Medium-sized businesses and others may choose to obtain a certificate from third party providers.</span></span> <span data-ttu-id="b061b-183">Esta es la opción recomendada para organizaciones sin suficiente experiencia de ti o equipo de seguridad de TI dedicado.</span><span class="sxs-lookup"><span data-stu-id="b061b-183">This is the recommended option for organizations without sufficient IT expertise or dedicated IT security team.</span></span>

- <span data-ttu-id="b061b-184">Como alternativa, puede generar un certificado autofirmado con un script de PowerShell por la siguiente documentación: [requisitos de certificados del modo de administración de Enterprise Surface](https://docs.microsoft.com/surface/surface-enterprise-management-mode#surface-enterprise-management-mode-certificate-requirements).</span><span class="sxs-lookup"><span data-stu-id="b061b-184">Alternatively, you can generate a self-signed certificate with a PowerShell script per the following documentation: [Surface Enterprise Management Mode certificate requirements](https://docs.microsoft.com/surface/surface-enterprise-management-mode#surface-enterprise-management-mode-certificate-requirements).</span></span> <span data-ttu-id="b061b-185">También puede usar PowerShell para crear su propio certificado por la siguiente documentación: [New-SelfSignedCertificate](https://docs.microsoft.com/powershell/module/pkiclient/new-selfsignedcertificate?view=win10-ps).</span><span class="sxs-lookup"><span data-stu-id="b061b-185">Or use PowerShell to create your own certificate per the following documentation: [New-SelfSignedCertificate](https://docs.microsoft.com/powershell/module/pkiclient/new-selfsignedcertificate?view=win10-ps).</span></span>

<span data-ttu-id="b061b-186">El paquete SEMM se debe proteger con un certificado para comprobar la firma de los archivos de configuración antes de que se pueda aplicar la configuración de UEFI.</span><span class="sxs-lookup"><span data-stu-id="b061b-186">The SEMM package must be secured with a certificate to verify the signature of configuration files before UEFI settings can be applied.</span></span> <span data-ttu-id="b061b-187">Para obtener más información, consulte la documentación del [modo de administración de Surface Enterprise](https://docs.microsoft.com/surface/surface-enterprise-management-mode) .</span><span class="sxs-lookup"><span data-stu-id="b061b-187">To learn more, see [Surface Enterprise Management Mode](https://docs.microsoft.com/surface/surface-enterprise-management-mode) documentation.</span></span>
 
 
### <span data-ttu-id="b061b-188">Crear paquete SEMM</span><span class="sxs-lookup"><span data-stu-id="b061b-188">Create SEMM package</span></span>

1. <span data-ttu-id="b061b-189">Abra el **configurador UEFI de superficie** y seleccione **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="b061b-189">Open **Surface UEFI Configurator** and select **Start**.</span></span>

   ![Configurador de Surface abierto UEFI](images/shm-fig2.png)
   
2. <span data-ttu-id="b061b-191">Seleccione **Surface Devices** y, después, **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-191">Select **Surface Devices** and then select **Next**.</span></span>

   ![Seleccionar dispositivos de Surface](images/shm-fig3.png)
  
3. <span data-ttu-id="b061b-193">Seleccione **paquete de configuración**.</span><span class="sxs-lookup"><span data-stu-id="b061b-193">Select **Configuration Package**.</span></span>

   ![Seleccionar paquete de configuración](images/shm-fig4.png)
  
4. <span data-ttu-id="b061b-195">Seleccione **protección de certificado**.</span><span class="sxs-lookup"><span data-stu-id="b061b-195">Select **Certificate Protection**.</span></span>

   ![Seleccionar protección de certificado](images/shm-fig5.png)

5. <span data-ttu-id="b061b-197">Se le pedirá que agregue el archivo Certificate. pfx.</span><span class="sxs-lookup"><span data-stu-id="b061b-197">You will be prompted to add your certificate .pfx file.</span></span>

   ![Se le pedirá que agregue su certificado](images/shm-fig6.png)
   
6. <span data-ttu-id="b061b-199">Escriba la **contraseña del certificado** y seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b061b-199">Enter your **Certificate password** and select **OK**.</span></span>

   ![Escriba la contraseña del certificado y seleccione Aceptar.](images/shm-fig7.png)

7. <span data-ttu-id="b061b-201">Seleccione **protección con contraseña** para agregar una contraseña a Surface UEFI.</span><span class="sxs-lookup"><span data-stu-id="b061b-201">Select **Password Protection** to add a password to Surface UEFI.</span></span> <span data-ttu-id="b061b-202">Esta contraseña será obligatoria cada vez que arranques en UEFI.</span><span class="sxs-lookup"><span data-stu-id="b061b-202">This password will be required whenever you boot to UEFI.</span></span> <span data-ttu-id="b061b-203">Es **muy recomendable** establecer una contraseña de UEFI que usarás en Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="b061b-203">It is **strongly recommended** to set a UEFI password you will use on Surface Hub 2S.</span></span>

   ![Haga clic en protección con contraseña](images/shm-fig8.png)
   
8. <span data-ttu-id="b061b-205">Establezca una **contraseña de UEFI** y seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b061b-205">Set a **UEFI password** and select **OK**.</span></span>

   ![Escribe tu contraseña de UEFI](images/shm-fig9.png)

   > [!IMPORTANT]
   > <span data-ttu-id="b061b-207">Tome nota de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b061b-207">Make a note of your password.</span></span> <span data-ttu-id="b061b-208">Si olvidas o pierdes tu contraseña, no hay proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="b061b-208">If you forget or lose your password, there is no recovery process.</span></span> 

9. <span data-ttu-id="b061b-209">Seleccione **Surface Hub 2s** y, a continuación, seleccione **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-209">Select **Surface Hub 2S** and then select **Next**.</span></span>

   ![Seleccionar Surface Hub 2S](images/shm-fig10.png)
   
10. <span data-ttu-id="b061b-211">Selecciona **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-211">Select **Next**.</span></span>

    ![Seleccione siguiente](images/shm-fig10a.png)

11. <span data-ttu-id="b061b-213">Para permitir la instalación de Windows 10 Pro o Enterprise, seleccione **EnableOsMigration.**</span><span class="sxs-lookup"><span data-stu-id="b061b-213">To allow installation of Windows 10 Pro or Enterprise, select **EnableOsMigration.**</span></span>

    ![Seleccione habilitar la migración del sistema operativo](images/shm-fig11.png)
    
12. <span data-ttu-id="b061b-215">Establezca **EnableOSMigration** en **on (encendido** ) y seleccione **Next (siguiente**).</span><span class="sxs-lookup"><span data-stu-id="b061b-215">Set **EnableOSMigration** to **On** and select **Next**.</span></span>

    ![Establecer habilitar la migración del sistema operativo en activado](images/shm-fig12.png)

> [!NOTE]
> <span data-ttu-id="b061b-217">Después de aplicar un paquete de SEMM, todos los ajustes de UEFI aparecerán en gris (bloqueado) en el menú de UEFI del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b061b-217">After you apply a SEMM package, all UEFI settings will display as grayed out (locked) in the UEFI menu on the device.</span></span> <span data-ttu-id="b061b-218">Esto incluye los valores predeterminados para otras opciones, como IPv6 para el arranque PXE.</span><span class="sxs-lookup"><span data-stu-id="b061b-218">This includes default values for other settings such as IPv6 for PXE Boot.</span></span> <span data-ttu-id="b061b-219">Para modificar la configuración de UEFI, tendrá que aplicar otro paquete de SEMM o anular la inscripción del dispositivo de SEMM.</span><span class="sxs-lookup"><span data-stu-id="b061b-219">To modify UEFI settings, you will need to apply another SEMM package or unenroll the device from SEMM.</span></span>

#### <span data-ttu-id="b061b-220">Guardar el paquete SEMM en la unidad USB</span><span class="sxs-lookup"><span data-stu-id="b061b-220">Save SEMM package to USB drive</span></span>

1. <span data-ttu-id="b061b-221">Conecte una unidad USB a su PC.</span><span class="sxs-lookup"><span data-stu-id="b061b-221">Connect a USB Drive to your PC.</span></span> <span data-ttu-id="b061b-222">Elija **Hub 2** y, después, **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-222">Choose **Hub 2S** and then select **Next**.</span></span>

   ![Seleccionar USB](images/shm-fig13.png)
   
2. <span data-ttu-id="b061b-224">Seleccione **generar**.</span><span class="sxs-lookup"><span data-stu-id="b061b-224">Select **Build**.</span></span>

   ![Seleccionar compilación](images/shm-fig14.png)

3. <span data-ttu-id="b061b-226">Capture una captura de pantalla de esta página y, a continuación, seleccione **fin**.</span><span class="sxs-lookup"><span data-stu-id="b061b-226">Capture a screenshot of this page and then select **End**.</span></span> <span data-ttu-id="b061b-227">El paquete SEMM está listo y contiene el paquete SEMM **DfciUpdate. DFI** y un archivo de texto con la huella digital SEMM (los dos últimos caracteres de la huella digital del certificado).</span><span class="sxs-lookup"><span data-stu-id="b061b-227">Your SEMM package is now ready and contains the SEMM package **DfciUpdate.dfi** and a text file with the SEMM thumbprint (the last two characters of the certificate’s thumbprint).</span></span>

   ![Seleccione fin](images/shm-fig15.png)
   
4. <span data-ttu-id="b061b-229">Guarde los 2 últimos caracteres de la huella digital del certificado, que es necesario para activar SEMM al aplicar el paquete en Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="b061b-229">Save the certificate thumbprint’s last 2 characters, which is required to activate SEMM when you apply the package on Surface Hub 2S.</span></span>

### <span data-ttu-id="b061b-230">Preparar una unidad flash USB que contenga la imagen de Windows 10, el paquete SEMM y el firmware y los drivers de Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-230">Prepare USB flash drive containing Windows 10 image, SEMM package, and Surface Hub 2 Drivers and Firmware</span></span>

<span data-ttu-id="b061b-231">Puede instalar una imagen de Windows 10 Pro o Enterprise (versión 1903 o posterior) con una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="b061b-231">You can install a Windows 10 Pro or Enterprise image (version 1903 or later) using one of the following options:</span></span>

- <span data-ttu-id="b061b-232">La solución de imagen actual.</span><span class="sxs-lookup"><span data-stu-id="b061b-232">Your current imaging solution.</span></span>

- <span data-ttu-id="b061b-233">El [acelerador de implementación de Surface](https://docs.microsoft.com/surface/microsoft-surface-deployment-accelerator) le permite crear una imagen de Windows 10 de arranque que puede incluir todas las actualizaciones actuales de Windows 10, Office, otras aplicaciones de su elección, así como los drivers y el firmware requeridos.</span><span class="sxs-lookup"><span data-stu-id="b061b-233">[Surface Deployment Accelerator](https://docs.microsoft.com/surface/microsoft-surface-deployment-accelerator) lets you create a bootable Windows 10 image which can include all of the current Windows 10 updates, Office, other apps of your choice, as well as the required drivers and firmware.</span></span> 

- <span data-ttu-id="b061b-234">Unidad flash USB con imagen de Windows 10 Pro o Enterprise seguida de la instalación de  [drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2](https://www.microsoft.com/download/details.aspx?id=101974).</span><span class="sxs-lookup"><span data-stu-id="b061b-234">USB flash drive with Windows 10 Pro or Enterprise image, followed by installing  [Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2](https://www.microsoft.com/download/details.aspx?id=101974).</span></span>
 

<span data-ttu-id="b061b-235">Este procedimiento describe la creación de una unidad flash USB desde medios de instalación y, después, la incorporación de los archivos y los drivers y el firmware de SEMM para Windows 10 Pro y Enterprise en Surface Hub 2. Archivo MSI.</span><span class="sxs-lookup"><span data-stu-id="b061b-235">This procedure describes creating a USB flash drive from installation media and then adding the SEMM package files and Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 .MSI file.</span></span> <span data-ttu-id="b061b-236">Si usa otros métodos de implementación, continúe con la siguiente sección: [actualice UEFI en Surface Hub 2S para habilitar la migración del sistema operativo](#update-uefi-on-surface-hub-2s-to-enable-os-migration).</span><span class="sxs-lookup"><span data-stu-id="b061b-236">If you’re using other deployment methods, proceed to the following section: [Update UEFI on Surface Hub 2S to enable OS migration](#update-uefi-on-surface-hub-2s-to-enable-os-migration).</span></span>

> [!NOTE]
> <span data-ttu-id="b061b-237">Una vez instalado, necesitarás una licencia válida para Windows 10 Pro o Windows 10 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b061b-237">Once installed, you will need a valid license for Windows 10 Pro or Windows 10 Enterprise.</span></span>

1. <span data-ttu-id="b061b-238">Para crear una instalación de Windows 10 Pro, siga las instrucciones de la página [Descargar Windows 10](https://www.microsoft.com/software-download/windows10) para usar la herramienta de **creación de medios** .</span><span class="sxs-lookup"><span data-stu-id="b061b-238">To create a Windows 10 Pro installation, follow the instructions on the [Download Windows 10](https://www.microsoft.com/software-download/windows10) page for using the **Media Creation** tool.</span></span> <span data-ttu-id="b061b-239">Para descargar Windows 10 Enterprise, vaya al [centro de servicios de licencias por volumen de Microsoft.](https://www.microsoft.com/licensing/servicecenter/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="b061b-239">To download Windows 10 Enterprise, go to the [Microsoft Volume Licensing Service Center.](https://www.microsoft.com/licensing/servicecenter/default.aspx).</span></span>

2. <span data-ttu-id="b061b-240">Inserte una nueva unidad de **almacenamiento USB** .</span><span class="sxs-lookup"><span data-stu-id="b061b-240">Insert a new **USB storage** drive.</span></span> <span data-ttu-id="b061b-241">Inicie la herramienta de **creación de medios** , seleccione **crear medios de instalación** y, después, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-241">Launch the **Media Creation** tool, select **Create installation media** and then select **Next**.</span></span>

   ![Crear medios de instalación](images/shm-fig16.png)
   
3. <span data-ttu-id="b061b-243">Seleccione el idioma, Windows 10 y 64 bits (x64) y, a continuación, seleccione **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-243">Select language, Windows 10, and 64-bit (x64) and then select **Next**.</span></span>

   ![Seleccione el idioma, Windows 10 y 64 bits & Seleccione siguiente](images/shm-fig17.png)
   
4. <span data-ttu-id="b061b-245">Seleccione **unidad flash USB** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b061b-245">Select **USB flash drive** and select **Next**.</span></span>

   ![Seleccione unidad flash USB y, a continuación, siguiente](images/shm-fig18.png)
   
5. <span data-ttu-id="b061b-247">Una vez completada la descarga, seleccione **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="b061b-247">When the download completes, select **Finish**.</span></span>

   ![Seleccione finalizar](images/shm-fig19.png)
   
6. <span data-ttu-id="b061b-249">Copie los archivos y los drivers y firmware de SEMM para Windows 10 Pro y Enterprise en Surface Hub 2. MSI a la unidad flash USB (**BOOTME**) que contiene la imagen de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="b061b-249">Copy the SEMM package files and Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 .MSI to the USB flash drive (**BOOTME**) containing your Windows 10 image:</span></span>

    - <span data-ttu-id="b061b-250">DfciUpdate. DFI</span><span class="sxs-lookup"><span data-stu-id="b061b-250">DfciUpdate.dfi</span></span>
    - <span data-ttu-id="b061b-251">Archivo de texto con la huella digital SEMM.</span><span class="sxs-lookup"><span data-stu-id="b061b-251">Text file with the SEMM thumbprint.</span></span> <span data-ttu-id="b061b-252">(En este ejemplo: SurfaceUEFI_2020Aug25_1058.txt)</span><span class="sxs-lookup"><span data-stu-id="b061b-252">(In this example: SurfaceUEFI_2020Aug25_1058.txt)</span></span>
    - <span data-ttu-id="b061b-253">Drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2 (SurfaceHub2S_Win10_18362_20.082.25682.0.msi)</span><span class="sxs-lookup"><span data-stu-id="b061b-253">Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 (SurfaceHub2S_Win10_18362_20.082.25682.0.msi)</span></span>

### <span data-ttu-id="b061b-254">Actualice UEFI en Surface Hub 2S para habilitar la migración del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b061b-254">Update UEFI on Surface Hub 2S to enable OS migration</span></span>

<span data-ttu-id="b061b-255">Use la unidad de **BOOTME** para instalar los archivos del paquete SEMM y actualizar el UEFI, habilitando Surface hub para que ejecute Windows 10 Pro o Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b061b-255">Use your **BOOTME** drive to install the SEMM package files and update the UEFI, enabling Surface Hub to run Windows 10 Pro or Enterprise.</span></span> <span data-ttu-id="b061b-256">Después, inicia desde la unidad **BOOTME** para instalar Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b061b-256">Then boot from the **BOOTME** drive to install Windows 10.</span></span>

1. <span data-ttu-id="b061b-257">Inserte la unidad de **BOOTME** que contiene SEMM archivos de paquete, drivers y firmware para Windows 10 Pro y Enterprise en Surface Hub 2. MSI y Windows 10 instalar archivos en el puerto USB: un puerto en Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="b061b-257">Insert your **BOOTME** drive containing SEMM package files, Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2 .MSI, and Windows 10 install files into the USB-A port on Surface Hub 2S.</span></span>  

2. <span data-ttu-id="b061b-258">Para arrancar en UEFI:</span><span class="sxs-lookup"><span data-stu-id="b061b-258">To boot into UEFI:</span></span>

   1. <span data-ttu-id="b061b-259">Primer apagado (apagado) de Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="b061b-259">First power off (shutdown) your Surface Hub 2S.</span></span>
   1. <span data-ttu-id="b061b-260">Mantén pulsado el **volumen +** y, a continuación, pulsa y suelta el botón de **encendido** .</span><span class="sxs-lookup"><span data-stu-id="b061b-260">Press and hold **Volume +** and then press and release the **Power** button.</span></span>
   1. <span data-ttu-id="b061b-261">Mantenga pulsado **volumen +** hasta que aparezca el menú UEFI.</span><span class="sxs-lookup"><span data-stu-id="b061b-261">Keep holding **Volume +** until the UEFI menu appears.</span></span>
   
      ![Mantener en espera el volumen hasta que aparezca el menú UEFI](images/shm-fig20.png)
      
3. <span data-ttu-id="b061b-263">Cuando se reinicie el dispositivo, escriba la contraseña de UEFI que creó anteriormente, si procede (muy recomendable).</span><span class="sxs-lookup"><span data-stu-id="b061b-263">When the device restarts, enter the UEFI password you created earlier, if applicable (strongly recommended).</span></span>

   ![Cuando se reinicie el dispositivo, escribe tu paassword UEFI](images/shm-fig22.png)
   
4. <span data-ttu-id="b061b-265">En el menú UEFI, seleccione **Management**  >  **instalación de administración desde USB**.</span><span class="sxs-lookup"><span data-stu-id="b061b-265">In the UEFI menu, select **Management** > **Install from USB**.</span></span>

   ![Seleccionar administración & instalar desde USB](images/shm-fig21.png)
   
5. <span data-ttu-id="b061b-267">Seleccione **reiniciar ahora**, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="b061b-267">Select **Restart now**, as shown below.</span></span> <span data-ttu-id="b061b-268">El dispositivo se cerrará.</span><span class="sxs-lookup"><span data-stu-id="b061b-268">The device will shut down.</span></span>

   ![Seleccione reiniciar ahora](images/shm-fig25.png)
   
6. <span data-ttu-id="b061b-270">Pulsa y suelta el botón de encendido, aparece una pantalla roja que te pide que actives el modo de administración de Surface Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b061b-270">Press and release the power button, a red screen will display prompting you to activate Surface Enterprise Management Mode.</span></span> 

7. <span data-ttu-id="b061b-271">Escriba la **huella digital del certificado**de dos caracteres, la **contraseña de configuración de UEFI** y, después, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b061b-271">Enter your two-character **certificate thumbprint**, your **UEFI settings password** and then select **OK**.</span></span>

   ![Escribe tu huella digital de certificado de 2 caracteres](images/shm-fig23.png)
 
   > [!NOTE]
   > <span data-ttu-id="b061b-273">Una vez que actives SEMM en tu dispositivo, se aplicará la nueva **EnableOSMigration** de configuración UEFI.</span><span class="sxs-lookup"><span data-stu-id="b061b-273">Once you activate SEMM on your device, the new UEFI setting **EnableOSMigration** is applied.</span></span> <span data-ttu-id="b061b-274">Ya no podrás acceder al equipo de Windows 10 y deberás continuar con el siguiente paso e instalar Windows 10 Pro o Windows 10 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b061b-274">You will no longer be able to access Windows 10 Team and must proceed to the next step and install Windows 10 Pro or Windows 10 Enterprise.</span></span> 

8. <span data-ttu-id="b061b-275">El dispositivo se reiniciará, se mostrará el blanco de 4 cuadrados en el centro de la pantalla y, a continuación, se desactivará.</span><span class="sxs-lookup"><span data-stu-id="b061b-275">The device will reboot, display the white 4-square in the middle of the screen, and then again turn off.</span></span>

### <span data-ttu-id="b061b-276">Instalar Windows 10 Pro o Enterprise</span><span class="sxs-lookup"><span data-stu-id="b061b-276">Install Windows 10 Pro or Enterprise</span></span>

1. <span data-ttu-id="b061b-277">Si la unidad de inicio de Windows 10 Pro o de la empresa no está ya en el puerto Hub 2 USB-A, insértela ahora y, después, presione y suelte el botón de encendido.</span><span class="sxs-lookup"><span data-stu-id="b061b-277">If your bootable Windows 10 Pro or Enterprise drive is not already in the Surface Hub 2 USB-A port, insert it now and then press and release the power button.</span></span>

2. <span data-ttu-id="b061b-278">El dispositivo se iniciará, verá el blanco de 4 cuadrados en el centro de la pantalla y, a continuación, verá un círculo giratorio debajo del logotipo blanco de cuatro cuadrados.</span><span class="sxs-lookup"><span data-stu-id="b061b-278">The device will start, you will see the white 4-square in the middle of the screen, and then you will see a spinning circle below the white four-square logo.</span></span>

3. <span data-ttu-id="b061b-279">Si el dispositivo no arranca automáticamente en la unidad USB, apague el dispositivo (desenchufe el cable de alimentación y conéctelo de nuevo), pulse y suelte el botón de encendido y, después, mantenga presionado el botón bajar del volumen hasta que vea el círculo giratorio debajo del logotipo blanco de cuatro cuadrados.</span><span class="sxs-lookup"><span data-stu-id="b061b-279">If the device does not automatically boot to the USB drive, power off the device (unplug the power cord and plug it back in),  press and release the power button and then press and hold the volume down button until you see the spinning circle below the white four-square logo.</span></span>
 
   ![Arranque en Windows 10 desde USB](images/shm-fig26.png)
   
4. <span data-ttu-id="b061b-281">Cuando se inicie el programa de instalación de la configuración rápida (OOBE), siga las instrucciones para instalar Windows 10 Pro o Enterprise (versión 1903 o posterior).</span><span class="sxs-lookup"><span data-stu-id="b061b-281">When the out of box experience (OOBE) setup launches, follow the instructions to install Windows 10 Pro or Enterprise (version 1903 or later).</span></span>

### <span data-ttu-id="b061b-282">Instalar drivers y firmware de Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="b061b-282">Install Surface Hub 2 drivers and firmware</span></span>

 - <span data-ttu-id="b061b-283">Para asegurarse de que el dispositivo tiene todas las actualizaciones y drivers más recientes, instale los [drivers y el firmware para Windows 10 Pro y Enterprise en Surface Hub 2](https://www.microsoft.com/download/details.aspx?id=101974).</span><span class="sxs-lookup"><span data-stu-id="b061b-283">To ensure your device has all the latest updates and drivers, install [Drivers and Firmware for Windows 10 Pro and Enterprise on Surface Hub 2](https://www.microsoft.com/download/details.aspx?id=101974).</span></span>
 
### <span data-ttu-id="b061b-284">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="b061b-284">Next steps</span></span>

<span data-ttu-id="b061b-285">Para configurar Surface Hub 2S como dispositivo de productividad personal, consulte [configurar Windows 10 Pro o Enterprise en Surface Hub 2](surface-hub-2-post-install.md).</span><span class="sxs-lookup"><span data-stu-id="b061b-285">To fully configure Surface Hub 2S as a personal productivity device, see [Configure Windows 10 Pro or Enterprise on Surface Hub 2](surface-hub-2-post-install.md).</span></span>

> [!NOTE]
><span data-ttu-id="b061b-286">Si seguir los pasos descritos en este documento no se realiza correctamente al migrar el dispositivo a Windows 10 Pro o Enterprise para Surface Hub 2, póngase en contacto [con el soporte de Surface Hub](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support).</span><span class="sxs-lookup"><span data-stu-id="b061b-286">If following the steps outlined in this document is unsuccessful in migrating your device to Windows 10 Pro or Enterprise for Surface Hub 2, please contact [Surface Hub Support](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support).</span></span>

