---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013312"
---
# <span data-ttu-id="62f1e-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62f1e-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="62f1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="62f1e-103">A megadott névvel vagy a kapcsolati figyelőket tartalmazó kapcsolat monitorát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="62f1e-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="62f1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62f1e-104">SYNTAX</span></span>

### <span data-ttu-id="62f1e-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62f1e-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62f1e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="62f1e-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62f1e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="62f1e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62f1e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="62f1e-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62f1e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="62f1e-109">DESCRIPTION</span></span>
<span data-ttu-id="62f1e-110">A Get-AzNetworkWatcherConnectionMonitor parancsmag a megadott nevű vagy resourceId, illetve a megadott Hálózatfigyelő vagy-helynek megfelelő kapcsolati monitorokat tartalmazó kapcsolati monitort adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="62f1e-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="62f1e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="62f1e-111">EXAMPLES</span></span>

### <span data-ttu-id="62f1e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="62f1e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="62f1e-113">Név: KK-azonosító:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm ETAG: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: a következő forrás: {"ResourceId": "/Subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/Providers/Microsoft. C ompute/virtualMachines/irinavm"; "Port": 0} cél: {"cím": "google.com"; "Port": 80} MonitoringIntervalInSeconds: 60 autostart: true kezdő időpont: 1/12/2018 7:19:28 PM MonitoringStatus: "centraluseuap": networkWatchers Type: Microsoft. Network/ConnectionMonitors</span><span class="sxs-lookup"><span data-stu-id="62f1e-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="62f1e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62f1e-114">PARAMETERS</span></span>

### <span data-ttu-id="62f1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f1e-115">-DefaultProfile</span></span>
<span data-ttu-id="62f1e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62f1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62f1e-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="62f1e-117">-Location</span></span>
<span data-ttu-id="62f1e-118">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="62f1e-118">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62f1e-119">-Name</span></span>
<span data-ttu-id="62f1e-120">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="62f1e-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f1e-121">-NetworkWatcher</span></span>
<span data-ttu-id="62f1e-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="62f1e-122">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="62f1e-123">-NetworkWatcherName</span></span>
<span data-ttu-id="62f1e-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="62f1e-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="62f1e-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="62f1e-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62f1e-127">-ResourceId</span></span>
<span data-ttu-id="62f1e-128">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="62f1e-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f1e-129">CommonParameters</span></span>
<span data-ttu-id="62f1e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62f1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f1e-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62f1e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f1e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f1e-132">INPUTS</span></span>

### <span data-ttu-id="62f1e-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f1e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="62f1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="62f1e-134">System.String</span></span>

## <span data-ttu-id="62f1e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f1e-135">OUTPUTS</span></span>

### <span data-ttu-id="62f1e-136">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="62f1e-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="62f1e-137">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="62f1e-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="62f1e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62f1e-138">NOTES</span></span>

## <span data-ttu-id="62f1e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62f1e-139">RELATED LINKS</span></span>
