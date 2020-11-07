---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672050"
---
# Remove-AzureRmTrafficManagerEndpointConfig

## Áttekintés
Eltávolítja a végpontot egy helyi forgalomirányító-profil objektumból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmTrafficManagerEndpointConfig** parancsmag eltávolítja a végpontot egy helyi Azure Traffic Manager-profil objektumból.
A Get-AzureRmTrafficManagerProfile parancsmag használatával is beszerezhet egy profilt.

Ez a parancsmag a helyi profil objektumon dolgozik.
Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.
Ha el szeretne távolítani egy végpontot, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Remove-AzureRmTrafficManagerEndpoint parancsmagot.

## Példák

### 1. példa: végpont eltávolítása
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.
A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.

A második parancs eltávolítja a contoso nevű Azure-végpontot az $TrafficManagerProfile tárolt profilból.
Ez a parancs csak a helyi objektumot módosítja.

A végleges parancs frissíti a ContosoProfile nevű forgalomirányítási profilt az $TrafficManagerProfile helyi értékének megfelelően.

## PARAMÉTEREK

### -EndpointName
Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag eltávolítja.

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

### -TrafficManagerProfile
Helyi **TrafficManagerProfile** -objektumot ad meg.
Ez a parancsmag módosította ezt a helyi objektumot.
**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.

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

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.

## KIMENETEK

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Ez a parancsmag egy módosított TrafficManagerProfile objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


