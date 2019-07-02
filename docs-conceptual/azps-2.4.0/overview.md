---
title: Az Azure PowerShell áttekintése
description: Az Azure PowerShell Az modul áttekintése, valamint a telepítéssel és az első lépésekkel kapcsolatos információk.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 710decaf8fcc0ba57e1e978a665474047393adc7
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516623"
---
# <a name="overview-of-azure-powershell"></a>Az Azure PowerShell áttekintése

Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyek az [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modellt használják az Azure-erőforrások kezeléséhez. Az Azure PowerShell a .NET Standardet használja, így Windows, macOS és Linux rendszereken is elérhető.
Az Azure PowerShell az Azure Cloud Shellben is elérhető.

## <a name="about-the-new-az-module"></a>Az új Az modul bemutatása

Ez a dokumentáció az Azure PowerShell új Az modulját ismerteti. Ez az új modul a .NET Standardre épül. A .NET Standard lehetővé teszi, hogy az Azure PowerShell a Windows rendszeren a PowerShell 5.1-es, más platformon pedig a PowerShell Core 6.x vagy újabb verziójával fusson. Mostantól az Az modul az elsődleges módja Azure-ral való kommunikációnak a PowerShellen keresztül.
Az AzureRM-hez továbbra is elérhetőek lesznek hibajavítások, azonban nem bővül a továbbiakban új funkciókkal.

[Az Azure PowerShell Az modul bemutatása](new-azureps-module-az.md) című cikkben találja az új modul összes részletét, beleértve a parancsok új nevét és az AzureRM karbantartási terveit. Ha azonnal meg szeretné kezdeni az új modul használatát, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.

Emellett az [AzureRM dokumentációja](/powershell/azure/azurerm) is elérhető.

> [!IMPORTANT]
>
> Bár az Azure-dokumentációban az új modul parancsmagneveinek frissítése folyamatban van, előfordulhat, hogy a cikkek még az AzureRM-parancsokat használják. Az Az modul telepítése után ajánlott engedélyezni az AzureRM-parancsmagaliasokat az `Enable-AzureRmAlias` paranccsal. További részleteket [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető cikkben talál.

## <a name="run-or-install"></a>Futtatás vagy telepítés

Az Azure PowerShell telepíthető a PowerShell 5.1-es vagy újabb verzióján a Windows rendszeren, a PowerShell Core 6.x vagy újabb verzióján bármely platformon, vagy az Azure Cloud Shellben is futtatható.

* Ha böngészőben szeretné futtatni az Azure Cloud Shell használatával, tekintse meg a [PowerShell Azure Cloud Shellben való használatát bemutató rövid útmutatót](/azure/cloud-shell/quickstart-powershell).
* Ha szeretné a rendszerére telepíteni az Azure PowerShellt, tekintse meg az[ Azure PowerShell telepítése](install-az-ps.md) című cikket.

A legújabb Azure PowerShell-kiadással kapcsolatos információkért tekintse meg a [kiadási megjegyzéseket](release-notes-azureps.md).

## <a name="get-started"></a>Első lépések

Az Azure PowerShell alapjainak megismeréséhez olvassa el az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket. Ha még nem ismeri a PowerShellt, érdemes lehet megtekintenie a bemutatókat:

* [A PowerShell telepítése](/powershell/scripting/install/installing-powershell)
* [Parancsprogram-kezelés a PowerShell-lel](/powershell/scripting/powershell-scripting)
* [A PowerShell alapjai: (1. rész) Ismerkedés a PowerShell-lel](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* Microsoft Virtual Academy – [A PowerShell első lépéseit bemutató rövid ismertető](https://mva.microsoft.com/liveevents/powershell-jumpstart)

A következő példák segítségével megismerheti az Azure néhány gyakori használati esetét:

* [Linux rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Windows rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL Database-adatbázisok](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Fejlessze a készségeit a Microsoft Learnnel

- [Azure-feladatok automatizálása szkriptek használatával a PowerShell-lel](/learn/modules/automate-azure-tasks-with-powershell/)
- [További interaktív oktatóanyagok...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Egyéb Azure PowerShell-modulok

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
