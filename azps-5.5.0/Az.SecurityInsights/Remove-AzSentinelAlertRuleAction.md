---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168939"
---
# <span data-ttu-id="43520-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="43520-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="43520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43520-102">SYNOPSIS</span></span>
<span data-ttu-id="43520-103">Automatikus válasz eltávolítása analyticből.</span><span class="sxs-lookup"><span data-stu-id="43520-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="43520-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43520-104">SYNTAX</span></span>

### <span data-ttu-id="43520-105">ActionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43520-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43520-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="43520-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43520-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43520-107">DESCRIPTION</span></span>
<span data-ttu-id="43520-108">A **Remove-AzSentinelAlertRuleAction** parancsmag véglegesen töröl egy automatikus választ a riasztási szabályból egy adott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="43520-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="43520-109">A **AlertRuleAction** objektumokat átadhatja a folyamat műveleti jelével, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="43520-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="43520-110">A Confirm paraméter és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="43520-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="43520-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43520-111">EXAMPLES</span></span>

### <span data-ttu-id="43520-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="43520-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="43520-113">Ez a parancs eltávolítja a riasztási szabályt a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="43520-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="43520-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43520-114">PARAMETERS</span></span>

### <span data-ttu-id="43520-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="43520-115">-ActionId</span></span>
<span data-ttu-id="43520-116">Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="43520-116">Action Id.</span></span>

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

### <span data-ttu-id="43520-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="43520-117">-AlertRuleId</span></span>
<span data-ttu-id="43520-118">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="43520-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43520-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43520-119">-DefaultProfile</span></span>
<span data-ttu-id="43520-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43520-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43520-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43520-121">-InputObject</span></span>
<span data-ttu-id="43520-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="43520-122">InputObject.</span></span>

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

### <span data-ttu-id="43520-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43520-123">-PassThru</span></span>
<span data-ttu-id="43520-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="43520-124">PassThru</span></span>

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

### <span data-ttu-id="43520-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43520-125">-ResourceGroupName</span></span>
<span data-ttu-id="43520-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43520-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43520-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43520-127">-WorkspaceName</span></span>
<span data-ttu-id="43520-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="43520-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43520-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43520-129">-Confirm</span></span>
<span data-ttu-id="43520-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43520-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43520-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43520-131">-WhatIf</span></span>
<span data-ttu-id="43520-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43520-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43520-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43520-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43520-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43520-134">CommonParameters</span></span>
<span data-ttu-id="43520-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43520-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43520-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43520-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43520-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43520-137">INPUTS</span></span>

### <span data-ttu-id="43520-138">System.String</span><span class="sxs-lookup"><span data-stu-id="43520-138">System.String</span></span>
### <span data-ttu-id="43520-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="43520-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="43520-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43520-140">OUTPUTS</span></span>

### <span data-ttu-id="43520-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="43520-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="43520-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43520-142">NOTES</span></span>

## <span data-ttu-id="43520-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43520-143">RELATED LINKS</span></span>
