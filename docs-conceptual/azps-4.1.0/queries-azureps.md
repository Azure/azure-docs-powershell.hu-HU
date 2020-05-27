---
title: Azure PowerShell-parancsmagok lekérdezésének kimenete
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: ebd108a2c13bdb376213d054fb72188e6205a565
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/19/2020
ms.locfileid: "83624302"
---
# <a name="query-output-of-azure-powershell"></a>Az Azure PowerShell lekérdezésének kimenete 

Az egyes Azure PowerShell-parancsmagok eredménye egy-egy Azure PowerShell-objektum. Még azok a parancsmagok is, amelyek nem kifejezetten `Get-` műveletek, visszaadhatnak egy megvizsgálható értéket, amely egy létrehozott vagy módosított erőforrásról nyújt információt. Bár a legtöbb parancsmag egyetlen objektumot ad vissza, némelyikük egy tömböt, amelyen végig kell haladni.

Az Azure PowerShellből szinte minden esetben a [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) parancsmaggal kérdezheti le a kimenetet, amelynek rövidítése gyakran `select`. A kimenetek a [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) parancsmaggal, illetve annak `where` aliasával szűrhetők.

## <a name="select-simple-properties"></a>Egyszerű tulajdonságok kiválasztása

Az alapértelmezett táblázatos formátumban az Azure PowerShell-parancsmagok nem jelenítik meg az összes elérhető tulajdonságukat. Minden tulajdonság a [Format-List](/powershell/module/microsoft.powershell.utility/format-list) parancsmaggal vagy a kimenet a `Select-Object *` parancshoz való átirányításával érhető el:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

Ha már tudja azoknak a tulajdonságoknak a nevét, amelyekre kíváncsi, ezeket a tulajdonságneveket közvetlenül lekérheti a `Select-Object` használatával:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

A `Select-Object` kimenete mindig úgy van formázva, hogy a kért adatokat jelenítse meg. Ha többet szeretne megtudni arról, hogyan használható a formázás a parancsmagok által visszaadott eredmények lekérdezésének részeként, tekintse meg az [Azure PowerShell-parancsmag kimenetének formázása](formatting-output.md) című részt.

## <a name="select-nested-properties"></a>Beágyazott tulajdonságok kiválasztása

Az Azure PowerShell-parancsmagok kimenetének néhány tulajdonsága beágyazott objektumokat használ. Ilyen például a `Get-AzVM` kimenet `StorageProfile` tulajdonsága. A beágyazott tulajdonság értékének lekéréséhez adja meg a megjelenítendő nevet és a megvizsgálni kívánt érték teljes elérési útvonalát a `Select-Object` parancshoz tartozó szótárargumentum részeként:

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

Minden szótárargumentum az objektum egy tulajdonságát választja ki. A kinyerni kívánt tulajdonságnak egy kifejezés részének kell lennie.

## <a name="filter-results"></a>Szűrés eredményei 

A `Where-Object` parancsmag használatával bármely tulajdonságérték alapján szűrheti az eredményeket, a beágyazott tulajdonságokat is beleértve. A következő példa bemutatja, hogyan használható a `Where-Object` egy Linux rendszerű virtuális gép megkeresésére egy erőforráscsoportban.

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

A `Select-Object` és a `Where-Object` eredményeit továbbíthatja az egyiktől a másiknak. A teljesítményt szem előtt tartva ajánlott a `Where-Object` műveletet a `Select-Object` elé helyezni:

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
