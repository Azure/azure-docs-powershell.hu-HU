---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184942"
---
# Remove-AzFunctionAppPlan

## Áttekintés
Egy Function app-terv törlése.

## SZINTAXISA

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

## Leírás
Egy Function app-terv törlése.

## Példák

### Példa 1: a Function app tervének beszerzése név alapján és törlése
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Ez a parancs a Function app tervét név alapján kapja meg, és törli azt.

### 2. példa: a Function app tervének törlése név szerint.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Ez a parancs törli a Function app tervét név szerint.

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

### -Force
Kényszeríti a parancsmagot a Function app-csomag eltávolítására a megerősítés kérése nélkül.

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

### -Name (név)
A függvény app neve.

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
Igaz érték visszaadása, ha a parancs sikeres.

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

### System. Boolean

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

