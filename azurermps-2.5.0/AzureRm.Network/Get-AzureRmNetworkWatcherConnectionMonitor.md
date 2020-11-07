---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848782"
---
# <span data-ttu-id="df088-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df088-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="df088-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df088-102">SYNOPSIS</span></span>
<span data-ttu-id="df088-103">A megadott névvel vagy a kapcsolati figyelőket tartalmazó kapcsolat monitorát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="df088-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df088-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df088-104">SYNTAX</span></span>

### <span data-ttu-id="df088-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df088-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="df088-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="df088-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="df088-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="df088-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="df088-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="df088-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="df088-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="df088-109">DESCRIPTION</span></span>
<span data-ttu-id="df088-110">A Get-AzureRmNetworkWatcherConnectionMonitor parancsmag a megadott nevű vagy resourceId, illetve a megadott Hálózatfigyelő vagy-helynek megfelelő kapcsolati monitorokat tartalmazó kapcsolati monitort adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="df088-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="df088-111">Példák</span><span class="sxs-lookup"><span data-stu-id="df088-111">EXAMPLES</span></span>

### <span data-ttu-id="df088-112">---------------Példa 1: a kapcsolat figyelésének beszerzése név szerint a megadott helyen---------------</span><span class="sxs-lookup"><span data-stu-id="df088-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
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

<span data-ttu-id="df088-113">Ebben a példában a kapcsolat monitort a megadott helyen, név szerint szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="df088-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="df088-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df088-114">PARAMETERS</span></span>

### <span data-ttu-id="df088-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df088-115">-AsJob</span></span>
<span data-ttu-id="df088-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="df088-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df088-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df088-117">-DefaultProfile</span></span>
<span data-ttu-id="df088-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df088-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df088-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="df088-119">-Location</span></span>
<span data-ttu-id="df088-120">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="df088-120">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df088-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df088-121">-Name</span></span>
<span data-ttu-id="df088-122">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="df088-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df088-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df088-123">-NetworkWatcher</span></span>
<span data-ttu-id="df088-124">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="df088-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="df088-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="df088-125">-NetworkWatcherName</span></span>
<span data-ttu-id="df088-126">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="df088-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df088-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df088-127">-ResourceGroupName</span></span>
<span data-ttu-id="df088-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df088-128">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df088-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df088-129">-ResourceId</span></span>
<span data-ttu-id="df088-130">A kapcsolat figyelője erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df088-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="df088-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df088-131">CommonParameters</span></span>
<span data-ttu-id="df088-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df088-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df088-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df088-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df088-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df088-134">INPUTS</span></span>

### <span data-ttu-id="df088-135">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df088-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="df088-136">System. String</span><span class="sxs-lookup"><span data-stu-id="df088-136">System.String</span></span>


## <span data-ttu-id="df088-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df088-137">OUTPUTS</span></span>

### <span data-ttu-id="df088-138">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="df088-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="df088-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df088-139">NOTES</span></span>
<span data-ttu-id="df088-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="df088-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="df088-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df088-141">RELATED LINKS</span></span>
<span data-ttu-id="df088-142">[Új – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="df088-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="df088-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="df088-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="df088-144">[Új – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Új – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="df088-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="df088-145">[Új – AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="df088-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
