---
title: Novedades en Windows 10, versión 1703 para Surface Hub
description: Windows 10, versión 1703 (Creators Update) ofrece nuevas características a Microsoft Surface Hub.
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 01/18/2018
ms.reviewer: ''
manager: laurawi
ms.localizationpriority: medium
ms.openlocfilehash: 722309a6b018c32bde329cb7b2cdd68b859fc1ca
ms.sourcegitcommit: 8e809e8481023fe4421abcdaa1e055a6f2f74f5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2020
ms.locfileid: "10924946"
---
# ¿Qué novedades hay en Windows 10, versión 1703 para Microsoft Surface Hub?

Mira al ingeniero de Surface Hub, Jordan Marchese, presentar las actualizaciones de Microsoft Surface Hub con Windows 10, versión 1703 (Windows 10 Creators Update). 

<a href="https://www.youtube.com/watch?v=R8tX10VIgq0" target="_blank"> <img src="images/whats-new-video-thumbnail.png" alt="Link to Surface Hub video on Youtube" /></a>

Windows 10, versión 1703 (también denominada Creators Update), presenta los siguientes cambios para Microsoft Surface Hub.

## Nueva configuración

Se ha agregado configuración para la administración de dispositivos móviles (MDM) y los proveedores de servicios de configuración (CSP) para ampliar las capacidades de administración de Surface Hub. [La configuración incluye](manage-settings-with-mdm-for-surface-hub.md):

- InBoxApps/SkypeForBusiness/DomainName
- InBoxApps/Connect/AutoLaunch
- Properties/DefaultVolume
- Properties/ScreenTimeout
- Properties/SessionTimeout
- Properties/SleepTimeout
- Properties/AllowSessionResume
- Properties/AllowAutoProxyAuth
- Properties/DisableSigninSuggestions
- Properties/DoNotShowMyMeetingsAndFiles
- System/AllowStorageCard

Además de la configuración basada en el nuevo [CSP de NetworkQoSPolicy](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/networkqospolicy-csp) y [CSP de NetworkProxy](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/networkproxy-csp).
</br>

## Asistente de aprovisionamiento

Un asistente fácil de usar que ayuda a crear rápidamente paquetes de aprovisionamiento que se pueden aplicar a varios dispositivos Surface Hub e incluye la unión en bloque a Azure Active Directory. [Obtén información sobre cómo crear un paquete de aprovisionamiento para Surface Hub.](provisioning-packages-for-certificates-surface-hub.md)

![pasos del asistente para aprovisionamiento de dispositivos Surface Hub](images/wcd-wizard.png)
    
## Miracast en la red inalámbrica o LAN existente 

Microsoft ha ampliado la capacidad de [enviar una emisión de Miracast a través de una red local](miracast-over-infrastructure.md), en lugar de a través de un vínculo directo inalámbrico. 
    
## Recuperación en la nube

Cuando se restablece un dispositivo Surface Hub, ahora tienes la capacidad de descargar de la nube una compilación de fábrica del sistema operativo e instalarla. [Más información sobre la recuperación en la nube.](device-reset-surface-hub.md#cloud-recovery)

>[!NOTE]
>La recuperación en la nube no funciona si usas servidores proxy.
    
![Reinstalar](images/reinstall.png)
    
## Finalizar sesión

**He terminado** es ahora **Finalizar sesión**. [Aprende a usar Finalizar sesión.](finishing-your-surface-hub-meeting.md) 

![finalizar sesión](images/end-session.png)



 

 
