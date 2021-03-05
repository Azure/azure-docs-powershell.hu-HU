---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012261"
---
# Get-AzContainerInstanceLog

## SYNOPSIS
Egy tárolócsoportban található tárolópéldány naplóinak lekérte.

## SZINTAXIS

### GetContainerInstanceLogByNamesParamSet (alapértelmezett)
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetContainerInstanceLogByPSContainerGroupParamSet
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetContainerInstanceLogByResourceIdParamSet
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzContainerInstanceLog** parancsmag egy tárolócsoportban található tároló naplóit kapja meg.

## PÉLDÁK

### 1. példa: Egy tárolópéldány farkanaplója
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

A napló `container1` lekérte a tárolócsoportból. `mycontainer` Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.

### 2. példa: A tárolócsoport nevével azonos nevű tárolópéldány naplója
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

A napló `mycontainer` lekérte a tárolócsoportból. `mycontainer` Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.

### 3. példa: Egy tárolópéldány 2. naplósorának lekérte
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

Szerezze be a 2 sornyi naplót a `container1` `mycontainer` tárolócsoportból.

### 4. példa: Egy tárolócsoportba bevezető tárolópéldány farkanaplója
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

A naplót a `mycontainer` tárolócsoportba bevezető naplóból szerezze `mycontainer` be. Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.

## PARAMETERS

### -ContainerGroupName
A tárolócsoport neve.

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputContainerGroup
A bemeneti tárolócsoport-objektum.

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A tárolópéldány neve a tárolócsoportban.
Alapértelmezett: ugyanaz, mint a tárolócsoport neve

```yaml
Type: System.String
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
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás azonosítója.

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tail
A naplót kiszéleső vonalak száma.
Ha nincs meg határozva, a parancsmag legfeljebb 4 MBszélű naplót fog visszaadni

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup

### System.String

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
