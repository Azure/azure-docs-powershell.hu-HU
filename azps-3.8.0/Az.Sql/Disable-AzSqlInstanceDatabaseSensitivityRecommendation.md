---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012955"
---
# <span data-ttu-id="35d7e-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="35d7e-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="35d7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="35d7e-103">Letiltja (elutasítja) az Azure SQL Managed instance-adatbázis oszlopaira vonatkozó tartalmi ajánlásokat.</span><span class="sxs-lookup"><span data-stu-id="35d7e-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="35d7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35d7e-104">SYNTAX</span></span>

### <span data-ttu-id="35d7e-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35d7e-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d7e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="35d7e-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d7e-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="35d7e-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d7e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="35d7e-108">DESCRIPTION</span></span>
<span data-ttu-id="35d7e-109">Az Disable-AzSqlInstanceDatabaseSensitivityRecommendation parancsmag az Azure SQL Managed instance Database-adatbázisban lévő oszlopokra vonatkozóan letiltja az elutasításokra vonatkozó ajánlásokat.</span><span class="sxs-lookup"><span data-stu-id="35d7e-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="35d7e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="35d7e-110">EXAMPLES</span></span>

### <span data-ttu-id="35d7e-111">1. példa: az adott oszlopra vonatkozó érzékenységi javaslatok letiltása egy Azure SQL-alapú, felügyelt példányban lévő adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="35d7e-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="35d7e-112">2. példa: az érzékenységi javaslatok letiltása az olyan oszlopokon, amelyekben az Azure SQL felügyelt példányok adatbázisában a csöveket tartalmazó adatok szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="35d7e-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="35d7e-113">3. példa: az adott oszlopra vonatkozó érzékenységi javaslatok letiltása egy Azure SQL-alapú, felügyelt példányban lévő adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="35d7e-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="35d7e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35d7e-114">PARAMETERS</span></span>

### <span data-ttu-id="35d7e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35d7e-115">-AsJob</span></span>
<span data-ttu-id="35d7e-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="35d7e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35d7e-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="35d7e-117">-ColumnName</span></span>
<span data-ttu-id="35d7e-118">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="35d7e-118">Name of column.</span></span>

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

### <span data-ttu-id="35d7e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35d7e-119">-DatabaseName</span></span>
<span data-ttu-id="35d7e-120">Az Azure SQL Managed instance-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="35d7e-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="35d7e-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="35d7e-121">-DatabaseObject</span></span>
<span data-ttu-id="35d7e-122">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="35d7e-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="35d7e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d7e-123">-DefaultProfile</span></span>
<span data-ttu-id="35d7e-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35d7e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d7e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35d7e-125">-InputObject</span></span>
<span data-ttu-id="35d7e-126">Az SQL felügyelt példány adatbázis-adatosztályozását jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="35d7e-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="35d7e-127">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="35d7e-127">-InstanceName</span></span>
<span data-ttu-id="35d7e-128">Azure SQL felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="35d7e-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="35d7e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35d7e-129">-PassThru</span></span>
<span data-ttu-id="35d7e-130">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="35d7e-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="35d7e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d7e-131">-ResourceGroupName</span></span>
<span data-ttu-id="35d7e-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35d7e-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="35d7e-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="35d7e-133">-SchemaName</span></span>
<span data-ttu-id="35d7e-134">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="35d7e-134">Name of schema.</span></span>

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

### <span data-ttu-id="35d7e-135">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="35d7e-135">-TableName</span></span>
<span data-ttu-id="35d7e-136">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="35d7e-136">Name of table.</span></span>

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

### <span data-ttu-id="35d7e-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35d7e-137">-Confirm</span></span>
<span data-ttu-id="35d7e-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35d7e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d7e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d7e-139">-WhatIf</span></span>
<span data-ttu-id="35d7e-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35d7e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35d7e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35d7e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d7e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d7e-142">CommonParameters</span></span>
<span data-ttu-id="35d7e-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35d7e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d7e-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="35d7e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d7e-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d7e-145">INPUTS</span></span>

### <span data-ttu-id="35d7e-146">Microsoft. Azure. Command. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="35d7e-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="35d7e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d7e-147">OUTPUTS</span></span>

### <span data-ttu-id="35d7e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35d7e-148">System.Boolean</span></span>

## <span data-ttu-id="35d7e-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35d7e-149">NOTES</span></span>

## <span data-ttu-id="35d7e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35d7e-150">RELATED LINKS</span></span>

[<span data-ttu-id="35d7e-151">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="35d7e-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)