---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935129"
---
# <span data-ttu-id="64d09-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="64d09-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="64d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d09-102">SYNOPSIS</span></span>
<span data-ttu-id="64d09-103">DigitalTwinsInstance végpont létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="64d09-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="64d09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64d09-104">SYNTAX</span></span>

### <span data-ttu-id="64d09-105">EventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64d09-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64d09-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="64d09-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64d09-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="64d09-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64d09-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64d09-108">DESCRIPTION</span></span>
<span data-ttu-id="64d09-109">DigitalTwinsInstance végpont létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="64d09-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="64d09-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64d09-110">EXAMPLES</span></span>

### <span data-ttu-id="64d09-111">1. példa: AzDigitalTwinsEndpoint létrehozása az Eventhubhoz</span><span class="sxs-lookup"><span data-stu-id="64d09-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="64d09-112">AzDigitalTwinsEndpoint for Eventhub létrehozása a connectionStringPrimaryKey segítségével</span><span class="sxs-lookup"><span data-stu-id="64d09-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="64d09-113">2. példa: AzDigitalTwinsEndpoint létrehozása az EventGrid számára</span><span class="sxs-lookup"><span data-stu-id="64d09-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="64d09-114">Az AzDigitalTwinsEndpoint létrehozása az Eventhubhoz a TopicEndpoint és az accessKey1 segítségével</span><span class="sxs-lookup"><span data-stu-id="64d09-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="64d09-115">3. példa: AzDigitalTwinsEndpoint for ServiceBus létrehozása</span><span class="sxs-lookup"><span data-stu-id="64d09-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="64d09-116">AzDigitalTwinsEndpoint for ServicBus létrehozása a PrimaryConnectionString szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="64d09-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="64d09-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64d09-117">PARAMETERS</span></span>

### <span data-ttu-id="64d09-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="64d09-118">-AccessKey1</span></span>
<span data-ttu-id="64d09-119">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d09-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64d09-120">-AsJob</span></span>
<span data-ttu-id="64d09-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="64d09-121">Run the command as a job</span></span>

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

### <span data-ttu-id="64d09-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="64d09-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="64d09-123">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d09-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="64d09-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="64d09-125">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d09-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="64d09-126">-DeadLetterSecret</span></span>
<span data-ttu-id="64d09-127">Elhalt levél tárolási titka.</span><span class="sxs-lookup"><span data-stu-id="64d09-127">Dead letter storage secret.</span></span>
<span data-ttu-id="64d09-128">Olvasottságkor el lesz havazva.</span><span class="sxs-lookup"><span data-stu-id="64d09-128">Will be obfuscated during read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d09-129">-DefaultProfile</span></span>
<span data-ttu-id="64d09-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64d09-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="64d09-131">-EndpointDescription</span></span>
<span data-ttu-id="64d09-132">DigitalTwinsInstance végpontforrás.</span><span class="sxs-lookup"><span data-stu-id="64d09-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="64d09-133">Ennek létrehozásáról az ENDPOINTDESCRIPTION tulajdonságokat ismertető MEGJEGYZÉSEK című szakaszban és egy kivonattáblát hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="64d09-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="64d09-134">-EndpointName</span></span>
<span data-ttu-id="64d09-135">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="64d09-135">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="64d09-136">-EndpointType</span></span>
<span data-ttu-id="64d09-137">A Digitális végpont típusa</span><span class="sxs-lookup"><span data-stu-id="64d09-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64d09-138">-NoWait</span></span>
<span data-ttu-id="64d09-139">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="64d09-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64d09-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="64d09-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="64d09-141">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d09-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d09-142">-ResourceGroupName</span></span>
<span data-ttu-id="64d09-143">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="64d09-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="64d09-144">-ResourceName</span></span>
<span data-ttu-id="64d09-145">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="64d09-145">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64d09-146">-SubscriptionId</span></span>
<span data-ttu-id="64d09-147">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d09-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="64d09-148">-TopicEndpoint</span></span>
<span data-ttu-id="64d09-149">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d09-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d09-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64d09-150">-Confirm</span></span>
<span data-ttu-id="64d09-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64d09-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d09-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d09-152">-WhatIf</span></span>
<span data-ttu-id="64d09-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64d09-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d09-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64d09-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d09-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d09-155">CommonParameters</span></span>
<span data-ttu-id="64d09-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d09-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d09-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64d09-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d09-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64d09-158">INPUTS</span></span>

### <span data-ttu-id="64d09-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="64d09-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="64d09-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64d09-160">OUTPUTS</span></span>

### <span data-ttu-id="64d09-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="64d09-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="64d09-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64d09-162">NOTES</span></span>

<span data-ttu-id="64d09-163">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="64d09-163">ALIASES</span></span>

<span data-ttu-id="64d09-164">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="64d09-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64d09-165">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="64d09-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64d09-166">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64d09-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64d09-167">ENDPOINTDESCRIPTION: <IDigitalTwinsEndpointResource> DigitalTwinsInstance endpoint resource.</span><span class="sxs-lookup"><span data-stu-id="64d09-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="64d09-168">`EndpointType <EndpointType>`: A Digitális végpont típusa</span><span class="sxs-lookup"><span data-stu-id="64d09-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="64d09-169">`[DeadLetterSecret <String>]`: Elhalt levél tárolási titka.</span><span class="sxs-lookup"><span data-stu-id="64d09-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="64d09-170">Olvasottságkor el lesz havazva.</span><span class="sxs-lookup"><span data-stu-id="64d09-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="64d09-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64d09-171">RELATED LINKS</span></span>

