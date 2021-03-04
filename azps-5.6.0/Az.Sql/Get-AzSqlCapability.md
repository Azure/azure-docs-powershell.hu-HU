---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 7c45cb511fe1466aa2ac210ceeb2b609f6c0e97a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939882"
---
# Get-AzSqlCapability

## SYNOPSIS
SQL-adatbázis-funkciókat kap az aktuális előfizetéshez.

## SZINTAXIS

### FilterResults (Alapértelmezett)
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DefaultResults
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzSqlCapability** parancsmag az Azure SQL-adatbázis funkcióit az aktuális előfizetésben elérhetővé válik egy adott régióhoz.
Ha megadja a *ServerVersionName,* *a EditionName* vagy a *ServiceObjectiveName* paramétert, ez a parancsmag a megadott értékeket és azok megelőzőit adja vissza.

## PÉLDÁK

### 1. példa: Képességek lekérte az aktuális előfizetést egy régióhoz
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

Ez a parancs a közép-amerikai régió aktuális előfizetésében lévő SQL-adatbázis-példányok képességeit adja vissza.

### 2. példa: Alapértelmezett funkciók lekérte az aktuális előfizetéshez egy régióhoz
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

Ez a parancs a közép-amerikai régió aktuális előfizetésében lévő SQL-adatbázisok alapértelmezett funkcióit adja vissza.

### 3. példa: Szolgáltatás-célkitűzés részleteinek lekérte
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

Ez a parancs az SQL-adatbázisok alapértelmezett funkcióit kapja az aktuális előfizetés megadott szolgáltatási célértékéhez.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Alapértékek
Azt jelzi, hogy ez a parancsmag csak alapértékeket kap.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EditionName
Annak az adatbázis-kiadásnak a neve, amelyhez a parancsmag képességeket kap.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocationName
Megadja annak a helynek a nevét, amelyhez a parancsmag képességeket kap.
További információt az Azure Régiók http://azure.microsoft.com/en-us/regions/ ( . http://azure.microsoft.com/en-us/regions/)

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

### -ServerVersionName
Annak a kiszolgálóverziónak a neve, amelyhez a parancsmag képességeket kap.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Annak a szolgáltatás-célnak a nevét adja meg, amelyhez a parancsmag képességeket kap.

```yaml
Type: System.String
Parameter Sets: FilterResults
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

## KIMENETEK

### Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
