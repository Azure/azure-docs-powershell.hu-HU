---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: c9aef3a38cc210615a1f663d6d6104ae40f66245
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015877"
---
# <span data-ttu-id="ed3a2-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="ed3a2-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="ed3a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3a2-103">Engedélyezi a bizalmasságra vonatkozó javaslatokat az oszlopokon (a javaslatok alapértelmezés szerint minden oszlopban engedélyezve vannak) az Azure SQL felügyeltpéldány-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ed3a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed3a2-104">SYNTAX</span></span>

### <span data-ttu-id="ed3a2-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed3a2-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3a2-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed3a2-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3a2-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed3a2-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed3a2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed3a2-108">DESCRIPTION</span></span>
<span data-ttu-id="ed3a2-109">A Enable-AzSqlInstanceDatabaseSensitivityRecommendation parancsmag bizalmasság-javaslatokat tesz lehetővé az Azure SQL felügyeltpéldány-adatbázis oszlopainál.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ed3a2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed3a2-110">EXAMPLES</span></span>

### <span data-ttu-id="ed3a2-111">1. példa: Bizalmasság-javaslatok engedélyezése egy Azure SQL felügyeltpéldány-adatbázis adott oszlopához.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="ed3a2-112">2. példa: Bizalmasság-javaslatok engedélyezése egy adott oszlopon egy Azure SQL felügyelt példány adatbázisában Piping utasítással.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="ed3a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed3a2-113">PARAMETERS</span></span>

### <span data-ttu-id="ed3a2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed3a2-114">-AsJob</span></span>
<span data-ttu-id="ed3a2-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ed3a2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed3a2-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ed3a2-116">-ColumnName</span></span>
<span data-ttu-id="ed3a2-117">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-117">Name of column.</span></span>

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

### <span data-ttu-id="ed3a2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed3a2-118">-DatabaseName</span></span>
<span data-ttu-id="ed3a2-119">Az Azure SQL felügyeltpéldány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="ed3a2-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ed3a2-120">-DatabaseObject</span></span>
<span data-ttu-id="ed3a2-121">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="ed3a2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3a2-122">-DefaultProfile</span></span>
<span data-ttu-id="ed3a2-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed3a2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3a2-124">-InputObject</span></span>
<span data-ttu-id="ed3a2-125">Egy SQL felügyeltpéldány-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3a2-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ed3a2-126">-InstanceName</span></span>
<span data-ttu-id="ed3a2-127">Azure SQL felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="ed3a2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed3a2-128">-PassThru</span></span>
<span data-ttu-id="ed3a2-129">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ed3a2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3a2-130">-ResourceGroupName</span></span>
<span data-ttu-id="ed3a2-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed3a2-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ed3a2-132">-SchemaName</span></span>
<span data-ttu-id="ed3a2-133">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-133">Name of schema.</span></span>

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

### <span data-ttu-id="ed3a2-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="ed3a2-134">-TableName</span></span>
<span data-ttu-id="ed3a2-135">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-135">Name of table.</span></span>

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

### <span data-ttu-id="ed3a2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed3a2-136">-Confirm</span></span>
<span data-ttu-id="ed3a2-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed3a2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed3a2-138">-WhatIf</span></span>
<span data-ttu-id="ed3a2-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed3a2-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed3a2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3a2-141">CommonParameters</span></span>
<span data-ttu-id="ed3a2-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3a2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3a2-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed3a2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3a2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed3a2-144">INPUTS</span></span>

### <span data-ttu-id="ed3a2-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ed3a2-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ed3a2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed3a2-146">OUTPUTS</span></span>

### <span data-ttu-id="ed3a2-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed3a2-147">System.Boolean</span></span>

## <span data-ttu-id="ed3a2-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed3a2-148">NOTES</span></span>

## <span data-ttu-id="ed3a2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed3a2-149">RELATED LINKS</span></span>

[<span data-ttu-id="ed3a2-150">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="ed3a2-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)