---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844869"
---
# New-AzsComputeQuota

## Áttekintés
Számítási kvótát hoz létre vagy frissít a megadott kvóta-paraméterekkel.

## SZINTAXISA

### CreateExpanded (alapértelmezett)
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Létrehozása
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Leírás
Számítási kvótát hoz létre vagy frissít a megadott kvóta-paraméterekkel.

## Példák

### Példa 1: számítási kvóta létrehozása alapértelmezett paraméterekkel
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

A nem meghatározott paraméterek a fenti alapértelmezett paraméternek megfelelőek lesznek.

### 2. példa: számítási kvóta létrehozása egyéni paraméterekkel
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

A kvótákat a paraméterekkel testre szabhatja. A nem meghatározott paraméterek alapértelmezett értékkel rendelkeznek.

## PARAMÉTEREK

### -AvailabilitySetCount
A rendelkezésre álló elérhetőségi készletek maximális száma

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### -CoresCount
Az engedélyezett magok maximális száma.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Hely
Az erőforrás helye.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Location1
Az erőforrás helye.

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (név)
A kvóta neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -NewQuota
Megtartja az erőforrás-hozzárendelés szabályozásához használt kvóta-információkat.
A kivitelezéshez tekintse meg a NEWQUOTA tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -PremiumManagedDiskAndSnapshotSize
A felügyelt lemezek és a prémium típusú Pillanatképek maximális száma

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### -StandardManagedDiskAndSnapshotSize
A felügyelt lemezek és a standard típusú Pillanatképek maximális száma.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.
Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -VirtualMachineCount
Engedélyezett virtuális gépek maximális száma

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -VMScaleSetCount
A méretarány maximális száma engedélyezett.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota



## MEGJEGYZI

KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.

NEWQUOTA <IQuota> : az erőforrás-hozzárendelés szabályozásához használt kvóta-információkat tartalmazza.
  - `[Location <String>]`: Az erőforrás helye.
  - `[AvailabilitySetCount <Int32?>]`: A rendelkezésre álló elérhetőségek száma maximálisan engedélyezett.
  - `[CoresLimit <Int32?>]`: Engedélyezett magok maximális száma.
  - `[PremiumManagedDiskAndSnapshotSize <Int32?>]`: A felügyelt lemezek és a prémium típusú Pillanatképek maximális száma
  - `[StandardManagedDiskAndSnapshotSize <Int32?>]`: A felügyelt lemezek és a standard típusú Pillanatképek maximális száma.
  - `[VMScaleSetCount <Int32?>]`: A méretarány-készletek maximális száma engedélyezett.
  - `[VirtualMachineCount <Int32?>]`: Engedélyezett virtuális gépek maximális száma.

## KAPCSOLÓDÓ HIVATKOZÁSOK

