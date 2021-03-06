---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492453"
---
# New-AzureRmTrafficManagerEndpoint

## Áttekintés
A forgalomirányító-profilban hoz létre végpontot.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRmTrafficManagerEndpoint** parancsmag létrehoz egy végpontot az Azure Traffic Manager-profilban.

Ez a parancsmag minden új végpontot véglegesít a forgalomirányítási szolgáltatással.
Ha több végpontot szeretne felvenni egy helyi forgalomirányítási profil objektumba, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Add-AzureRmTrafficManagerEndpointConfig parancsmagot.

## Példák

### Példa 1: külső végpont létrehozása profilhoz
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Ez a parancs létrehoz egy contoso nevű külső végpontot a ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljában.

### 2. példa: Azure-végpont létrehozása profilhoz
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

A parancs létrehoz egy contoso nevű Azure-végpontot az erőforráscsoport ResouceGroup11 nevű ContosoProfile-profilban.
Az Azure-végpont arra az Azure Web App-pontra mutat, amelynek az Azure Resource Manager AZONOSÍTÓját az *TARGETRESOURCEID* URI elérési útja adja meg.
A parancs nem adja meg a *EndpointLocation* paramétert, mert a Web App-erőforrás megadja a helyet.

## PARAMÉTEREK

### -EndpointLocation
A teljesítmény-továbbítási módszerben használandó végpont helyét adja meg.
Ez a paraméter csak a ExternalEndpoints vagy a NestedEndpoints típusú végpontokra érvényes.
Ezt a paramétert akkor kell megadnia, ha a teljesítményadatok-útválasztási módszert használja.

Adjon meg egy Azure region nevet.
Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .

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
A végpont állapotát adja meg.
Az érvényes értékek a következők: 

- Engedélyezve 
- Tiltva 

Ha az állapot engedélyezve van, akkor a végpontok állapotát a program kikapcsolja, és a forgalom-útválasztási módszer tartalmazza.

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
A végponthoz rendelt régiók listája a földrajzi forgalom útválasztási módszerének használatakor. Kérjük, hogy az elfogadott értékek teljes listáját a Traffic Manager dokumentációjában találja.
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

### -MinChildEndpoints
Adjon meg egy Azure region nevet.
Az Azure-régiók teljes listáját az Azure Regions () című témakörben találhatja meg https://azure.microsoft.com/regions/ https://azure.microsoft.com/regions/) .

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

### -Name (név)
Annak a forgalmi vezető végpontnak a nevét adja meg, amelyet a parancsmag hoz létre.

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

### – Prioritás
Azt a prioritást adja meg, amelyet a forgalomirányítási rendel a végponthoz.
Ez a paraméter csak akkor használatos, ha a forgalomirányítási profil a Priority Traffic-Routing metódussal van konfigurálva.
Az érvényes értékek 1 és 1000 közötti egész számok.
Az alacsonyabb értékek magasabb prioritást jelentenek.

Ha prioritást ad meg, a profil minden végpontján meg kell adnia a prioritást, és nincs két végpont sem osztható meg ugyanazzal a prioritási értékkel.
Ha nem adja meg a prioritásokat, a forgalomirányító a végpontokhoz rendeli az alapértelmezett prioritási értékeket a végpontokhoz (1) kezdve, abban a sorrendben, ahogyan a profil a végpontokat sorolja fel.

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

### -Fájlnév
Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag hozzáadja a végpontot.
Ha profilt szeretne beolvasni, használja az New-AzureRmTrafficManagerProfile vagy Get-AzureRmTrafficManagerProfile parancsmagot.

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
Ez a parancsmag egy forgalomirányítási végpontot hoz létre abban a csoportban, amelyben ez a paraméter adja meg.

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

### -Target (cél)
A végpont teljesen minősített DNS-nevét adja meg.
A Traffic Manager ezt az értéket a DNS-válaszokban akkor jeleníti meg, amikor a forgalmat a végpontra irányítja.
Ezt a paramétert csak a ExternalEndpoints végpont típusára adja meg.
A többi végpont típusnál adja meg ehelyett a *TargetResourceId* paramétert.

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
A cél erőforrás-AZONOSÍTÓját adja meg.
Ezt a paramétert csak a AzureEndpoints és a NestedEndpoints végpont típusához adja meg.
A ExternalEndpoints végpont típusnál adja meg ehelyett a *cél* paramétert.

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

### -Type (típus)
Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.
Az érvényes értékek a következők: 

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

### -Weight (súly)
A forgalomirányító által a végponthoz hozzárendelt vastagságot adja meg.
Az érvényes értékek 1 és 1000 közötti egész számok.
Az alapértelmezett érték egy (1).
Ez a paraméter csak akkor használatos, ha a Traffic Manager profilja a súlyozott forgalom-útválasztási módszerrel van konfigurálva.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzureRmTrafficManagerEndpoint](./Disable-AzureRmTrafficManagerEndpoint.md)

[Enable-AzureRmTrafficManagerEndpoint](./Enable-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerEndpoint](./Get-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Új – AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


