---
title: Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban
description: Arra vonatkozó tájékoztatás, hogyan futtathat Azure PowerShell-parancsmagokat párhuzamosan vagy háttérfeladatként az -AsJob és a Start-Job segítségével.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b76e310e1677e539927ebc4746df67c1d1accc16
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410128"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban

Az Azure PowerShell működése az Azure-felhőkhöz való csatlakozástól és az onnan kapott válaszoktól függ, ezért a parancsmagok többsége blokkolja a PowerShell-munkamenetet, amíg választ nem kap a felhőtől.
A PowerShell-feladatok lehetővé teszik, hogy egyetlen PowerShell-munkamenetből futtasson parancsmagokat a háttérben vagy végezzen egyszerre több feladatot az Azure-ban.

Ez a cikk rövid áttekintést nyújt az Azure PowerShell-parancsmagok PowerShell-feladatként való futtatásáról és annak ellenőrzéséről, hogy a feladatok befejeződtek-e. A parancsok Azure PowerShellben való futtatásához Azure PowerShell-környezeteket kell használni, amelyekről részletesen [az Azure-környezeteket és a bejelentkezési hitelesítő adatokat](context-persistence.md) ismertető témakörben olvashat.
További információ a PowerShell-feladatokról: [A PowerShell-feladatok ismertetése](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Azure-környezetek és PowerShell-feladatok

A PowerShell-feladatok külön folyamatokként futnak, társított PowerShell-munkamenet nélkül, ezért meg kell osztani velük az Azure-beli hitelesítő adatokat. A rendszer Azure-beli környezeti objektumként, az alábbi módszerek valamelyikével adja át a hitelesítő adatokat:

* Automatikus környezetmegőrzés. A környezetmegőrzés alapértelmezés szerint engedélyezve van, és több munkamenetre kiterjedően megőrzi a bejelentkezési adatokat. Ha engedélyezve van a környezetmegőrzés, a rendszer átadja az aktuális Azure-környezetet az új folyamatnak:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Azure-beli környezeti objektum megadásához használja az `-AzContext` paramétert bármelyik Azure PowerShell-parancsmaggal:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Ha a környezetmegőrzés le van tiltva, meg kell adni az `-AzContext` argumentumot.

* Használja az egyes Azure PowerShell-parancsmagok által biztosított `-AsJob` kapcsolót. Ez a kapcsoló automatikusan elindítja a parancsmagot PowerShell-feladatként, az aktív Azure-környezet használatával:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Ha ellenőrizni szeretné, hogy az adott parancsmag támogatja-e az `-AsJob` kapcsolót, tekintse meg a referenciadokumentációját. Az `-AsJob` kapcsoló használatához nem kell engedélyezni a környezet automatikus mentését.

A futó feladatok állapotát a [Get-Job](/powershell/module/microsoft.powershell.core/get-job) parancsmaggal ellenőrizheti. Egy feladat pillanatnyi kimenetének lekéréséhez használja a [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) parancsmagot.

Ha távolról szeretné ellenőrizni egy művelet állapotát az Azure-on, használja a feladat által módosított erőforrás típusához társított `Get-` parancsmagokat:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Lásd még:

* [Azure PowerShell-környezetek](context-persistence.md)
* [A PowerShell-feladatok ismertetése](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Get-Job referencia](/powershell/module/microsoft.powershell.core/get-job)
* [Receive-Job referencia](/powershell/module/microsoft.powershell.core/receive-job)
