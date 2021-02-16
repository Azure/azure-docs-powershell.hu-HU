---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163451"
---
# <span data-ttu-id="9e330-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9e330-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="9e330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e330-102">SYNOPSIS</span></span>
<span data-ttu-id="9e330-103">Letiltja (mellőzi) a bizalmasságra vonatkozó javaslatokat az adatbázis oszlopainál.</span><span class="sxs-lookup"><span data-stu-id="9e330-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="9e330-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e330-104">SYNTAX</span></span>

### <span data-ttu-id="9e330-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e330-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e330-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e330-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e330-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e330-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e330-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e330-108">DESCRIPTION</span></span>
<span data-ttu-id="9e330-109">A Disable-AzSqlDatabaseSensitivityRecommendation parancsmag letiltja (mellőzi) az adatbázis oszlopaira vonatkozó bizalmasság-javaslatokat.</span><span class="sxs-lookup"><span data-stu-id="9e330-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="9e330-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e330-110">EXAMPLES</span></span>

### <span data-ttu-id="9e330-111">1. példa: Egy Azure SQL-adatbázis adott oszlopában tiltsa le a bizalmasságra vonatkozó javaslatokat.</span><span class="sxs-lookup"><span data-stu-id="9e330-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9e330-112">2. példa: Tiltsa le a bizalmasság-javaslatokat olyan oszlopokban, amelyek bizalmasságra vonatkozó javaslatokat tartalmaznak egy Azure SQL-adatbázisban a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="9e330-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="9e330-113">3. példa: A Bizalmasság-javaslatok letiltása egy Azure SQL-adatbázis adott oszlopában a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="9e330-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9e330-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e330-114">PARAMETERS</span></span>

### <span data-ttu-id="9e330-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e330-115">-AsJob</span></span>
<span data-ttu-id="9e330-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9e330-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e330-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9e330-117">-ColumnName</span></span>
<span data-ttu-id="9e330-118">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9e330-118">Name of column.</span></span>

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

### <span data-ttu-id="9e330-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9e330-119">-DatabaseName</span></span>
<span data-ttu-id="9e330-120">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9e330-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="9e330-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9e330-121">-DatabaseObject</span></span>
<span data-ttu-id="9e330-122">Az SQL-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="9e330-122">The SQL database object.</span></span>

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

### <span data-ttu-id="9e330-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e330-123">-DefaultProfile</span></span>
<span data-ttu-id="9e330-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e330-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e330-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e330-125">-InputObject</span></span>
<span data-ttu-id="9e330-126">Egy SQL-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="9e330-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="9e330-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e330-127">-PassThru</span></span>
<span data-ttu-id="9e330-128">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="9e330-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9e330-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e330-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e330-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e330-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e330-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9e330-131">-SchemaName</span></span>
<span data-ttu-id="9e330-132">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="9e330-132">Name of schema.</span></span>

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

### <span data-ttu-id="9e330-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e330-133">-ServerName</span></span>
<span data-ttu-id="9e330-134">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9e330-134">SQL server name.</span></span>

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

### <span data-ttu-id="9e330-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="9e330-135">-TableName</span></span>
<span data-ttu-id="9e330-136">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="9e330-136">Name of table.</span></span>

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

### <span data-ttu-id="9e330-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e330-137">-Confirm</span></span>
<span data-ttu-id="9e330-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9e330-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e330-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e330-139">-WhatIf</span></span>
<span data-ttu-id="9e330-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9e330-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e330-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e330-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e330-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e330-142">CommonParameters</span></span>
<span data-ttu-id="9e330-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e330-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e330-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e330-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e330-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e330-145">INPUTS</span></span>

### <span data-ttu-id="9e330-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9e330-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9e330-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e330-147">OUTPUTS</span></span>

### <span data-ttu-id="9e330-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e330-148">System.Boolean</span></span>

## <span data-ttu-id="9e330-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e330-149">NOTES</span></span>

## <span data-ttu-id="9e330-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e330-150">RELATED LINKS</span></span>

[<span data-ttu-id="9e330-151">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="9e330-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)