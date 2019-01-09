---
title: Az Azure PowerShell áttekintése
description: Az Azure PowerShell Az modul áttekintése, valamint a telepítéssel és az első lépésekkel kapcsolatos információk.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736460"
---
# <a name="overview-of-azure-powershell"></a>Az Azure PowerShell áttekintése

Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez. Az Azure PowerShell a .NET Standardet használja, így Windows, macOS és Linux rendszereken is elérhető.
Az Azure PowerShell az Azure Cloud Shellből is elérhető.

Az [Azure Cloud Shell-lel](/azure/cloud-shell/overview) futtassa az Azure PowerShellt a böngészőben, vagy [telepítse helyileg](install-az-ps.md). Az Azure PowerShell alapjainak megismeréséhez és az Azure használatának megkezdéséhez olvassa el az [első lépésekről](get-started-azureps.md) szóló cikket.

A legújabb Azure PowerShell-kiadással kapcsolatos információkért tekintse meg a [kiadási megjegyzéseket](release-notes-azureps.md).

## <a name="about-the-new-az-module"></a>Az új Az modul bemutatása

Ez a dokumentáció az Azure PowerShell új Az modulját ismerteti. Ez az új modul a .NET Standardre épül. A .NET Standard lehetővé teszi, hogy az Azure PowerShell Windows rendszeren a PowerShell 5.x, más platformon a PowerShell 6 verziójával fusson. Mostantól az Az modul az elsődleges módja Azure-ral való kommunikációnak a PowerShellen keresztül.
Az AzureRM-hez továbbra is elérhetőek lesznek hibajavítások, azonban nem bővül a továbbiakban új funkciókkal.

[Az Azure PowerShell Az modul bemutatása](new-azureps-module-az.md) című cikkben találja az új modul összes részletét, beleértve a parancsok új nevét és az AzureRM karbantartási terveit. Ha azonnal meg szeretné kezdeni az új modul használatát, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.

Emellett az [AzureRM dokumentációja](/powershell/azure/azurerm) is elérhető.

> [!IMPORTANT]
>
> Bár az Azure-dokumentációban az új modul parancsmagneveinek frissítése folyamatban van, előfordulhat, hogy a cikkek még az AzureRM-parancsokat használják. Az Az modul telepítése után ajánlott engedélyezni az AzureRM-parancsmagaliasokat az `Enable-AzureRmAlias` paranccsal. További részleteket [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető cikkben talál.

## <a name="common-scenarios"></a>Gyakori forgatókönyvek

A következő példák segítenek megismerkedni az Azure PowerShell általános forgatókönyveinek végrehajtásával:

* [Linux rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Windows rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL Database-adatbázisok](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a>A PowerShell alapjai

Ha még nem ismeri a PowerShellt, érdemes lehet megtekintenie a bemutatóját.

* [A PowerShell telepítése](/powershell/scripting/setup/installing-windows-powershell)
* [Parancsprogram-kezelés a PowerShell-lel](/powershell/scripting/powershell-scripting)

Az alábbi videót is megtekintheti: [A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).

Vagy részt vehet a Microsoft Virtual Academy a [PowerShell első lépéseit](https://mva.microsoft.com/liveevents/powershell-jumpstart) ismertető képzésén.

## <a name="build-your-skills-with-microsoft-learn"></a>Fejlessze a készségeit a Microsoft Learnnel

- [Azure-feladatok automatizálása szkriptek használatával a PowerShell-lel](/learn/modules/automate-azure-tasks-with-powershell/)
- [További interaktív oktatóanyagok...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Egyéb Azure PowerShell-modulok

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Information Protection](/powershell/azure/aip/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
