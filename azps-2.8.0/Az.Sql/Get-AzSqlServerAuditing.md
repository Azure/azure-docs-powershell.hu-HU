---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839456"
---
# <span data-ttu-id="5cc2e-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="5cc2e-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="5cc2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cc2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc2e-103">**Fontos: Ez a parancsmag elavult, a [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) a helyére lép.**</span><span class="sxs-lookup"><span data-stu-id="5cc2e-103">**Important: This cmdlet is deprecated, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="5cc2e-104">Egy Azure SQL Server naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-104">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="5cc2e-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cc2e-105">SYNTAX</span></span>

### <span data-ttu-id="5cc2e-106">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5cc2e-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc2e-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="5cc2e-107">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc2e-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="5cc2e-108">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc2e-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="5cc2e-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc2e-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="5cc2e-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc2e-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="5cc2e-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc2e-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cc2e-112">DESCRIPTION</span></span>
<span data-ttu-id="5cc2e-113">A **Get-AzSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-113">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="5cc2e-114">Adja meg a kiszolgáló azonosítóját a *ResourceGroupName* és a *kiszolgálónév* paraméterben.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-114">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="5cc2e-115">A naplók rendeltetési helyét az alábbi kapcsoló paraméterek egyikének megadásával határozhatja meg: BlobStorage, LogAnalytics vagy EventHub (ha nincs megadva, az alapértelmezett érték a BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="5cc2e-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="5cc2e-116">Példák</span><span class="sxs-lookup"><span data-stu-id="5cc2e-116">EXAMPLES</span></span>

### <span data-ttu-id="5cc2e-117">Példa 1: a blob-tároló naplózási beállításainak beszerzése Azure SQL Server esetén</span><span class="sxs-lookup"><span data-stu-id="5cc2e-117">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="5cc2e-118">2. példa: a blob-tároló naplózási beállításainak beszerzése Azure SQL Server esetén</span><span class="sxs-lookup"><span data-stu-id="5cc2e-118">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="5cc2e-119">3. példa: az Azure SQL Server blob-tárterület naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="5cc2e-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="5cc2e-120">4. példa: az esemény-hub naplózási beállításainak beszerzése Azure SQL Server esetén</span><span class="sxs-lookup"><span data-stu-id="5cc2e-120">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="5cc2e-121">Példa 5: az Azure SQL Server esemény-központi naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="5cc2e-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="5cc2e-122">Példa 6: az Azure SQL Server log Analytics naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="5cc2e-122">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="5cc2e-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cc2e-123">PARAMETERS</span></span>

### <span data-ttu-id="5cc2e-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="5cc2e-124">-BlobStorage</span></span>
<span data-ttu-id="5cc2e-125">Megadja, hogy a naplók a blob-tárolók legyenek</span><span class="sxs-lookup"><span data-stu-id="5cc2e-125">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="5cc2e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc2e-126">-DefaultProfile</span></span>
<span data-ttu-id="5cc2e-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cc2e-128">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5cc2e-128">-EventHub</span></span>
<span data-ttu-id="5cc2e-129">Azt adja meg, hogy a naplók cél az esemény középpontja</span><span class="sxs-lookup"><span data-stu-id="5cc2e-129">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="5cc2e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cc2e-130">-InputObject</span></span>
<span data-ttu-id="5cc2e-131">A kiszolgálói objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-131">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc2e-132">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="5cc2e-132">-LogAnalytics</span></span>
<span data-ttu-id="5cc2e-133">Azt adja meg, hogy a naplók a naplózási naplókat jelentik</span><span class="sxs-lookup"><span data-stu-id="5cc2e-133">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="5cc2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="5cc2e-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="5cc2e-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5cc2e-136">-ServerName</span></span>
<span data-ttu-id="5cc2e-137">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-137">SQL server name.</span></span>

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

### <span data-ttu-id="5cc2e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cc2e-138">-Confirm</span></span>
<span data-ttu-id="5cc2e-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc2e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc2e-140">-WhatIf</span></span>
<span data-ttu-id="5cc2e-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cc2e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc2e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc2e-143">CommonParameters</span></span>
<span data-ttu-id="5cc2e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cc2e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc2e-145">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc2e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cc2e-146">INPUTS</span></span>

### <span data-ttu-id="5cc2e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc2e-147">System.String</span></span>

### <span data-ttu-id="5cc2e-148">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5cc2e-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5cc2e-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5cc2e-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5cc2e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cc2e-150">OUTPUTS</span></span>

### <span data-ttu-id="5cc2e-151">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="5cc2e-151">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="5cc2e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cc2e-152">NOTES</span></span>

## <span data-ttu-id="5cc2e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cc2e-153">RELATED LINKS</span></span>
