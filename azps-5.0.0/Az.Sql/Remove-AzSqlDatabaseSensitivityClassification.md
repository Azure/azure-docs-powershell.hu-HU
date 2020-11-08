---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195304"
---
# <span data-ttu-id="208dd-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="208dd-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="208dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="208dd-102">SYNOPSIS</span></span>
<span data-ttu-id="208dd-103">Eltávolítja az adatbázis oszlopainak adattípusait és érzékenységi címkéit.</span><span class="sxs-lookup"><span data-stu-id="208dd-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="208dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="208dd-104">SYNTAX</span></span>

### <span data-ttu-id="208dd-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="208dd-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208dd-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="208dd-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208dd-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="208dd-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208dd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="208dd-108">DESCRIPTION</span></span>
<span data-ttu-id="208dd-109">Az Remove-AzSqlDatabaseSensitivityClassification parancsmag eltávolítja az adatbázis oszlopainak adattípusait és érzékenységi címkéit.</span><span class="sxs-lookup"><span data-stu-id="208dd-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="208dd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="208dd-110">EXAMPLES</span></span>

### <span data-ttu-id="208dd-111">1. példa: az Azure SQL-adatbázisban lévő oszlopok információs típusa és érzékenységi címke eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="208dd-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="208dd-112">2. példa: az Azure SQL-adatbázisok aktuális adattípusai és érzékenységi címkéjének eltávolítása az Azure SQL-adatbázisokban csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="208dd-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="208dd-113">3. példa: az Azure SQL-adatbázisok adattípusát és érzékenységi címkéjét a csővezetékek segítségével távolíthatja el.</span><span class="sxs-lookup"><span data-stu-id="208dd-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="208dd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="208dd-114">PARAMETERS</span></span>

### <span data-ttu-id="208dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="208dd-115">-AsJob</span></span>
<span data-ttu-id="208dd-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="208dd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="208dd-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="208dd-117">-ClassificationObject</span></span>
<span data-ttu-id="208dd-118">SQL-adatbázis érzékenységi besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="208dd-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="208dd-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="208dd-119">-ColumnName</span></span>
<span data-ttu-id="208dd-120">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="208dd-120">Name of column.</span></span>

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

### <span data-ttu-id="208dd-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="208dd-121">-DatabaseName</span></span>
<span data-ttu-id="208dd-122">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="208dd-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="208dd-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="208dd-123">-DatabaseObject</span></span>
<span data-ttu-id="208dd-124">Az SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="208dd-124">The SQL database object.</span></span>

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

### <span data-ttu-id="208dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208dd-125">-DefaultProfile</span></span>
<span data-ttu-id="208dd-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="208dd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="208dd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="208dd-127">-PassThru</span></span>
<span data-ttu-id="208dd-128">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="208dd-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="208dd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208dd-129">-ResourceGroupName</span></span>
<span data-ttu-id="208dd-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="208dd-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="208dd-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="208dd-131">-SchemaName</span></span>
<span data-ttu-id="208dd-132">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="208dd-132">Name of schema.</span></span>

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

### <span data-ttu-id="208dd-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="208dd-133">-ServerName</span></span>
<span data-ttu-id="208dd-134">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="208dd-134">SQL server name.</span></span>

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

### <span data-ttu-id="208dd-135">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="208dd-135">-TableName</span></span>
<span data-ttu-id="208dd-136">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="208dd-136">Name of table.</span></span>

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

### <span data-ttu-id="208dd-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="208dd-137">-Confirm</span></span>
<span data-ttu-id="208dd-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="208dd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208dd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208dd-139">-WhatIf</span></span>
<span data-ttu-id="208dd-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="208dd-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="208dd-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="208dd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208dd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208dd-142">CommonParameters</span></span>
<span data-ttu-id="208dd-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="208dd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208dd-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="208dd-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208dd-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="208dd-145">INPUTS</span></span>

### <span data-ttu-id="208dd-146">Microsoft. Azure. Command. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="208dd-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="208dd-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="208dd-147">OUTPUTS</span></span>

### <span data-ttu-id="208dd-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="208dd-148">System.Boolean</span></span>

## <span data-ttu-id="208dd-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="208dd-149">NOTES</span></span>

## <span data-ttu-id="208dd-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="208dd-150">RELATED LINKS</span></span>

[<span data-ttu-id="208dd-151">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="208dd-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
