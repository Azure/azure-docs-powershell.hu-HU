---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144234"
---
# <span data-ttu-id="3f872-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3f872-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="3f872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f872-102">SYNOPSIS</span></span>
<span data-ttu-id="3f872-103">Engedélyezi a bizalmasságra vonatkozó javaslatokat az oszlopokon (a javaslatok alapértelmezés szerint minden oszlopban engedélyezve vannak) az adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="3f872-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="3f872-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f872-104">SYNTAX</span></span>

### <span data-ttu-id="3f872-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f872-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f872-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f872-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f872-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f872-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f872-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f872-108">DESCRIPTION</span></span>
<span data-ttu-id="3f872-109">A Enable-AzSqlDatabaseSensitivityRecommendation parancsmag bizalmasság-javaslatokat tesz az adatbázis oszlopaira.</span><span class="sxs-lookup"><span data-stu-id="3f872-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="3f872-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f872-110">EXAMPLES</span></span>

### <span data-ttu-id="3f872-111">1. példa: Bizalmasság-javaslatok engedélyezése egy Azure SQL-adatbázis adott oszlopához.</span><span class="sxs-lookup"><span data-stu-id="3f872-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3f872-112">2. példa: Bizalmasság-javaslatok engedélyezése egy adott oszlopra vonatkozó Azure SQL-adatbázishoz a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="3f872-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3f872-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f872-113">PARAMETERS</span></span>

### <span data-ttu-id="3f872-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f872-114">-AsJob</span></span>
<span data-ttu-id="3f872-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f872-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f872-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3f872-116">-ColumnName</span></span>
<span data-ttu-id="3f872-117">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="3f872-117">Name of column.</span></span>

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

### <span data-ttu-id="3f872-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f872-118">-DatabaseName</span></span>
<span data-ttu-id="3f872-119">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3f872-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="3f872-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3f872-120">-DatabaseObject</span></span>
<span data-ttu-id="3f872-121">Az SQL-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="3f872-121">The SQL database object.</span></span>

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

### <span data-ttu-id="3f872-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f872-122">-DefaultProfile</span></span>
<span data-ttu-id="3f872-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f872-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f872-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f872-124">-InputObject</span></span>
<span data-ttu-id="3f872-125">Egy SQL-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="3f872-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f872-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f872-126">-PassThru</span></span>
<span data-ttu-id="3f872-127">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="3f872-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3f872-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f872-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f872-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f872-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f872-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3f872-130">-SchemaName</span></span>
<span data-ttu-id="3f872-131">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="3f872-131">Name of schema.</span></span>

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

### <span data-ttu-id="3f872-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f872-132">-ServerName</span></span>
<span data-ttu-id="3f872-133">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3f872-133">SQL server name.</span></span>

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

### <span data-ttu-id="3f872-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="3f872-134">-TableName</span></span>
<span data-ttu-id="3f872-135">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="3f872-135">Name of table.</span></span>

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

### <span data-ttu-id="3f872-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f872-136">-Confirm</span></span>
<span data-ttu-id="3f872-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f872-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f872-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f872-138">-WhatIf</span></span>
<span data-ttu-id="3f872-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f872-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f872-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f872-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f872-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f872-141">CommonParameters</span></span>
<span data-ttu-id="3f872-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f872-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f872-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f872-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f872-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f872-144">INPUTS</span></span>

### <span data-ttu-id="3f872-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3f872-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="3f872-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f872-146">OUTPUTS</span></span>

### <span data-ttu-id="3f872-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f872-147">System.Boolean</span></span>

## <span data-ttu-id="3f872-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f872-148">NOTES</span></span>

## <span data-ttu-id="3f872-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f872-149">RELATED LINKS</span></span>

[<span data-ttu-id="3f872-150">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="3f872-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)