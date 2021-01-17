---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465925"
---
# <span data-ttu-id="fe2eb-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="fe2eb-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="fe2eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2eb-103">A Microsoft támogatási műveleteinek naplózási beállításait kapja meg egy Azure SQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="fe2eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe2eb-104">SYNTAX</span></span>

### <span data-ttu-id="fe2eb-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe2eb-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2eb-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe2eb-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe2eb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe2eb-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2eb-108">A **Get-AzSqlServerMSSupportAudit** parancsmag megkapja egy Azure SQL-kiszolgáló Microsoft támogatási műveleteinek naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="fe2eb-109">A *kiszolgáló azonosításához adja* meg a ResourceGroupName és *a ServerName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="fe2eb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe2eb-110">EXAMPLES</span></span>

### <span data-ttu-id="fe2eb-111">1. példa: A Microsoft támogatási műveleteinek naplózási beállításai egy Azure SQL-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="fe2eb-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="fe2eb-112">2. példa: Egy Azure SQL-kiszolgáló Microsoft támogatási műveleteinek naplózási beállításainak be- és beállítása a folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="fe2eb-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="fe2eb-113">3. példa: A Microsoft támogatási műveleteinek naplózási beállításainak lekérte egy Azure SQL-kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="fe2eb-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="fe2eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe2eb-114">PARAMETERS</span></span>

### <span data-ttu-id="fe2eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe2eb-115">-AsJob</span></span>
<span data-ttu-id="fe2eb-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fe2eb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe2eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2eb-117">-DefaultProfile</span></span>
<span data-ttu-id="fe2eb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe2eb-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe2eb-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe2eb-121">-ServerName</span></span>
<span data-ttu-id="fe2eb-122">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-122">SQL server name.</span></span>

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

### <span data-ttu-id="fe2eb-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="fe2eb-123">-ServerObject</span></span>
<span data-ttu-id="fe2eb-124">A naplózási házirend kezeléséhez megfelelő kiszolgálóobjektum.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="fe2eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2eb-125">CommonParameters</span></span>
<span data-ttu-id="fe2eb-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2eb-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe2eb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2eb-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe2eb-128">INPUTS</span></span>

### <span data-ttu-id="fe2eb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fe2eb-129">System.String</span></span>

### <span data-ttu-id="fe2eb-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fe2eb-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="fe2eb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe2eb-131">OUTPUTS</span></span>

### <span data-ttu-id="fe2eb-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="fe2eb-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="fe2eb-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe2eb-133">NOTES</span></span>

## <span data-ttu-id="fe2eb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe2eb-134">RELATED LINKS</span></span>
