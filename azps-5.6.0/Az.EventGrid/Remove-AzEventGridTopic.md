---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3960f73d115b881bdffab89c225a9321e19af067
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938689"
---
# <span data-ttu-id="90f95-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="90f95-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="90f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90f95-102">SYNOPSIS</span></span>
<span data-ttu-id="90f95-103">Eltávolít egy Azure Event Grid-témakört.</span><span class="sxs-lookup"><span data-stu-id="90f95-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="90f95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90f95-104">SYNTAX</span></span>

### <span data-ttu-id="90f95-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90f95-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f95-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f95-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f95-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f95-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f95-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90f95-108">DESCRIPTION</span></span>
<span data-ttu-id="90f95-109">Eltávolít egy Azure Event Grid-témakört.</span><span class="sxs-lookup"><span data-stu-id="90f95-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="90f95-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90f95-110">EXAMPLES</span></span>

### <span data-ttu-id="90f95-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="90f95-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="90f95-112">Eltávolítja az Eseményrács témakör Topic1 részét \` \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="90f95-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="90f95-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="90f95-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="90f95-114">Eltávolítja az Eseményrács témakör Topic1 részét \` \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="90f95-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="90f95-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90f95-115">PARAMETERS</span></span>

### <span data-ttu-id="90f95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f95-116">-DefaultProfile</span></span>
<span data-ttu-id="90f95-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="90f95-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90f95-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90f95-118">-InputObject</span></span>
<span data-ttu-id="90f95-119">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="90f95-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f95-120">-Name</span><span class="sxs-lookup"><span data-stu-id="90f95-120">-Name</span></span>
<span data-ttu-id="90f95-121">EventGrid-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="90f95-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f95-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90f95-122">-PassThru</span></span>
<span data-ttu-id="90f95-123">Az Eltávolítás művelet állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="90f95-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="90f95-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="90f95-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="90f95-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f95-125">-ResourceGroupName</span></span>
<span data-ttu-id="90f95-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="90f95-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f95-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90f95-127">-ResourceId</span></span>
<span data-ttu-id="90f95-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="90f95-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f95-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90f95-129">-Confirm</span></span>
<span data-ttu-id="90f95-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90f95-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f95-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f95-131">-WhatIf</span></span>
<span data-ttu-id="90f95-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90f95-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90f95-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90f95-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f95-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f95-134">CommonParameters</span></span>
<span data-ttu-id="90f95-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f95-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f95-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90f95-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f95-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90f95-137">INPUTS</span></span>

### <span data-ttu-id="90f95-138">System.String</span><span class="sxs-lookup"><span data-stu-id="90f95-138">System.String</span></span>

### <span data-ttu-id="90f95-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="90f95-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="90f95-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90f95-140">OUTPUTS</span></span>

### <span data-ttu-id="90f95-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90f95-141">System.Boolean</span></span>

## <span data-ttu-id="90f95-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90f95-142">NOTES</span></span>

## <span data-ttu-id="90f95-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90f95-143">RELATED LINKS</span></span>
