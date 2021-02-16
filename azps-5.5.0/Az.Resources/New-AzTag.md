---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150883"
---
# New-AzTag

## SYNOPSIS
Előre definiált Azure-címkét hoz létre, vagy értékeket ad hozzá egy meglévő | Létrehozza vagy frissíti a címkék teljes készletét egy erőforráson vagy előfizetésen.

## SZINTAXIS

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## LEÍRÁS

**CreatePredefinedTagSet:** A **New-AzTag** parancsmag létrehoz egy előre definiált Azure-címkét egy opcionális előre definiált értékkel.
Emellett további értékeket is hozzáadhat a meglévő előre definiált címkékhez.
Előre definiált címke létrehozásához adjon meg egy egyedi címkenevet.
Ha egy meglévő előre definiált címkéhez szeretne értéket adni, adja meg a meglévő címke nevét és az új értéket.
Ez a parancsmag egy olyan objektumot ad vissza, amely az új vagy módosított címkét az értékeivel és az erőforrások számával együtt képviseli.
Az Azure Címkék modul, amely részét képezi a **New-AzTag,** segíthet az előre definiált Azure-címkék kezelésében.
Az Azure-címkék olyan névérték-párok, amelyek segítségével kategorizálhatja azure-erőforrásait és erőforráscsoportját, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokra és csoportokra vonatkozó megjegyzéseket vagy megjegyzéseket.
Egyetlen lépésben definiálhat és alkalmazhat címkéket, az előre definiált címkékkel azonban szabványos, egységes, kiszámítható neveket és értékeket határozhat meg az előfizetésében szereplő címkékhez.
Ha előre definiált címkét szeretne alkalmazni egy  erőforrásra vagy erőforráscsoportra, használja a New-AzTag címke paraméterét.
Ha egy megadott címkenévvel vagy névvel és  értékkel megadott erőforráscsoportokat keres, használja a Get-AzResourceGroup parancsmag címke paraméterét.
Minden címkének van neve.
Az értékek megadása nem kötelező.
Az előre definiált Azure-címkéknek több értékük is lehet, de amikor a címkét egy erőforrásra vagy erőforráscsoportra alkalmazza, a címke nevét és csak az egyik értékét alkalmazza.
Létrehozhat például egy előre definiált Részleg címkét, amely minden részleghez egy-egy értéket (például Pénzügy, Emberi erőforrások és It-részleg) igényel.
Amikor a Department címkét egy erőforrásra alkalmazza, csak egy előre definiált értéket (például Pénzügy) alkalmaz.

**CreateByResourceIdParameterSet:** A **ResourceId** azonosítóval létrehozott **New-AzTag** parancsmag létrehozza vagy frissíti egy erőforrás vagy előfizetés címkéinek teljes készletét.
Ez a művelet lehetővé teszi a címkék teljes készletének hozzáadását vagy cseréjét a megadott erőforráson vagy előfizetésen. A megadott entitás legfeljebb 50 címkével lehet.

## PÉLDÁK

### 1. példa: Előre definiált címke létrehozása
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.
Ez a címke nem tartalmaz értékeket.
Az erőforrás- vagy erőforráscsoportokra érték nélkül is alkalmazhat értékeket, illetve a **New-AzTag** segítségével is hozzáadhat értékeket a címkéhez.
A címkének az erőforrásra vagy erőforráscsoportra való alkalmazásakor is megadhat egy értéket.

### 2. példa: Előre definiált címke létrehozása értékkel
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Ez a parancs létrehoz egy Részleg nevű előre definiált címkét pénzügyi értékkel.

### 3. példa: Érték hozzáadása előre definiált címkéhez
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Ezek a parancsok egy Előre definiált Részleg nevű címkét hoznak létre két értékkel.
Ha a címke neve létezik, a **New-AzTag** új címke létrehozása helyett hozzáadja az értéket a meglévő címkéhez.

### 4. példa: Előre definiált címke használata
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

A példában a parancsok előre definiált címkét hoznak létre és használnak.

### 5. példa: Címkék teljes készletét hozza létre vagy frissíti az előfizetésben

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Ez a parancs létrehozza vagy frissíti az előfizetésben található címkék teljes készletét a(z) {subId} értékkel.

### 6. példa: Létrehozza vagy frissíti az erőforrás teljes címkéit

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Ez a parancs létrehozza vagy frissíti az erőforrás teljes címkéit a(z) {resourceId} értékkel.

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
Az előre definiált címke nevét adja meg.
Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.
Ha egy meglévő címkéhez szeretne értéket adni, írja be a meglévő címke nevét.
Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzTag** új címke létrehozása helyett hozzáadja a megadott értéket (ha van ilyen) a címkéhez.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Érték
Egy előre definiált címkeértéket ad meg.
Az előre definiált címkéknek több értékük is lehet, de minden parancsban csak egy értéket lehet megadni.
Ez a paraméter nem kötelező, mivel a címkéknek érték nélküli neve is lehet.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
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
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Az erőforrásra vonatkozó címkék.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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

### System.Collections.Hashtable

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)