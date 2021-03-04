---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 9fe0fad7ec353b3805bb941b62f6f6b6ee83e157
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935777"
---
# <span data-ttu-id="f59ec-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="f59ec-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="f59ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f59ec-103">Beállítja egy eseményrács-témakör tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f59ec-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="f59ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f59ec-104">SYNTAX</span></span>

### <span data-ttu-id="f59ec-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f59ec-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f59ec-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f59ec-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f59ec-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f59ec-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f59ec-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f59ec-108">DESCRIPTION</span></span>
<span data-ttu-id="f59ec-109">Beállítja egy eseményrács-témakör tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f59ec-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="f59ec-110">Ezzel lecserélheti az Eseményrács témakör címkéit.</span><span class="sxs-lookup"><span data-stu-id="f59ec-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="f59ec-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f59ec-111">EXAMPLES</span></span>

### <span data-ttu-id="f59ec-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f59ec-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="f59ec-113">Beállítja a MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek 1. tulajdonságát, hogy a címkéket a \` \` megadott "Részleg" és \` \` "Környezet" címkékre cserélje.</span><span class="sxs-lookup"><span data-stu-id="f59ec-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="f59ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f59ec-114">PARAMETERS</span></span>

### <span data-ttu-id="f59ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59ec-115">-DefaultProfile</span></span>
<span data-ttu-id="f59ec-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f59ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f59ec-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="f59ec-117">-InboundIpRule</span></span>
<span data-ttu-id="f59ec-118">A bejövő IP-szabályok listáját képviselő kivonat.</span><span class="sxs-lookup"><span data-stu-id="f59ec-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="f59ec-119">Minden szabály megadja az IP-címet a CIDR-ként megadott címként (például 10.0.0.0/8) a megfelelő Műveletekkel együtt, az IpMask egyezése vagy egyezése alapján.</span><span class="sxs-lookup"><span data-stu-id="f59ec-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="f59ec-120">Lehetséges műveletértékek: Csak az Allow (Csak engedélyezése) érték</span><span class="sxs-lookup"><span data-stu-id="f59ec-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="f59ec-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f59ec-121">-InputObject</span></span>
<span data-ttu-id="f59ec-122">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="f59ec-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f59ec-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f59ec-123">-Name</span></span>
<span data-ttu-id="f59ec-124">EventGrid-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="f59ec-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="f59ec-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f59ec-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="f59ec-126">Ez határozza meg, hogy a forgalom engedélyezett-e nyilvános hálózaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="f59ec-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="f59ec-127">Alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="f59ec-127">By default it is enabled.</span></span> <span data-ttu-id="f59ec-128">Az InboundIpRule paramétereinek konfigurálásával tovább korlátozhatja az egyes IP-eket.</span><span class="sxs-lookup"><span data-stu-id="f59ec-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="f59ec-129">Az engedélyezett értékek le vannak tiltva és engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="f59ec-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="f59ec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59ec-130">-ResourceGroupName</span></span>
<span data-ttu-id="f59ec-131">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f59ec-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="f59ec-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f59ec-132">-ResourceId</span></span>
<span data-ttu-id="f59ec-133">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="f59ec-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="f59ec-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="f59ec-134">-Tag</span></span>
<span data-ttu-id="f59ec-135">Az erőforráscímkéket képviselő hashtables.</span><span class="sxs-lookup"><span data-stu-id="f59ec-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="f59ec-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f59ec-136">-Confirm</span></span>
<span data-ttu-id="f59ec-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f59ec-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59ec-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59ec-138">-WhatIf</span></span>
<span data-ttu-id="f59ec-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f59ec-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f59ec-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f59ec-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59ec-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59ec-141">CommonParameters</span></span>
<span data-ttu-id="f59ec-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59ec-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59ec-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f59ec-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59ec-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f59ec-144">INPUTS</span></span>

### <span data-ttu-id="f59ec-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f59ec-145">System.String</span></span>

### <span data-ttu-id="f59ec-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="f59ec-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="f59ec-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f59ec-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f59ec-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f59ec-148">OUTPUTS</span></span>

### <span data-ttu-id="f59ec-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="f59ec-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f59ec-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f59ec-150">NOTES</span></span>

## <span data-ttu-id="f59ec-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f59ec-151">RELATED LINKS</span></span>
