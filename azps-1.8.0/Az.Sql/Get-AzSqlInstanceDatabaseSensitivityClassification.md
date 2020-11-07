---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 89190f171ec9634e13eaa56499f6eca87e75ccf5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668971"
---
# <span data-ttu-id="4112c-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4112c-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="4112c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4112c-102">SYNOPSIS</span></span>
<span data-ttu-id="4112c-103">Az Azure SQL felügyelt példány adatbázisában az oszlopok aktuális adattípusai és az adatközlők érzékenységi címkéi.</span><span class="sxs-lookup"><span data-stu-id="4112c-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4112c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4112c-104">SYNTAX</span></span>

### <span data-ttu-id="4112c-105">DatabaseObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4112c-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4112c-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="4112c-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4112c-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4112c-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4112c-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4112c-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4112c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4112c-109">DESCRIPTION</span></span>
<span data-ttu-id="4112c-110">A Get-AzSqlInstanceDatabaseSensitivityClassification parancsmag az Azure SQL Managed instance-adatbázisban lévő oszlopok aktuális adattípusait és érzékenységi címkéit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4112c-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4112c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4112c-111">EXAMPLES</span></span>

### <span data-ttu-id="4112c-112">1. példa: az Azure SQL-alapú, felügyelt példányok adatbázisának aktuális adattípusai és érzékenységi címkéi</span><span class="sxs-lookup"><span data-stu-id="4112c-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="4112c-113">2. példa: a jelenlegi adattípusok és az Azure SQL-alapú felügyelt adatbázis adattípusai és érzékenységi címkéi a csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="4112c-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="4112c-114">3. példa: az Azure SQL felügyelt példány-adatbázis adott oszlopának aktuális információs típusának és érzékenységi címkéjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4112c-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="4112c-115">4. példa: az Azure SQL felügyelt példány egy adott oszlopának aktuális adattípusa és érzékenységi címkéje csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="4112c-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="4112c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4112c-116">PARAMETERS</span></span>

### <span data-ttu-id="4112c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4112c-117">-AsJob</span></span>
<span data-ttu-id="4112c-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4112c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4112c-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4112c-119">-ColumnName</span></span>
<span data-ttu-id="4112c-120">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="4112c-120">Name of column.</span></span>

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

### <span data-ttu-id="4112c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4112c-121">-DatabaseName</span></span>
<span data-ttu-id="4112c-122">Az Azure SQL Managed instance-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4112c-122">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4112c-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4112c-123">-DatabaseObject</span></span>
<span data-ttu-id="4112c-124">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="4112c-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4112c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4112c-125">-DefaultProfile</span></span>
<span data-ttu-id="4112c-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4112c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4112c-127">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="4112c-127">-InstanceName</span></span>
<span data-ttu-id="4112c-128">Azure SQL felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="4112c-128">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4112c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4112c-129">-ResourceGroupName</span></span>
<span data-ttu-id="4112c-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4112c-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4112c-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4112c-131">-SchemaName</span></span>
<span data-ttu-id="4112c-132">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="4112c-132">Name of schema.</span></span>

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

### <span data-ttu-id="4112c-133">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="4112c-133">-TableName</span></span>
<span data-ttu-id="4112c-134">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="4112c-134">Name of table.</span></span>

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

### <span data-ttu-id="4112c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4112c-135">CommonParameters</span></span>
<span data-ttu-id="4112c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4112c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4112c-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4112c-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4112c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4112c-138">INPUTS</span></span>

### <span data-ttu-id="4112c-139">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4112c-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="4112c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4112c-140">OUTPUTS</span></span>

### <span data-ttu-id="4112c-141">Microsoft. Azure. Command. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4112c-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="4112c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4112c-142">NOTES</span></span>

## <span data-ttu-id="4112c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4112c-143">RELATED LINKS</span></span>

[<span data-ttu-id="4112c-144">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="4112c-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
