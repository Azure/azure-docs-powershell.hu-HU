---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94023977"
---
# Update-AzFunctionAppPlan

## Áttekintés
A Function app szolgáltatási tervének frissítése

## SZINTAXISA

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

## Leírás
A Function app szolgáltatási tervének frissítése

## Példák

### 1. példa: az alkalmazás-szolgáltatási terv frissítése a EP2 SKU-ra a húsz legnagyobb dolgozóval.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Ez a parancs egy app-szolgáltatási csomagot frissít a EP2 SKU-ra húsz maximális munkással.

## PARAMÉTEREK

### -AsJob
Futtassa a parancsot munkaként.

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
A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

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
A munkavállalók maximális száma az alkalmazás-szolgáltatási tervben.

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
A munkavállalók minimális száma az alkalmazás-szolgáltatási tervben.

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

### -Name (név)
Az alkalmazás szolgáltatási tervének neve.

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

### -Várva
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
Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.

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

### -SKU
Az SKU-terv.
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

### -Címke
Erőforrás-címkék.

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

### Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Erőforrás helye.
  - `[Kind <String>]`: Az erőforrás típusa.
  - `[Tag <IResourceTags>]`: Erőforrás-címkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[Capacity <Int32?>]`: Az erőforráshoz rendelt példányok aktuális száma.
  - `[FreeOfferExpirationTime <DateTime?>]`: A kiszolgálófarm ingyenes ajánlatának lejárati időpontja.
  - `[HostingEnvironmentProfileId <String>]`: Az alkalmazás szolgáltatási környezetének erőforrás-azonosítója.
  - `[HyperV <Boolean?>]`: Ha a Hyper-V Container app Service csomagja <code>true</code> <code>false</code> másképpen van.
  - `[IsSpot <Boolean?>]`: Ha <code>true</code> Ez az alkalmazás-szolgáltatási terv a helyszíni példányokat is tulajdonosa.
  - `[IsXenon <Boolean?>]`: Elavult: Ha a Hyper-V Container app Service Plane ( <code>true</code> <code>false</code> egyéb).
  - `[MaximumElasticWorkerCount <Int32?>]`: A ElasticScaleEnabled-app szolgáltatási csomagjában engedélyezett teljes foglalkoztatottak maximális száma
  - `[PerSiteScaling <Boolean?>]`: Ha <code>true</code> az alkalmazás-szolgáltatási csomaghoz rendelt alkalmazások egymástól függetlenül is méretezhetők.         Ha <code>false</code> az alkalmazás-szolgáltatási csomaghoz rendelt alkalmazások átlépték a terv összes példányára.
  - `[Reserved <Boolean?>]`: Ha a Linux app Service Plan ( <code>true</code> <code>false</code> egyéb esetben)
  - `[SkuCapability <ICapability[]>]`: A SKU képességei, például a Traffic Manager engedélyezve van?
    - `[Name <String>]`: A SKU-kapacitás neve.
    - `[Reason <String>]`: A SKU-kapacitás oka.
    - `[Value <String>]`: A SKU tulajdonság értéke.
  - `[SkuCapacityDefault <Int32?>]`: A munkavállalók alapértelmezett száma az alkalmazás-szolgáltatási csomag SKU-hoz.
  - `[SkuCapacityMaximum <Int32?>]`: A munkavállalók maximális száma az alkalmazás-szolgáltatási csomag SKU-hoz.
  - `[SkuCapacityMinimum <Int32?>]`: Az alkalmazás-szolgáltatási csomag SKU-hoz szükséges dolgozók minimális száma.
  - `[SkuCapacityScaleType <String>]`: A rendelkezésre álló méretarány-konfigurációk egy app-szolgáltatási csomaghoz.
  - `[SkuFamily <String>]`: Az erőforrás-SKU családi kódja.
  - `[SkuLocation <String[]>]`: A SKU helye.
  - `[SkuName <String>]`: Az erőforrás SKU neve.
  - `[SkuSize <String>]`: Az erőforrás-SKU méretének megadása
  - `[SkuTier <String>]`: Az erőforrás-SKU szolgáltatási rétege.
  - `[SpotExpirationTime <DateTime?>]`: A kiszolgálófarm elévülési ideje. Csak akkor érvényes, ha az a hely kiszolgálófarm.
  - `[TargetWorkerCount <Int32?>]`: A munkavégzők számának méretezése.
  - `[TargetWorkerSizeId <Int32?>]`: A munkavégző méret-AZONOSÍTÓjának méretezése
  - `[WorkerTierName <String>]`: Az alkalmazás-szolgáltatási csomaghoz hozzárendelt célzott munkafolyamat-szint

## KAPCSOLÓDÓ HIVATKOZÁSOK

