---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148386"
---
# New-AzCustomProvider

## SYNOPSIS
Létrehozza vagy frissíti az egyéni erőforrás-szolgáltatót.

## SZINTAXIS

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Létrehozza vagy frissíti az egyéni erőforrás-szolgáltatót.

## PÉLDÁK

### 1. példa: Egyéni szolgáltató létrehozása
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Egyéni erőforrás-szolgáltató létrehozása

### 2. példa: Egyéni szolgáltató létrehozása társításokkal
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Egyéni szolgáltató létrehozása egyéni szolgáltató-társítások útvonalával.

## PARAMETERS

### -Action
Az egyéni erőforrás-szolgáltató által implementálja a műveletek listáját.
Az ACTION tulajdonságok létrehozásáról és a kivonattáblák létrehozásáról a NOTES (MEGJEGYZÉSEK) című szakaszban található.

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
A parancs futtatása feladatként

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Location
Erőforrás helye

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

### -Name
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

### -NoWait
A parancs futtatása aszinkron módon

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
Az egyéni erőforrásszolgáltató által implementálja az erőforrástípusok listáját.
Az ERŐFORRÁSTÍPUS tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban talál további konstrukciót.

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
Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-00000-0000000000000)

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

### -Tag
Erőforráscímkék

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

### -Validation
Az egyéni erőforrás-szolgáltató kérései alapján futtatható érvényesítések listája.
Ennek létrehozásáról az ÉRVÉNYESÍTési tulajdonságokat és a kivonattáblát a JEGYZETEK szakaszban láthatja.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


ACTION <ICustomRpActionRouteDefinition[]>: Az egyéni erőforrás-szolgáltató által implementálható műveletek listája.
  - `Endpoint <String>`: Az útvonaldefiníciós végpont URI-ja, amelyhez az egyéni erőforrás-szolgáltató proxyt kér. Ez lehet egy sima URI (például ' '), vagy megadhatja, hogy az útvonalon https://testendpoint/ (például ' ') keresztül https://testendpoint/{requestPath} halad-e.
  - `Name <String>`: Az útvonaldefiníció neve. Ez lesz az ARM-bővítmény neve (pl. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ActionRouting?>]`: A műveletkérések által támogatott útválasztási típusok.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: Az egyéni erőforrásszolgáltató által implementálható erőforrástípusok listája.
  - `Endpoint <String>`: Az útvonaldefiníciós végpont URI-ja, amelyhez az egyéni erőforrás-szolgáltató proxyt kér. Ez lehet egy sima URI (például ' '), vagy megadhatja, hogy az útvonalon https://testendpoint/ (például ' ') keresztül https://testendpoint/{requestPath} halad-e.
  - `Name <String>`: Az útvonaldefiníció neve. Ez lesz az ARM-bővítmény neve (pl. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ResourceTypeRouting?>]`: Az erőforrás-kérelmekhez támogatott útválasztási típusok.

VALIDATION <ICustomRpValidations[]>: Az egyéni erőforrás-szolgáltató kérésén futtatható érvényesítések listája.
  - `Specification <String>`: Az érvényesítési specifikációra mutató hivatkozás. A specifikációt az adott raw.githubusercontent.com.
  - `[ValidationType <ValidationType?>]`: Az egyező kérésen futtatott érvényesítés típusa.

## KAPCSOLÓDÓ HIVATKOZÁSOK

