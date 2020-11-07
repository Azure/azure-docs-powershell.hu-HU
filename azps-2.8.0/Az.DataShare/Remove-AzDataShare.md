---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: b16e5a9ff2c6e5a898baf56cf237676665bc12c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666700"
---
# Remove-AzDataShare

## Áttekintés
Eltávolítja az adatmegosztást.

## SZINTAXISA

### ByFieldsParameterSet (alapértelmezett)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzDataShare** parancsmag eltávolítja az adatmegosztást.

## Példák

### Példa 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Ez a parancs eltávolítja a AdsShare nevű adatmegosztást az Azure Data Share-fiók WikiAds. 

## PARAMÉTEREK

### -AccountName
Azure Data Share-fiók neve

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

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

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -InputObject
Azure Data Share Object ' ' ' YAML típusa: PSDataShare paraméter-készletek: ByObjectParameterSet aliasok: 

Kötelező: igaz pozíció: névvel ellátott alapértelmezett érték: nincs elfogadás csővezeték-bevitel: igaz (ByValue) elfogadja a helyettesítő karaktereket: false


### -Name (név)
Azure-adatmegosztás neve

YAML típusa: karakterlánc-paraméterek halmaza: ByFieldsParameterSet aliasok: 

Kötelező: igaz pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false


### -PassThru
Visszatérési objektum (ha meg van adva)

YAML típus: SwitchParameter paraméterek: (all) aliasok: 

Kötelező: hamis pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false


### -ResourceGroupName
Az Azure Data Share-fiók erőforráscsoport-neve

YAML típusa: karakterlánc-paraméterek halmaza: ByFieldsParameterSet aliasok: 

Kötelező: igaz pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false


### -ResourceId
Az Azure-adatmegosztás erőforrás-azonosítója

YAML típusa: karakterlánc-paraméterek halmaza: ByResourceIdParameterSet aliasok: 

Kötelező: igaz pozíció: névvel ellátott alapértelmezett érték: nincs elfogadás csővezeték-bevitel: igaz (ByPropertyName) elfogadja a helyettesítő karaktereket: false


### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

YAML típus: SwitchParameter paraméterek: (all) aliasok: CF

Kötelező: hamis pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false


### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

YAML típus: SwitchParameter paraméterek: (all) aliasok: Wi

Kötelező: hamis pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Azure-adatmegosztás neve

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Visszatérési objektum (ha meg van adva)

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

### -ResourceGroupName
Az Azure Data Share-fiók erőforráscsoport-neve

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Az Azure-adatmegosztás erőforrás-azonosítója

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
