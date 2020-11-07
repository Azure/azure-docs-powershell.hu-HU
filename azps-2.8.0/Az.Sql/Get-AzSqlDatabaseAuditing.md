---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839263"
---
# <span data-ttu-id="31a78-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="31a78-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="31a78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31a78-102">SYNOPSIS</span></span>
<span data-ttu-id="31a78-103">**Fontos: Ez a parancsmag elavult, a [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) a helyére lép.**</span><span class="sxs-lookup"><span data-stu-id="31a78-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="31a78-104">Egy Azure SQL-adatbázis naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31a78-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="31a78-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31a78-105">SYNTAX</span></span>

### <span data-ttu-id="31a78-106">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31a78-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a78-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="31a78-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a78-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="31a78-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a78-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="31a78-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a78-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="31a78-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a78-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="31a78-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a78-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="31a78-112">DESCRIPTION</span></span>
<span data-ttu-id="31a78-113">A **Get-AzSqlDatabaseAuditing** parancsmag az Azure SQL-adatbázisok naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31a78-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="31a78-114">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="31a78-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="31a78-115">A naplók rendeltetési helyét az alábbi kapcsoló paraméterek egyikének megadásával határozhatja meg: BlobStorage, LogAnalytics vagy EventHub (ha nincs megadva, az alapértelmezett érték a BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="31a78-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="31a78-116">Példák</span><span class="sxs-lookup"><span data-stu-id="31a78-116">EXAMPLES</span></span>

### <span data-ttu-id="31a78-117">Példa 1: a blob-tároló naplózási beállításainak beszerzése Azure SQL-adatbázisból</span><span class="sxs-lookup"><span data-stu-id="31a78-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="31a78-118">2. példa: a blob-tárterület naplózási beállításainak beszerzése Azure SQL-adatbázisból</span><span class="sxs-lookup"><span data-stu-id="31a78-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="31a78-119">3. példa: az Azure SQL-adatbázisok blob-tárterületének naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="31a78-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="31a78-120">Példa 4: az esemény központi naplózási beállításainak beszerzése Azure SQL-adatbázisból</span><span class="sxs-lookup"><span data-stu-id="31a78-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="31a78-121">Példa 5: az Azure SQL-adatbázisok esemény-központi naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="31a78-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="31a78-122">Példa 6: az Azure SQL-adatbázisok naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="31a78-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="31a78-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31a78-123">PARAMETERS</span></span>

### <span data-ttu-id="31a78-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="31a78-124">-BlobStorage</span></span>
<span data-ttu-id="31a78-125">Megadja, hogy a naplók a blob-tárolók legyenek</span><span class="sxs-lookup"><span data-stu-id="31a78-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31a78-126">-DatabaseName</span></span>
<span data-ttu-id="31a78-127">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="31a78-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a78-128">-DefaultProfile</span></span>
<span data-ttu-id="31a78-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31a78-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a78-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="31a78-130">-EventHub</span></span>
<span data-ttu-id="31a78-131">Azt adja meg, hogy a naplók cél az esemény középpontja</span><span class="sxs-lookup"><span data-stu-id="31a78-131">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31a78-132">-InputObject</span></span>
<span data-ttu-id="31a78-133">Az adatbázis-objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="31a78-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="31a78-134">-LogAnalytics</span></span>
<span data-ttu-id="31a78-135">Azt adja meg, hogy a naplók a naplózási naplókat jelentik</span><span class="sxs-lookup"><span data-stu-id="31a78-135">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a78-136">-ResourceGroupName</span></span>
<span data-ttu-id="31a78-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="31a78-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-138">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="31a78-138">-ServerName</span></span>
<span data-ttu-id="31a78-139">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="31a78-139">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a78-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31a78-140">-Confirm</span></span>
<span data-ttu-id="31a78-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31a78-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a78-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a78-142">-WhatIf</span></span>
<span data-ttu-id="31a78-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31a78-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31a78-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31a78-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a78-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a78-145">CommonParameters</span></span>
<span data-ttu-id="31a78-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31a78-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a78-147">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31a78-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a78-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a78-148">INPUTS</span></span>

### <span data-ttu-id="31a78-149">System. String</span><span class="sxs-lookup"><span data-stu-id="31a78-149">System.String</span></span>

### <span data-ttu-id="31a78-150">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="31a78-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="31a78-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31a78-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31a78-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a78-152">OUTPUTS</span></span>

### <span data-ttu-id="31a78-153">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="31a78-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="31a78-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31a78-154">NOTES</span></span>

## <span data-ttu-id="31a78-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31a78-155">RELATED LINKS</span></span>
