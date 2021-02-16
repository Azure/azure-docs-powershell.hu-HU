---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203154"
---
# Get-AzApplicationGatewaySslProfile

## SYNOPSIS
Egy alkalmazás-átjáró SSL-profilját kapja meg.

## SZINTAXIS

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzApplicationGatewaySslProfile** parancsmag egy alkalmazás-átjáró SSL-profilját kapja meg.

## PÉLDÁK

### 1. példa
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs az SSL-profil SslProfile01-et kap a $AppGw és tárolja a $profile változóban.

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
Az ssl-profil neve

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzApplicationGatewaySslProfile](./New-AzApplicationGatewaySslProfile.md)

[Add-AzApplicationGatewaySslProfile](./Add-AzApplicationGatewaySslProfile.md)

[Remove-AzApplicationGatewaySslProfile](./Remove-AzApplicationGatewaySslProfile.md)

[Set-AzApplicationGatewaySslProfile](./Set-AzApplicationGatewaySslProfile.md)