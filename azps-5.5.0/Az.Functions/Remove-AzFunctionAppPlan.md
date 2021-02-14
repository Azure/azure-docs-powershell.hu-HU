---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147842"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
Függvényalkalmazás-terv törlése.

## SZINTAXIS

### ByName (alapértelmezett)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Függvényalkalmazás-terv törlése.

## PÉLDÁK

### 1. példa: Függvényalkalmazásterv lekért név szerint, és törlése.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Ez a parancs név szerint lekért egy függvényalkalmazástervet, és törli azt.

### 2. példa: Függvényalkalmazás tervének törlése név szerint.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Ez a parancs név szerint töröl egy függvényalkalmazástervet.

## PARAMETERS

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

### -Force
Kényszeríti a parancsmagot, hogy a függvényalkalmazás-tervet jóváhagyás kérése nélkül távolítsa el.

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

### -InputObject
Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A függvényalkalmazás neve.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Eredménye igaz, ha a parancs sikeres.

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


```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az Azure-előfizetés azonosítója.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IAppServicePlan> 
  - `Location <String>`: Erőforrás helye.
  - `[Kind <String>]`: Az erőforrás fajtája.
  - `[Tag <IResourceTags>]`: Erőforráscímkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[Capacity <Int32?>]`: Az erőforráshoz rendelt példányok aktuális száma.
  - `[FreeOfferExpirationTime <DateTime?>]`: A kiszolgálófarm ingyenes ajánlatának lejárati ideje.
  - `[HostingEnvironmentProfileId <String>]`: Az app szolgáltatási környezetének erőforrás-azonosítója.
  - `[HyperV <Boolean?>]`: Ha a Hyper-V tároló appszolgáltatás-csomagja <code>true</code> , <code>false</code> egyébként.
  - `[IsSpot <Boolean?>]`: Ha <code>true</code> ez az appszolgáltatás-csomag rendelkezik direkt példányokkal.
  - `[IsXenon <Boolean?>]`: Elavult: Ha a Hyper-V tárolóalkalmazás szolgáltatási <code>true</code> csomagja , <code>false</code> egyébként.
  - `[MaximumElasticWorkerCount <Int32?>]`: A RugalmasságiSkálaEnabled appszolgáltatás-csomaghoz engedélyezett összes dolgozó maximális száma
  - `[PerSiteScaling <Boolean?>]`: Ha az appszolgáltatás-csomaghoz rendelt appok egymástól függetlenül <code>true</code> skálázhatóak.         Ha az appszolgáltatás-csomaghoz rendelt appok a csomag összes példányához <code>false</code> méretre fognak méretezve.
  - `[Reserved <Boolean?>]`: Ha a Linux appszolgáltatás-csomagja <code>true</code> , <code>false</code> egyébként.
  - `[SkuCapability <ICapability[]>]`: A termékváltozat képességei, például engedélyezve vannak a forgalomkezelők?
    - `[Name <String>]`: A termékváltozat-képesség neve.
    - `[Reason <String>]`: A termékváltozat-képesség oka.
    - `[Value <String>]`: A termékváltozat-képesség értéke.
  - `[SkuCapacityDefault <Int32?>]`: Az appszolgáltatás-csomag termékváltozatának alapértelmezett dolgozói száma.
  - `[SkuCapacityMaximum <Int32?>]`: Az appszolgáltatás-csomag termékváltozatában dolgozók maximális száma.
  - `[SkuCapacityMinimum <Int32?>]`: Az appszolgáltatás-csomag termékváltozatában dolgozók minimális száma.
  - `[SkuCapacityScaleType <String>]`: Az appszolgáltatás-csomaghoz rendelkezésre álló méretarány-konfigurációk.
  - `[SkuFamily <String>]`: Az erőforrás-termékváltozat családi kódja.
  - `[SkuLocation <String[]>]`: A termékváltozat helye.
  - `[SkuName <String>]`: Az erőforrás-termékváltozat neve.
  - `[SkuSize <String>]`: Az erőforrás-termékváltozat méretkierőszője.
  - `[SkuTier <String>]`: Az erőforrás-termékváltozat szolgáltatási rétege.
  - `[SpotExpirationTime <DateTime?>]`: A kiszolgálófarm lejáratának ideje. Csak akkor érvényes, ha direkt kiszolgálófarmról van szükség.
  - `[TargetWorkerCount <Int32?>]`: A dolgozók száma.
  - `[TargetWorkerSizeId <Int32?>]`: A dolgozók méretazonosítójának méretezése.
  - `[WorkerTierName <String>]`: Az appszolgáltatás-csomaghoz hozzárendelt célmunkási szint.

## KAPCSOLÓDÓ HIVATKOZÁSOK

