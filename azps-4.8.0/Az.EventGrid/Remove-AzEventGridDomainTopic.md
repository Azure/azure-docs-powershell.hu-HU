---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184989"
---
# <span data-ttu-id="29788-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="29788-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="29788-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29788-102">SYNOPSIS</span></span>
<span data-ttu-id="29788-103">Az Azure Event Grid domain-témájának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="29788-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="29788-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29788-104">SYNTAX</span></span>

### <span data-ttu-id="29788-105">DomainTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29788-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29788-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="29788-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29788-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29788-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29788-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29788-108">DESCRIPTION</span></span>
<span data-ttu-id="29788-109">Az Azure Event Grid domain-témájának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="29788-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="29788-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29788-110">EXAMPLES</span></span>

### <span data-ttu-id="29788-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29788-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="29788-112">Eltávolítja az esemény rácsa \` téma1 a \` tartomány \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="29788-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="29788-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="29788-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="29788-114">Eltávolítja az esemény rácsa \` téma1 a \` tartomány \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="29788-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="29788-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29788-115">PARAMETERS</span></span>

### <span data-ttu-id="29788-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29788-116">-DefaultProfile</span></span>
<span data-ttu-id="29788-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29788-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29788-118">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="29788-118">-DomainName</span></span>
<span data-ttu-id="29788-119">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="29788-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29788-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29788-120">-InputObject</span></span>
<span data-ttu-id="29788-121">EventGrid objektum</span><span class="sxs-lookup"><span data-stu-id="29788-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29788-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29788-122">-Name</span></span>
<span data-ttu-id="29788-123">EventGrid a tartomány témájának nevét.</span><span class="sxs-lookup"><span data-stu-id="29788-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29788-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29788-124">-PassThru</span></span>
<span data-ttu-id="29788-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="29788-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29788-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29788-126">-ResourceGroupName</span></span>
<span data-ttu-id="29788-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="29788-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29788-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29788-128">-ResourceId</span></span>
<span data-ttu-id="29788-129">Az Event Grid domain témakört megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="29788-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29788-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29788-130">-Confirm</span></span>
<span data-ttu-id="29788-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29788-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29788-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29788-132">-WhatIf</span></span>
<span data-ttu-id="29788-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29788-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29788-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29788-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29788-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29788-135">CommonParameters</span></span>
<span data-ttu-id="29788-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29788-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29788-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29788-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29788-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29788-138">INPUTS</span></span>

### <span data-ttu-id="29788-139">System. String</span><span class="sxs-lookup"><span data-stu-id="29788-139">System.String</span></span>

### <span data-ttu-id="29788-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="29788-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="29788-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29788-141">OUTPUTS</span></span>

### <span data-ttu-id="29788-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29788-142">System.Boolean</span></span>

## <span data-ttu-id="29788-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29788-143">NOTES</span></span>

## <span data-ttu-id="29788-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29788-144">RELATED LINKS</span></span>