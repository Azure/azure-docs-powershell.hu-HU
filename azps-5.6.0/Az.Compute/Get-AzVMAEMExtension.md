---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: ed5f79763d8e9786f0a502f404474eeef2f641f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922113"
---
# Get-AzVMAEMExtension

## SYNOPSIS
Információkat kap az AEM bővítményről.

## SZINTAXIS

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzVMAEMExtension** parancsmag információt kap az Azure Enhanced Monitoring (AEM) bővítményről.

## PÉLDÁK

### 1. példa: Az AEM-bővítmény lekérte
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Ez a parancs információkat kap a contoso-kiszolgáló nevű virtuális gép AEM-bővítményéhez.

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
Egy virtuális gép nevét adja meg.
Ez a parancsmag információt kap az AEM bővítményről a parancsmag által megadott virtuális gépen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
Az operációs rendszer lemezének típusát határozza meg.
Ha az operációs rendszer lemezének nincs típusa, meg kell adnia ezt a paramétert.
A paraméter elfogadható értékei a következőek: Windows és Linux.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy virtuális gép erőforráscsoportját adja meg.
Ez a parancsmag információt kap a virtuális gépen található AEM-bővítményről.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
Azt jelzi, hogy ez a parancsmag csak az AEM kiterjesztés példánynézetét kapja meg.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Egy virtuális gép nevét adja meg.
Ez a parancsmag információt kap a paraméter által megadott virtuális gép AEM-bővítményével kapcsolatban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Set-AzVMAEMExtension](./Set-AzVMAEMExtension.md)

[Test-AzVMAEMExtension](./Test-AzVMAEMExtension.md)


