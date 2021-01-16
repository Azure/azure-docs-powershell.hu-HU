---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341417"
---
# <span data-ttu-id="3f16d-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3f16d-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="3f16d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f16d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f16d-103">Eltávolít egy Azure Event Grid-témakört.</span><span class="sxs-lookup"><span data-stu-id="3f16d-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="3f16d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f16d-104">SYNTAX</span></span>

### <span data-ttu-id="3f16d-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f16d-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f16d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f16d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f16d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f16d-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f16d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f16d-108">DESCRIPTION</span></span>
<span data-ttu-id="3f16d-109">Eltávolít egy Azure Event Grid-témakört.</span><span class="sxs-lookup"><span data-stu-id="3f16d-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="3f16d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f16d-110">EXAMPLES</span></span>

### <span data-ttu-id="3f16d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f16d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="3f16d-112">Eltávolítja az Eseményrács témakör Topic1 részét \` \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3f16d-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3f16d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3f16d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="3f16d-114">Eltávolítja az Eseményrács témakör Topic1 részét \` \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3f16d-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3f16d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f16d-115">PARAMETERS</span></span>

### <span data-ttu-id="3f16d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f16d-116">-DefaultProfile</span></span>
<span data-ttu-id="3f16d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f16d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f16d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f16d-118">-InputObject</span></span>
<span data-ttu-id="3f16d-119">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="3f16d-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="3f16d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f16d-120">-Name</span></span>
<span data-ttu-id="3f16d-121">EventGrid-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="3f16d-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="3f16d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f16d-122">-PassThru</span></span>
<span data-ttu-id="3f16d-123">Az Eltávolítás művelet állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3f16d-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="3f16d-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3f16d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f16d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f16d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f16d-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f16d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="3f16d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f16d-127">-ResourceId</span></span>
<span data-ttu-id="3f16d-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="3f16d-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="3f16d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f16d-129">-Confirm</span></span>
<span data-ttu-id="3f16d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f16d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f16d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f16d-131">-WhatIf</span></span>
<span data-ttu-id="3f16d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f16d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f16d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f16d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f16d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f16d-134">CommonParameters</span></span>
<span data-ttu-id="3f16d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f16d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f16d-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f16d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f16d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f16d-137">INPUTS</span></span>

### <span data-ttu-id="3f16d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3f16d-138">System.String</span></span>

### <span data-ttu-id="3f16d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="3f16d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="3f16d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f16d-140">OUTPUTS</span></span>

### <span data-ttu-id="3f16d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f16d-141">System.Boolean</span></span>

## <span data-ttu-id="3f16d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f16d-142">NOTES</span></span>

## <span data-ttu-id="3f16d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f16d-143">RELATED LINKS</span></span>
