---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195754"
---
# <span data-ttu-id="a5b64-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a5b64-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a5b64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5b64-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b64-103">Ütemezett lekérdezési erőforrások beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5b64-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="a5b64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5b64-104">SYNTAX</span></span>

### <span data-ttu-id="a5b64-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5b64-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b64-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="a5b64-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b64-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b64-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5b64-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5b64-108">DESCRIPTION</span></span>
<span data-ttu-id="a5b64-109">Ütemezett lekérdezési erőforrások beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5b64-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="a5b64-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5b64-110">EXAMPLES</span></span>

### <span data-ttu-id="a5b64-111">Példa 1: lista előfizetés vagy erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="a5b64-111">Example 1: List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="a5b64-112">2. példa: beolvasás szabály neve</span><span class="sxs-lookup"><span data-stu-id="a5b64-112">Example 2: Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="a5b64-113">3. példa: erőforrás-azonosító szerinti beolvasás</span><span class="sxs-lookup"><span data-stu-id="a5b64-113">Example 3: Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="a5b64-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5b64-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b64-115">-DefaultProfile</span></span>
<span data-ttu-id="a5b64-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5b64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b64-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5b64-117">-Name</span></span>
<span data-ttu-id="a5b64-118">Az értesítési szabály neve</span><span class="sxs-lookup"><span data-stu-id="a5b64-118">The alert rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b64-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5b64-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a5b64-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b64-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b64-121">-ResourceId</span></span>
<span data-ttu-id="a5b64-122">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a5b64-122">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b64-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b64-123">CommonParameters</span></span>
<span data-ttu-id="a5b64-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5b64-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b64-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5b64-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b64-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5b64-126">INPUTS</span></span>

### <span data-ttu-id="a5b64-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5b64-127">None</span></span>

## <span data-ttu-id="a5b64-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5b64-128">OUTPUTS</span></span>

### <span data-ttu-id="a5b64-129">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a5b64-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a5b64-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5b64-130">NOTES</span></span>

## <span data-ttu-id="a5b64-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5b64-131">RELATED LINKS</span></span>