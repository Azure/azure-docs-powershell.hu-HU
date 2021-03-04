---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 4dfe4f52a344b8d2308288cfb659792c7b4aabab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921978"
---
# Get-AzDataMigrationService

## SYNOPSIS
Beolvassa az Azure Adatbázis-áttelepítési szolgáltatás egy példányához tartozó tulajdonságokat. 

## SZINTAXIS

### ResourceGroupSet (alapértelmezett)
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ServiceNameGroupSet
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzDataMigrationService parancsmag beolvassa az Azure Database Migration Service egy példányához társított tulajdonságokat a szolgáltatás neve és az Azure Erőforráscsoport neve alapján bemeneti paraméterekként. 

## PÉLDÁK

### 1. példa
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

A fenti példa beolvassa a testService nevű Azure Database Migration Service példány tulajdonságait. 

### 2. példa
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

A fenti példa beolvassa az Azure Database Migration Services szolgáltatást a testResourceGroup nevű erőforráscsoportban. 

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
Az adatbázis-áttelepítési szolgáltatás neve.

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
DataMigrationService Resource Id.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
