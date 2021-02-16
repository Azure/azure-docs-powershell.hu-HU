---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203264"
---
# Add-AzApplicationGatewayBackendAddressPool

## SYNOPSIS
Háttércímkészletet ad hozzá egy alkalmazás-átjáróhoz.

## SZINTAXIS

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzApplicationGatewayBackendAddressPool** parancsmag hozzáad egy háttércímkészletet egy alkalmazás-átjáróhoz.
A háttércímek IP-címek, teljes tartománynév (FQDN) vagy IP-konfigurációs IP-címek használatával is megadva.

## PÉLDÁK

### 1. példa: Háttércímkészlet hozzáadása háttérkiszolgáló teljes tartományának használatával
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs a teljes tartományon keresztül hozzáadja a $AppGw az alkalmazás-átjáró háttércímkészletét.

### 2. példa: Háttércímkészlet hozzáadása háttérkiszolgálói IP-címek használatával
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs IP-címek használatával hozzáadja az adott helyen tárolt alkalmazás$AppGw címkészletét.

## PARAMETERS

### -ApplicationGateway
Megadja azt az alkalmazás-átjárót, amelyhez ez a parancsmag hozzáad egy háttércímkészletet.

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

### -BackendFqdns
Megadja a háttérkiszolgálói FQDN-ek listáját, amelyeket ez a parancsmag háttérkiszolgáló-készletként ad hozzá.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendIPAddresses
Megadja a háttér-IP-címek listáját, amelyeket ez a parancsmag háttérkiszolgáló-készletként ad hozzá.

```yaml
Type: System.String[]
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

### -Name
A parancsmag által hozzáadt háttérkiszolgáló-készlet neve.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[Remove-AzApplicationGatewayBackendAddressPool](./Remove-AzApplicationGatewayBackendAddressPool.md)

[Set-AzApplicationGatewayBackendAddressPool](./Set-AzApplicationGatewayBackendAddressPool.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)
