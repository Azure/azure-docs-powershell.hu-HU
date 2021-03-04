---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fac62ac0e75587e19a9ba0a5e99461693ce31c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922289"
---
# <span data-ttu-id="6d9a0-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="6d9a0-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="6d9a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9a0-103">Beállítja az Azure SQL felügyeltpéldány-adatbázisban az oszlopok adattípusát és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="6d9a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d9a0-104">SYNTAX</span></span>

### <span data-ttu-id="6d9a0-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d9a0-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d9a0-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9a0-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d9a0-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9a0-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9a0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d9a0-108">DESCRIPTION</span></span>
<span data-ttu-id="6d9a0-109">A Set-AzSqlInstanceDatabaseSensitivityClassification parancsmag az Azure SQL felügyeltpéldány-adatbázisban állítja be az oszlopok adattípusát és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="6d9a0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d9a0-110">EXAMPLES</span></span>

### <span data-ttu-id="6d9a0-111">1. példa: Egy Azure SQL felügyeltpéldány-adatbázisban lévő oszlop adattípusának és bizalmasság-címkéinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="6d9a0-112">2. példa: Az Azure SQL felügyeltpéldány-adatbázisok oszlopainak ajánlott adattípusainak és bizalmasság-címkéinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="6d9a0-113">3. példa: Az Azure SQL felügyeltpéldány-adatbázisban lévő oszlopok adattípusának és bizalmasság-címkéinek beállítása pipázás használatával.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="6d9a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9a0-114">PARAMETERS</span></span>

### <span data-ttu-id="6d9a0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d9a0-115">-AsJob</span></span>
<span data-ttu-id="6d9a0-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6d9a0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d9a0-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="6d9a0-117">-ClassificationObject</span></span>
<span data-ttu-id="6d9a0-118">Egy SQL felügyeltpéldány-adatbázis bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="6d9a0-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="6d9a0-119">-ColumnName</span></span>
<span data-ttu-id="6d9a0-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-120">Name of column.</span></span>

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

### <span data-ttu-id="6d9a0-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d9a0-121">-DatabaseName</span></span>
<span data-ttu-id="6d9a0-122">Az Azure SQL felügyeltpéldány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="6d9a0-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6d9a0-123">-DatabaseObject</span></span>
<span data-ttu-id="6d9a0-124">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="6d9a0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9a0-125">-DefaultProfile</span></span>
<span data-ttu-id="6d9a0-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9a0-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="6d9a0-127">-InformationType</span></span>
<span data-ttu-id="6d9a0-128">Az oszlopban tárolt adatok adattípusát leíró név.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="6d9a0-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6d9a0-129">-InstanceName</span></span>
<span data-ttu-id="6d9a0-130">Azure SQL felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="6d9a0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d9a0-131">-PassThru</span></span>
<span data-ttu-id="6d9a0-132">Megadja, hogy kimenetként adja-e meg a bizalmasság-besorolási modell kimenetét a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="6d9a0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9a0-133">-ResourceGroupName</span></span>
<span data-ttu-id="6d9a0-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d9a0-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="6d9a0-135">-SchemaName</span></span>
<span data-ttu-id="6d9a0-136">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-136">Name of schema.</span></span>

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

### <span data-ttu-id="6d9a0-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="6d9a0-137">-SensitivityLabel</span></span>
<span data-ttu-id="6d9a0-138">Az oszlopban tárolt adatok bizalmasságát leíró név.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="6d9a0-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="6d9a0-139">-TableName</span></span>
<span data-ttu-id="6d9a0-140">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-140">Name of table.</span></span>

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

### <span data-ttu-id="6d9a0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d9a0-141">-Confirm</span></span>
<span data-ttu-id="6d9a0-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9a0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9a0-143">-WhatIf</span></span>
<span data-ttu-id="6d9a0-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d9a0-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9a0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9a0-146">CommonParameters</span></span>
<span data-ttu-id="6d9a0-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9a0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9a0-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d9a0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9a0-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d9a0-149">INPUTS</span></span>

### <span data-ttu-id="6d9a0-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="6d9a0-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="6d9a0-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d9a0-151">OUTPUTS</span></span>

### <span data-ttu-id="6d9a0-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d9a0-152">System.Boolean</span></span>

## <span data-ttu-id="6d9a0-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d9a0-153">NOTES</span></span>

## <span data-ttu-id="6d9a0-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d9a0-154">RELATED LINKS</span></span>

[<span data-ttu-id="6d9a0-155">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="6d9a0-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
