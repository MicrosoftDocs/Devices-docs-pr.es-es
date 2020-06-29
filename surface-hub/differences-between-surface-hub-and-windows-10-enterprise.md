---
title: Conceptos básicos del sistema operativo (Surface Hub)
description: En este tema, se explican los aspectos únicos del sistema operativo Windows 10 Team y cómo difiere de Windows 10 Enterprise.
keywords: historial de cambios
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 06/20/2019
ms.reviewer: ''
manager: laurawi
ms.localizationpriority: medium
ms.openlocfilehash: 92a634e897d3e0c9163fe092aaf7992f625de991
ms.sourcegitcommit: 109d1d7608ac4667564fa5369e8722e569b8ea36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/27/2020
ms.locfileid: "10835505"
---
# Conceptos básicos del sistema operativo (Surface Hub)

El sistema operativo de Surface Hub, Windows 10 Team, se basa en Windows 10 Enterprise y proporciona compatibilidad enriquecida para la administración empresarial, la seguridad y otras características. Sin embargo, hay importantes diferencias entre las dos versiones. Si bien la edición Enterprise está diseñada para equipos PC, Windows 10 Team está diseñado desde el principio para pantallas de gran tamaño y salas de reuniones. Al evaluar los requisitos de seguridad y administración de Surface Hub, es mejor considerarlo como un nuevo sistema operativo. Este artículo está diseñado para ayudar a destacar las diferencias clave entre Windows 10 Team en Surface Hub y Windows 10 Enterprise y qué significan las diferencias para las organizaciones.

## Interfaz de usuario

### Shell (interfaz de usuario del sistema operativo)

El shell de Surface Hub está diseñado desde el principio de modo optimizado para pantallas de gran tamaño y táctiles. No usa el mismo shell que Windows 10 Enterprise.

*Directivas de la organización que esto puede afectar:* <br> La configuración relacionada con los controles el shell de Windows 10 Enterprise no se aplica s Surface Hub.

### Protector de pantalla y pantalla de bloqueo

Surface Hub no tiene pantalla de bloqueo ni protector de pantalla, pero tiene una característica similar denominada la pantalla de inicio de sesión. La pantalla de inicio muestra las reuniones programadas el calendario de la cuenta del dispositivo y puntos de entrada fácil a las aplicaciones principales de Surface Hub - Skype Empresarial, la Pizarra interactiva y Conectar.

*Directivas de la organización que esto puede afectar:* <br> La configuración de la pantalla de bloqueo, el tiempo de espera de pantalla y el protector de pantalla no se aplican a Surface Hub.

### Inicio de sesión de usuario

Surface Hub está diseñado para usarse en espacios comunes, como las salas de reunión. A diferencia de los equipos con Windows, cualquier persona puede acercarse y usar Surface Hub sin iniciar sesión. Para habilitar esta funcionalidad común, Surface Hub no admite el inicio de sesión de Windows, mientras que Windows 10 Enterprise sí lo permite (por ejemplo, iniciar sesión con un usuario en el sistema operativo y usar esas credenciales en todo el sistema operativo). En su lugar, siempre hay un usuario local conectado automáticamente y con privilegios bajos que ha iniciado sesión en Surface Hub. No es compatible con el inicio de sesión de cualquier usuario adicional, incluyendo los usuarios administradores (por ejemplo, cuando un usuario administrador inicia sesión, no han iniciado sesión en el sistema operativo).

Los usuarios pueden iniciar sesión en Surface Hub, pero no iniciarán sesión en el sistema operativo. Por ejemplo, cuando un usuario inicia sesión en Aplicaciones o Mi reuniones y archivos, solo tiene acceso a las aplicaciones o servicios, no al sistema operativo. Como resultado, el usuario que inició sesión es capaz de recuperar sus archivos y reuniones personales almacenadas de la nube, y estas credenciales se descartan al activar **Finalizar sesión**.


*Directivas de la organización que esto puede afectar:* <br> Por lo general, Surface Hub usa características de bloqueo en lugar del control de acceso de usuario para aplicar la seguridad. Las directivas relacionadas con los requisitos de contraseña, el inicio de sesión interactivo, las cuentas de usuario y el control de acceso no se aplican a Surface Hub.

### Guardar y explorar archivos

Los usuarios tienen acceso a un conjunto limitado de directorios en Surface Hub:
- Música
- Vídeos
- Documentos
- Imágenes
- Descargas

Los archivos que se guardan localmente en estos directorios se eliminan cuando los usuarios presionen **Terminar la sesión**. Para guardar contenido creado durante una reunión, los usuarios deben guardar los archivos en una unidad USB o en OneDrive.

*Directivas de la organización que esto puede afectar:* <br> Las directivas relacionadas con los permisos de acceso y la posesión de los archivos y las carpetas no se aplican a Surface Hub. Los usuarios no pueden explorar ni guardar archivos en directorios del sistema ni carpetas de red.

## Aplicaciones

### Aplicaciones predeterminadas

Con pocas excepciones, las aplicaciones predeterminadas para la Plataforma universal de Windows (UWP) de Surface Hub también están disponibles en los equipos con Windows 10.

Aplicaciones para UWP instaladas previamente en Surface Hub:
- Alarmas y reloj
- Calculadora
- Conectar
- Excel Mobile
- Centro de opiniones
- Explorador de archivos*
- Introducción
- Mapas
- Microsoft Edge
- Microsoft Power BI
- OneDrive
- Fotos
- PowerPoint Mobile
- Configuración*
- Skype Empresarial*
- Tienda
- Pizarra interactiva*
- Word Mobile

*Las aplicaciones con un asterisco (&ast;) son exclusivas de Surface Hub*

*Directivas de la organización que esto puede afectar:* <br> Usa las directrices de Windows 10 Enterprise para determinar las características y los requisitos de red de las aplicaciones predeterminadas en Surface Hub.

### Instalar aplicaciones, controladores y servicios

Para ayudar a mantener la naturaleza del dispositivo, Surface Hub solo admite la instalación de aplicaciones para la Plataforma universal de Windows (UWP) y no admite la instalación de aplicaciones, servicios ni controladores clásicos de Win32. Asimismo, solo los administradores tienen acceso para instalar aplicaciones para UWP.

*Directivas de la organización que esto puede afectar:* <br> Los empleados solo pueden usar las aplicaciones que hayan instalado los administradores, lo que ayuda a mitigar contra un uso no intencionado. Surface Hub no admite la instalación de los agentes de Win32 que la mayoría de las herramientas de administración y supervisión de PC tradicionales.

## Seguridad y bloqueo

Para que Surface Hub se use en espacios comunes, como reuniones de las salas, su sistema operativo personalizado implementa muchas de las características de seguridad y bloqueo disponibles en Windows 10.

Surface Hub implementa las siguientes características de seguridad de Windows 10:
- [Arranque seguro de la UEFI](https://msdn.microsoft.com/windows/hardware/commercialize/manufacture/desktop/secure-boot-overview)
- [Integridad de código del modo de usuario (UMCI) con Device Guard](https://technet.microsoft.com/itpro/windows/keep-secure/introduction-to-device-guard-virtualization-based-security-and-code-integrity-policies)
- [Directivas de restricción de aplicaciones con AppLocker](https://technet.microsoft.com/itpro/windows/keep-secure/applocker-overview)
- [Cifrado de unidad BitLocker](https://technet.microsoft.com/itpro/windows/keep-secure/bitlocker-overview)
- [Módulo de plataforma segura (TPM)](https://technet.microsoft.com/itpro/windows/keep-secure/trusted-platform-module-overview)
- [Windows Defender](https://technet.microsoft.com/itpro/windows/keep-secure/windows-defender-in-windows-10)
- [Control de cuentas de usuario (UAC)](https://technet.microsoft.com/itpro/windows/keep-secure/user-account-control-overview) para acceder a la aplicación Configuración

Las siguientes características de Surface Hub proporcionan seguridad adicional:
- Firmware UEFI personalizado
- El shell y el menú Inicio personalizados limitan al dispositivo a las funciones de reunión
- El Explorador de archivos personalizado solo concede acceso a los archivos y las carpetas de Mis documentos
- La aplicación Configuración personalizada solo permite a los administradores modificar la configuración del dispositivo
- La descarga de controladores Plug and Play avanzados está deshabilitada

*Directivas de la organización que esto puede afectar:* <br> Ten en cuenta las siguientes características al realizar la evaluación de seguridad de Surface Hub.

## Administración

### Configuración de dispositivo

Las opciones del dispositivo se pueden configurar a través de la aplicación Configuración. La aplicación Configuración está personalizada para Surface Hub, pero también contiene muchas de las opciones de configuración familiares de Windows 10 Escritorio. Un mensaje de Control de cuentas de usuario (UAC) aparece en la pantalla cuando se abre la aplicación Configuración para comprobar las credenciales del administrador, pero este proceso no inicia la sesión del administrador.

*Directivas de la organización que esto puede afectar:* <br> Los empleados pueden usar Surface Hub para reuniones, pero no pueden modificar las opciones de configuración del dispositivo. Además de las características de bloqueo, esto garantiza que los empleados solo usarán el dispositivo para las funciones de reunión.

### Características de administración

Las características administrativas de Windows 10 Enterprise, como Microsoft Management Console, Ejecutar, Símbolo del sistema, PowerShell, Editor del registro, Visor de eventos y Administrador de tareas administrativas, no se admiten en Surface Hub. La aplicación Configuración contiene todas las características administrativas disponibles localmente en Surface Hub.

*Directivas de la organización que esto puede afectar:* <br> Los dispositivos Surface Hub no se administran como equipos tradicionales. Usa MDM para configurar las opciones de configuración y OMS para supervisar Surface Hub.

### Administración y supervisión remotas

Surface Hub admite la administración remota a través de soluciones de administración de dispositivos móviles (MDM), como [Microsoft Intune](https://docs.microsoft.com/intune/) y supervisión a través de [Azure monitor](https://azure.microsoft.com/services/monitor/). 

*Directivas de la organización que esto puede afectar:* <br> Surface Hub no admite la instalación de los agentes de Win32 que requiere la mayoría de las herramientas de administración y supervisión de equipos tradicionales, como System Center Operations Manager.

### Directiva de grupo

Surface Hub no admite la Directiva de grupo de Windows, incluidas las auditorías. En su lugar, usa MDM para aplicar directivas a Surface Hub. Para obtener más información sobre MDM, consulta [Administrar la configuración con un proveedor de MDM (Surface Hub)](manage-settings-with-mdm-for-surface-hub.md).

*Directivas de la organización que esto puede afectar:* <br> Usa MDM para administrar Surface Hub en lugar de directivas de grupo.

### Asistencia remota

Surface Hub no admite la asistencia remota.

*Directivas de la organización que esto puede afectar:* <br> Las directivas relacionadas con la asistencia remota no se aplican a Surface Hub.

## Red

### Unirse a un dominio y unirse Azure Active Directory (Azure AD) 

Surface Hub usa la unión a un dominio y la unión a Azure AD principalmente para proporcionar un grupo de administradores respaldados por el directorio. Los usuarios no pueden iniciar sesión con una cuenta de dominio. Para obtener más información, consulta [Administración del grupo de administradores](admin-group-management-for-surface-hub.md).

*Directivas de la organización que esto puede afectar:* <br> Las directivas de grupo no se aplican cuando un dispositivo Surface Hub está unido al dominio. Las directivas relacionadas con la pertenencia a un dominio no se aplican a Surface Hub.

### Acceder a los recursos de dominio

Los usuarios pueden iniciar sesión en Microsoft Edge para acceder a sitios de intranet y recursos en línea (como Office 365). Si Surface Hub está configurado con una cuenta de dispositivo, el sistema la usa para acceder a Exchange y Skype Empresarial. Sin embargo, Surface Hub no admite el acceso a recursos de dominio, como recursos compartidos de archivos e impresoras.

*Directivas de la organización que esto puede afectar:* <br> Las directivas relacionadas con el acceso a objetos de dominio no se aplican a Surface Hub.

<!--
### Endpoints



*Organization policies that this may affect:* <br> 
-->

### Datos de diagnóstico

El sistema de operativo de Surface Hub usa el componente Experiencia del usuario y telemetría asociadas de Windows 10 para recopilar y transmitir datos de diagnóstico. Para obtener más información, consulta [Configurar los datos de diagnóstico de Windows en la organización](https://technet.microsoft.com/itpro/windows/manage/configure-windows-diagnostic-data-in-your-organization).

*Directivas de la organización que esto puede afectar:* <br> Configura los niveles de datos de diagnóstico de Surface Hub de la misma manera que lo harías para Windows 10 Enterprise.
