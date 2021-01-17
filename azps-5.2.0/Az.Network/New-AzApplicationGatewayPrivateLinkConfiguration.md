---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371684"
---
# New-AzApplicationGatewayPrivateLinkConfiguration

## SYNOPSIS
Privát csatolási konfigurációt hoz létre egy alkalmazás-átjáróhoz

## SZINTAXIS

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzApplicationGatewayPrivateLinkConfiguration** parancsmag létrehoz egy PrivateLink-konfigurációt egy Azure-alkalmazásátjáróhoz.
A privát csatolási funkciót csak előlapi IP-konfigurációval lehet konfigurálni.
Egy privát csatolás-konfigurációt legalább egy előlapi IP-konfigurációhoz lehet társítva az alkalmazás-átjárón.

## PÉLDÁK

### 1. példa: Privát hivatkozás konfigurálása egyetlen IP-konfigurációval
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

Ez a parancs létrehoz egy "privateLinkConfig01" nevű PrivateLink-konfigurációt, és az eredményt a következő nevű változóban $PrivateLinkConfiguration.

### 2. példa: Privát hivatkozáskonfiguráció létrehozása több IP-konfigurációval
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

Ez a parancs létrehoz egy "privateLinkConfig01" nevű PrivateLink-konfigurációt két ipConfigurációval, és az eredményt a $PrivateLinkConfiguration. 

## PARAMETERS

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

### -IpConfiguration
Az ipConfiguration listája

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
A privateLink-konfiguráció neve

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApplicationGatewayPrivateLinkConfiguration](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[Add-AzApplicationGatewayPrivateLinkConfiguration](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[Remove-AzApplicationGatewayPrivateLinkConfiguration](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[Set-AzApplicationGatewayPrivateLinkConfiguration](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
