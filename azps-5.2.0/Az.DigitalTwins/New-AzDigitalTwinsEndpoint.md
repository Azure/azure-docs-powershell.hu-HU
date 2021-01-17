---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347009"
---
# <span data-ttu-id="cd502-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd502-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="cd502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd502-102">SYNOPSIS</span></span>
<span data-ttu-id="cd502-103">DigitalTwinsInstance végpont létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="cd502-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="cd502-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd502-104">SYNTAX</span></span>

### <span data-ttu-id="cd502-105">EventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd502-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd502-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd502-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd502-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd502-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd502-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd502-108">DESCRIPTION</span></span>
<span data-ttu-id="cd502-109">DigitalTwinsInstance végpont létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="cd502-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="cd502-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd502-110">EXAMPLES</span></span>

### <span data-ttu-id="cd502-111">1. példa: AzDigitalTwinsEndpoint létrehozása az Eventhubhoz</span><span class="sxs-lookup"><span data-stu-id="cd502-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="cd502-112">AzDigitalTwinsEndpoint for Eventhub létrehozása a connectionStringPrimaryKey segítségével</span><span class="sxs-lookup"><span data-stu-id="cd502-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="cd502-113">2. példa: AzDigitalTwinsEndpoint létrehozása az EventGrid számára</span><span class="sxs-lookup"><span data-stu-id="cd502-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="cd502-114">Az AzDigitalTwinsEndpoint létrehozása az Eventhubhoz a TopicEndpoint és az accessKey1 segítségével</span><span class="sxs-lookup"><span data-stu-id="cd502-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="cd502-115">3. példa: AzDigitalTwinsEndpoint for ServiceBus létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd502-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="cd502-116">AzDigitalTwinsEndpoint for ServicBus létrehozása a PrimaryConnectionString szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="cd502-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="cd502-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd502-117">PARAMETERS</span></span>

### <span data-ttu-id="cd502-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="cd502-118">-AccessKey1</span></span>
<span data-ttu-id="cd502-119">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd502-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="cd502-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd502-120">-AsJob</span></span>
<span data-ttu-id="cd502-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="cd502-121">Run the command as a job</span></span>

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

### <span data-ttu-id="cd502-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cd502-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="cd502-123">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd502-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="cd502-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cd502-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="cd502-125">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd502-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="cd502-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="cd502-126">-DeadLetterSecret</span></span>
<span data-ttu-id="cd502-127">Elhalt levél tárolási titka.</span><span class="sxs-lookup"><span data-stu-id="cd502-127">Dead letter storage secret.</span></span>
<span data-ttu-id="cd502-128">Olvasottságkor el lesz havazva.</span><span class="sxs-lookup"><span data-stu-id="cd502-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="cd502-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd502-129">-DefaultProfile</span></span>
<span data-ttu-id="cd502-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd502-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd502-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="cd502-131">-EndpointDescription</span></span>
<span data-ttu-id="cd502-132">DigitalTwinsInstance végpontforrás.</span><span class="sxs-lookup"><span data-stu-id="cd502-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="cd502-133">Ennek létrehozásáról az ENDPOINTDESCRIPTION tulajdonságokat ismertető MEGJEGYZÉSEK című szakaszban és egy kivonattáblát hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="cd502-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd502-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cd502-134">-EndpointName</span></span>
<span data-ttu-id="cd502-135">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cd502-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="cd502-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cd502-136">-EndpointType</span></span>
<span data-ttu-id="cd502-137">A Digitális végpont típusa</span><span class="sxs-lookup"><span data-stu-id="cd502-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="cd502-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd502-138">-NoWait</span></span>
<span data-ttu-id="cd502-139">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="cd502-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd502-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="cd502-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="cd502-141">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd502-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="cd502-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd502-142">-ResourceGroupName</span></span>
<span data-ttu-id="cd502-143">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd502-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="cd502-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cd502-144">-ResourceName</span></span>
<span data-ttu-id="cd502-145">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="cd502-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="cd502-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd502-146">-SubscriptionId</span></span>
<span data-ttu-id="cd502-147">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd502-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="cd502-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd502-148">-TopicEndpoint</span></span>
<span data-ttu-id="cd502-149">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd502-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="cd502-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd502-150">-Confirm</span></span>
<span data-ttu-id="cd502-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd502-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd502-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd502-152">-WhatIf</span></span>
<span data-ttu-id="cd502-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd502-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd502-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd502-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd502-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd502-155">CommonParameters</span></span>
<span data-ttu-id="cd502-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd502-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd502-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd502-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd502-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd502-158">INPUTS</span></span>

### <span data-ttu-id="cd502-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="cd502-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="cd502-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd502-160">OUTPUTS</span></span>

### <span data-ttu-id="cd502-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="cd502-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="cd502-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd502-162">NOTES</span></span>

<span data-ttu-id="cd502-163">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cd502-163">ALIASES</span></span>

<span data-ttu-id="cd502-164">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="cd502-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd502-165">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cd502-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd502-166">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd502-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd502-167">ENDPOINTDESCRIPTION: <IDigitalTwinsEndpointResource> DigitalTwinsInstance végpontforrás.</span><span class="sxs-lookup"><span data-stu-id="cd502-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="cd502-168">`EndpointType <EndpointType>`: A Digitális végpont típusa</span><span class="sxs-lookup"><span data-stu-id="cd502-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="cd502-169">`[DeadLetterSecret <String>]`: Elhalt levél tárolási titka.</span><span class="sxs-lookup"><span data-stu-id="cd502-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="cd502-170">Olvasottságkor el lesz havazva.</span><span class="sxs-lookup"><span data-stu-id="cd502-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="cd502-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd502-171">RELATED LINKS</span></span>

