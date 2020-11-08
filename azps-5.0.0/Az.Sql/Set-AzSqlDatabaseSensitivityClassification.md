---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186964"
---
# <span data-ttu-id="248e8-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="248e8-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="248e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="248e8-102">SYNOPSIS</span></span>
<span data-ttu-id="248e8-103">Az adatbázis oszlopainak információs típusait és érzékenységi címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="248e8-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="248e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="248e8-104">SYNTAX</span></span>

### <span data-ttu-id="248e8-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="248e8-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="248e8-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="248e8-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="248e8-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="248e8-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="248e8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="248e8-108">DESCRIPTION</span></span>
<span data-ttu-id="248e8-109">Az Set-AzSqlDatabaseSensitivityClassification parancsmag az adatbázis oszlopainak adattípusait és érzékenységi címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="248e8-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="248e8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="248e8-110">EXAMPLES</span></span>

### <span data-ttu-id="248e8-111">1. példa: az Azure SQL-adatbázisban tárolt oszlopok adattípusának és érzékenységi címkéjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="248e8-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="248e8-112">2. példa: az Azure SQL-adatbázisban az ajánlott adattípusokat és az oszlopok érzékenységi címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="248e8-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="248e8-113">3. példa: az Azure SQL-adatbázisban lévő oszlopok adattípusának és érzékenységi címkéjének beállítása csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="248e8-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="248e8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="248e8-114">PARAMETERS</span></span>

### <span data-ttu-id="248e8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="248e8-115">-AsJob</span></span>
<span data-ttu-id="248e8-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="248e8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="248e8-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="248e8-117">-ClassificationObject</span></span>
<span data-ttu-id="248e8-118">SQL-adatbázis érzékenységi besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="248e8-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="248e8-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="248e8-119">-ColumnName</span></span>
<span data-ttu-id="248e8-120">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="248e8-120">Name of column.</span></span>

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

### <span data-ttu-id="248e8-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="248e8-121">-DatabaseName</span></span>
<span data-ttu-id="248e8-122">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="248e8-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="248e8-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="248e8-123">-DatabaseObject</span></span>
<span data-ttu-id="248e8-124">Az SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="248e8-124">The SQL database object.</span></span>

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

### <span data-ttu-id="248e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248e8-125">-DefaultProfile</span></span>
<span data-ttu-id="248e8-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="248e8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="248e8-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="248e8-127">-InformationType</span></span>
<span data-ttu-id="248e8-128">Az oszlopban tárolt adatok adattípusát leíró név.</span><span class="sxs-lookup"><span data-stu-id="248e8-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="248e8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="248e8-129">-PassThru</span></span>
<span data-ttu-id="248e8-130">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="248e8-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="248e8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="248e8-131">-ResourceGroupName</span></span>
<span data-ttu-id="248e8-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="248e8-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="248e8-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="248e8-133">-SchemaName</span></span>
<span data-ttu-id="248e8-134">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="248e8-134">Name of schema.</span></span>

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

### <span data-ttu-id="248e8-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="248e8-135">-SensitivityLabel</span></span>
<span data-ttu-id="248e8-136">Az oszlopban tárolt adatmennyiség érzékenységét leíró név.</span><span class="sxs-lookup"><span data-stu-id="248e8-136">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="248e8-137">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="248e8-137">-ServerName</span></span>
<span data-ttu-id="248e8-138">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="248e8-138">SQL server name.</span></span>

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

### <span data-ttu-id="248e8-139">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="248e8-139">-TableName</span></span>
<span data-ttu-id="248e8-140">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="248e8-140">Name of table.</span></span>

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

### <span data-ttu-id="248e8-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="248e8-141">-Confirm</span></span>
<span data-ttu-id="248e8-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="248e8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="248e8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="248e8-143">-WhatIf</span></span>
<span data-ttu-id="248e8-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="248e8-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="248e8-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="248e8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="248e8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248e8-146">CommonParameters</span></span>
<span data-ttu-id="248e8-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="248e8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248e8-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="248e8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248e8-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="248e8-149">INPUTS</span></span>

### <span data-ttu-id="248e8-150">Microsoft. Azure. Command. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="248e8-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="248e8-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="248e8-151">OUTPUTS</span></span>

### <span data-ttu-id="248e8-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="248e8-152">System.Boolean</span></span>

## <span data-ttu-id="248e8-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="248e8-153">NOTES</span></span>

## <span data-ttu-id="248e8-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="248e8-154">RELATED LINKS</span></span>

[<span data-ttu-id="248e8-155">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="248e8-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)