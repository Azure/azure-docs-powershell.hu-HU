---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: f9afc10613024d99cfa6b03b260324b3e5d22586
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669325"
---
# Remove-AzTag

## Áttekintés
Előre definiált Azure-címkék vagy-értékek törlése

## SZINTAXISA

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzTag** parancsmag előre definiált Azure-címkéket és-értékeket töröl az előfizetésből.
Ha egy előre definiált címkéből szeretne bizonyos értékeket törölni, használja az *érték* paramétert.
A **Remove-AzTag** alapértelmezés szerint törli a megadott címkét és annak minden értékét. Az erőforrásokra vagy erőforrásokra jelenleg alkalmazott címke vagy érték nem törölhető.
Mielőtt a **Remove-AzTag** használja, az Set-AzResourceGroup parancsmag *címke* paraméterével törölheti az erőforrás vagy az erőforrás csoport címkéjét vagy értékét.
Az Azure címkék modul, amely **eltávolítja a-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.
Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.
A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.

## Példák

### Példa 1: előre definiált címke törlése
```
PS C:\>Remove-AzTag -Name "Department"
```

Ez a parancs törli a részleg és az összes erőforrása nevű előre definiált címkét.
Ha a címkét erőforrásokra vagy erőforrás-csoportokra alkalmazta, akkor a parancs nem működik.

### 2. példa: az előre definiált címke értékének törlése
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Ez a parancs törli az HumanResources értéket az előre definiált részleg címkéből.
Nem törli a címkét.
Ha az érték minden erőforrásra vagy erőforrás-csoportra érvényes, a parancs nem működik.

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
A törlendő címke nevét adja meg.
A **Remove-AzTag** alapértelmezés szerint eltávolítja a megadott címkét és annak minden értékét.
Ha törölni szeretné a kijelölt értékeket, de nem szeretné törölni a címkét, használja az *érték* paramétert.

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

### -PassThru
Egy olyan objektumot ad eredményül, amely a törölt címkét vagy az eredményül kapott címkét jelöli a törölt értékekkel.

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

### -Value (érték)
Törli a megadott értékeket az előre definiált címkéből, de nem törli a címkét.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. string []

### System. Management. Automation. SwitchParameter

## KIMENETEK

### Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzTag](./Get-AzTag.md)

[Új – AzTag](./New-AzTag.md)


