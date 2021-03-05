---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002117"
---
# New-AzAppServiceEnvironmentInboundServices

## SYNOPSIS
Bejövő szolgáltatásokat hoz létre az app szolgáltatási környezetéhez. Az ASEv2 ILB esetén ez létrehoz egy Azure Private DNS-zónát, és a belső IP-címnek megfelelő rekordokat hoz létre. Az ASEv3 esetén továbbá gondoskodni fog arról, hogy az alhálózat letiltotta a hálózati házirendet, és létrehozzon egy privát végpontot.

## SZINTAXIS

### SubnetNameParameterSet
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SubnetIdParameterSet
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzAppServiceEnvironmentInboundServices** parancsmag bejövő szolgáltatásokat hoz létre az appszolgáltatási környezethez.

## PÉLDÁK

### 1. példa: Privát DNS-zóna és rekordok létrehozása az ASEv2 szolgáltatáshoz
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

Create Private DNS Zone and records for ASEv2

### 2. példa: Privát végpont, privát DNS-zóna és ASEv3-rekordok létrehozása
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

Create private endpoint, Private DNS Zone and records for ASEv3

### 3. példa: Privát végpont létrehozása az ASEv3-hoz
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

Privát végpont létrehozása AZ ASEv3-hoz

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
Visszaküldés állapota.

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

### -SkipDns
Ne hozzon létre Azure Private DNS Zone-t és -rekordokat.

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

### -SubnetId
Az alhálózat azonosítója.

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
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
Parameter Sets: SubnetNameParameterSet
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
Parameter Sets: SubnetNameParameterSet
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

[New-AzAppServiceEnvironment](./New-AzAppServiceEnvironment.md)

[Get-AzAppServiceEnvironment](./Get-AzAppServiceEnvironment.md)

[Remove-AzAppServiceEnvironment](./Remove-AzAppServiceEnvironment.md)