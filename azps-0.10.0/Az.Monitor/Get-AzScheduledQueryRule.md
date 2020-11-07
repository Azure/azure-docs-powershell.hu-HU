---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 1cb05a83ccbe1786392867f4714553413fe635c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842014"
---
# <span data-ttu-id="866a1-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="866a1-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="866a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="866a1-102">SYNOPSIS</span></span>
<span data-ttu-id="866a1-103">Ütemezett lekérdezési erőforrások beolvasása</span><span class="sxs-lookup"><span data-stu-id="866a1-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="866a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="866a1-104">SYNTAX</span></span>

### <span data-ttu-id="866a1-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="866a1-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="866a1-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="866a1-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="866a1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="866a1-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="866a1-108">DESCRIPTION</span></span>
<span data-ttu-id="866a1-109">Ütemezett lekérdezési erőforrások beolvasása</span><span class="sxs-lookup"><span data-stu-id="866a1-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="866a1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="866a1-110">EXAMPLES</span></span>

### <span data-ttu-id="866a1-111">Példa 1 – lista előfizetés vagy erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="866a1-111">Example 1 - List by subscription or resource group</span></span>
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

### <span data-ttu-id="866a1-112">Példa 2 – Get by szabály neve</span><span class="sxs-lookup"><span data-stu-id="866a1-112">Example 2 - Get by rule name</span></span>
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

### <span data-ttu-id="866a1-113">Példa 3 – az erőforrás-azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="866a1-113">Example 3 - Get by resource Id</span></span>
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

## <span data-ttu-id="866a1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="866a1-114">PARAMETERS</span></span>

### <span data-ttu-id="866a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866a1-115">-DefaultProfile</span></span>
<span data-ttu-id="866a1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="866a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="866a1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="866a1-117">-Name</span></span>
<span data-ttu-id="866a1-118">Az értesítési szabály neve</span><span class="sxs-lookup"><span data-stu-id="866a1-118">The alert rule name</span></span>

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

### <span data-ttu-id="866a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="866a1-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="866a1-120">The resource group name</span></span>

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

### <span data-ttu-id="866a1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="866a1-121">-ResourceId</span></span>
<span data-ttu-id="866a1-122">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="866a1-122">The resource Id</span></span>

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

### <span data-ttu-id="866a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866a1-123">CommonParameters</span></span>
<span data-ttu-id="866a1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="866a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866a1-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="866a1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866a1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="866a1-126">INPUTS</span></span>

### <span data-ttu-id="866a1-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="866a1-127">None</span></span>

## <span data-ttu-id="866a1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="866a1-128">OUTPUTS</span></span>

### <span data-ttu-id="866a1-129">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="866a1-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="866a1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="866a1-130">NOTES</span></span>

## <span data-ttu-id="866a1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="866a1-131">RELATED LINKS</span></span>
