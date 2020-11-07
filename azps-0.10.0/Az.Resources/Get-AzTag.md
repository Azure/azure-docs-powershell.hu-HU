---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 1f2289351da276a0422828c082bb51d8dc267a20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843389"
---
# Get-AzTag

## Áttekintés
Előre definiált Azure-címkéket kap.

## SZINTAXISA

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzTag** parancsmag előre meghatározott Azure-címkéket kap az előfizetésben.
Ez a parancsmag alapvető információkat ad a címkékről vagy a címkékről és az azok értékeiről.
Minden kimeneti objektum tartalmazza a Count tulajdonságot, amely az erőforrások és az erőforráscsoportok számát adja meg, és a címkéket és az értékeket alkalmazza.
A **Get-AzTag** Azure címkéi modul segítséget nyújt az előre definiált Azure-címkék kezelésében.
Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.
A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.
Ha előre definiált címkét szeretne létrehozni, használja az New-AzTag parancsmagot.
Ha egy erőforráscsoport számára előre meghatározott címkét szeretne alkalmazni, használja az New-AzTag parancsmag *címke* paraméterét.
Ha egy adott címke vagy név és érték esetén szeretne erőforrás-csoportokat keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.

## Példák

### Példa 1: az összes előre definiált címke beolvasása
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Ez a parancs az előfizetésben minden előre definiált címkét kap.
A Count tulajdonság azt jeleníti meg, hogy hányszor alkalmazta a címkét az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.

### 2. példa: név szerinti címke beszerzése
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Ez a parancs részletes információkat kap a részleg címkéről és annak értékeiről.
A Count tulajdonság azt jeleníti meg, hogy hányszor lett alkalmazva a címke és az egyes értékek az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.

### 3. példa: az összes címke értékének beolvasása
```
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Ez a parancs a *részletes* adatokat részletesen részletezi az előfizetésben szereplő összes előre definiált címkével kapcsolatban.
A *részletes* paraméter a minden címkéhez tartozó *Name* paramétert használja.

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

### – Részletes
Azt jelzi, hogy ez a művelet a kimenetre vonatkozó értékek címkézésével kapcsolatos információkat ad hozzá.

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

### -Name (név)
A beolvasott címke nevét adja meg.
Alapértelmezés szerint a **Get-AzTag** az előfizetésben szereplő összes előre definiált címkére vonatkozó alapvető információkat kapja meg.
A *Name* paraméter megadásakor a *részletes* paraméternek nincs eredménye.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Management. Automation. SwitchParameter

## KIMENETEK

### Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

