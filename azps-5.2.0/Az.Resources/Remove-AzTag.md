---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354822"
---
# Remove-AzTag

## SYNOPSIS
Előre definiált Azure-címkék vagy -értékek törlése | Törli egy erőforrás vagy előfizetés címkéinek teljes készletét.

## SZINTAXIS

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## LEÍRÁS

**RemovePredefinedTagSet:** A **Remove-AzTag** parancsmag törli az előre definiált Azure-címkéket és -értékeket az előfizetéséből.
Ha törölni szeretne bizonyos értékeket egy előre definiált címkéből, használja az *Érték paramétert.*
Alapértelmezés szerint **a Remove-AzTag** törli a megadott címkét és annak összes értékét. Az erőforrás- vagy erőforráscsoportokra jelenleg alkalmazott címkék és értékek nem törölhetők.
A **Remove-AzTag** parancsmag  használata előtt a Set-AzResourceGroup parancsmag Címke paraméterével törölje a címkét vagy értékeket az erőforrás- vagy erőforráscsoportból.
Az Azure Tags modul, amely a **Remove-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.
Az Azure-címkék olyan névérték-párok, amelyek segítségével kategorizálhatja azure-erőforrásait és erőforráscsoportját, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokra és csoportokra vonatkozó megjegyzéseket vagy megjegyzéseket.
Egyetlen lépésben definiálhat és alkalmazhat címkéket, az előre definiált címkékkel azonban szabványos, egységes, kiszámítható neveket és értékeket határozhat meg az előfizetésében szereplő címkékhez.

**RemoveByResourceIdParameterSet:** A **Remove-AzTag** parancsmag egy **ResourceId** értékkel törli egy erőforrás vagy előfizetés címkéinek teljes készletét.

## PÉLDÁK

### 1. példa: Előre definiált címke törlése
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Ez a parancs törli a Department (Részleg) nevű előre definiált címkét és annak összes értékét.
Ha a címkét bármely erőforrásra vagy erőforráscsoportra alkalmazta, a parancs nem fog sikerülni.

### 2. példa: Érték törlése egy előre definiált címkéből
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Ez a parancs törli a HumanResources értéket az előre definiált Department címkéből.
Nem törli a címkét.
Ha az értéket valamelyik erőforrásra vagy erőforráscsoportra alkalmazta, a parancs nem fog sikerülni.

### 3. példa: Az előfizetés teljes címkéinek törlése

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Ez a parancs törli az előfizetés összes címkéét a(z) {subId} azonosítóval. Nem fogja visszaadni a törölt objektumot, ha nem adja át a "-PassThru" adatokat.

### 4. példa: Az erőforrás teljes címkéinek törlése

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Ezzel a paranccsal az erőforrás összes címkéje törölhető a következővel: {resourceId}. Visszaadja a töröltectect értéket, amikor a "-PassThru" értéket adja át.

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
Az eltávolítandó előre definiált címke nevét adja meg.
Alapértelmezés szerint **a Remove-AzTag** eltávolítja a megadott címkét és annak összes értékét.
Ha törölni szeretné a kijelölt értékeket, de a címkét nem, használja az *Érték paramétert.*

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Érték
Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A címkézett entitás erőforrás-azonosítója. Előfordulhat, hogy egy erőforrás, erőforráscsoport vagy előfizetés meg van címkézve.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Visszaad egy objektumot, amely a törölt címkét vagy a törölt értékkel létrehozott címkét jelöli.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.String[]

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)