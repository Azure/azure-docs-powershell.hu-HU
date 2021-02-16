---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161642"
---
# <span data-ttu-id="69b7b-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="69b7b-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="69b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="69b7b-103">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="69b7b-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="69b7b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69b7b-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69b7b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="69b7b-106">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="69b7b-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="69b7b-107">A tartomány létrehozása után egy alkalmazás közzéteheti az eseményeket a témakör végpontjára.</span><span class="sxs-lookup"><span data-stu-id="69b7b-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="69b7b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69b7b-108">EXAMPLES</span></span>

### <span data-ttu-id="69b7b-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="69b7b-109">Example 1</span></span>

<span data-ttu-id="69b7b-110">Létrehozza az Eseményrács tartomány1 tartományt a westus2 megadott földrajzi \` \` \` \` helyen, a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="69b7b-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="69b7b-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="69b7b-111">Example 2</span></span>

<span data-ttu-id="69b7b-112">Létrehozza az Eseményrács tartomány1 tartományát a westus2 megadott földrajzi helyen, a MyResourceGroupName erőforráscsoportban a \` \` megadott \` "Department" és \` \` \` "Environment" címkével.</span><span class="sxs-lookup"><span data-stu-id="69b7b-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="69b7b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69b7b-113">PARAMETERS</span></span>

### <span data-ttu-id="69b7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b7b-114">-DefaultProfile</span></span>
<span data-ttu-id="69b7b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69b7b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b7b-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="69b7b-116">-InboundIpRule</span></span>
<span data-ttu-id="69b7b-117">A bejövő IP-szabályok listáját képviselő kivonat.</span><span class="sxs-lookup"><span data-stu-id="69b7b-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="69b7b-118">Minden szabály megadja az IP-címet a CIDR-címként megadott címként (például 10.0.0.0/8) a megfelelő Műveletekkel együtt, az IpMask egyezése vagy egyezése alapján.</span><span class="sxs-lookup"><span data-stu-id="69b7b-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="69b7b-119">Lehetséges műveletértékek: Csak az Allow (Csak engedélyezése) érték</span><span class="sxs-lookup"><span data-stu-id="69b7b-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="69b7b-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="69b7b-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="69b7b-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="69b7b-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="69b7b-122">Az engedélyezett kulcsnevek a következőek: tárgy, eseménytípus és dataversion.</span><span class="sxs-lookup"><span data-stu-id="69b7b-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="69b7b-123">Ezt akkor használja a rendszer, ha az InputSchemaHelp csak customeventschema.</span><span class="sxs-lookup"><span data-stu-id="69b7b-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="69b7b-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="69b7b-124">-InputMappingField</span></span>
<span data-ttu-id="69b7b-125">Hashtable which represents the input mapping fields in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="69b7b-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="69b7b-126">Az engedélyezett kulcsnevek a következőek: id, topic, eventtime, subject, eventtype, and dataversion.</span><span class="sxs-lookup"><span data-stu-id="69b7b-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="69b7b-127">Ezt akkor használja a rendszer, ha az InputSchemaHelp csak customeventschema.</span><span class="sxs-lookup"><span data-stu-id="69b7b-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="69b7b-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="69b7b-128">-InputSchema</span></span>
<span data-ttu-id="69b7b-129">A témakör bemeneti eseményeinek sémája.</span><span class="sxs-lookup"><span data-stu-id="69b7b-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="69b7b-130">Az engedélyezett értékek: eventgridschema, customeventschema vagy cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="69b7b-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="69b7b-131">Az alapértelmezett érték az eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="69b7b-131">Default value is eventgridschema.</span></span> <span data-ttu-id="69b7b-132">Ne feledje, hogy ha a customeventschema paraméter meg van adva, akkor az InputMappingField vagy/és az InputMappingDefaultValue paramétert is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="69b7b-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="69b7b-133">-Location</span><span class="sxs-lookup"><span data-stu-id="69b7b-133">-Location</span></span>
<span data-ttu-id="69b7b-134">A tartomány helye.</span><span class="sxs-lookup"><span data-stu-id="69b7b-134">The location of the domain.</span></span>

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

### <span data-ttu-id="69b7b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="69b7b-135">-Name</span></span>
<span data-ttu-id="69b7b-136">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="69b7b-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b7b-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="69b7b-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="69b7b-138">Ez határozza meg, hogy a forgalom engedélyezett-e nyilvános hálózaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="69b7b-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="69b7b-139">Alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="69b7b-139">By default it is enabled.</span></span> <span data-ttu-id="69b7b-140">Az InboundIpRule paramétereinek konfigurálásával tovább korlátozhatja az egyes IP-eket.</span><span class="sxs-lookup"><span data-stu-id="69b7b-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="69b7b-141">Az engedélyezett értékek le vannak tiltva és engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="69b7b-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="69b7b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b7b-142">-ResourceGroupName</span></span>
<span data-ttu-id="69b7b-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="69b7b-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="69b7b-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="69b7b-144">-Tag</span></span>
<span data-ttu-id="69b7b-145">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="69b7b-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="69b7b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69b7b-146">-Confirm</span></span>
<span data-ttu-id="69b7b-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69b7b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b7b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b7b-148">-WhatIf</span></span>
<span data-ttu-id="69b7b-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69b7b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b7b-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69b7b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b7b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b7b-151">CommonParameters</span></span>
<span data-ttu-id="69b7b-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b7b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b7b-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69b7b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b7b-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69b7b-154">INPUTS</span></span>

### <span data-ttu-id="69b7b-155">System.String</span><span class="sxs-lookup"><span data-stu-id="69b7b-155">System.String</span></span>

### <span data-ttu-id="69b7b-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="69b7b-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="69b7b-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69b7b-157">OUTPUTS</span></span>

### <span data-ttu-id="69b7b-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="69b7b-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="69b7b-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69b7b-159">NOTES</span></span>

## <span data-ttu-id="69b7b-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69b7b-160">RELATED LINKS</span></span>
