---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 3c9b9b97e26738234acdf2c8f09c0e1da5eae2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918689"
---
# Set-AzApplicationGatewayTrustedClientCertificate

## SYNOPSIS
Módosítja egy alkalmazás-átjáró megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncát.

## SZINTAXIS

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzApplicationGatewayTrustedClientCertificate** parancsmag módosítja egy alkalmazás-átjáró megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncát.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

A fenti példa azt mutatja be, hogy miként frissíthet egy megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát. Az első parancs egy alkalmazás-átjárót kap, és a $gw tárolja. A második parancs módosítja a meglévő megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncobjektumát egy új hitelesítésszolgáltatói tanúsítványláncfájllal. A harmadik parancs frissíti az alkalmazás-átjárót az Azure-on.

## PARAMETERS

### -ApplicationGateway
Az applicationGateway

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificateFile
A megbízható ügyfél-hitelesítésszolgáltató tanúsítványának láncfájlja elérési útja

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve

```yaml
Type: String
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApplicationGatewayTrustedClientCertificate](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[New-AzApplicationGatewayTrustedClientCertificate](./New-AzApplicationGatewayTrustedClientCertificate.md)

[Get-AzApplicationGatewayTrustedClientCertificate](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[Remove-AzApplicationGatewayTrustedClientCertificate](./Remove-AzApplicationGatewayTrustedClientCertificate.md)