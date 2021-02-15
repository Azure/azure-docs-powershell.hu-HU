---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163402"
---
# <span data-ttu-id="f3c88-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f3c88-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="f3c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c88-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c88-103">Az Azure SQL felügyeltpéldány-adatbázisban található oszlopok ajánlott adattípusait és bizalmasság-címkéit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f3c88-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="f3c88-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3c88-104">SYNTAX</span></span>

### <span data-ttu-id="f3c88-105">DatabaseObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3c88-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c88-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c88-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c88-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3c88-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c88-108">A Get-AzSqlInstanceDatabaseSensitivityRecommendation parancsmag az Azure SQL felügyeltpéldány-adatbázisban lévő oszlopok ajánlott adattípusait és bizalmasság-címkéit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f3c88-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="f3c88-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3c88-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c88-110">1. példa: Az Azure SQL felügyeltpéldány-adatbázis ajánlott adattípusai és bizalmasság-címkéinek begyűjtése.</span><span class="sxs-lookup"><span data-stu-id="f3c88-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="f3c88-111">2. példa: A Piping használatával az Azure SQL által felügyelt példányadatbázis ajánlott adattípusai és bizalmasság-címkéinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="f3c88-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
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

## <span data-ttu-id="f3c88-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3c88-112">PARAMETERS</span></span>

### <span data-ttu-id="f3c88-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3c88-113">-AsJob</span></span>
<span data-ttu-id="f3c88-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f3c88-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3c88-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3c88-115">-DatabaseName</span></span>
<span data-ttu-id="f3c88-116">Az Azure SQL felügyeltpéldány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f3c88-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="f3c88-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f3c88-117">-DatabaseObject</span></span>
<span data-ttu-id="f3c88-118">Az Azure SQL felügyelt példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="f3c88-118">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="f3c88-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c88-119">-DefaultProfile</span></span>
<span data-ttu-id="f3c88-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3c88-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c88-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f3c88-121">-InstanceName</span></span>
<span data-ttu-id="f3c88-122">Azure SQL által felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="f3c88-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="f3c88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c88-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3c88-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3c88-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3c88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c88-125">CommonParameters</span></span>
<span data-ttu-id="f3c88-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c88-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3c88-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c88-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3c88-128">INPUTS</span></span>

### <span data-ttu-id="f3c88-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f3c88-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="f3c88-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3c88-130">OUTPUTS</span></span>

### <span data-ttu-id="f3c88-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f3c88-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="f3c88-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3c88-132">NOTES</span></span>

## <span data-ttu-id="f3c88-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3c88-133">RELATED LINKS</span></span>

[<span data-ttu-id="f3c88-134">További információ az Azure SQL Database adatfeltárásról és -besorolásról</span><span class="sxs-lookup"><span data-stu-id="f3c88-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
