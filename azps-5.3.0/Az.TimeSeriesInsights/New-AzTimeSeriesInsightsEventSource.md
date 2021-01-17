---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467065"
---
# <span data-ttu-id="1c574-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="1c574-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="1c574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c574-102">SYNOPSIS</span></span>
<span data-ttu-id="1c574-103">Hozzon létre egy eseményforrást a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="1c574-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="1c574-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c574-104">SYNTAX</span></span>

### <span data-ttu-id="1c574-105">eventhub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c574-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c574-106">iothub</span><span class="sxs-lookup"><span data-stu-id="1c574-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c574-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c574-107">DESCRIPTION</span></span>
<span data-ttu-id="1c574-108">Hozzon létre egy eseményforrást a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="1c574-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="1c574-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c574-109">EXAMPLES</span></span>

### <span data-ttu-id="1c574-110">1. példa: Eseményhub eseményforrás létrehozása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="1c574-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="1c574-111">Ez a parancs eseményhub eseményforrást hoz létre a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="1c574-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="1c574-112">2. példa: iothub eseményforrás létrehozása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="1c574-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="1c574-113">Ez a parancs egy iothub eseményforrást hoz létre a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="1c574-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="1c574-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c574-114">PARAMETERS</span></span>

### <span data-ttu-id="1c574-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="1c574-115">-ConsumerGroupName</span></span>
<span data-ttu-id="1c574-116">Az esemény/iot-központ fogyasztói csoportjának neve, amely tartalmazza az eseményeket olvasott partíciókat.</span><span class="sxs-lookup"><span data-stu-id="1c574-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="1c574-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c574-117">-DefaultProfile</span></span>
<span data-ttu-id="1c574-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c574-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c574-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1c574-119">-EnvironmentName</span></span>
<span data-ttu-id="1c574-120">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="1c574-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1c574-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1c574-121">-EventHubName</span></span>
<span data-ttu-id="1c574-122">Az eseményközpont neve.</span><span class="sxs-lookup"><span data-stu-id="1c574-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1c574-123">-EventSourceResourceId</span></span>
<span data-ttu-id="1c574-124">Az Azure Resource Manager eseményforrásának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c574-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="1c574-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="1c574-125">-IoTHubName</span></span>
<span data-ttu-id="1c574-126">Az iot-központ neve.</span><span class="sxs-lookup"><span data-stu-id="1c574-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1c574-127">-KeyName</span></span>
<span data-ttu-id="1c574-128">Annak az SAS-kulcsnak a neve, amely hozzáférést biztosít a Time Series Insights szolgáltatásnak az eseményhez/iot-központhoz.</span><span class="sxs-lookup"><span data-stu-id="1c574-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="1c574-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="1c574-129">-Kind</span></span>
<span data-ttu-id="1c574-130">Az eseményforrás fajtája.</span><span class="sxs-lookup"><span data-stu-id="1c574-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-131">-Location</span><span class="sxs-lookup"><span data-stu-id="1c574-131">-Location</span></span>
<span data-ttu-id="1c574-132">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1c574-132">The location of the resource.</span></span>

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

### <span data-ttu-id="1c574-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1c574-133">-Name</span></span>
<span data-ttu-id="1c574-134">Az eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1c574-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c574-135">-ResourceGroupName</span></span>
<span data-ttu-id="1c574-136">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c574-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1c574-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="1c574-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="1c574-138">Az eseményközpontot tartalmazó szolgáltatásbusz neve.</span><span class="sxs-lookup"><span data-stu-id="1c574-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="1c574-139">-SharedAccessKey</span></span>
<span data-ttu-id="1c574-140">Annak a megosztott hozzáférési kulcsnak az értéke, amely olvasási hozzáférést biztosít a Time Series Insights szolgáltatásnak az eseményhez/iot-központhoz.</span><span class="sxs-lookup"><span data-stu-id="1c574-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c574-141">-SubscriptionId</span></span>
<span data-ttu-id="1c574-142">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c574-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1c574-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c574-143">-Tag</span></span>
<span data-ttu-id="1c574-144">Key-value pairs of additional properties for the resource.</span><span class="sxs-lookup"><span data-stu-id="1c574-144">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c574-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="1c574-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="1c574-146">Az eseményforrás időbélyegeként használt eseménytulajdonság.</span><span class="sxs-lookup"><span data-stu-id="1c574-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="1c574-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c574-147">-Confirm</span></span>
<span data-ttu-id="1c574-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1c574-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c574-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c574-149">-WhatIf</span></span>
<span data-ttu-id="1c574-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1c574-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c574-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c574-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c574-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c574-152">CommonParameters</span></span>
<span data-ttu-id="1c574-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c574-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c574-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c574-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c574-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c574-155">INPUTS</span></span>

## <span data-ttu-id="1c574-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c574-156">OUTPUTS</span></span>

### <span data-ttu-id="1c574-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="1c574-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="1c574-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c574-158">NOTES</span></span>

<span data-ttu-id="1c574-159">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1c574-159">ALIASES</span></span>

## <span data-ttu-id="1c574-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c574-160">RELATED LINKS</span></span>

