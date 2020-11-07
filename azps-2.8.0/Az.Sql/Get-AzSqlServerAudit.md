---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: eda8123b9ff309f4834f6e954e5e0b1e01b3f1e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839171"
---
# <span data-ttu-id="f660b-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f660b-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="f660b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f660b-102">SYNOPSIS</span></span>
<span data-ttu-id="f660b-103">Egy Azure SQL Server naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f660b-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="f660b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f660b-104">SYNTAX</span></span>

### <span data-ttu-id="f660b-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f660b-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f660b-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f660b-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f660b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f660b-107">DESCRIPTION</span></span>
<span data-ttu-id="f660b-108">A **Get-AzSqlServerAudit** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f660b-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="f660b-109">Adja meg a kiszolgáló azonosítóját a *ResourceGroupName* és a *kiszolgálónév* paraméterben.</span><span class="sxs-lookup"><span data-stu-id="f660b-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="f660b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f660b-110">EXAMPLES</span></span>

### <span data-ttu-id="f660b-111">1. példa: az Azure SQL Server naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="f660b-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="f660b-112">2. példa: az Azure SQL Server naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="f660b-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="f660b-113">3. példa: az Azure SQL Server naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="f660b-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="f660b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f660b-114">PARAMETERS</span></span>

### <span data-ttu-id="f660b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f660b-115">-AsJob</span></span>
<span data-ttu-id="f660b-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f660b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f660b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f660b-117">-DefaultProfile</span></span>
<span data-ttu-id="f660b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f660b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f660b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f660b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f660b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f660b-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f660b-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f660b-121">-ServerName</span></span>
<span data-ttu-id="f660b-122">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f660b-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f660b-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="f660b-123">-ServerObject</span></span>
<span data-ttu-id="f660b-124">A kiszolgálói objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f660b-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f660b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f660b-125">CommonParameters</span></span>
<span data-ttu-id="f660b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f660b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f660b-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f660b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f660b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f660b-128">INPUTS</span></span>

### <span data-ttu-id="f660b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f660b-129">System.String</span></span>

### <span data-ttu-id="f660b-130">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f660b-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f660b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f660b-131">OUTPUTS</span></span>

### <span data-ttu-id="f660b-132">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="f660b-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="f660b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f660b-133">NOTES</span></span>

## <span data-ttu-id="f660b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f660b-134">RELATED LINKS</span></span>
