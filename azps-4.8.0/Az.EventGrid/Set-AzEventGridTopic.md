---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184976"
---
# <span data-ttu-id="50562-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="50562-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="50562-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50562-102">SYNOPSIS</span></span>
<span data-ttu-id="50562-103">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="50562-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="50562-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50562-104">SYNTAX</span></span>

### <span data-ttu-id="50562-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50562-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50562-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="50562-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50562-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50562-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50562-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="50562-108">DESCRIPTION</span></span>
<span data-ttu-id="50562-109">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="50562-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="50562-110">Ezzel a művelettel lecserélheti az esemény rácsvonalai című témakör címkéit.</span><span class="sxs-lookup"><span data-stu-id="50562-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="50562-111">Példák</span><span class="sxs-lookup"><span data-stu-id="50562-111">EXAMPLES</span></span>

### <span data-ttu-id="50562-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="50562-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="50562-113">A \` \` \` \` "részleg" és a "környezet" kifejezésekre cseréli a címkéket a Téma1 MyResourceGroupName az esemény rácsa témakörben.</span><span class="sxs-lookup"><span data-stu-id="50562-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="50562-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50562-114">PARAMETERS</span></span>

### <span data-ttu-id="50562-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50562-115">-DefaultProfile</span></span>
<span data-ttu-id="50562-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="50562-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50562-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="50562-117">-InboundIpRule</span></span>
<span data-ttu-id="50562-118">A Hashtable, amely a bejövő IP-szabályok listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="50562-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="50562-119">Mindegyik szabály az IP-címet adja meg a CIDR (például 10.0.0.0/8), a megfelelő művelettel együtt, amelyet a IpMask egyezés vagy nem egyezik.</span><span class="sxs-lookup"><span data-stu-id="50562-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="50562-120">A lehetséges műveleti értékek csak az engedélyezést tartalmazzák</span><span class="sxs-lookup"><span data-stu-id="50562-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50562-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50562-121">-InputObject</span></span>
<span data-ttu-id="50562-122">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="50562-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="50562-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50562-123">-Name</span></span>
<span data-ttu-id="50562-124">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="50562-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="50562-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="50562-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="50562-126">Ez a beállítás azt határozza meg, hogy a forgalom engedélyezett-e nyilvános hálózaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="50562-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="50562-127">Alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="50562-127">By default it is enabled.</span></span> <span data-ttu-id="50562-128">A InboundIpRule paramétereinek beállításával tovább korlátozhatja a konkrét IP-ket.</span><span class="sxs-lookup"><span data-stu-id="50562-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="50562-129">A megengedett értékek le vannak tiltva és engedélyezve vannak.</span><span class="sxs-lookup"><span data-stu-id="50562-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50562-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50562-130">-ResourceGroupName</span></span>
<span data-ttu-id="50562-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="50562-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="50562-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50562-132">-ResourceId</span></span>
<span data-ttu-id="50562-133">EventGrid téma ResourceID.</span><span class="sxs-lookup"><span data-stu-id="50562-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50562-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="50562-134">-Tag</span></span>
<span data-ttu-id="50562-135">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="50562-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50562-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50562-136">-Confirm</span></span>
<span data-ttu-id="50562-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50562-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50562-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50562-138">-WhatIf</span></span>
<span data-ttu-id="50562-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50562-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50562-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50562-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50562-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50562-141">CommonParameters</span></span>
<span data-ttu-id="50562-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50562-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50562-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="50562-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50562-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50562-144">INPUTS</span></span>

### <span data-ttu-id="50562-145">System. String</span><span class="sxs-lookup"><span data-stu-id="50562-145">System.String</span></span>

### <span data-ttu-id="50562-146">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="50562-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="50562-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50562-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="50562-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50562-148">OUTPUTS</span></span>

### <span data-ttu-id="50562-149">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="50562-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="50562-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50562-150">NOTES</span></span>

## <span data-ttu-id="50562-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50562-151">RELATED LINKS</span></span>
