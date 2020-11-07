---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c476f19f8c2ab8af334f92e75b67aeee151793fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839335"
---
# <span data-ttu-id="6cc05-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="6cc05-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="6cc05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cc05-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc05-103">Az Azure SQL felügyelt példány adatbázisában található oszlopok adattípusait és érzékenységi címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cc05-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="6cc05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cc05-104">SYNTAX</span></span>

### <span data-ttu-id="6cc05-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cc05-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc05-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cc05-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc05-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cc05-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc05-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cc05-108">DESCRIPTION</span></span>
<span data-ttu-id="6cc05-109">Az Set-AzSqlInstanceDatabaseSensitivityClassification parancsmag az Azure SQL Managed instance-adatbázisban található oszlopok adattípusait és érzékenységi címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="6cc05-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="6cc05-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6cc05-110">EXAMPLES</span></span>

### <span data-ttu-id="6cc05-111">1. példa: az Azure SQL felügyelt példány adatbázisában lévő oszlop adattípusának és érzékenységi címkéjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="6cc05-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="6cc05-112">2. példa: az Azure SQL-alapú SQL-adatbázisokban a javasolt adattípusok és az oszlopok érzékenységi címkéi adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="6cc05-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="6cc05-113">3. példa: a csővezetékek segítségével egy Azure SQL-alapú SQL-alapú SQL Server-adatbázisban lévő oszlop adattípusának és érzékenységi címkéjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="6cc05-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="6cc05-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cc05-114">PARAMETERS</span></span>

### <span data-ttu-id="6cc05-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cc05-115">-AsJob</span></span>
<span data-ttu-id="6cc05-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6cc05-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cc05-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="6cc05-117">-ClassificationObject</span></span>
<span data-ttu-id="6cc05-118">Az SQL felügyelt példány adatbázis-adatosztályozását jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="6cc05-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="6cc05-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="6cc05-119">-ColumnName</span></span>
<span data-ttu-id="6cc05-120">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="6cc05-120">Name of column.</span></span>

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

### <span data-ttu-id="6cc05-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cc05-121">-DatabaseName</span></span>
<span data-ttu-id="6cc05-122">Az Azure SQL Managed instance-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6cc05-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="6cc05-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6cc05-123">-DatabaseObject</span></span>
<span data-ttu-id="6cc05-124">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="6cc05-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="6cc05-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc05-125">-DefaultProfile</span></span>
<span data-ttu-id="6cc05-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cc05-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc05-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="6cc05-127">-InformationType</span></span>
<span data-ttu-id="6cc05-128">Az oszlopban tárolt adatok adattípusát leíró név.</span><span class="sxs-lookup"><span data-stu-id="6cc05-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="6cc05-129">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="6cc05-129">-InstanceName</span></span>
<span data-ttu-id="6cc05-130">Azure SQL felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="6cc05-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="6cc05-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cc05-131">-PassThru</span></span>
<span data-ttu-id="6cc05-132">Azt adja meg, hogy a parancsmag-végrehajtás végén az érzékenységi besorolási modellt szeretné-e exportálni</span><span class="sxs-lookup"><span data-stu-id="6cc05-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="6cc05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc05-133">-ResourceGroupName</span></span>
<span data-ttu-id="6cc05-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cc05-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cc05-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="6cc05-135">-SchemaName</span></span>
<span data-ttu-id="6cc05-136">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="6cc05-136">Name of schema.</span></span>

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

### <span data-ttu-id="6cc05-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="6cc05-137">-SensitivityLabel</span></span>
<span data-ttu-id="6cc05-138">Az oszlopban tárolt adatmennyiség érzékenységét leíró név.</span><span class="sxs-lookup"><span data-stu-id="6cc05-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="6cc05-139">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="6cc05-139">-TableName</span></span>
<span data-ttu-id="6cc05-140">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="6cc05-140">Name of table.</span></span>

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

### <span data-ttu-id="6cc05-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cc05-141">-Confirm</span></span>
<span data-ttu-id="6cc05-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cc05-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc05-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc05-143">-WhatIf</span></span>
<span data-ttu-id="6cc05-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cc05-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cc05-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cc05-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc05-146">CommonParameters</span></span>
<span data-ttu-id="6cc05-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cc05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc05-148">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6cc05-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc05-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc05-149">INPUTS</span></span>

### <span data-ttu-id="6cc05-150">Microsoft. Azure. Command. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="6cc05-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="6cc05-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc05-151">OUTPUTS</span></span>

### <span data-ttu-id="6cc05-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cc05-152">System.Boolean</span></span>

## <span data-ttu-id="6cc05-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cc05-153">NOTES</span></span>

## <span data-ttu-id="6cc05-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cc05-154">RELATED LINKS</span></span>

[<span data-ttu-id="6cc05-155">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="6cc05-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
