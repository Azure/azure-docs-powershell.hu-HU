---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 6b07ba5e31ab8e301d94b50170aca3869f9dea65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476674"
---
# <span data-ttu-id="fb59e-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fb59e-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="fb59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb59e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb59e-103">Egy Azure SQL-kiszolgáló naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb59e-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="fb59e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb59e-104">SYNTAX</span></span>

### <span data-ttu-id="fb59e-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb59e-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb59e-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb59e-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb59e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb59e-107">DESCRIPTION</span></span>
<span data-ttu-id="fb59e-108">A **Get-AzSqlServerAudit** parancsmag megkapja egy Azure SQL-kiszolgáló naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="fb59e-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="fb59e-109">A *kiszolgáló azonosításához adja* meg a ResourceGroupName és *a ServerName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="fb59e-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="fb59e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb59e-110">EXAMPLES</span></span>

### <span data-ttu-id="fb59e-111">1. példa: Azure SQL-kiszolgáló naplózási beállításainak leellenőrzése</span><span class="sxs-lookup"><span data-stu-id="fb59e-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="fb59e-112">2. példa: Egy Azure SQL-kiszolgáló naplózási beállításainak be- és beállítása folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="fb59e-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="fb59e-113">3. példa: Azure SQL-kiszolgáló naplózási beállításainak leellenőrzése</span><span class="sxs-lookup"><span data-stu-id="fb59e-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="fb59e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb59e-114">PARAMETERS</span></span>

### <span data-ttu-id="fb59e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb59e-115">-AsJob</span></span>
<span data-ttu-id="fb59e-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fb59e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb59e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb59e-117">-DefaultProfile</span></span>
<span data-ttu-id="fb59e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb59e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb59e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb59e-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb59e-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb59e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb59e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb59e-121">-ServerName</span></span>
<span data-ttu-id="fb59e-122">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fb59e-122">SQL server name.</span></span>

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

### <span data-ttu-id="fb59e-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="fb59e-123">-ServerObject</span></span>
<span data-ttu-id="fb59e-124">A naplózási házirend kezeléséhez megfelelő kiszolgálóobjektum.</span><span class="sxs-lookup"><span data-stu-id="fb59e-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="fb59e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb59e-125">CommonParameters</span></span>
<span data-ttu-id="fb59e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb59e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb59e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb59e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb59e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb59e-128">INPUTS</span></span>

### <span data-ttu-id="fb59e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fb59e-129">System.String</span></span>

### <span data-ttu-id="fb59e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fb59e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="fb59e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb59e-131">OUTPUTS</span></span>

### <span data-ttu-id="fb59e-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="fb59e-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="fb59e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb59e-133">NOTES</span></span>

## <span data-ttu-id="fb59e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb59e-134">RELATED LINKS</span></span>
