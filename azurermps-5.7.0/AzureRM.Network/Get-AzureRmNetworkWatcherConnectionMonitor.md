---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493761"
---
# <span data-ttu-id="ffe87-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ffe87-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ffe87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffe87-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe87-103">A megadott névvel vagy a kapcsolati figyelőket tartalmazó kapcsolat monitorát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ffe87-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffe87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffe87-104">SYNTAX</span></span>

### <span data-ttu-id="ffe87-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ffe87-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe87-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ffe87-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe87-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ffe87-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe87-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffe87-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffe87-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffe87-109">DESCRIPTION</span></span>
<span data-ttu-id="ffe87-110">A Get-AzureRmNetworkWatcherConnectionMonitor parancsmag a megadott nevű vagy resourceId, illetve a megadott Hálózatfigyelő vagy-helynek megfelelő kapcsolati monitorokat tartalmazó kapcsolati monitort adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ffe87-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="ffe87-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ffe87-111">EXAMPLES</span></span>

### <span data-ttu-id="ffe87-112">Példa 1: a kapcsolat monitorjának beszerzése név szerint a megadott helyen</span><span class="sxs-lookup"><span data-stu-id="ffe87-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="ffe87-113">Ebben a példában a kapcsolat monitort a megadott helyen, név szerint szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="ffe87-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="ffe87-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffe87-114">PARAMETERS</span></span>

### <span data-ttu-id="ffe87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe87-115">-DefaultProfile</span></span>
<span data-ttu-id="ffe87-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffe87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="ffe87-117">-Location</span></span>
<span data-ttu-id="ffe87-118">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="ffe87-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffe87-119">-Name</span></span>
<span data-ttu-id="ffe87-120">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="ffe87-120">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ffe87-121">-NetworkWatcher</span></span>
<span data-ttu-id="ffe87-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ffe87-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ffe87-123">-NetworkWatcherName</span></span>
<span data-ttu-id="ffe87-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ffe87-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe87-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffe87-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ffe87-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffe87-127">-ResourceId</span></span>
<span data-ttu-id="ffe87-128">A kapcsolat figyelője erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ffe87-128">Resource ID of the connection monitor.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe87-129">CommonParameters</span></span>
<span data-ttu-id="ffe87-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffe87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ffe87-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe87-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe87-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe87-132">INPUTS</span></span>

### <span data-ttu-id="ffe87-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ffe87-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ffe87-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ffe87-134">System.String</span></span>

## <span data-ttu-id="ffe87-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe87-135">OUTPUTS</span></span>

### <span data-ttu-id="ffe87-136">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ffe87-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ffe87-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffe87-137">NOTES</span></span>
<span data-ttu-id="ffe87-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="ffe87-138">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ffe87-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffe87-139">RELATED LINKS</span></span>

[<span data-ttu-id="ffe87-140">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ffe87-140">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ffe87-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ffe87-141">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ffe87-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ffe87-142">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ffe87-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ffe87-143">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="ffe87-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ffe87-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="ffe87-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ffe87-145">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="ffe87-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ffe87-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="ffe87-147">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ffe87-147">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ffe87-148">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ffe87-148">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="ffe87-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ffe87-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ffe87-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ffe87-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ffe87-151">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ffe87-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ffe87-152">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ffe87-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ffe87-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ffe87-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="ffe87-154">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ffe87-154">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ffe87-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ffe87-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ffe87-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ffe87-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ffe87-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ffe87-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
