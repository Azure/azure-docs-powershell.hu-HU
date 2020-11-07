---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672649"
---
# New-AzureRmDataMigrationTask

## Áttekintés
Áttelepítési feladatot hoz létre és indít el az Azure adatbázis-áttelepítési szolgáltatásban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ComponentNameParameterSet (alapértelmezett)
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### ComponentObjectParameterSet
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### ResourceIdParameterSet
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## Leírás
Az New-AzureRmDataMigrationTask parancsmag adatáttelepítési feladatot hoz létre. Ez a parancsmag a feladattípusok enumerálása, az Azure Resource Group, a kapcsolódó Azure-áttelepítési szolgáltatás és a projekt mint bemenet paramétereit veszi figyelembe. 

## Példák

### Példa 1
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
Az alábbi példa azt szemlélteti, hogy miként hozhat létre egy MyMigrationTask nevű új adatáttelepítési feladatot a TestService nevű myDMSProject és szolgáltatás nevű projektben. 

## PARAMÉTEREK

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
PSProject objektum

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A tevékenység neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Projektnév
A projekt neve.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Projekt-erőforrás azonosítója

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Az adatáttelepítési szolgáltatás neve.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskType
Tevékenység típusa

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## BEMENETEK

### Microsoft. Azure. Command. DataMigration. models. PSProject
System. String


## KIMENETEK

### Microsoft. Azure. Command. DataMigration. models. PSProjectTask


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK


