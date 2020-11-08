---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184981"
---
# <span data-ttu-id="fcaa6-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="fcaa6-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="fcaa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="fcaa6-103">Azure-esemény rácsvonal-témakörének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fcaa6-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="fcaa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcaa6-104">SYNTAX</span></span>

### <span data-ttu-id="fcaa6-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcaa6-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcaa6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcaa6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcaa6-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcaa6-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcaa6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcaa6-108">DESCRIPTION</span></span>
<span data-ttu-id="fcaa6-109">Azure-esemény rácsvonal-témakörének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fcaa6-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="fcaa6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fcaa6-110">EXAMPLES</span></span>

### <span data-ttu-id="fcaa6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fcaa6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="fcaa6-112">Eltávolítja az esemény rács témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fcaa6-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fcaa6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fcaa6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="fcaa6-114">Eltávolítja az esemény rács témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fcaa6-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fcaa6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcaa6-115">PARAMETERS</span></span>

### <span data-ttu-id="fcaa6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcaa6-116">-DefaultProfile</span></span>
<span data-ttu-id="fcaa6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fcaa6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcaa6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcaa6-118">-InputObject</span></span>
<span data-ttu-id="fcaa6-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="fcaa6-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="fcaa6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fcaa6-120">-Name</span></span>
<span data-ttu-id="fcaa6-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="fcaa6-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="fcaa6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcaa6-122">-PassThru</span></span>
<span data-ttu-id="fcaa6-123">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="fcaa6-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcaa6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcaa6-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcaa6-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcaa6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcaa6-127">-ResourceId</span></span>
<span data-ttu-id="fcaa6-128">EventGrid téma ResourceID.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="fcaa6-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fcaa6-129">-Confirm</span></span>
<span data-ttu-id="fcaa6-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcaa6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcaa6-131">-WhatIf</span></span>
<span data-ttu-id="fcaa6-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcaa6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcaa6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcaa6-134">CommonParameters</span></span>
<span data-ttu-id="fcaa6-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcaa6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcaa6-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fcaa6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcaa6-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcaa6-137">INPUTS</span></span>

### <span data-ttu-id="fcaa6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fcaa6-138">System.String</span></span>

### <span data-ttu-id="fcaa6-139">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="fcaa6-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="fcaa6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcaa6-140">OUTPUTS</span></span>

### <span data-ttu-id="fcaa6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcaa6-141">System.Boolean</span></span>

## <span data-ttu-id="fcaa6-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcaa6-142">NOTES</span></span>

## <span data-ttu-id="fcaa6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcaa6-143">RELATED LINKS</span></span>