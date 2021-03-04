---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924137"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Frissíti a függvényalkalmazások szolgáltatástervét.

## SZINTAXIS

### ByName (alapértelmezett)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Frissíti a függvényalkalmazások szolgáltatástervét.

## PÉLDÁK

### 1. példa: Egy appszolgáltatás-csomag frissítése EP2-termékváltozatra húsz legnagyobb dolgozóval.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Ez a parancs egy appszolgáltatás-tervet frissíti EP2-termékváltozatra, amely húsz legnagyobb dolgozót foglalkoztat.

## PARAMETERS

### -AsJob
Futtassa a parancsot feladatként.

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

### -MaximumWorkerCount
Az appszolgáltatás-csomag dolgozóinak maximális száma.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
Az appszolgáltatás-csomaghoz minimálisan szükséges számú dolgozó.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Az appszolgáltatás-csomag neve.

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

### -NoWait
Futtassa a parancsot aszinkron módon.

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
Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.

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

### -Termékváltozat
A csomag termékváltozata.
Érvényes bemenetek: EP1, EP2, EP3

```yaml
Type: System.String
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

### -Tag
Erőforráscímkék.

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

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

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
  - `[SkuCapability <ICapability[]>]`: A termékváltozat képességei, például engedélyezve van a forgalomkezelő?
    - `[Name <String>]`: A termékváltozat-képesség neve.
    - `[Reason <String>]`: A termékváltozat-képesség oka.
    - `[Value <String>]`: A termékváltozat-képesség értéke.
  - `[SkuCapacityDefault <Int32?>]`: Az appszolgáltatás-csomaghoz az alapértelmezett dolgozók száma.
  - `[SkuCapacityMaximum <Int32?>]`: Az appszolgáltatás-csomag termékváltozatában dolgozók maximális száma.
  - `[SkuCapacityMinimum <Int32?>]`: Az appszolgáltatás-csomaghoz minimálisan szükséges dolgozók száma.
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

