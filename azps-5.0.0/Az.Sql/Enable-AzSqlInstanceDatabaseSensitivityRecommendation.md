---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186710"
---
# <span data-ttu-id="67c25-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="67c25-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="67c25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67c25-102">SYNOPSIS</span></span>
<span data-ttu-id="67c25-103">Az Azure SQL Managed instance Database (minden oszlopban alapértelmezés szerint engedélyezett) az oszlopokra vonatkozó érzékenységi javaslatok engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="67c25-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="67c25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67c25-104">SYNTAX</span></span>

### <span data-ttu-id="67c25-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67c25-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c25-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c25-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c25-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c25-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c25-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="67c25-108">DESCRIPTION</span></span>
<span data-ttu-id="67c25-109">Az Enable-AzSqlInstanceDatabaseSensitivityRecommendation parancsmag az Azure SQL Managed instance-adatbázisban lévő oszlopokra vonatkozó érzékenységi javaslatokat tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="67c25-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="67c25-110">Példák</span><span class="sxs-lookup"><span data-stu-id="67c25-110">EXAMPLES</span></span>

### <span data-ttu-id="67c25-111">1. példa: az adott oszlopra vonatkozó érzékenységi javaslatok engedélyezése az Azure SQL-alapú, felügyelt példányokat tartalmazó adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="67c25-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="67c25-112">2. példa: az adott oszlopra vonatkozó érzékenységi javaslatok engedélyezése az Azure SQL-alapú felügyelt példányok adatbázisában a csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="67c25-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="67c25-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67c25-113">PARAMETERS</span></span>

### <span data-ttu-id="67c25-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67c25-114">-AsJob</span></span>
<span data-ttu-id="67c25-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="67c25-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67c25-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="67c25-116">-ColumnName</span></span>
<span data-ttu-id="67c25-117">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="67c25-117">Name of column.</span></span>

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

### <span data-ttu-id="67c25-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67c25-118">-DatabaseName</span></span>
<span data-ttu-id="67c25-119">Az Azure SQL Managed instance-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="67c25-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="67c25-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="67c25-120">-DatabaseObject</span></span>
<span data-ttu-id="67c25-121">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="67c25-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="67c25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c25-122">-DefaultProfile</span></span>
<span data-ttu-id="67c25-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67c25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c25-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c25-124">-InputObject</span></span>
<span data-ttu-id="67c25-125">Az SQL felügyelt példány adatbázis-adatosztályozását jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="67c25-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="67c25-126">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="67c25-126">-InstanceName</span></span>
<span data-ttu-id="67c25-127">Azure SQL felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="67c25-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="67c25-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67c25-128">-PassThru</span></span>
<span data-ttu-id="67c25-129">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="67c25-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="67c25-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c25-130">-ResourceGroupName</span></span>
<span data-ttu-id="67c25-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67c25-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="67c25-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="67c25-132">-SchemaName</span></span>
<span data-ttu-id="67c25-133">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="67c25-133">Name of schema.</span></span>

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

### <span data-ttu-id="67c25-134">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="67c25-134">-TableName</span></span>
<span data-ttu-id="67c25-135">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="67c25-135">Name of table.</span></span>

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

### <span data-ttu-id="67c25-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67c25-136">-Confirm</span></span>
<span data-ttu-id="67c25-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67c25-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c25-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c25-138">-WhatIf</span></span>
<span data-ttu-id="67c25-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67c25-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67c25-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67c25-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c25-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c25-141">CommonParameters</span></span>
<span data-ttu-id="67c25-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67c25-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c25-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67c25-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c25-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67c25-144">INPUTS</span></span>

### <span data-ttu-id="67c25-145">Microsoft. Azure. Command. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="67c25-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="67c25-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67c25-146">OUTPUTS</span></span>

### <span data-ttu-id="67c25-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67c25-147">System.Boolean</span></span>

## <span data-ttu-id="67c25-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67c25-148">NOTES</span></span>

## <span data-ttu-id="67c25-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67c25-149">RELATED LINKS</span></span>

[<span data-ttu-id="67c25-150">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="67c25-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)