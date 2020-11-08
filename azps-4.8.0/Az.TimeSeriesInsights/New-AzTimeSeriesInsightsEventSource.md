---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182473"
---
# <span data-ttu-id="c57f9-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="c57f9-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="c57f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c57f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c57f9-103">Eseményforrás létrehozása a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c57f9-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="c57f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c57f9-104">SYNTAX</span></span>

### <span data-ttu-id="c57f9-105">eventhub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c57f9-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c57f9-106">iothub</span><span class="sxs-lookup"><span data-stu-id="c57f9-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c57f9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c57f9-107">DESCRIPTION</span></span>
<span data-ttu-id="c57f9-108">Eseményforrás létrehozása a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c57f9-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="c57f9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c57f9-109">EXAMPLES</span></span>

### <span data-ttu-id="c57f9-110">1. példa: eventhub-eseményforrás létrehozása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="c57f9-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="c57f9-111">A parancs létrehoz egy eventhub-eseményforrás a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c57f9-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="c57f9-112">2. példa: iothub-eseményforrás létrehozása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="c57f9-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="c57f9-113">A parancs létrehoz egy iothub-eseményforrás a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c57f9-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="c57f9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c57f9-114">PARAMETERS</span></span>

### <span data-ttu-id="c57f9-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c57f9-115">-ConsumerGroupName</span></span>
<span data-ttu-id="c57f9-116">Az esemény/IOT hub fogyasztói csoportjának neve, amely azokat a partíciókat tárolja, amelyekből az események olvashatók lesznek.</span><span class="sxs-lookup"><span data-stu-id="c57f9-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="c57f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57f9-117">-DefaultProfile</span></span>
<span data-ttu-id="c57f9-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c57f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c57f9-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="c57f9-119">-EnvironmentName</span></span>
<span data-ttu-id="c57f9-120">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="c57f9-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="c57f9-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="c57f9-121">-EventHubName</span></span>
<span data-ttu-id="c57f9-122">Az esemény központja neve.</span><span class="sxs-lookup"><span data-stu-id="c57f9-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="c57f9-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="c57f9-123">-EventSourceResourceId</span></span>
<span data-ttu-id="c57f9-124">Az eseményforrás erőforrás-azonosítója az Azure Resource Managerben.</span><span class="sxs-lookup"><span data-stu-id="c57f9-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="c57f9-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="c57f9-125">-IoTHubName</span></span>
<span data-ttu-id="c57f9-126">Az IOT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="c57f9-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="c57f9-127">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="c57f9-127">-KeyName</span></span>
<span data-ttu-id="c57f9-128">Annak a SAS-kulcsnak a neve, amely az idősorozat-betekintést adja az esemény/IOT-központ eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="c57f9-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="c57f9-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="c57f9-129">-Kind</span></span>
<span data-ttu-id="c57f9-130">Az eseményforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="c57f9-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="c57f9-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="c57f9-131">-Location</span></span>
<span data-ttu-id="c57f9-132">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c57f9-132">The location of the resource.</span></span>

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

### <span data-ttu-id="c57f9-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c57f9-133">-Name</span></span>
<span data-ttu-id="c57f9-134">Az eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c57f9-134">Name of the event source.</span></span>

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

### <span data-ttu-id="c57f9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57f9-135">-ResourceGroupName</span></span>
<span data-ttu-id="c57f9-136">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c57f9-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c57f9-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="c57f9-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="c57f9-138">Annak a buszjáratnak a neve, amely az esemény hub-ot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c57f9-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="c57f9-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="c57f9-139">-SharedAccessKey</span></span>
<span data-ttu-id="c57f9-140">Az idősoros elemzést támogató megosztott hozzáférési kulcs értéke az esemény/IOT hub olvasási jogosultságával.</span><span class="sxs-lookup"><span data-stu-id="c57f9-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="c57f9-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c57f9-141">-SubscriptionId</span></span>
<span data-ttu-id="c57f9-142">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="c57f9-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c57f9-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="c57f9-143">-Tag</span></span>
<span data-ttu-id="c57f9-144">Az erőforrás további tulajdonságainak kulcs-érték párjai</span><span class="sxs-lookup"><span data-stu-id="c57f9-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="c57f9-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="c57f9-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="c57f9-146">Az esemény-tulajdonság, amelyet az eseményforrás időbélyegzőként fog használni.</span><span class="sxs-lookup"><span data-stu-id="c57f9-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="c57f9-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c57f9-147">-Confirm</span></span>
<span data-ttu-id="c57f9-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c57f9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57f9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57f9-149">-WhatIf</span></span>
<span data-ttu-id="c57f9-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c57f9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c57f9-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c57f9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57f9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57f9-152">CommonParameters</span></span>
<span data-ttu-id="c57f9-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c57f9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57f9-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c57f9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57f9-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c57f9-155">INPUTS</span></span>

## <span data-ttu-id="c57f9-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c57f9-156">OUTPUTS</span></span>

### <span data-ttu-id="c57f9-157">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="c57f9-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="c57f9-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c57f9-158">NOTES</span></span>

<span data-ttu-id="c57f9-159">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c57f9-159">ALIASES</span></span>

## <span data-ttu-id="c57f9-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c57f9-160">RELATED LINKS</span></span>

