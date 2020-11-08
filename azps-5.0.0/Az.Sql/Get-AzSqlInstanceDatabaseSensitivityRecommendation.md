---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195153"
---
# <span data-ttu-id="690e5-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="690e5-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="690e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="690e5-102">SYNOPSIS</span></span>
<span data-ttu-id="690e5-103">Beolvassa az Azure SQL Managed instance (Azure SQL Managed instance Database) adatbázis oszlopainak ajánlott információs típusait és érzékenységi címkéit.</span><span class="sxs-lookup"><span data-stu-id="690e5-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="690e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="690e5-104">SYNTAX</span></span>

### <span data-ttu-id="690e5-105">DatabaseObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="690e5-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="690e5-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="690e5-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="690e5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="690e5-107">DESCRIPTION</span></span>
<span data-ttu-id="690e5-108">A Get-AzSqlInstanceDatabaseSensitivityRecommendation parancsmag az Azure SQL Managed instance (Azure SQL Managed instance Database) adatbázis oszlopainak ajánlott adattípusait és érzékenységi címkéit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="690e5-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="690e5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="690e5-109">EXAMPLES</span></span>

### <span data-ttu-id="690e5-110">1. példa: az Azure SQL-alapú felügyelt adatbázis ajánlott adattípusai és érzékenységi címkéjének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="690e5-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="690e5-111">2. példa: ajánlott adattípusok és az Azure SQL-alapú felügyelt példányok adatfeliratai a csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="690e5-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="690e5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="690e5-112">PARAMETERS</span></span>

### <span data-ttu-id="690e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="690e5-113">-AsJob</span></span>
<span data-ttu-id="690e5-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="690e5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="690e5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="690e5-115">-DatabaseName</span></span>
<span data-ttu-id="690e5-116">Az Azure SQL Managed instance-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="690e5-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="690e5-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="690e5-117">-DatabaseObject</span></span>
<span data-ttu-id="690e5-118">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="690e5-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="690e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690e5-119">-DefaultProfile</span></span>
<span data-ttu-id="690e5-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="690e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="690e5-121">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="690e5-121">-InstanceName</span></span>
<span data-ttu-id="690e5-122">Azure SQL felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="690e5-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="690e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="690e5-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="690e5-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="690e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690e5-125">CommonParameters</span></span>
<span data-ttu-id="690e5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="690e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690e5-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="690e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690e5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="690e5-128">INPUTS</span></span>

### <span data-ttu-id="690e5-129">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="690e5-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="690e5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="690e5-130">OUTPUTS</span></span>

### <span data-ttu-id="690e5-131">Microsoft. Azure. Command. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="690e5-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="690e5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="690e5-132">NOTES</span></span>

## <span data-ttu-id="690e5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="690e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="690e5-134">További információ az Azure SQL adatbázis-adatfeltárásról és-osztályozásról</span><span class="sxs-lookup"><span data-stu-id="690e5-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
