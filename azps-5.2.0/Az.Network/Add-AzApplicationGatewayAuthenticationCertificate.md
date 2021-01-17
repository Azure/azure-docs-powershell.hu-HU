---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335285"
---
# Add-AzApplicationGatewayAuthenticationCertificate

## SYNOPSIS
Hozzáad egy hitelesítési tanúsítványt egy alkalmazás-átjáróhoz.

## SZINTAXIS

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzApplicationGatewayAuthenticationCertificate parancsmag** hozzáad egy hitelesítési tanúsítványt egy Azure-alkalmazás-átjáróhoz.

## PÉLDÁK

### 1. példa: Hitelesítési tanúsítvány hozzáadása alkalmazás-átjáróhoz
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

Az első parancs egy appGwName nevű alkalmazás-átjárót kap, és egy $appgw tárolja.
A második parancs hozzáadja a cert01 nevű hitelesítési tanúsítványt az alkalmazás-átjáróhoz.
A harmadik parancs frissíti az alkalmazás átjáróját.

## PARAMETERS

### -ApplicationGateway
Megadja annak az alkalmazás-átjárónak a nevét, amelyhez ez a parancsmag hozzáad egy hitelesítési tanúsítványt.

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

### -CertificateFile
A parancsmag által megadott hitelesítési tanúsítvány elérési útját adja meg.

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
Annak a tanúsítványnak a nevét adja meg, amely az alkalmazás-átjáróhoz hozzáadható.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApplicationGatewayAuthenticationCertificate](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[New-AzApplicationGatewayAuthenticationCertificate](./New-AzApplicationGatewayAuthenticationCertificate.md)

[Remove-AzApplicationGatewayAuthenticationCertificate](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[Set-AzApplicationGatewayAuthenticationCertificate](./Set-AzApplicationGatewayAuthenticationCertificate.md)


