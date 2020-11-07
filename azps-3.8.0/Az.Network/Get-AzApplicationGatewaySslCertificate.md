---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846198"
---
# Get-AzApplicationGatewaySslCertificate

## Áttekintés
SSL-tanúsítványt kap egy alkalmazás-átjáróhoz.

## SZINTAXISA

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzApplicationGatewaySslCertificate** parancsmag SSL-tanúsítványt kap az alkalmazás-átjáróhoz.

## Példák

### 1. példa: adott SSL-tanúsítvány beszerzése
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.
A második parancs a Cert01 nevű SSL-tanúsítványt kapja meg az $AppGW nevű változóban tárolt alkalmazás-átjáróban.
A parancs a $Cert nevű változóban tárolja a tanúsítványt.

### 2. példa: az SSL-tanúsítványok listájának beszerzése
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.
Ez a második parancs a $AppGW nevű változóban tárolt alkalmazás-átjáróból kapja meg az SSL-tanúsítványok listáját.
A parancs ezután a $Certs nevű változóban tárolja az eredményeket.

## PARAMÉTEREK

### -ApplicationGateway
Az SSL-tanúsítványt tartalmazó Application Gateway-objektum.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak az SSL-tanúsítványtárolónak a nevét adja meg, amelyre a parancsmag bekerül.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGateway

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewaySslCertificate](./Add-AzApplicationGatewaySslCertificate.md)

[Új – AzApplicationGatewaySslCertificate](./New-AzApplicationGatewaySslCertificate.md)

[Remove-AzApplicationGatewaySslCertificate](./Remove-AzApplicationGatewaySslCertificate.md)

[Set-AzApplicationGatewaySslCertificate](./Set-AzApplicationGatewaySslCertificate.md)


