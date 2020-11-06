---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502363"
---
# Remove-AzureRmSiteRecoveryNetworkMapping

## Áttekintés
Hálózati megfeleltetés eltávolítása az aktuális webhely-helyreállítási boltozatról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRMSiteRecoveryNetworkMapping** parancsmag eltávolít egy hálózati megfeleltetést az aktuális Azure webhely-helyreállítási boltozatból.

## Példák

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkMapping
A hálózati megfeleltetési objektumot adja meg.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### ASRNetworkMapping
A ' NetworkMapping ' paraméter az "ASRNetworkMapping" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. SiteRecovery. ASRJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSiteRecoveryNetworkMapping](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[Új – AzureRmSiteRecoveryNetworkMapping](./New-AzureRmSiteRecoveryNetworkMapping.md)
