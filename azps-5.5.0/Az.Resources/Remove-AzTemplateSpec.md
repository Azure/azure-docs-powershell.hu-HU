---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156450"
---
# Remove-AzTemplateSpec

## SYNOPSIS
Sablon specifikációjának eltávolítása

## SZINTAXIS

### RemoveByNameParameterSet (alapértelmezett)
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByIdParameterSet
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Eltávolít egy adott sablon specifikációját. Ha a **version -Version paraméter** meg van adva, csak a megadott verzió lesz eltávolítva. Ha nem ad meg konkrét verziót, a Sablon specifikációja és annak összes verziója törlődik. Ha a **-Force** jelölő jelen van, nem lesz eltávolításra vonatkozó megerősítő üzenet.

## PÉLDÁK

### 1. példa: Egy adott verzió eltávolítása név szerint
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Eltávolítja a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját a "myRG" erőforráscsoporton belül.

### 2. példa: Adott verzió eltávolítása erőforrás-azonosító alapján
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Eltávolítja a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verzióját az előfizetés alazonosítójának "myRG" \{ erőforráscsoportján \} belül.

### 3. példa: Sablon specifikációjának és minden verziójának eltávolítása név szerint
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Eltávolítja a "MyTemplateSpec" nevű sablon specifikációját és annak összes verzióját a "myRG" erőforráscsoporton belül.

### 3. példa: Sablon specifikációjának és minden verziójának eltávolítása erőforrás-azonosító alapján
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

Eltávolítja a "MyTemplateSpec" nevű sablont és annak összes verzióját az előfizetés alazonosítójának "myRG" \{ erőforráscsoportján \} belül.

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

### -Force
Ne kérjen megerősítést.

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

### -Name
A sablon specifikációjának neve.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A sablon specifikációjának erőforráscsoportjának neve.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A törölni kívánt sablonverzió.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
