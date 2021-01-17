---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330474"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Végpontot hoz létre a Traffic Manager-profilban.

## SZINTAXIS

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzTrafficManagerEndpoint** parancsmag létrehoz egy végpontot egy Azure Traffic Manager-profilban.

Ez a parancsmag minden új végpontot véglegesen a Traffic Manager szolgáltatáshoz.
Ha több végpontot szeretne hozzáadni egy helyi Traffic Manager-profilobjektumhoz, és egyetlen művelettel szeretne módosításokat véglegesni, használja a Add-AzTrafficManagerEndpointConfig parancsmagot.

## PÉLDÁK

### 1. példa: Külső végpont létrehozása profilhoz
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Ez a parancs létrehoz egy contoso nevű külső végpontot a ContosoProfile nevű profilban az Erőforráscsoport11 erőforráscsoportban.

### 2. példa: Azure-végpont létrehozása profilhoz
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Ez a parancs létrehoz egy contoso nevű Azure-végpontot az Erőforráscsoport11 erőforráscsoport ContosoProfile nevű profiljában.
Az Azure-végpont az Azure Web Appra mutat, amelynek Azure Resource Manager-azonosítóját a *TargetResourceId* URI elérési útja tartalmazza.
A parancs nem adja meg az *EndpointLocation* paramétert, mert a Web App erőforrás adja meg a helyet.

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

### -EndpointStatus
A végpont állapotát határozza meg.
Érvényes értékek: 

- Engedélyezve 
- Letiltva 

Ha az állapot engedélyezve van, a végpont a végpont állapotát jelzi, és szerepel a forgalom útválasztási metódusában.

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
A végpontnak megfeleltetett régiók listája a "Földrajzi" forgalom útválasztási metódusának használata esetén. Az elfogadott értékek teljes listáját a Traffic Manager dokumentációjában találhatja meg.

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
Adjon meg egy Azure-régiónevet.
Az Azure-régiók teljes listáját az Azure Régiók http://azure.microsoft.com/regions/ ( ( ) http://azure.microsoft.com/regions/) tartalmazza.

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

### -Name
A parancsmag által létrehozott Traffic Manager-végpont nevét adja meg.

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

### -ProfileName
Megadja annak a Traffic Manager-profilnak a nevét, amelyhez a parancsmag hozzáad egy végpontot.
Profil beszerzéséhez használja a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile parancsmagokat.

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

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
Ez a parancsmag létrehoz egy Traffic Manager-végpontot a paraméter által megadott csoportban.

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

### -SubnetMapping
A végpontnak megfeleltetett címtartományok vagy alhálózatok listája az "Alhálózati" adatforgalom-útválasztási módszer használata esetén.

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

### -Type
Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá a Traffic Manager-profilhoz.
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

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


