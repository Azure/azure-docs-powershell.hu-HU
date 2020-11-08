---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186988"
---
# <span data-ttu-id="6193e-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="6193e-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="6193e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6193e-102">SYNOPSIS</span></span>
<span data-ttu-id="6193e-103">Az oszlopokra vonatkozó érzékenységi javaslatok engedélyezése (a javaslatok alapértelmezés szerint engedélyezve vannak az összes oszlopban) az adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="6193e-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="6193e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6193e-104">SYNTAX</span></span>

### <span data-ttu-id="6193e-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6193e-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6193e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6193e-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6193e-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6193e-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6193e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6193e-108">DESCRIPTION</span></span>
<span data-ttu-id="6193e-109">Az Enable-AzSqlDatabaseSensitivityRecommendation parancsmag az adatbázis oszlopaira vonatkozó érzékenységi javaslatokat tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="6193e-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="6193e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6193e-110">EXAMPLES</span></span>

### <span data-ttu-id="6193e-111">1. példa: az egyes oszlopokra vonatkozó érzékenységi javaslatok engedélyezése Azure SQL-adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="6193e-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="6193e-112">2. példa: az érzékenységi javaslatok engedélyezése egy adott oszlop Azure SQL-adatbázisban csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="6193e-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="6193e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6193e-113">PARAMETERS</span></span>

### <span data-ttu-id="6193e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6193e-114">-AsJob</span></span>
<span data-ttu-id="6193e-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6193e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6193e-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="6193e-116">-ColumnName</span></span>
<span data-ttu-id="6193e-117">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="6193e-117">Name of column.</span></span>

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

### <span data-ttu-id="6193e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6193e-118">-DatabaseName</span></span>
<span data-ttu-id="6193e-119">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6193e-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="6193e-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6193e-120">-DatabaseObject</span></span>
<span data-ttu-id="6193e-121">Az SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="6193e-121">The SQL database object.</span></span>

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

### <span data-ttu-id="6193e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6193e-122">-DefaultProfile</span></span>
<span data-ttu-id="6193e-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6193e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6193e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6193e-124">-InputObject</span></span>
<span data-ttu-id="6193e-125">SQL-adatbázis érzékenységi besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="6193e-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="6193e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6193e-126">-PassThru</span></span>
<span data-ttu-id="6193e-127">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="6193e-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="6193e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6193e-128">-ResourceGroupName</span></span>
<span data-ttu-id="6193e-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6193e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="6193e-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="6193e-130">-SchemaName</span></span>
<span data-ttu-id="6193e-131">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="6193e-131">Name of schema.</span></span>

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

### <span data-ttu-id="6193e-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6193e-132">-ServerName</span></span>
<span data-ttu-id="6193e-133">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6193e-133">SQL server name.</span></span>

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

### <span data-ttu-id="6193e-134">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="6193e-134">-TableName</span></span>
<span data-ttu-id="6193e-135">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="6193e-135">Name of table.</span></span>

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

### <span data-ttu-id="6193e-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6193e-136">-Confirm</span></span>
<span data-ttu-id="6193e-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6193e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6193e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6193e-138">-WhatIf</span></span>
<span data-ttu-id="6193e-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6193e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6193e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6193e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6193e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6193e-141">CommonParameters</span></span>
<span data-ttu-id="6193e-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6193e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6193e-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6193e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6193e-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6193e-144">INPUTS</span></span>

### <span data-ttu-id="6193e-145">Microsoft. Azure. Command. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="6193e-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="6193e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6193e-146">OUTPUTS</span></span>

### <span data-ttu-id="6193e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6193e-147">System.Boolean</span></span>

## <span data-ttu-id="6193e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6193e-148">NOTES</span></span>

## <span data-ttu-id="6193e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6193e-149">RELATED LINKS</span></span>

[<span data-ttu-id="6193e-150">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="6193e-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)