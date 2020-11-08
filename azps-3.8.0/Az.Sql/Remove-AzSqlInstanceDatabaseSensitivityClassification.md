---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013481"
---
# <span data-ttu-id="7205d-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="7205d-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="7205d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7205d-102">SYNOPSIS</span></span>
<span data-ttu-id="7205d-103">Eltávolítja az Azure SQL Managed instance-adatbázisban az oszlopok adattípusait és érzékenységi címkéit.</span><span class="sxs-lookup"><span data-stu-id="7205d-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7205d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7205d-104">SYNTAX</span></span>

### <span data-ttu-id="7205d-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7205d-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7205d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7205d-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7205d-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7205d-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7205d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7205d-108">DESCRIPTION</span></span>
<span data-ttu-id="7205d-109">A Remove-AzSqlInstanceDatabaseSensitivityClassification parancsmag eltávolítja az Azure SQL Managed instance-adatbázisban az oszlopok adattípusait és érzékenységi címkéit.</span><span class="sxs-lookup"><span data-stu-id="7205d-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7205d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7205d-110">EXAMPLES</span></span>

### <span data-ttu-id="7205d-111">1. példa: az Azure SQL-alapú SQL-adatbázisokban tárolt oszlopok adattípusának és érzékenységi címkéjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7205d-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7205d-112">2. példa: a jelenlegi adattípusok és a bennük található adatfeliratok eltávolítása Azure SQL-alapú SQL-alapú SQL Server-adatbázisból csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="7205d-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="7205d-113">3. példa: az Azure SQL felügyelt példányban lévő adatbázis adattípusának és érzékenységi címkéjának eltávolítása csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="7205d-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7205d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7205d-114">PARAMETERS</span></span>

### <span data-ttu-id="7205d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7205d-115">-AsJob</span></span>
<span data-ttu-id="7205d-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7205d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7205d-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="7205d-117">-ClassificationObject</span></span>
<span data-ttu-id="7205d-118">Az SQL felügyelt példány adatbázis-adatosztályozását jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="7205d-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="7205d-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7205d-119">-ColumnName</span></span>
<span data-ttu-id="7205d-120">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="7205d-120">Name of column.</span></span>

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

### <span data-ttu-id="7205d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7205d-121">-DatabaseName</span></span>
<span data-ttu-id="7205d-122">Az Azure SQL Managed instance-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7205d-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="7205d-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7205d-123">-DatabaseObject</span></span>
<span data-ttu-id="7205d-124">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="7205d-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="7205d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7205d-125">-DefaultProfile</span></span>
<span data-ttu-id="7205d-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7205d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7205d-127">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="7205d-127">-InstanceName</span></span>
<span data-ttu-id="7205d-128">Azure SQL felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="7205d-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="7205d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7205d-129">-PassThru</span></span>
<span data-ttu-id="7205d-130">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="7205d-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7205d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7205d-131">-ResourceGroupName</span></span>
<span data-ttu-id="7205d-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7205d-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="7205d-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7205d-133">-SchemaName</span></span>
<span data-ttu-id="7205d-134">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="7205d-134">Name of schema.</span></span>

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

### <span data-ttu-id="7205d-135">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="7205d-135">-TableName</span></span>
<span data-ttu-id="7205d-136">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="7205d-136">Name of table.</span></span>

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

### <span data-ttu-id="7205d-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7205d-137">-Confirm</span></span>
<span data-ttu-id="7205d-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7205d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7205d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7205d-139">-WhatIf</span></span>
<span data-ttu-id="7205d-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7205d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7205d-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7205d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7205d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7205d-142">CommonParameters</span></span>
<span data-ttu-id="7205d-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7205d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7205d-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7205d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7205d-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7205d-145">INPUTS</span></span>

### <span data-ttu-id="7205d-146">Microsoft. Azure. Command. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7205d-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7205d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7205d-147">OUTPUTS</span></span>

### <span data-ttu-id="7205d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7205d-148">System.Boolean</span></span>

## <span data-ttu-id="7205d-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7205d-149">NOTES</span></span>

## <span data-ttu-id="7205d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7205d-150">RELATED LINKS</span></span>

[<span data-ttu-id="7205d-151">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="7205d-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
