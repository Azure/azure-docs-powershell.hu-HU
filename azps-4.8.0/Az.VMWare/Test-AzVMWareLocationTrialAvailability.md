---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017442"
---
# Test-AzVMWareLocationTrialAvailability

## Áttekintés
Az előfizetések visszaadási állapota régiónként

## SZINTAXISA

### Ellenőrzés (alapértelmezett)
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CheckViaIdentity
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## Leírás
Az előfizetések visszaadási állapota régiónként

## Példák

### Példa 1: a próbaverzió elérhetőségének ellenőrzése
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

Próbaverzió elérhetőségének ellenőrzése

## PARAMÉTEREK

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

### -InputObject
Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Hely
Azure Region (Azure)

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A cél-előfizetés azonosítója.

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. ITrial

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


INPUTOBJECT <IVMWareIdentity> : Identity paraméter
  - `[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben
  - `[ClusterName <String>]`: A fürt neve a privát felhőben
  - `[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: Azure region
  - `[PrivateCloudName <String>]`: A privát felhő neve
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve. A név a kis-és nagybetűk megkülönböztetésére szolgál.
  - `[SubscriptionId <String>]`: A cél-előfizetés azonosítója.

## KAPCSOLÓDÓ HIVATKOZÁSOK

