---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008709"
---
# Set-AzServiceEndpointPolicy

## SYNOPSIS
Szolgáltatásvégpont-házirend frissítése.

## SZINTAXIS

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzServiceEndpointPolicy** parancsmag szolgáltatási végponti házirendet hoz létre.

## PÉLDÁK

### 1. példa: Szolgáltatásvégpont-házirendet állít be
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

Ez a parancs frissíti az "erőforráscsoport1" erőforráscsoporthoz tartozó objektumobjektum által $serviceEndpointPolicy Házirend1 nevű szolgáltatásvégpont-házirendet.

## PARAMETERS

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

### -ServiceEndpointPolicy
The ServiceEndpointPolicy

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzServiceEndpointPolicy](./Get-AzServiceEndpointPolicy.md)

[New-AzServiceEndpointPolicy](./New-AzServiceEndpointPolicy.md)

[Remove-AzServiceEndpointPolicy](./Remove-AzServiceEndpointPolicy.md)
