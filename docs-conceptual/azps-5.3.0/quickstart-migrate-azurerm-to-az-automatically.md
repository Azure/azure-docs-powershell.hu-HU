---
title: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba
description: Ismerje meg, hogyan migrálhatók automatikusan a PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893790"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Gyorsútmutató: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba

Ez a cikk ismerteti, hogyan lehet az Az.Tools.Migration PowerShell-modul használatával automatikusan frissíteni a PowerShell-szkripteket és -szkriptmodulokat az AzureRM modulból az Az PowerShell-modulba. A további migrálási lehetőségekért lásd [Az Azure PowerShell migrálása az AzureRM modulból az Az modulba](/powershell/azure/migrate-from-azurerm-to-az) című cikket.

## <a name="requirements"></a>Követelmények

* Frissítse meglévő PowerShell-szkriptjeit az [AzureRM PowerShell-modul legújabb verziójára (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Telepítse az Az.Tools.Migration PowerShell-modult.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>1\. lépés: Egy frissítési terv létrehozása

A **`New-AzUpgradeModulePlan`** parancsmaggal hozzon létre egy frissítési tervet, amellyel migrálhatja szkriptjeit és moduljait az Az PowerShell-modulba. A parancsmag nem módosítja a meglévő szkriptjeit. Adott szkript kiválasztásához használja a **`FilePath`** paramétert, egy adott mappa összes szkriptjének kiválasztásához pedig a **`DirectoryPath`** paramétert.

> [!NOTE]
> A **`New-AzUpgradeModulePlan`** parancsmag nem hajtja végre a tervet, csak létrehozza a frissítési lépéseket.

A következő példa a _`C:\Scripts`_ mappában található összes szkripthez hoz létre tervet. Az **`OutVariable`** paraméter megadásának eredményeképpen a rendszer visszaadja az eredményeket, és egyidejűleg egy **`Plan`** nevű változóban tárolja el őket.

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Amint az alábbi kimenetben látható, a frissítési terv részletezi, hogy melyik fájlt és mely eltolási pontokat kell módosítani az AzureRM-ről az Az PowerShell-parancsmagokra való áttéréskor.

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

A frissítés elvégzése előtt meg kell tekintenie a problémákra vonatkozó terv eredményeit. A következő példa a parancsfájloknak és a parancsfájlok azon elemeinek listáját adja vissza, amelyek megakadályozzák, hogy a rendszer automatikusan frissítse őket.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

A következő kimenetben látható elemek nem frissülnek automatikusan, amíg nem javítja ki manuálisan a problémákat.

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a>2\. lépés: A frissítés végrehajtása

> [!CAUTION]
> A parancsnak nincs visszavonási művelete. Mindig győződjön meg arról, hogy a frissítendő PowerShell-szkriptek és -modulok esetén rendelkezik biztonsági másolattal.

Ha elégedett a tervvel, a frissítés az **`Invoke-AzUpgradeModulePlan`** parancsmaggal hajtható végre. Az eredeti parancsfájlokon végzett módosítások megakadályozásához a **`SaveChangesToNewFiles`** értéket adja meg a **`FileEditMode`** paraméter értékeként. Ha ezt a módot használja, a frissítés során másolat készül a kiválasztott szkriptekről, és a rendszer az _`_az_upgraded`_ karakterláncot fűzi hozzá a fájlnevekhez.

> [!WARNING]
> Az **`Invoke-AzUpgradeModulePlan`** parancsmag végleges károkat okozhat, ha meg van adva a **`-FileEditMode ModifyExistingFiles`** beállítás. Ez a parancsmag helyben módosítja a szkripteket és függvényeket a **`New-AzUpgradeModulePlan`** parancsmag által létrehozott modulfrissítési tervnek megfelelően. A károk megelőzéséhez adja meg ehelyett a **`-FileEditMode SaveChangesToNewFiles`** beállítást.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

Ha bármilyen hibát kap eredményül, a következő paranccsal kérhet bővebb információkat a hibás eredményekről.

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a>Korlátozások

* A fájlok írási és olvasási műveletei az alapértelmezett kódolás használatával történnek. A szokatlan fájlkódolási helyzetek problémákhoz vezethetnek.
* A rendszer nem észleli az olyan AzureRM-parancsmagokat, amelyek a Pester egységtesztelési utasításaihoz tartozó argumentumokként lettek átadva.
* Jelenleg kizárólag az Az PowerShell-modul 5.2.0-s verziója támogatott célként.

## <a name="how-to-report-issues"></a>Útmutató a problémák bejelentéséhez

Az Az.Tools.Migration PowerShell-modullal kapcsolatos visszajelzések és problémák bejelentéséhez használja a [GitHub-problémajelentést](https://github.com/Azure/azure-powershell-migration/issues) az `azure-powershell-migration` adattárban.

## <a name="next-steps"></a>Következő lépések

Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell dokumentációját](/powershell/azure/).
