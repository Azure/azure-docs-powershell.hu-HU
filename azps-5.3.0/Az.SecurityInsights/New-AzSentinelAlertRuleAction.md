---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479721"
---
# <span data-ttu-id="e3298-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="e3298-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="e3298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3298-102">SYNOPSIS</span></span>
<span data-ttu-id="e3298-103">Automatikus válasz hozzáadása az analátikumhoz.</span><span class="sxs-lookup"><span data-stu-id="e3298-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="e3298-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3298-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3298-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3298-105">DESCRIPTION</span></span>
<span data-ttu-id="e3298-106">A **New-AzSentinelAlertRuleAction** parancsmag létrehoz egy automatikus választ egy riasztási szabályhoz a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="e3298-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="e3298-107">Meg kell adnia a Logic App Resorce-azonosítóját és a Trigger Uri azonosítót, amely a Logic App modul használatával található meg.</span><span class="sxs-lookup"><span data-stu-id="e3298-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="e3298-108">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="e3298-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e3298-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3298-109">EXAMPLES</span></span>

### <span data-ttu-id="e3298-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e3298-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="e3298-111">Ebben a példában létrehoz egy **AlertRuleActiont** a megadott riasztási szabályhoz a Logic app tulajdonságaival, majd azt a $AlertRuleAction változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e3298-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="e3298-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3298-112">PARAMETERS</span></span>

### <span data-ttu-id="e3298-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="e3298-113">-ActionId</span></span>
<span data-ttu-id="e3298-114">Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="e3298-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3298-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e3298-115">-AlertRuleId</span></span>
<span data-ttu-id="e3298-116">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e3298-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="e3298-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3298-117">-DefaultProfile</span></span>
<span data-ttu-id="e3298-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3298-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3298-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="e3298-119">-LogicAppResourceId</span></span>
<span data-ttu-id="e3298-120">Action Logic App Resource Id.</span><span class="sxs-lookup"><span data-stu-id="e3298-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="e3298-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3298-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3298-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3298-122">Resource group name.</span></span>

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

### <span data-ttu-id="e3298-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="e3298-123">-TriggerUri</span></span>
<span data-ttu-id="e3298-124">Action Logic App Trigger Uri.</span><span class="sxs-lookup"><span data-stu-id="e3298-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="e3298-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e3298-125">-WorkspaceName</span></span>
<span data-ttu-id="e3298-126">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e3298-126">Workspace Name.</span></span>

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

### <span data-ttu-id="e3298-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3298-127">-Confirm</span></span>
<span data-ttu-id="e3298-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3298-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3298-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3298-129">-WhatIf</span></span>
<span data-ttu-id="e3298-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3298-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3298-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3298-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3298-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3298-132">CommonParameters</span></span>
<span data-ttu-id="e3298-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3298-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3298-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3298-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3298-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3298-135">INPUTS</span></span>

### <span data-ttu-id="e3298-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="e3298-136">None</span></span>
## <span data-ttu-id="e3298-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3298-137">OUTPUTS</span></span>

### <span data-ttu-id="e3298-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="e3298-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="e3298-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3298-139">NOTES</span></span>

## <span data-ttu-id="e3298-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3298-140">RELATED LINKS</span></span>
