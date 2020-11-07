---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: ccef6b60dd33ebc584f782899134509a4e89f2be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672214"
---
# Get-AzureRmApplicationGatewayBackendAddressPool

## Áttekintés
A back-end-címkészlet egy alkalmazás átjárója számára.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás

## Példák

### Példa 1: meghatározott back-end Server-készlet beszerzése
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.
A második parancs a $AppGw nevű Pool01 társított back-end címkészletet kapja meg, és a $BackendPool változóban tárolja.

### 2. példa: a back-end Server-készlet listájának beszerzése
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.
A második parancs a $AppGwhoz társított back-end-címkészlet listáját kapja, és a listát a $BackendPools változóban tárolja.

## PARAMÉTEREK

### -ApplicationGateway
A **Get-AzureRmApplicationGatewayBackendAddressPool** parancsmag a back-end címkészletet adja az alkalmazás-átjárók számára.

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

### -Name (név)
Annak a végpontnak a neve, amely a parancsmagot kapja.

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

### Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmApplicationGatewayBackendAddressPool](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[Új – AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[Remove-AzureRmApplicationGatewayBackendAddressPool](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[Set-AzureRmApplicationGatewayBackendAddressPool](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


