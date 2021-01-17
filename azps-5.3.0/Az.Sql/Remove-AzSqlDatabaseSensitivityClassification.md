---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467118"
---
# <span data-ttu-id="7ae2c-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="7ae2c-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="7ae2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ae2c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae2c-103">Eltávolítja az adatbázis oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="7ae2c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ae2c-104">SYNTAX</span></span>

### <span data-ttu-id="7ae2c-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ae2c-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ae2c-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae2c-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ae2c-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae2c-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ae2c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ae2c-108">DESCRIPTION</span></span>
<span data-ttu-id="7ae2c-109">A Remove-AzSqlDatabaseSensitivityClassification parancsmag eltávolítja az adatbázis oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="7ae2c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ae2c-110">EXAMPLES</span></span>

### <span data-ttu-id="7ae2c-111">1. példa: Távolítsa el egy Azure SQL-adatbázis oszlopának adattípus- és bizalmasság-címkéjét.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7ae2c-112">2. példa: A Piping használatával eltávolíthatja az Azure SQL-adatbázisok oszlopainak aktuális adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="7ae2c-113">3. példa: A Piping használatával eltávolíthatja egy Azure SQL-adatbázis oszlopának adattípus- és bizalmasság-címkéjét.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7ae2c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ae2c-114">PARAMETERS</span></span>

### <span data-ttu-id="7ae2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ae2c-115">-AsJob</span></span>
<span data-ttu-id="7ae2c-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7ae2c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ae2c-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="7ae2c-117">-ClassificationObject</span></span>
<span data-ttu-id="7ae2c-118">Egy SQL-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7ae2c-119">-ColumnName</span></span>
<span data-ttu-id="7ae2c-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7ae2c-121">-DatabaseName</span></span>
<span data-ttu-id="7ae2c-122">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7ae2c-123">-DatabaseObject</span></span>
<span data-ttu-id="7ae2c-124">Az SQL-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae2c-125">-DefaultProfile</span></span>
<span data-ttu-id="7ae2c-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae2c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ae2c-127">-PassThru</span></span>
<span data-ttu-id="7ae2c-128">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7ae2c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae2c-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ae2c-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7ae2c-131">-SchemaName</span></span>
<span data-ttu-id="7ae2c-132">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-132">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ae2c-133">-ServerName</span></span>
<span data-ttu-id="7ae2c-134">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-134">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="7ae2c-135">-TableName</span></span>
<span data-ttu-id="7ae2c-136">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-136">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ae2c-137">-Confirm</span></span>
<span data-ttu-id="7ae2c-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ae2c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae2c-139">-WhatIf</span></span>
<span data-ttu-id="7ae2c-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ae2c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ae2c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae2c-142">CommonParameters</span></span>
<span data-ttu-id="7ae2c-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae2c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae2c-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ae2c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae2c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ae2c-145">INPUTS</span></span>

### <span data-ttu-id="7ae2c-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7ae2c-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7ae2c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ae2c-147">OUTPUTS</span></span>

### <span data-ttu-id="7ae2c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7ae2c-148">System.Boolean</span></span>

## <span data-ttu-id="7ae2c-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ae2c-149">NOTES</span></span>

## <span data-ttu-id="7ae2c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ae2c-150">RELATED LINKS</span></span>

[<span data-ttu-id="7ae2c-151">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="7ae2c-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
