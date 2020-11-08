---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194411"
---
# <span data-ttu-id="49aab-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="49aab-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="49aab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49aab-102">SYNOPSIS</span></span>
<span data-ttu-id="49aab-103">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="49aab-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="49aab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49aab-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49aab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49aab-105">DESCRIPTION</span></span>
<span data-ttu-id="49aab-106">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="49aab-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="49aab-107">Miután létrehozta a témát, az alkalmazás közzéteheti az eseményeket a téma végpontjának segítségével.</span><span class="sxs-lookup"><span data-stu-id="49aab-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="49aab-108">Példák</span><span class="sxs-lookup"><span data-stu-id="49aab-108">EXAMPLES</span></span>

### <span data-ttu-id="49aab-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49aab-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="49aab-110">A \` \` megadott földrajzi hely \` westus2 \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény rácshoz tartozó téma1.</span><span class="sxs-lookup"><span data-stu-id="49aab-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="49aab-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="49aab-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="49aab-112">A megadott \` \` földrajzi hely \` westus2 \` , az erőforráscsoport \` MyResourceGroupName \` a megadott címkéket a "részleg" és a "környezet" téma1 hozza létre az esemény táblázatát.</span><span class="sxs-lookup"><span data-stu-id="49aab-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="49aab-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49aab-113">PARAMETERS</span></span>

### <span data-ttu-id="49aab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49aab-114">-DefaultProfile</span></span>
<span data-ttu-id="49aab-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49aab-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49aab-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="49aab-116">-InboundIpRule</span></span>
<span data-ttu-id="49aab-117">A Hashtable, amely a bejövő IP-szabályok listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="49aab-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="49aab-118">Mindegyik szabály az IP-címet adja meg a CIDR (például 10.0.0.0/8), a megfelelő művelettel együtt, amelyet a IpMask egyezés vagy nem egyezik.</span><span class="sxs-lookup"><span data-stu-id="49aab-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="49aab-119">A lehetséges műveleti értékek csak az engedélyezést tartalmazzák</span><span class="sxs-lookup"><span data-stu-id="49aab-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="49aab-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="49aab-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="49aab-121">A Hashtable, amely a beviteli megfeleltetési mezőket az alapértelmezett érték szóközzel tagolt kulcs = érték formátumban jelöli.</span><span class="sxs-lookup"><span data-stu-id="49aab-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="49aab-122">A megengedett kulcsok nevei a következők: tárgy, EventType és dataversion.</span><span class="sxs-lookup"><span data-stu-id="49aab-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="49aab-123">Ez akkor használatos, ha csak a InputSchemaHelp customeventschema.</span><span class="sxs-lookup"><span data-stu-id="49aab-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="49aab-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="49aab-124">-InputMappingField</span></span>
<span data-ttu-id="49aab-125">A Hashtable, amely a bemeneti megfeleltetési mezőket az szóközzel tagolt kulcs = érték formátumban jelöli.</span><span class="sxs-lookup"><span data-stu-id="49aab-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="49aab-126">A megengedett kulcsok nevei: azonosító, témakör, eventtime, tárgy, EventType és dataversion.</span><span class="sxs-lookup"><span data-stu-id="49aab-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="49aab-127">Ez akkor használatos, ha csak a InputSchemaHelp customeventschema.</span><span class="sxs-lookup"><span data-stu-id="49aab-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="49aab-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="49aab-128">-InputSchema</span></span>
<span data-ttu-id="49aab-129">A témakör bemeneti eseményeinek sémája.</span><span class="sxs-lookup"><span data-stu-id="49aab-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="49aab-130">A megengedett értékek a következők: eventgridschema, customeventschema vagy cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="49aab-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="49aab-131">Az alapértelmezett érték a eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="49aab-131">Default value is eventgridschema.</span></span> <span data-ttu-id="49aab-132">Ne feledje, hogy ha a customeventschema meg van adva, akkor a InputMappingField vagy/vagy a InputMappingDefaultValue paramétert is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="49aab-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="49aab-133">-Hely</span><span class="sxs-lookup"><span data-stu-id="49aab-133">-Location</span></span>
<span data-ttu-id="49aab-134">A témakör helye</span><span class="sxs-lookup"><span data-stu-id="49aab-134">The location of the topic</span></span>

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

### <span data-ttu-id="49aab-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49aab-135">-Name</span></span>
<span data-ttu-id="49aab-136">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="49aab-136">The name of the topic.</span></span>

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

### <span data-ttu-id="49aab-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="49aab-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="49aab-138">Ez a beállítás azt határozza meg, hogy a forgalom engedélyezett-e nyilvános hálózaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="49aab-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="49aab-139">Alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="49aab-139">By default it is enabled.</span></span> <span data-ttu-id="49aab-140">A InboundIpRule paramétereinek beállításával tovább korlátozhatja a konkrét IP-ket.</span><span class="sxs-lookup"><span data-stu-id="49aab-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="49aab-141">A megengedett értékek le vannak tiltva és engedélyezve vannak.</span><span class="sxs-lookup"><span data-stu-id="49aab-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="49aab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49aab-142">-ResourceGroupName</span></span>
<span data-ttu-id="49aab-143">Az az erőforráscsoport, amelyben a témakört létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="49aab-143">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="49aab-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="49aab-144">-Tag</span></span>
<span data-ttu-id="49aab-145">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="49aab-145">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="49aab-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49aab-146">-Confirm</span></span>
<span data-ttu-id="49aab-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49aab-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49aab-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49aab-148">-WhatIf</span></span>
<span data-ttu-id="49aab-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49aab-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49aab-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49aab-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49aab-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49aab-151">CommonParameters</span></span>
<span data-ttu-id="49aab-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49aab-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49aab-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49aab-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49aab-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49aab-154">INPUTS</span></span>

### <span data-ttu-id="49aab-155">System. String</span><span class="sxs-lookup"><span data-stu-id="49aab-155">System.String</span></span>

### <span data-ttu-id="49aab-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="49aab-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49aab-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49aab-157">OUTPUTS</span></span>

### <span data-ttu-id="49aab-158">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="49aab-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="49aab-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49aab-159">NOTES</span></span>

## <span data-ttu-id="49aab-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49aab-160">RELATED LINKS</span></span>
