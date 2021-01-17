---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375323"
---
# <span data-ttu-id="fdf37-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="fdf37-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="fdf37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdf37-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf37-103">Letiltja (mellőzi) a bizalmasságra vonatkozó javaslatokat az Azure SQL felügyeltpéldány-adatbázis oszlopainál.</span><span class="sxs-lookup"><span data-stu-id="fdf37-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="fdf37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdf37-104">SYNTAX</span></span>

### <span data-ttu-id="fdf37-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdf37-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdf37-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf37-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdf37-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf37-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf37-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdf37-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf37-109">A Disable-AzSqlInstanceDatabaseSensitivityRecommendation parancsmag letiltja (mellőzi) a bizalmasságra vonatkozó javaslatokat az Azure SQL felügyeltpéldány-adatbázis oszlopainál.</span><span class="sxs-lookup"><span data-stu-id="fdf37-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="fdf37-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdf37-110">EXAMPLES</span></span>

### <span data-ttu-id="fdf37-111">1. példa: Bizalmasság-javaslatok letiltása egy Azure SQL felügyeltpéldány-adatbázis adott oszlopában.</span><span class="sxs-lookup"><span data-stu-id="fdf37-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="fdf37-112">2. példa: Tiltsa le a bizalmasság-javaslatokat olyan oszlopokban, amelyek bizalmasságra vonatkozó javaslatokat tartalmaznak a Pipinget tartalmazó Azure SQL felügyelt példány-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="fdf37-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="fdf37-113">3. példa: A bizalmasságra vonatkozó javaslatok letiltása egy Azure SQL-alapú felügyelt példány-adatbázisban a Piping funkcióval egy adott oszlopban.</span><span class="sxs-lookup"><span data-stu-id="fdf37-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="fdf37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdf37-114">PARAMETERS</span></span>

### <span data-ttu-id="fdf37-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdf37-115">-AsJob</span></span>
<span data-ttu-id="fdf37-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fdf37-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdf37-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fdf37-117">-ColumnName</span></span>
<span data-ttu-id="fdf37-118">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="fdf37-118">Name of column.</span></span>

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

### <span data-ttu-id="fdf37-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fdf37-119">-DatabaseName</span></span>
<span data-ttu-id="fdf37-120">Az Azure SQL felügyeltpéldány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fdf37-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="fdf37-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fdf37-121">-DatabaseObject</span></span>
<span data-ttu-id="fdf37-122">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="fdf37-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="fdf37-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-123">-DefaultProfile</span></span>
<span data-ttu-id="fdf37-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdf37-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf37-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf37-125">-InputObject</span></span>
<span data-ttu-id="fdf37-126">Egy SQL felügyeltpéldány-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="fdf37-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="fdf37-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fdf37-127">-InstanceName</span></span>
<span data-ttu-id="fdf37-128">Azure SQL által felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="fdf37-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="fdf37-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdf37-129">-PassThru</span></span>
<span data-ttu-id="fdf37-130">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="fdf37-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="fdf37-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf37-131">-ResourceGroupName</span></span>
<span data-ttu-id="fdf37-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fdf37-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdf37-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fdf37-133">-SchemaName</span></span>
<span data-ttu-id="fdf37-134">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="fdf37-134">Name of schema.</span></span>

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

### <span data-ttu-id="fdf37-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="fdf37-135">-TableName</span></span>
<span data-ttu-id="fdf37-136">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="fdf37-136">Name of table.</span></span>

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

### <span data-ttu-id="fdf37-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdf37-137">-Confirm</span></span>
<span data-ttu-id="fdf37-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fdf37-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdf37-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf37-139">-WhatIf</span></span>
<span data-ttu-id="fdf37-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fdf37-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdf37-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdf37-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdf37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf37-142">CommonParameters</span></span>
<span data-ttu-id="fdf37-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf37-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdf37-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf37-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdf37-145">INPUTS</span></span>

### <span data-ttu-id="fdf37-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="fdf37-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="fdf37-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdf37-147">OUTPUTS</span></span>

### <span data-ttu-id="fdf37-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fdf37-148">System.Boolean</span></span>

## <span data-ttu-id="fdf37-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdf37-149">NOTES</span></span>

## <span data-ttu-id="fdf37-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdf37-150">RELATED LINKS</span></span>

[<span data-ttu-id="fdf37-151">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="fdf37-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)