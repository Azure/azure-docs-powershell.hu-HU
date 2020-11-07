---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845877"
---
# New-AzTag

## Áttekintés
Előre definiált Azure címkét hoz létre, vagy hozzáadott értékeket egy meglévő címkéhez | A teljes címkéket létrehoz vagy frissít egy erőforrásban vagy előfizetésben.

## SZINTAXISA

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

## Leírás

**CreatePredefinedTagSet** : a **New-AzTag** parancsmag egy előre definiált, előre meghatározott értéket tartalmazó, előre meghatározott Azure-címkét hoz létre.
Azt is megteheti, hogy további értékeket is felvehet a meglévő előre definiált címkékbe.
Ha előre definiált címkét szeretne létrehozni, adjon meg egy egyedi címkét.
Ha egy meglévő előre definiált címkéhez szeretne értéket hozzáadni, adja meg a meglévő címke nevét és az új értéket.
Ez a parancsmag egy olyan objektumot ad eredményül, amely az új vagy módosított címkét tartalmazza az értékekkel és a hozzájuk rendelt erőforrások számával.
Az Azure címkék modul, amely a **New-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.
Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.
A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.
Ha előre definiált címkét szeretne alkalmazni egy erőforrásra vagy erőforrás-csoportra, használja az New-AzTag parancsmag *címke* paraméterét.
Ha a megadott címke nevével vagy névvel és értékkel rendelkező erőforráscsoportokat szeretne keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.
Minden címkéhez tartozik egy név.
Az értékek nem kötelezők.
Az előre definiált Azure-címkék több értéket is tartalmazhatnak, de ha a címkét erőforrás-vagy erőforrás-csoportra alkalmazza, akkor a címke nevét és csak egy értékét kell alkalmaznia.
Létrehozhat például egy előre definiált részleg címkét, amely egy értékkel rendelkezik az egyes részlegekhez, például a pénzügyi, az emberi erőforrások és az IT-részleghez.
Amikor az osztály címkét egy erőforrásra alkalmazza, csak egy előre meghatározott értéket (például pénzügy) kell alkalmaznia.

**CreateByResourceIdParameterSet** : a **New-AzTag** parancsmag egy **ResourceId** létrehoz vagy frissít egy erőforrás vagy előfizetés teljes címkéket.
Ez a művelet lehetővé teszi a megadott erőforrás vagy előfizetés teljes csoportjának hozzáadását vagy cseréjét. A megadott entitásnak legfeljebb 50 címkéje lehet.

## Példák

### Példa 1: előre definiált címke létrehozása
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.
Ebben a címkében nincs érték.
Egy erőforrás vagy erőforráscsoport értékeit nem tartalmazó címkét alkalmazhat, illetve a **New-AzTag** segítségével értékeket adhat a címkéhez.
Ha a címkét az erőforrás vagy az erőforrás csoportra alkalmazza, akkor megadhat egy értéket is.

### 2. példa: egy értékkel rendelkező előre definiált címke létrehozása
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

A parancs a Pénzügy nevű osztály nevű előre definiált címkét hoz létre.

### 3. példa: érték hozzáadása egy előre definiált címkéhez
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

Ezek a parancsok két értékkel rendelkező részleg nevű előre definiált címkét hoznak létre.
Ha létezik a címke neve, a **New-AzTag** hozzáadja az értéket a meglévő címkéhez, nem pedig új létrehozása helyett.

### 4. példa: előre definiált címke használata
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

Az ebben a példában szereplő parancsok az előre definiált címke létrehozása és használata.

### Példa 5: az előfizetéshez tartozó címkék teljes készletének létrehozása vagy frissítése

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

Ezzel a paranccsal létrehozhatja vagy frissítheti az előfizetéshez tartozó teljes címkéket {subId}.

### 6. példa: az erőforrásokban a teljes címkéket hozza létre vagy frissíti.

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

Ezzel a paranccsal létrehozhatja vagy frissítheti az erőforrás teljes csoportját {resourceId}.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
Az előre definiált címke nevét adja meg.
Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.
Ha egy meglévő címkéhez értéket szeretne hozzáadni, írja be a meglévő címke nevét.
Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzTag** hozzáadja az adott nevet tartalmazó címkét az új címke létrehozása helyett.

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

### -Value (érték)
Az előre definiált címke értékét adja meg.
Az előre definiált címkék több értéket is tartalmazhatnak, de mindegyik parancsban csak egy érték adhatók meg.
Ez a paraméter nem kötelező, mert a címkék értékek nélküli neveket is tartalmazhatnak.

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
A címkézett entitás erőforrás-azonosítója. Lehet, hogy egy erőforrás, egy erőforráscsoport vagy egy előfizetés címkézve van.

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

### -Címke
Az erőforrásra helyezett címkék.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. Collections. Hashtable

## KIMENETEK

### Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag | Microsoft. Azure. Command. Tags. Model. PSTagResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
