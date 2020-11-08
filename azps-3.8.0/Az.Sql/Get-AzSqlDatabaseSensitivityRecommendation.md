---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011621"
---
# <span data-ttu-id="23a9b-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="23a9b-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="23a9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="23a9b-103">Az adatbázis oszlopainak ajánlott adattípusai és érzékenységi címkéi</span><span class="sxs-lookup"><span data-stu-id="23a9b-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="23a9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23a9b-104">SYNTAX</span></span>

### <span data-ttu-id="23a9b-105">DatabaseObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23a9b-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23a9b-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="23a9b-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23a9b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23a9b-107">DESCRIPTION</span></span>
<span data-ttu-id="23a9b-108">A Get-AzSqlDatabaseSensitivityRecommendation parancsmag az adatbázis oszlopainak ajánlott adattípusait és érzékenységi címkéit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="23a9b-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="23a9b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23a9b-109">EXAMPLES</span></span>

### <span data-ttu-id="23a9b-110">1. példa: az Azure SQL-adatbázisok ajánlott adattípusai és érzékenységi címkéi</span><span class="sxs-lookup"><span data-stu-id="23a9b-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

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

### <span data-ttu-id="23a9b-111">2. példa: az Azure SQL-adatbázisok ajánlott adattípusai és érzékenységi címkéi a csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="23a9b-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

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

## <span data-ttu-id="23a9b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23a9b-112">PARAMETERS</span></span>

### <span data-ttu-id="23a9b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23a9b-113">-AsJob</span></span>
<span data-ttu-id="23a9b-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="23a9b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23a9b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23a9b-115">-DatabaseName</span></span>
<span data-ttu-id="23a9b-116">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="23a9b-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a9b-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="23a9b-117">-DatabaseObject</span></span>
<span data-ttu-id="23a9b-118">Az SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="23a9b-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23a9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a9b-119">-DefaultProfile</span></span>
<span data-ttu-id="23a9b-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23a9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23a9b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a9b-121">-ResourceGroupName</span></span>
<span data-ttu-id="23a9b-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23a9b-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a9b-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="23a9b-123">-ServerName</span></span>
<span data-ttu-id="23a9b-124">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="23a9b-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a9b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a9b-125">CommonParameters</span></span>
<span data-ttu-id="23a9b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23a9b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a9b-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23a9b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a9b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23a9b-128">INPUTS</span></span>

### <span data-ttu-id="23a9b-129">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="23a9b-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="23a9b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23a9b-130">OUTPUTS</span></span>

### <span data-ttu-id="23a9b-131">Microsoft. Azure. Command. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="23a9b-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="23a9b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23a9b-132">NOTES</span></span>

## <span data-ttu-id="23a9b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23a9b-133">RELATED LINKS</span></span>

[<span data-ttu-id="23a9b-134">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="23a9b-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
