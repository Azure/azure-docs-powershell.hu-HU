---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203383"
---
# <span data-ttu-id="01569-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01569-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="01569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01569-102">SYNOPSIS</span></span>
<span data-ttu-id="01569-103">Naplóriasztás-szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="01569-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="01569-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01569-104">SYNTAX</span></span>

### <span data-ttu-id="01569-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01569-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01569-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="01569-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01569-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01569-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01569-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01569-108">DESCRIPTION</span></span>
<span data-ttu-id="01569-109">Naplóriasztás-szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="01569-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="01569-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01569-110">EXAMPLES</span></span>

### <span data-ttu-id="01569-111">1. példa: Eltávolítás szabálynév szerint</span><span class="sxs-lookup"><span data-stu-id="01569-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="01569-112">2. példa: Eltávolítás bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="01569-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="01569-113">3. példa: Eltávolítás erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="01569-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="01569-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01569-114">PARAMETERS</span></span>

### <span data-ttu-id="01569-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01569-115">-DefaultProfile</span></span>
<span data-ttu-id="01569-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01569-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01569-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01569-117">-InputObject</span></span>
<span data-ttu-id="01569-118">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="01569-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="01569-119">-Name</span><span class="sxs-lookup"><span data-stu-id="01569-119">-Name</span></span>
<span data-ttu-id="01569-120">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="01569-120">The alert name</span></span>

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

### <span data-ttu-id="01569-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01569-121">-PassThru</span></span>
<span data-ttu-id="01569-122">Egy sikeres vagy sikertelenséget jelző értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="01569-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="01569-123">Ez a parancsmag nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="01569-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01569-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01569-124">-ResourceGroupName</span></span>
<span data-ttu-id="01569-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="01569-125">The resource group name</span></span>

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

### <span data-ttu-id="01569-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01569-126">-ResourceId</span></span>
<span data-ttu-id="01569-127">Az erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="01569-127">The resource Id</span></span>

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

### <span data-ttu-id="01569-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01569-128">-Confirm</span></span>
<span data-ttu-id="01569-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01569-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01569-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01569-130">-WhatIf</span></span>
<span data-ttu-id="01569-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01569-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01569-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01569-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01569-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01569-133">CommonParameters</span></span>
<span data-ttu-id="01569-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01569-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01569-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01569-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01569-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01569-136">INPUTS</span></span>

### <span data-ttu-id="01569-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="01569-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="01569-138">System.String</span><span class="sxs-lookup"><span data-stu-id="01569-138">System.String</span></span>

## <span data-ttu-id="01569-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01569-139">OUTPUTS</span></span>

### <span data-ttu-id="01569-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01569-140">System.Boolean</span></span>

## <span data-ttu-id="01569-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01569-141">NOTES</span></span>

## <span data-ttu-id="01569-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01569-142">RELATED LINKS</span></span>
