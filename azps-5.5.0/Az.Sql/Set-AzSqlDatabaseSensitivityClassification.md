---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145579"
---
# <span data-ttu-id="5a724-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="5a724-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="5a724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a724-102">SYNOPSIS</span></span>
<span data-ttu-id="5a724-103">Beállítja az adatbázis oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="5a724-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="5a724-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a724-104">SYNTAX</span></span>

### <span data-ttu-id="5a724-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a724-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a724-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a724-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a724-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a724-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a724-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a724-108">DESCRIPTION</span></span>
<span data-ttu-id="5a724-109">A Set-AzSqlDatabaseSensitivityClassification parancsmag beállítja az adatbázis oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="5a724-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="5a724-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a724-110">EXAMPLES</span></span>

### <span data-ttu-id="5a724-111">1. példa: Egy Azure SQL-adatbázisban lévő oszlop adattípusának és bizalmasság-címkéinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="5a724-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="5a724-112">2. példa: Az Azure SQL-adatbázisok oszlopainak ajánlott adattípusainak és bizalmasság-címkéinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="5a724-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="5a724-113">3. példa: Egy Azure SQL-adatbázisban lévő oszlop adattípusának és bizalmasság-címkéinek beállítása pipázás használatával.</span><span class="sxs-lookup"><span data-stu-id="5a724-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="5a724-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a724-114">PARAMETERS</span></span>

### <span data-ttu-id="5a724-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a724-115">-AsJob</span></span>
<span data-ttu-id="5a724-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5a724-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a724-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="5a724-117">-ClassificationObject</span></span>
<span data-ttu-id="5a724-118">Egy SQL-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="5a724-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="5a724-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5a724-119">-ColumnName</span></span>
<span data-ttu-id="5a724-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="5a724-120">Name of column.</span></span>

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

### <span data-ttu-id="5a724-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a724-121">-DatabaseName</span></span>
<span data-ttu-id="5a724-122">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5a724-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="5a724-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5a724-123">-DatabaseObject</span></span>
<span data-ttu-id="5a724-124">Az SQL-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="5a724-124">The SQL database object.</span></span>

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

### <span data-ttu-id="5a724-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a724-125">-DefaultProfile</span></span>
<span data-ttu-id="5a724-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a724-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a724-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="5a724-127">-InformationType</span></span>
<span data-ttu-id="5a724-128">Az oszlopban tárolt adatok adattípusát leíró név.</span><span class="sxs-lookup"><span data-stu-id="5a724-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a724-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a724-129">-PassThru</span></span>
<span data-ttu-id="5a724-130">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="5a724-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="5a724-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a724-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a724-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a724-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="5a724-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5a724-133">-SchemaName</span></span>
<span data-ttu-id="5a724-134">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="5a724-134">Name of schema.</span></span>

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

### <span data-ttu-id="5a724-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="5a724-135">-SensitivityLabel</span></span>
<span data-ttu-id="5a724-136">Az oszlopban tárolt adatok bizalmasságát leíró név.</span><span class="sxs-lookup"><span data-stu-id="5a724-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a724-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a724-137">-ServerName</span></span>
<span data-ttu-id="5a724-138">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5a724-138">SQL server name.</span></span>

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

### <span data-ttu-id="5a724-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="5a724-139">-TableName</span></span>
<span data-ttu-id="5a724-140">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="5a724-140">Name of table.</span></span>

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

### <span data-ttu-id="5a724-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a724-141">-Confirm</span></span>
<span data-ttu-id="5a724-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a724-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a724-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a724-143">-WhatIf</span></span>
<span data-ttu-id="5a724-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a724-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a724-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a724-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a724-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a724-146">CommonParameters</span></span>
<span data-ttu-id="5a724-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a724-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a724-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a724-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a724-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a724-149">INPUTS</span></span>

### <span data-ttu-id="5a724-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5a724-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="5a724-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a724-151">OUTPUTS</span></span>

### <span data-ttu-id="5a724-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a724-152">System.Boolean</span></span>

## <span data-ttu-id="5a724-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a724-153">NOTES</span></span>

## <span data-ttu-id="5a724-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a724-154">RELATED LINKS</span></span>

[<span data-ttu-id="5a724-155">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="5a724-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
