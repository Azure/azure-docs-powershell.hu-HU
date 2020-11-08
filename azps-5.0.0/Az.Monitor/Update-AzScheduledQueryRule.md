---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195737"
---
# <span data-ttu-id="db2dc-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="db2dc-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="db2dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="db2dc-103">Naplózási riasztási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="db2dc-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="db2dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db2dc-104">SYNTAX</span></span>

### <span data-ttu-id="db2dc-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db2dc-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2dc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db2dc-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2dc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db2dc-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2dc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="db2dc-108">DESCRIPTION</span></span>
<span data-ttu-id="db2dc-109">Naplózási riasztási szabály frissítése, ha a parancs támogatja a csak az "enabled" tulajdonság frissítését.</span><span class="sxs-lookup"><span data-stu-id="db2dc-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="db2dc-110">A többi tulajdonság frissítéséről a [set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) parancs nyújt tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="db2dc-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="db2dc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="db2dc-111">EXAMPLES</span></span>

### <span data-ttu-id="db2dc-112">Példa 1: szabály nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="db2dc-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
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

### <span data-ttu-id="db2dc-113">2. példa: beviteli objektum általi frissítés</span><span class="sxs-lookup"><span data-stu-id="db2dc-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
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

### <span data-ttu-id="db2dc-114">3. példa: erőforrás-azonosító szerinti frissítés</span><span class="sxs-lookup"><span data-stu-id="db2dc-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
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

## <span data-ttu-id="db2dc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db2dc-115">PARAMETERS</span></span>

### <span data-ttu-id="db2dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2dc-116">-DefaultProfile</span></span>
<span data-ttu-id="db2dc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db2dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db2dc-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="db2dc-118">-Enabled</span></span>
<span data-ttu-id="db2dc-119">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="db2dc-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2dc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db2dc-120">-InputObject</span></span>
<span data-ttu-id="db2dc-121">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="db2dc-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db2dc-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db2dc-122">-Name</span></span>
<span data-ttu-id="db2dc-123">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="db2dc-123">The alert name</span></span>

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

### <span data-ttu-id="db2dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="db2dc-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="db2dc-125">The resource group name</span></span>

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

### <span data-ttu-id="db2dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db2dc-126">-ResourceId</span></span>
<span data-ttu-id="db2dc-127">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="db2dc-127">The resource Id</span></span>

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

### <span data-ttu-id="db2dc-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db2dc-128">-Confirm</span></span>
<span data-ttu-id="db2dc-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db2dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2dc-130">-WhatIf</span></span>
<span data-ttu-id="db2dc-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db2dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2dc-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db2dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2dc-133">CommonParameters</span></span>
<span data-ttu-id="db2dc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db2dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2dc-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db2dc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2dc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db2dc-136">INPUTS</span></span>

### <span data-ttu-id="db2dc-137">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="db2dc-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="db2dc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="db2dc-138">System.String</span></span>

## <span data-ttu-id="db2dc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db2dc-139">OUTPUTS</span></span>

### <span data-ttu-id="db2dc-140">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="db2dc-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="db2dc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db2dc-141">NOTES</span></span>

## <span data-ttu-id="db2dc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db2dc-142">RELATED LINKS</span></span>
