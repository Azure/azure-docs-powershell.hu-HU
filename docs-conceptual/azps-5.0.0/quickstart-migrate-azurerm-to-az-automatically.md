---
title: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba
description: Ismerje meg, hogyan migrálhatók automatikusan a PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753649"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Gyorsútmutató: PowerShell-szkriptek automatikus migrálása az AzureRM modulból az Az PowerShell-modulba

Ez a cikk ismerteti, hogyan lehet az Az.Tools.Migration PowerShell-modul használatával automatikusan frissíteni a PowerShell-szkripteket és -szkriptmodulokat az AzureRM modulból az Az PowerShell-modulba.

> [!IMPORTANT]
> Az Az.Tools.Migration PowerShell-modul jelenleg nyilvános előzetes verzióban érhető el. Erre az előzetes verzióra nem vonatkozik szolgáltatói szerződés. Az előzetes verzió használata NEM javasolt éles számítási feladatok esetén. Előfordulhat, hogy néhány funkció nem támogatott, vagy korlátozott képességekkel rendelkezik. További információ: [Kiegészítő használati feltételek a Microsoft Azure előzetes verziójú termékeihez](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Az Az.Tools.Migration PowerShell-modullal kapcsolatos visszajelzések és problémák bejelentéséhez használja a [GitHub-problémajelentést](https://github.com/Azure/azure-powershell-migration/issues) az `azure-powershell-migration` adattárban.

## <a name="requirements"></a>Követelmények

* Frissítse meglévő PowerShell-szkriptjeit az [AzureRM PowerShell-modul legújabb verziójára (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Telepítse az Az.Tools.Migration PowerShell-modult.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>1\. lépés: Egy frissítési terv létrehozása

A `New-AzUpgradeModulePlan` parancsmaggal hozzon létre egy frissítési tervet, amellyel migrálhatja szkriptjeit és moduljait az Az PowerShell-modulba. A frissítési terv részletezi, hogy melyik fájlt és mely eltolási pontokat kell módosítani az AzureRM-ről az Az PowerShell-parancsmagokra való áttéréskor.

> [!NOTE]
> A `New-AzUpgradeModulePlan` parancsmag nem hajtja végre a tervet, csak létrehozza a frissítési lépéseket.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Tekintse át a frissítési terv eredményeit.

```powershell
# Show the entire upgrade plan
$Plan
```

Futtassa a következő parancsot, amely kiszűri az eredmények közül azokat a parancsokat, amelyekhez figyelmeztetés vagy hiba tartozik. Ez a nagy méretű eredményhalmazok esetében segíthet a hibák gyors azonosításában a frissítés végrehajtása előtt.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>2\. lépés: A frissítés végrehajtása

A frissítési terv végrehajtásához az `Invoke-AzUpgradeModulePlan` parancsmagot kell futtatni. Ez a parancs végrehajtja a megadott fájlok vagy mappák frissítését, kivéve a `New-AzUpgradeModulePlan` parancsmag által azonosított hibák esetében.

Ehhez a parancshoz meg kell adni, hogy a fájlok az eredeti helyükön legyenek-e módosítva, vagy mentse őket új helyre a parancs (az eredeti példányokat pedig hagyja módosítatlanul).

> [!CAUTION]
> A parancsnak nincs visszavonási művelete. Mindig győződjön meg arról, hogy a frissítendő PowerShell-szkriptek és -modulok esetén rendelkezik biztonsági másolattal.

> [!WARNING]
> Az `Invoke-AzUpgradeModulePlan` parancsmag végleges károkat okozhat, ha meg van adva a `-FileEditMode ModifyExistingFiles` beállítás. Ez helyben módosítja a szkripteket és függvényeket a `New-AzUpgradeModulePlan` parancsmag által létrehozott modulfrissítési tervnek megfelelően. A károk megelőzéséhez adja meg ehelyett a `-FileEditMode SaveChangesToNewFiles` beállítást.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Tekintse át a frissítési művelet eredményeit.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Ha bármilyen hibát kap eredményül, a következő paranccsal kérhet bővebb információkat a hibás eredményekről.

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Korlátozások

* Az automatizált paraméternév-frissítés nem támogatott a szétterített paraméterkészletek esetében. Ha a parancs ilyet talál a frissítési terv létrehozása közben, akkor egy figyelmeztetést ad vissza.
* A fájlok írási és olvasási műveletei az alapértelmezett kódolás használatával történnek. A szokatlan fájlkódolási helyzetek problémákhoz vezethetnek.
* A rendszer nem észleli az olyan AzureRM-parancsmagokat, amelyek a Pester egységtesztelési utasításaihoz tartozó argumentumokként lettek átadva.
* Jelenleg kizárólag az Az PowerShell-modul 4.6.1-es verziója támogatott célként.

## <a name="next-steps"></a>Következő lépések

Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell dokumentációját](https://docs.microsoft.com/powershell/azure/).