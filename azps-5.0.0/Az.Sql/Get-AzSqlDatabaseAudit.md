---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186694"
---
# <span data-ttu-id="f4fcc-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f4fcc-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="f4fcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fcc-103">Egy Azure SQL-adatbázis naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="f4fcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4fcc-104">SYNTAX</span></span>

### <span data-ttu-id="f4fcc-105">DatabaseParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4fcc-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4fcc-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4fcc-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4fcc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="f4fcc-108">A **Get-AzSqlDatabaseAudit** parancsmag az Azure SQL-adatbázisok naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="f4fcc-109">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="f4fcc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f4fcc-110">EXAMPLES</span></span>

### <span data-ttu-id="f4fcc-111">Példa 1: Azure SQL-adatbázis naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="f4fcc-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="f4fcc-112">2. példa: az Azure SQL-adatbázisok naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="f4fcc-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="f4fcc-113">3. példa: az Azure SQL-adatbázisok naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="f4fcc-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="f4fcc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4fcc-114">PARAMETERS</span></span>

### <span data-ttu-id="f4fcc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4fcc-115">-DatabaseName</span></span>
<span data-ttu-id="f4fcc-116">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcc-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f4fcc-117">-DatabaseObject</span></span>
<span data-ttu-id="f4fcc-118">Az adatbázis-objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-118">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="f4fcc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fcc-119">-DefaultProfile</span></span>
<span data-ttu-id="f4fcc-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4fcc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fcc-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4fcc-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcc-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f4fcc-123">-ServerName</span></span>
<span data-ttu-id="f4fcc-124">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fcc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fcc-125">CommonParameters</span></span>
<span data-ttu-id="f4fcc-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4fcc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fcc-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4fcc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fcc-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4fcc-128">INPUTS</span></span>

### <span data-ttu-id="f4fcc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f4fcc-129">System.String</span></span>

### <span data-ttu-id="f4fcc-130">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f4fcc-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f4fcc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4fcc-131">OUTPUTS</span></span>

### <span data-ttu-id="f4fcc-132">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="f4fcc-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="f4fcc-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4fcc-133">NOTES</span></span>

## <span data-ttu-id="f4fcc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4fcc-134">RELATED LINKS</span></span>
