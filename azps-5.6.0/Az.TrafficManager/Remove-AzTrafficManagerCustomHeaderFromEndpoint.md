---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936466"
---
# Remove-AzTrafficManagerCustomHeaderFromEndpoint

## SYNOPSIS
Eltávolítja az egyéni fejlécadatokat egy helyi Traffic Manager-végpontobjektumból.

## SZINTAXIS

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzTrafficManagerCustomHeaderFromEndpoint** parancsmag eltávolítja az egyéni fejlécadatokat egy helyi Azure Traffic Manager-végpontobjektumból.
Végpontot a New-AzTrafficManagerEndpoint parancsmagok Get-AzTrafficManagerEndpoint le.

Ez a parancsmag a helyi végpontobjektumon működik.
A Módosítások véglegesítése a Forgalomkezelő végpontjára a Set-AzTrafficManagerEndpoint parancsmag használatával.

## PÉLDÁK

### 1. példa: Egyéni alhálózati adatok eltávolítása egy végpontról
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Az első parancs a Contoso nevű Azure-végpontot a ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljából kapja meg, majd az objektumot a $TrafficManagerEndpoint tárolja.
A második parancs eltávolítja az egyéni fejlécadatokat a $TrafficManagerEndpoint.
Az utolsó parancs frissíti a Traffic Managerben a végpontot úgy, hogy megfeleljen a helyi $TrafficManagerEndpoint.

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

### -Name
Az eltávolítható egyéni fejlécinformációk nevét adja meg.

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

### -TrafficManagerEndpoint
Helyi **TrafficManagerEndpoint-objektumot ad** meg.
Ez a parancsmag módosítja ezt a helyi objektumot.
A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## KIMENETEK

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzTrafficManagerCustomHeaderToEndpoint](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
