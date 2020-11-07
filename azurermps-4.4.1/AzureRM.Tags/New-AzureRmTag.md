---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679306"
---
# New-AzureRmTag

## Áttekintés
Előre definiált Azure címkét hoz létre, vagy értékeket ad hozzá egy meglévő címkéhez.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRmTag** parancsmag egy előre definiált, előre meghatározott értéket tartalmazó Azure címkét hoz létre.
Azt is megteheti, hogy további értékeket is felvehet a meglévő előre definiált címkékbe.
Ha előre definiált címkét szeretne létrehozni, adjon meg egy egyedi címkét.
Ha egy meglévő előre definiált címkéhez szeretne értéket hozzáadni, adja meg a meglévő címke nevét és az új értéket.

Ez a parancsmag egy olyan objektumot ad eredményül, amely az új vagy módosított címkét tartalmazza az értékekkel és a hozzájuk rendelt erőforrások számával.

Az Azure címkék modul, amely a **New-AzureRmTag** része, segíthet az előre definiált Azure-címkék kezelésében.
Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.

A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.
Ha az előfizetéshez tartozik egy előre definiált címke, az előfizetésben nem alkalmazhat definiálatlan címkéket vagy értékeket az előfizetésben szereplő erőforrásokra vagy erőforrás-csoportokra.

Ha előre definiált címkét szeretne alkalmazni egy erőforrásra vagy erőforrás-csoportra, használja az New-AzureRmTag parancsmag *címke* paraméterét.
Ha a megadott címke nevével vagy névvel és értékkel rendelkező erőforráscsoportokat szeretne keresni, használja az Get-AzureRMResourceGroup parancsmag *címke* paraméterét.

Minden címkéhez tartozik egy név.
Az értékek nem kötelezők.
Az előre definiált Azure-címkék több értéket is tartalmazhatnak, de ha a címkét erőforrás-vagy erőforrás-csoportra alkalmazza, akkor a címke nevét és csak egy értékét kell alkalmaznia.
Létrehozhat például egy előre definiált részleg címkét, amely egy értékkel rendelkezik az egyes részlegekhez, például a pénzügyi, az emberi erőforrások és az IT-részleghez.
Amikor az osztály címkét egy erőforrásra alkalmazza, csak egy előre meghatározott értéket (például pénzügy) kell alkalmaznia.

## Példák

### Példa 1: előre definiált címke létrehozása
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

Ez a parancs létrehoz egy FY2015 nevű előre definiált címkét.
Ebben a címkében nincs érték.
Egy erőforrás vagy erőforráscsoport értékeit nem tartalmazó címkét alkalmazhat, illetve a **New-AzureRmTag** segítségével értékeket adhat a címkéhez.
Ha a címkét az erőforrás vagy az erőforrás csoportra alkalmazza, akkor megadhat egy értéket is.

### 2. példa: egy értékkel rendelkező előre definiált címke létrehozása
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

A parancs a Pénzügy nevű osztály nevű előre definiált címkét hoz létre.

### 3. példa: érték hozzáadása egy előre definiált címkéhez
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Ezek a parancsok két értékkel rendelkező részleg nevű előre definiált címkét hoznak létre.
Ha létezik a címke neve, a **New-AzureRmTag** hozzáadja az értéket a meglévő címkéhez, nem pedig új létrehozása helyett.

### 4. példa: előre definiált címke használata
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

## PARAMÉTEREK

### -Name (név)
A címke nevét adja meg.
Új előre definiált címke létrehozásához adjon meg egy egyedi nevet.

Ha egy meglévő címkéhez értéket szeretne hozzáadni, írja be a meglévő címke nevét.
Ha egy meglévő előre definiált címke rendelkezik a megadott névvel, a **New-AzureRmTag** hozzáadja az adott nevet tartalmazó címkét az új címke létrehozása helyett.

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

### -Value (érték)
A címke értékét adja meg.
Az előre definiált címkék több értéket is tartalmazhatnak, de mindegyik parancsban csak egy érték adhatók meg.
Ez a paraméter nem kötelező, mert a címkék értékek nélküli neveket is tartalmazhatnak.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. Tags. Model. PSTag

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


