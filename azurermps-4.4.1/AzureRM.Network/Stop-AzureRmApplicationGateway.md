---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493406"
---
# Stop-AzureRmApplicationGateway

## Áttekintés
Az alkalmazás-átjáró leállítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **stop-AzureRmApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.

## Példák

### 1. példa: az alkalmazás-átjáró leállítása
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.

## PARAMÉTEREK

### -ApplicationGateway
Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
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

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGateway

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Új – AzureRmApplicationGateway](./New-AzureRmApplicationGateway.md)

[Remove-AzureRmApplicationGateway](./Remove-AzureRmApplicationGateway.md)

[Set-AzureRmApplicationGateway](./Set-AzureRmApplicationGateway.md)

[Start-AzureRmApplicationGateway](./Start-AzureRmApplicationGateway.md)


