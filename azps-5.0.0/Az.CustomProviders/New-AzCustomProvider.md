---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298946"
---
# New-AzCustomProvider

## Áttekintés
Az egyéni erőforrás-szolgáltató létrehozása vagy frissítése

## SZINTAXISA

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Leírás
Az egyéni erőforrás-szolgáltató létrehozása vagy frissítése

## Példák

### Példa 1: egyéni szolgáltató létrehozása
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Egyéni erőforrás-szolgáltató létrehozása

### 2. példa: egyéni szolgáltató létrehozása társításokkal
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Egyéni szolgáltató létrehozása az egyéni szolgáltatói társítások útvonalával.

## PARAMÉTEREK

### -Műveletek
Az egyéni erőforrás-szolgáltató által megvalósított műveletek listája.
A kivitelezéshez lásd a megjegyzések szakaszt a műveletek tulajdonságaihoz, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
A parancs futtatása munkaként

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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
Erőforrás-hely

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az erőforrás-szolgáltató neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Várva
A parancs aszinkron futtatása

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Az egyéni erőforrás-szolgáltató által megvalósított erőforrástípusok listája.
A kivitelezéshez tekintse meg a RESOURCETYPE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az Azure-előfizetés azonosítója.
Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)

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

### -Címke
Erőforrás-Címkék

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Érvényesítés
Az egyéni erőforrás-szolgáltató kérésein futtatandó érvényes érvényesítések listája.
A kivitelezéshez tekintse meg az ÉRVÉNYESÍTÉSi tulajdonságok megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
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

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. modellek. Api20180901Preview. ICustomRpManifest

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


MŰVELET <ICustomRpActionRouteDefinition [] >: az egyéni erőforrás-szolgáltató által megvalósított műveletek listája.
  - `Endpoint <String>`: Az útvonal-definíciós végpontok URI-ja, amelyet az egyéni erőforrás-szolgáltató meghatalmazotti a kérésekre. Ez lehet egy sima URI (például ' ' https://testendpoint/ ), vagy az útvonalon keresztüli útvonal (például ' https://testendpoint/{requestPath} ') formájában.
  - `Name <String>`: Az útvonal-definíció neve. Ez lesz a kar kiterjesztésének neve (például "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")
  - `[RoutingType <ActionRouting?>]`: A műveleti kérések által támogatott műveletterv-típusok.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: az egyéni erőforrás-szolgáltató által megvalósított erőforrástípusok listája.
  - `Endpoint <String>`: Az útvonal-definíciós végpontok URI-ja, amelyet az egyéni erőforrás-szolgáltató meghatalmazotti a kérésekre. Ez lehet egy sima URI (például ' ' https://testendpoint/ ), vagy az útvonalon keresztüli útvonal (például ' https://testendpoint/{requestPath} ') formájában.
  - `Name <String>`: Az útvonal-definíció neve. Ez lesz a kar kiterjesztésének neve (például "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")
  - `[RoutingType <ResourceTypeRouting?>]`: Az erőforrás-kérelmekben támogatott műveletterv-típusok.

VALIDATion <ICustomRpValidations [] >: az egyéni erőforrás-szolgáltató kérésein futtatandó érvényes érvényesítések listája.
  - `Specification <String>`: Az érvényesítési specifikációra mutató hivatkozás. A specifikációnak a raw.githubusercontent.com-on kell lennie.
  - `[ValidationType <ValidationType?>]`: Az érvényesítés típusa a megfelelő kéréshez képest.

## KAPCSOLÓDÓ HIVATKOZÁSOK

