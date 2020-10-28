---
title: Instalar la versión preliminar de la actualización 2020 de Windows10 Team
description: La actualización más reciente del sistema operativo Surface Hub, Windows 10 Team 2020, ahora está disponible.
keywords: separar valores con comas
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 10/27/2020
ms.localizationpriority: Medium
ms.openlocfilehash: 6d370db0232ae1f93d1ba6b8ff15b5ff2cfa9f10
ms.sourcegitcommit: 19d2a78242777590bd09af3ac6552c07b032e0a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2020
ms.locfileid: "11142909"
---
# Instalar la versión preliminar de la actualización 2020 de Windows10 Team 

La versión preliminar del sistema operativo Surface Hub, **Windows 10 Team 2020 Update Preview**, está disponible sin cargo adicional por parte del [programa Windows Insider](https://insider.windows.com). 

> [!NOTE] 
> La versión final de la actualización de Windows 10 Team 2020 ahora está disponible. Para obtener más información, vea [Windows 10 Team 2020 Update](surface-hub-2020-update.md).

Windows 10 Team 2020 Update ofrece mejoras importantes en la implementación y administración de dispositivos junto con las características más recientes de Windows 10. Para obtener más información sobre las novedades, consulte la siguiente entrada de blog: [nueva actualización del sistema operativo de Surface Hub publicada para la versión preliminar pública.](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/new-surface-hub-os-update-released-for-public-preview/ba-p/1534823) Para obtener los problemas conocidos, consulte [problemas conocidos: actualización 2020 equipo de Windows 10](surface-hub-2020-team-update-known-issues.md)
 
## Requisitos previos

- Regístrate en el [programa Windows Insider](https://insider.windows.com/).
- Descargue la compilación vista previa de Windows 10 Team 2020 desde el canal rápido del programa Windows Insider.
- Después de instalar la versión preliminar, descargue las actualizaciones de firmware necesarias. Nota: las actualizaciones de firmware no se pueden desinstalar incluso si decide abandonar el programa Windows Insider.

## Preparar su Surface Hub

Antes de empezar, compruebe que su Surface Hub tenga las actualizaciones más recientes de Windows Update y asegúrese de que guarda la clave de BitLocker asociada con el dispositivo.

**Para buscar actualizaciones de forma manual:**

1. En Surface Hub, Abra **configuración** y escriba sus credenciales de administrador cuando se le solicite.
2. Vaya a **Actualizar & seguridad**de  >  **Windows Update** y, después, seleccione **Buscar actualizaciones**.

Para obtener más información, vea [administrar actualizaciones de Windows en Surface Hub](https://docs.microsoft.com/surface-hub/manage-windows-updates-for-surface-hub).

**Para guardar manualmente la clave de BitLocker:**

1. Inserte una unidad USB en Surface Hub.
2. En Surface Hub, Abra **configuración** y escriba sus credenciales de administrador cuando se le solicite.
3. Vaya a **Actualizar &** la  >  **recuperación**de seguridad.
4. En **BitLocker**, seleccione **Guardar**. La clave de BitLocker se guarda en un archivo de texto en la unidad USB.

Para obtener más información, vea [guardar la clave de BitLocker](https://docs.microsoft.com/surface-hub/save-bitlocker-key-surface-hub).
 
## Instalar la compilación de Windows 10 Team 2020 Update Preview

1. En Surface Hub, Abra **configuración** y escriba sus credenciales de administrador cuando se le solicite.
2. Navegue a la **privacidad > diagnósticos & comentarios** y establezca los datos de diagnóstico en **completo**. Es posible que algunas regiones o organizaciones necesiten aplicar esta configuración a través de la Directiva MDM o el archivo PPKG:
   - **Para MDM:** Establezca la siguiente directiva:. **/Vendor/msft/Policy/System/AllowTelemetry** con el valor entero 3:
    
        ![Establecer AllowTelemetry en 3](images/hub-2020-allow-telemetry.png)

    - **Para PPKG:** Descargue el [archivo PPKG](https://aka.ms/HubTltmtry).

3. Vaya a **Actualizar &** programa de seguridad de  >  **Windows Insider** y, a continuación, seleccione **Introducción** a la inscripción.
4. Siga las indicaciones para registrarse como Windows Insider con su cuenta profesional (recomendado) o con su cuenta personal de Microsoft. Para obtener más información sobre las ventajas de registrarse con su cuenta del trabajo, consulte [registrarse para el programa Windows Insider para empresas](https://docs.microsoft.com/windows-insider/at-work-pro/wip-4-biz-register).
5. En **elegir la configuración de Insider**, seleccione **rápido**.
6. Permitir que Surface Hub instale automáticamente la versión preliminar y las actualizaciones de firmware necesarias durante los próximos 3 a 4 días. El dispositivo descargará e instalará automáticamente las actualizaciones durante las [ventanas de mantenimiento](https://docs.microsoft.com/surface-hub/manage-windows-updates-for-surface-hub#maintenance-window)diario. Por ejemplo:

- Durante la primera ventana de mantenimiento, Surface Hub comienza a descargar la versión preliminar de Windows Update.
- Durante una segunda ventana de mantenimiento, el dispositivo se reinicia para completar la actualización.
- Durante una tercera ventana de mantenimiento, el dispositivo descarga e instala las actualizaciones de firmware necesarias.

> [!IMPORTANT]
> Microsoft recomienda reservar el Surface Hub durante 3-4 días para permitir que el dispositivo termine de instalar la versión preliminar y las actualizaciones de firmware necesarias. Es posible que se produzcan problemas de gráficos, audio y interfaz de usuario si usas el dispositivo durante este proceso.

### Si opta por instalar manualmente la compilación de vista previa y las actualizaciones de firmware necesarias:

1. Una vez que te hayas registrado con el programa Windows Insider, ve a **configuración**  >  **Update & seguridad**de  >  **Windows Update** y selecciona **Buscar actualizaciones** para instalar la versión preliminar.
2. Una vez que se instale la compilación de versión preliminar (puede demorar hasta 14 horas), seleccione **reiniciar ahora** para completar la instalación.
3. Después de que se reinicie el dispositivo, vaya a **configuración**  >  **Update & seguridad**de  >  **Windows Update**y seleccione **Buscar actualizaciones para instalar las actualizaciones de firmware necesarias**.
4. Una vez que el firmware se instale, seleccione **reiniciar ahora**.

> [!WARNING]
> Es posible que vea problemas de gráficos, audio y interfaz de usuario si instala la versión preliminar sin instalar las actualizaciones de firmware necesarias.

> [!NOTE]
> Si decides abandonar el programa Windows Insider y revertir tu Surface Hub a una versión anterior del sistema operativo, primero debes [restablecer el dispositivo](https://docs.microsoft.com/surface-hub/device-reset-surface-hub). Después, tendrá que pasar por el [primer programa](https://docs.microsoft.com/surface-hub/first-run-program-surface-hub) para volver a configurar el dispositivo.
 

## Obtén más información

- [Problemas conocidos: actualización de Windows 10 Team 2020](surface-hub-2020-team-update-known-issues.md)
- [Nueva actualización del sistema operativo Surface Hub publicada para la versión preliminar pública.](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/new-surface-hub-os-update-released-for-public-preview/ba-p/1534823)
- [Tareas iniciales con el programa Windows Insider para empresas](https://docs.microsoft.com/windows-insider/at-work-pro/wip-4-biz-manage)