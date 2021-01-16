---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363718"
---
# <span data-ttu-id="a45d9-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a45d9-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="a45d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a45d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a45d9-103">Létrehoz egy új Azure Event Grid-témakört.</span><span class="sxs-lookup"><span data-stu-id="a45d9-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a45d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a45d9-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a45d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a45d9-105">DESCRIPTION</span></span>
<span data-ttu-id="a45d9-106">Létrehoz egy új Azure Event Grid-témakört.</span><span class="sxs-lookup"><span data-stu-id="a45d9-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="a45d9-107">A témakör létrehozása után egy alkalmazás közzéteheti az eseményeket a témakör végpontja számára.</span><span class="sxs-lookup"><span data-stu-id="a45d9-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="a45d9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a45d9-108">EXAMPLES</span></span>

### <span data-ttu-id="a45d9-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="a45d9-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="a45d9-110">Létrehozza a Topic1 eseményrács témakört a westus2 megadott földrajzi \` \` \` \` helyén, a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="a45d9-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a45d9-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a45d9-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a45d9-112">Létrehozza a Topic1 eseményrács témakört a westus2 megadott földrajzi helyén, a MyResourceGroupName erőforráscsoportban a \` \` megadott \` \` \` "Department" (Részleg) és \` "Environment" (Környezet) címkével.</span><span class="sxs-lookup"><span data-stu-id="a45d9-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a45d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a45d9-113">PARAMETERS</span></span>

### <span data-ttu-id="a45d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45d9-114">-DefaultProfile</span></span>
<span data-ttu-id="a45d9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a45d9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a45d9-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="a45d9-116">-InboundIpRule</span></span>
<span data-ttu-id="a45d9-117">A bejövő IP-szabályok listáját képviselő kivonat.</span><span class="sxs-lookup"><span data-stu-id="a45d9-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="a45d9-118">Minden szabály megadja az IP-címet a CIDR-ként megadott címként (például 10.0.0.0/8) a megfelelő Műveletekkel együtt, az IpMask egyezése vagy egyezése alapján.</span><span class="sxs-lookup"><span data-stu-id="a45d9-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="a45d9-119">Lehetséges műveletértékek: Csak az Allow (Csak engedélyezése) érték</span><span class="sxs-lookup"><span data-stu-id="a45d9-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a45d9-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="a45d9-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="a45d9-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="a45d9-122">Az engedélyezett kulcsnevek a következőek: tárgy, eseménytípus és adatverzió.</span><span class="sxs-lookup"><span data-stu-id="a45d9-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="a45d9-123">Ezt akkor használja a rendszer, ha az InputSchemaHelp csak customeventschema.</span><span class="sxs-lookup"><span data-stu-id="a45d9-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="a45d9-124">-InputMappingField</span></span>
<span data-ttu-id="a45d9-125">Hashtable which represents the input mapping fields in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="a45d9-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="a45d9-126">Az engedélyezett kulcsnevek a következőek: id, topic, eventtime, subject, eventtype, and dataversion.</span><span class="sxs-lookup"><span data-stu-id="a45d9-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="a45d9-127">Ezt akkor használja a rendszer, ha az InputSchemaHelp csak customeventschema.</span><span class="sxs-lookup"><span data-stu-id="a45d9-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="a45d9-128">-InputSchema</span></span>
<span data-ttu-id="a45d9-129">A témakör bemeneti eseményeinek sémája.</span><span class="sxs-lookup"><span data-stu-id="a45d9-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="a45d9-130">Az engedélyezett értékek: eventgridschema, customeventschema vagy cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="a45d9-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="a45d9-131">Az alapértelmezett érték az eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="a45d9-131">Default value is eventgridschema.</span></span> <span data-ttu-id="a45d9-132">Ne feledje, hogy ha a customeventschema paraméter meg van adva, akkor az InputMappingField vagy/és az InputMappingDefaultValue paramétert is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="a45d9-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-133">-Location</span><span class="sxs-lookup"><span data-stu-id="a45d9-133">-Location</span></span>
<span data-ttu-id="a45d9-134">A témakör helye</span><span class="sxs-lookup"><span data-stu-id="a45d9-134">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a45d9-135">-Name</span></span>
<span data-ttu-id="a45d9-136">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="a45d9-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a45d9-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="a45d9-138">Ez határozza meg, hogy a forgalom engedélyezett-e nyilvános hálózaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="a45d9-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="a45d9-139">Alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a45d9-139">By default it is enabled.</span></span> <span data-ttu-id="a45d9-140">Az InboundIpRule paramétereinek konfigurálásával tovább korlátozhatja az egyes IP-eket.</span><span class="sxs-lookup"><span data-stu-id="a45d9-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="a45d9-141">Az engedélyezett értékek le vannak tiltva és engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="a45d9-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a45d9-142">-ResourceGroupName</span></span>
<span data-ttu-id="a45d9-143">Az erőforráscsoport, amelyben létre kell hozatni a témakört.</span><span class="sxs-lookup"><span data-stu-id="a45d9-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a45d9-144">-Tag</span></span>
<span data-ttu-id="a45d9-145">Erőforráscímkéket képviselő hashtables.</span><span class="sxs-lookup"><span data-stu-id="a45d9-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d9-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a45d9-146">-Confirm</span></span>
<span data-ttu-id="a45d9-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a45d9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a45d9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a45d9-148">-WhatIf</span></span>
<span data-ttu-id="a45d9-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a45d9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a45d9-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a45d9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a45d9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45d9-151">CommonParameters</span></span>
<span data-ttu-id="a45d9-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a45d9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45d9-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a45d9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45d9-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a45d9-154">INPUTS</span></span>

### <span data-ttu-id="a45d9-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a45d9-155">System.String</span></span>

### <span data-ttu-id="a45d9-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a45d9-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a45d9-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a45d9-157">OUTPUTS</span></span>

### <span data-ttu-id="a45d9-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="a45d9-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a45d9-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a45d9-159">NOTES</span></span>

## <span data-ttu-id="a45d9-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a45d9-160">RELATED LINKS</span></span>
