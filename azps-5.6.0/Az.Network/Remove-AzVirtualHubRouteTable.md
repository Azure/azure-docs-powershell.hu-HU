---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: ecec3482c06c77063ebac71788d5bf2058c9ce64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006086"
---
# Remove-AzVirtualHubRouteTable

## SYNOPSIS
Virtuális központi útvonaltábla-erőforrás törlése egy virtuális központhoz társítva.

## SZINTAXIS

### ByVirtualHubRouteTableName (alapértelmezett)
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubObject
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubRouteTableObject
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubRouteTableResourceId
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Törli a megadott virtuális központhoz társított útvonaltáblát.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

Ez a parancs törli a virtuális hub westushubjáról a routeTable1-et.

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HubName
A szülőerőforrás neve.

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Az eltávolítható virtualhubroutetable erőforrás.

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Az erőforrás neve.

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.

```yaml
Type: SwitchParameter
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
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A virtuálishubroutetable eltávolítható erőforrás erőforrás-azonosítója.

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualHub
{{ Fill VirtualHub Description }}

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.Commands.Network.Models.PSVirtualHub

### Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable

### System.String

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
