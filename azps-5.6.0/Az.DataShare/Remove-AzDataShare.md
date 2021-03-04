---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924978"
---
# Remove-AzDataShare

## SYNOPSIS
Eltávolítja az adat megosztást.

## SZINTAXIS

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

## LEÍRÁS
A **Remove-AzDataShare** parancsmag eltávolítja az adatmegosztást.

## PÉLDÁK

### 1. példa
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Ez a parancs eltávolítja az AdsShare nevű adatmegosztást a WikiAds Azure-adatmegosztási fiókból. 

## PARAMETERS

### -AccountName
Azure data share account name

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

### -InputObject
Azure data share object' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases: 

Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (Érték) Fogadja el a helyettesítő karaktereket: Hamis

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

### -Name
Azure-adatok megosztásának neve

yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases: 

Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: False Accept helyettesítő karakterek: Hamis

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
Visszatérési objektum (ha meg van adva).

yaml Type: SwitchParameter Parameter Sets: (All) Aliass: 

Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False

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
Az azure-adat-megosztási fiók erőforráscsoportneve

yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases: 

Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: False Accept helyettesítő karakterek: Hamis

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
Az Azure-adat megosztásának erőforrás-azonosítója

yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases: 

Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (ByPropertyName) Fogadja el a helyettesítő karaktereket: Hamis

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf

Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

yaml Type: SwitchParameter Parameter Sets: (All) Aliass: wi

Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False




yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:

Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (Érték) Fogadja el a helyettesítő karaktereket: Hamis

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

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
