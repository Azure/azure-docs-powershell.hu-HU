---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7f5dbd73158e5328ece78b1064a78ff5c4627035
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924017"
---
# Get-AzApplicationGatewayAuthenticationCertificate

## SYNOPSIS
Hitelesítési tanúsítványt kap egy alkalmazás-átjáróhoz.

## SZINTAXIS

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzApplicationGatewayAuthenticationCertificate parancsmag egy Azure-alkalmazás** átjáróhoz kap egy hitelesítési tanúsítványt.

## PÉLDÁK

### 1. példa: Megadott hitelesítési tanúsítvány lekérve
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és a $appgw tárolja.
A második parancs lekéri a cert01 nevű hitelesítési tanúsítványt, és a hitelesítő $cert tárolja.

## PARAMETERS

### -ApplicationGateway
Megadja annak az alkalmazás-átjárónak a nevét, amelyhez ez a parancsmag hitelesítési tanúsítványt kap.

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

### -Name
Annak a hitelesítési tanúsítványnak a nevét adja meg, amely a parancsmagot kapja.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewayAuthenticationCertificate](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[New-AzApplicationGatewayAuthenticationCertificate](./New-AzApplicationGatewayAuthenticationCertificate.md)

[Remove-AzApplicationGatewayAuthenticationCertificate](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[Set-AzApplicationGatewayAuthenticationCertificate](./Set-AzApplicationGatewayAuthenticationCertificate.md)


