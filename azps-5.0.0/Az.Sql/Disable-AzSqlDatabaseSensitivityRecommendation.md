---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185681"
---
# <span data-ttu-id="e0b22-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e0b22-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="e0b22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0b22-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b22-103">Az adatbázis oszlopaihoz tartozó érzékenységi javaslatok letiltása (elutasítja)</span><span class="sxs-lookup"><span data-stu-id="e0b22-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="e0b22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0b22-104">SYNTAX</span></span>

### <span data-ttu-id="e0b22-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0b22-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b22-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b22-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b22-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b22-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b22-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0b22-108">DESCRIPTION</span></span>
<span data-ttu-id="e0b22-109">Az Disable-AzSqlDatabaseSensitivityRecommendation parancsmag letiltja (elutasítja) az adatbázis oszlopaihoz tartozó érzékenységi javaslatokat.</span><span class="sxs-lookup"><span data-stu-id="e0b22-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="e0b22-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e0b22-110">EXAMPLES</span></span>

### <span data-ttu-id="e0b22-111">Példa 1: az Azure SQL-adatbázisokban az adott oszlopokra vonatkozó érzékenységi javaslatok letiltása.</span><span class="sxs-lookup"><span data-stu-id="e0b22-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="e0b22-112">2. példa: az érzékenységi javaslatok letiltása olyan oszlopokon, amelyekben az Azure SQL-adatbázisokban a csöveket használva érzékenységi javaslatok szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="e0b22-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="e0b22-113">3. példa: az egyes oszlopokra vonatkozó érzékenységi javaslatok letiltása az Azure SQL-adatbázisokban csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="e0b22-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="e0b22-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0b22-114">PARAMETERS</span></span>

### <span data-ttu-id="e0b22-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0b22-115">-AsJob</span></span>
<span data-ttu-id="e0b22-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e0b22-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0b22-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e0b22-117">-ColumnName</span></span>
<span data-ttu-id="e0b22-118">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="e0b22-118">Name of column.</span></span>

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

### <span data-ttu-id="e0b22-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0b22-119">-DatabaseName</span></span>
<span data-ttu-id="e0b22-120">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e0b22-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="e0b22-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e0b22-121">-DatabaseObject</span></span>
<span data-ttu-id="e0b22-122">Az SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="e0b22-122">The SQL database object.</span></span>

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

### <span data-ttu-id="e0b22-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b22-123">-DefaultProfile</span></span>
<span data-ttu-id="e0b22-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0b22-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b22-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b22-125">-InputObject</span></span>
<span data-ttu-id="e0b22-126">SQL-adatbázis érzékenységi besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="e0b22-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e0b22-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b22-127">-PassThru</span></span>
<span data-ttu-id="e0b22-128">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="e0b22-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e0b22-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b22-129">-ResourceGroupName</span></span>
<span data-ttu-id="e0b22-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0b22-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0b22-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e0b22-131">-SchemaName</span></span>
<span data-ttu-id="e0b22-132">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="e0b22-132">Name of schema.</span></span>

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

### <span data-ttu-id="e0b22-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e0b22-133">-ServerName</span></span>
<span data-ttu-id="e0b22-134">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e0b22-134">SQL server name.</span></span>

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

### <span data-ttu-id="e0b22-135">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="e0b22-135">-TableName</span></span>
<span data-ttu-id="e0b22-136">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="e0b22-136">Name of table.</span></span>

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

### <span data-ttu-id="e0b22-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0b22-137">-Confirm</span></span>
<span data-ttu-id="e0b22-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0b22-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b22-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b22-139">-WhatIf</span></span>
<span data-ttu-id="e0b22-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0b22-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0b22-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0b22-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b22-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b22-142">CommonParameters</span></span>
<span data-ttu-id="e0b22-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0b22-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b22-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0b22-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b22-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b22-145">INPUTS</span></span>

### <span data-ttu-id="e0b22-146">Microsoft. Azure. Command. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e0b22-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e0b22-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b22-147">OUTPUTS</span></span>

### <span data-ttu-id="e0b22-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0b22-148">System.Boolean</span></span>

## <span data-ttu-id="e0b22-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0b22-149">NOTES</span></span>

## <span data-ttu-id="e0b22-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0b22-150">RELATED LINKS</span></span>

[<span data-ttu-id="e0b22-151">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="e0b22-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)