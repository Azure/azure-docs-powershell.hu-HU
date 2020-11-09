---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296702"
---
# <span data-ttu-id="0a963-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0a963-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="0a963-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a963-102">SYNOPSIS</span></span>
<span data-ttu-id="0a963-103">Beolvassa a jelenlegi adattípusokat és az adatbázis oszlopainak érzékenységi címkéit.</span><span class="sxs-lookup"><span data-stu-id="0a963-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="0a963-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a963-104">SYNTAX</span></span>

### <span data-ttu-id="0a963-105">DatabaseObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a963-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a963-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a963-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a963-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a963-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a963-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a963-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a963-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a963-109">DESCRIPTION</span></span>
<span data-ttu-id="0a963-110">A Get-AzSqlDatabaseSensitivityClassification parancsmag az Azure SQL-adatbázis oszlopainak aktuális adattípusait és érzékenységi címkéit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0a963-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="0a963-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0a963-111">EXAMPLES</span></span>

### <span data-ttu-id="0a963-112">1. példa: az Azure SQL-adatbázisok aktuális adattípusai és érzékenységi címkéjének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="0a963-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="0a963-113">2. példa: az Azure SQL-adatbázisok aktuális információs típusainak és érzékenységi címkéinak beolvasása a csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="0a963-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="0a963-114">3. példa: az Azure SQL-adatbázisok adott oszlopának aktuális információs típusának és érzékenységi címkéjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="0a963-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="0a963-115">Példa 4: az Azure SQL-adatbázisok aktuális adattípusának és érzékenységi címkéjának beszerzése csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="0a963-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="0a963-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a963-116">PARAMETERS</span></span>

### <span data-ttu-id="0a963-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a963-117">-AsJob</span></span>
<span data-ttu-id="0a963-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0a963-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a963-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0a963-119">-ColumnName</span></span>
<span data-ttu-id="0a963-120">Oszlop neve</span><span class="sxs-lookup"><span data-stu-id="0a963-120">Name of column.</span></span>

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

### <span data-ttu-id="0a963-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a963-121">-DatabaseName</span></span>
<span data-ttu-id="0a963-122">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0a963-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="0a963-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0a963-123">-DatabaseObject</span></span>
<span data-ttu-id="0a963-124">Az SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="0a963-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a963-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a963-125">-DefaultProfile</span></span>
<span data-ttu-id="0a963-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a963-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a963-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a963-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a963-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a963-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a963-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0a963-129">-SchemaName</span></span>
<span data-ttu-id="0a963-130">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="0a963-130">Name of schema.</span></span>

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

### <span data-ttu-id="0a963-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0a963-131">-ServerName</span></span>
<span data-ttu-id="0a963-132">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0a963-132">SQL server name.</span></span>

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

### <span data-ttu-id="0a963-133">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="0a963-133">-TableName</span></span>
<span data-ttu-id="0a963-134">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="0a963-134">Name of table.</span></span>

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

### <span data-ttu-id="0a963-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a963-135">CommonParameters</span></span>
<span data-ttu-id="0a963-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a963-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a963-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0a963-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a963-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a963-138">INPUTS</span></span>

### <span data-ttu-id="0a963-139">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0a963-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0a963-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a963-140">OUTPUTS</span></span>

### <span data-ttu-id="0a963-141">Microsoft. Azure. Command. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0a963-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0a963-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a963-142">NOTES</span></span>

## <span data-ttu-id="0a963-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a963-143">RELATED LINKS</span></span>

[<span data-ttu-id="0a963-144">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="0a963-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
