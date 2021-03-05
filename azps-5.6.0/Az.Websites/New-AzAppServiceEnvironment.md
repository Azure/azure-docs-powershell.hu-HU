---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011141"
---
# New-AzAppServiceEnvironment

## SYNOPSIS
Appszolgáltatás-környezetet hoz létre, beleértve az ajánlott útválasztási táblát és hálózati biztonsági csoportot

## SZINTAXIS

### ASEv2SubnetNameParameterSet
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ASEv3SubnetNameParameterSet
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ASEv2SubnetIdParameterSet
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ASEv3SubnetIdParameterSet
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzAppServiceEnvironment** parancsmag appszolgáltatási környezetet hoz létre.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group

### 2. példa
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

A MyAseV2 nevű appszolgáltatás-környezet létrehozása ajánlott útválasztási tábla és hálózati biztonsági csoport nélkül.
Ezeket az appszolgáltatás-környezet kiépítése előtt vagy közvetlenül az után kell létrehoznia, hogy a megfelelő példány működőképes legyen.

## PARAMETERS

### -AsJob
Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### -Kind
Az app szolgáltatási környezetének verziója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerMode
Az app szolgáltatási környezet terheléselosztási módja.

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Az appszolgáltatás környezetének helye, például: Nyugat-Európa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Az app szolgáltatási környezetének neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Adja vissza az app szolgáltatási környezetének objektumát.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNetworkSecurityGroup
Ne hozza létre az ajánlott hálózatbiztonsági csoportot az app szolgáltatási környezete részeként.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipRouteTable
Ne hozza létre az ajánlott útvonaltáblát az app szolgáltatási környezete részeként.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Az alhálózat azonosítója.

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Az alhálózat neve. A -VirtualNetworkName névvel együtt használható, és az ASE-val azonos erőforráscsoportban kell lennie. Ha nem, használja az -SubnetId

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
A vNet neve. -Alhálózatnévvel együtt használható, és az ASE-val azonos erőforráscsoportban kell lennie. Ha nem, használja az -SubnetId

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### System.Object
## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAppServiceEnvironment](./Get-AzAppServiceEnvironment.md)

[New-AzAppServiceEnvironmentInboundServices](./New-AzAppServiceEnvironmentInboundServices.md)

[Remove-AzAppServiceEnvironment](./Remove-AzAppServiceEnvironment.md)
