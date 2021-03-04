---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 369a9f0f9bb475d27512eb13047a5a4ffe334573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926337"
---
# <span data-ttu-id="74f33-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="74f33-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="74f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f33-102">SYNOPSIS</span></span>
<span data-ttu-id="74f33-103">Eltávolítja az oszlopok adattípusait és bizalmasság-címkéit az Azure SQL felügyeltpéldány-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="74f33-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="74f33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74f33-104">SYNTAX</span></span>

### <span data-ttu-id="74f33-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74f33-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f33-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f33-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f33-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f33-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f33-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74f33-108">DESCRIPTION</span></span>
<span data-ttu-id="74f33-109">A Remove-AzSqlInstanceDatabaseSensitivityClassification parancsmag eltávolítja az Azure SQL felügyeltpéldány-adatbázisban található oszlopok adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="74f33-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="74f33-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74f33-110">EXAMPLES</span></span>

### <span data-ttu-id="74f33-111">1. példa: Távolítsa el egy Azure SQL felügyeltpéldány-adatbázisban lévő oszlop adattípusát és bizalmasság-címkéjét.</span><span class="sxs-lookup"><span data-stu-id="74f33-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="74f33-112">2. példa: Távolítsa el az oszlopok aktuális adattípusait és bizalmasság-címkéit egy, a Pipinget tartalmazó Azure SQL felügyeltpéldány-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="74f33-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="74f33-113">3. példa: Távolítsa el egy Oszlop adattípusát és bizalmasság-címkéjét egy Azure SQL felügyeltpéldány-adatbázisban a Piping utasítással.</span><span class="sxs-lookup"><span data-stu-id="74f33-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="74f33-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f33-114">PARAMETERS</span></span>

### <span data-ttu-id="74f33-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74f33-115">-AsJob</span></span>
<span data-ttu-id="74f33-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74f33-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74f33-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="74f33-117">-ClassificationObject</span></span>
<span data-ttu-id="74f33-118">Egy SQL felügyeltpéldány-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="74f33-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74f33-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="74f33-119">-ColumnName</span></span>
<span data-ttu-id="74f33-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="74f33-120">Name of column.</span></span>

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

### <span data-ttu-id="74f33-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74f33-121">-DatabaseName</span></span>
<span data-ttu-id="74f33-122">Az Azure SQL felügyeltpéldány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="74f33-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="74f33-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="74f33-123">-DatabaseObject</span></span>
<span data-ttu-id="74f33-124">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="74f33-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74f33-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f33-125">-DefaultProfile</span></span>
<span data-ttu-id="74f33-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74f33-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f33-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="74f33-127">-InstanceName</span></span>
<span data-ttu-id="74f33-128">Azure SQL felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="74f33-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="74f33-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74f33-129">-PassThru</span></span>
<span data-ttu-id="74f33-130">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="74f33-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="74f33-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f33-131">-ResourceGroupName</span></span>
<span data-ttu-id="74f33-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="74f33-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="74f33-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="74f33-133">-SchemaName</span></span>
<span data-ttu-id="74f33-134">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="74f33-134">Name of schema.</span></span>

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

### <span data-ttu-id="74f33-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="74f33-135">-TableName</span></span>
<span data-ttu-id="74f33-136">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="74f33-136">Name of table.</span></span>

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

### <span data-ttu-id="74f33-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74f33-137">-Confirm</span></span>
<span data-ttu-id="74f33-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74f33-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f33-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f33-139">-WhatIf</span></span>
<span data-ttu-id="74f33-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74f33-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74f33-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74f33-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f33-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f33-142">CommonParameters</span></span>
<span data-ttu-id="74f33-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f33-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f33-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74f33-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f33-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74f33-145">INPUTS</span></span>

### <span data-ttu-id="74f33-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="74f33-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="74f33-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74f33-147">OUTPUTS</span></span>

### <span data-ttu-id="74f33-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74f33-148">System.Boolean</span></span>

## <span data-ttu-id="74f33-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74f33-149">NOTES</span></span>

## <span data-ttu-id="74f33-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74f33-150">RELATED LINKS</span></span>

[<span data-ttu-id="74f33-151">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="74f33-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
