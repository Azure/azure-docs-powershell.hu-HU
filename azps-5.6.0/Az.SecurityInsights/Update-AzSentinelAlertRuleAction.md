---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 3feb6a9cfa06e06a4759c34e3c0b2cd624559d2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920441"
---
# <span data-ttu-id="bd86f-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="bd86f-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="bd86f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd86f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd86f-103">Automatikus válasz (értesítési szabály- művelet) frissítése</span><span class="sxs-lookup"><span data-stu-id="bd86f-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="bd86f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd86f-104">SYNTAX</span></span>

### <span data-ttu-id="bd86f-105">ActionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd86f-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd86f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bd86f-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd86f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd86f-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd86f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd86f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd86f-109">Az **Update-AzSentinelAlertRuleAction** parancsmag frissíti a könyvjelzőt a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="bd86f-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="bd86f-110">A **AlertRuleAction** objektumokat paraméterként vagy a folyamat műveleti jelének használatával is átadhatja, vagy megadhatja a *AlertRuleId* és *az ActionId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="bd86f-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="bd86f-111">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="bd86f-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bd86f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd86f-112">EXAMPLES</span></span>

### <span data-ttu-id="bd86f-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="bd86f-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="bd86f-114">Ebben a példában egy **AlertRuleAction frissül,** amely a meglévő *műveletet* új tulajdonságokra cseréli.</span><span class="sxs-lookup"><span data-stu-id="bd86f-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="bd86f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="bd86f-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="bd86f-116">Ebben a példában egy **AlertRuleAction** frissül egy InputObject művelettel, amely egy meglévő *műveletet* új tulajdonságokra cserél.</span><span class="sxs-lookup"><span data-stu-id="bd86f-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="bd86f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd86f-117">PARAMETERS</span></span>

### <span data-ttu-id="bd86f-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="bd86f-118">-ActionId</span></span>
<span data-ttu-id="bd86f-119">Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="bd86f-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="bd86f-120">-AlertRuleId</span></span>
<span data-ttu-id="bd86f-121">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd86f-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd86f-122">-DefaultProfile</span></span>
<span data-ttu-id="bd86f-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd86f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd86f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd86f-124">-InputObject</span></span>
<span data-ttu-id="bd86f-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="bd86f-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="bd86f-126">-LogicAppResourceId</span></span>
<span data-ttu-id="bd86f-127">Action Logic App Resource Id.</span><span class="sxs-lookup"><span data-stu-id="bd86f-127">Action Logic App Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd86f-128">-ResourceGroupName</span></span>
<span data-ttu-id="bd86f-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd86f-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd86f-130">-ResourceId</span></span>
<span data-ttu-id="bd86f-131">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bd86f-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="bd86f-132">-TriggerUri</span></span>
<span data-ttu-id="bd86f-133">Action Logic App Trigger Uri.</span><span class="sxs-lookup"><span data-stu-id="bd86f-133">Action Logic App Trigger Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd86f-134">-WorkspaceName</span></span>
<span data-ttu-id="bd86f-135">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="bd86f-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd86f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd86f-136">-Confirm</span></span>
<span data-ttu-id="bd86f-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd86f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd86f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd86f-138">-WhatIf</span></span>
<span data-ttu-id="bd86f-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd86f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd86f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd86f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd86f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd86f-141">CommonParameters</span></span>
<span data-ttu-id="bd86f-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd86f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd86f-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd86f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd86f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd86f-144">INPUTS</span></span>

### <span data-ttu-id="bd86f-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="bd86f-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="bd86f-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="bd86f-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="bd86f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bd86f-147">System.String</span></span>

## <span data-ttu-id="bd86f-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd86f-148">OUTPUTS</span></span>

### <span data-ttu-id="bd86f-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="bd86f-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="bd86f-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd86f-150">NOTES</span></span>

## <span data-ttu-id="bd86f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd86f-151">RELATED LINKS</span></span>
