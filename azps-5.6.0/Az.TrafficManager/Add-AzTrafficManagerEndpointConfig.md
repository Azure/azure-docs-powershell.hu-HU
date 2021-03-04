---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936522"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
Hozzáad egy végpontot egy helyi Traffic Manager-profilobjektumhoz.

## SZINTAXIS

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzTrafficManagerEndpointConfig parancsmag** hozzáad egy végpontot egy helyi Azure Traffic Manager-profilobjektumhoz.
A profilt a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile használhatja.

Ez a parancsmag a helyi profilobjektumon működik.
A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.
Végpont létrehozásához és a módosítás egyetlen művelettel való véglegesítéshez használja a New-AzTrafficManagerEndpoint parancsmagot.

## PÉLDÁK

### 1. példa: Végpont hozzáadása profilhoz
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.
A parancs a helyi profilt a $TrafficManagerProfile tárolja.

A második parancs hozzáadja a contoso nevű végpontot a $TrafficManagerProfile.
A parancs a végpont konfigurációs adatait tartalmazza.
Ez a parancs csak a helyi objektumot módosítja.

Az utolsó parancs frissíti a Traffic Manager-profilt az Azure-ban úgy, hogy megfeleljen a helyi $TrafficManagerProfile.

## PARAMETERS

### -CustomHeader
Egyéni fejlécnév és értékpárok listája a kérések igényléséhez.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
Megadja a végpontnak a Performance traffic-routing metódusban használnia kell helyét.
Ez a paraméter csak az ExternalEndpoints vagy NestedEndpoints típusú végpontokra vonatkozik.
Ezt a paramétert a Performance traffic-routing metódus használata esetén kell megadnia.

Adjon meg egy Azure-régiónevet.
Az Azure-régiók teljes listáját az Azure Régiók http://azure.microsoft.com/regions/ ( ( ) http://azure.microsoft.com/regions/) tartalmazza.

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

### -EndpointName
Megadja annak a Traffic Manager-végpontnak a nevét, amelybe ez a parancsmag hozzáadja.

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

### -EndpointStatus
A végpont állapotát határozza meg.
Érvényes értékek: 

- Engedélyezve 
- Letiltva 

Ha az állapot engedélyezve van, a végpont a végpont állapotát jelzi, és szerepel a forgalom-útválasztási metódusban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoMapping
Az ehhez a végponthoz csatlakoztatott régiók listája a "Földrajzi" forgalom útválasztási metódusának használata esetén. Az elfogadott értékek teljes listáját a Traffic Manager [dokumentációjában találhatja meg.](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinDentEndpoints
Azon végpontok minimális száma, amelyeknek elérhetőnek kell lennie a gyermekprofilban ahhoz, hogy a szülőprofil beágyazott végpontja elérhetőnek számítson.
Csak a "NestedEndpoints" típusú végpontokra alkalmazható.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Megadja a Traffic Manager által a végponthoz hozzárendelt prioritást.
Ezt a paramétert csak akkor használja a rendszer, ha a Traffic Manager-profil a Prioritás forgalomirányítási módszerrel van konfigurálva.
Az érvényes értékek az 1 és 1000 között egész értékek.
Az alacsonyabb értékek magasabb prioritást jelentenek.

Prioritás megadása esetén a profil összes végpontja számára meg kell adnia a prioritást, és két végpont nem oszthatja meg ugyanazt a prioritásértéket.
Ha nem ad meg prioritást, a Traffic Manager egy (1) értékkel kezdődően alapértelmezett prioritásértékeket rendel a végpontokhoz abban a sorrendben, amely a végpontokat felsorolja.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetMapping
A végpontnak megfeleltetett címtartományok vagy alhálózatok listája az alhálózati forgalom útválasztási metódusának használata esetén.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target
A végpont teljes DNS-nevét adja meg.
A Traffic Manager ezt az értéket adja vissza a DNS-válaszokban, amikor a forgalmat erre a végpontra irányítja.
Ezt a paramétert csak az ExternalEndpoints végponttípushoz adja meg.
Más végponttípusok esetén adja meg a *TargetResourceId* paramétert.

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

### -TargetResourceId
A cél erőforrás-azonosítóját adja meg.
Ezt a paramétert csak az AzureEndpoints és NestedEndpoints végponttípusainál adja meg.
Az ExternalEndpoints végponttípusnál adja meg a *Cél paramétert.*

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

### -TrafficManagerProfile
Helyi **TrafficManagerProfile objektumot** ad meg.
Ez a parancsmag módosítja ezt a helyi objektumot.
A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Type
Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá az Azure Traffic Manager-profilhoz.
Érvényes értékek: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
A Traffic Manager által a végponthoz hozzárendelt súly megadása.
Az érvényes értékek az 1 és 1000 között egész értékek.
Az alapértelmezett érték egy (1).
Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja súlyozott forgalom-útválasztási módszerrel van konfigurálva.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## KIMENETEK

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


