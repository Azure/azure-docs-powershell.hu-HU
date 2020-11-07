---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841593"
---
# <span data-ttu-id="0eeaf-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eeaf-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="0eeaf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0eeaf-102">SYNOPSIS</span></span>
<span data-ttu-id="0eeaf-103">A Hálózatfigyelő tulajdonságait kapja meg</span><span class="sxs-lookup"><span data-stu-id="0eeaf-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="0eeaf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0eeaf-104">SYNTAX</span></span>

### <span data-ttu-id="0eeaf-105">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0eeaf-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0eeaf-106">Lista</span><span class="sxs-lookup"><span data-stu-id="0eeaf-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eeaf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0eeaf-107">DESCRIPTION</span></span>
<span data-ttu-id="0eeaf-108">A Get-AzNetworkWatcher parancsmag egy vagy több Azure Network Watcher-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="0eeaf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0eeaf-109">EXAMPLES</span></span>

### <span data-ttu-id="0eeaf-110">--------------------------Példa 1: hálózati figyelő beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="0eeaf-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="0eeaf-111">A NetworkWatcher_westcentralus nevű Hálózatfigyelőt kapja az erőforráscsoport NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="0eeaf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-112">PARAMETERS</span></span>

### <span data-ttu-id="0eeaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eeaf-113">-DefaultProfile</span></span>
<span data-ttu-id="0eeaf-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eeaf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0eeaf-115">-Name</span></span>
<span data-ttu-id="0eeaf-116">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eeaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eeaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="0eeaf-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eeaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eeaf-119">CommonParameters</span></span>
<span data-ttu-id="0eeaf-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0eeaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eeaf-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eeaf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eeaf-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-122">INPUTS</span></span>

### <span data-ttu-id="0eeaf-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0eeaf-123">None</span></span>

## <span data-ttu-id="0eeaf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-124">OUTPUTS</span></span>

### <span data-ttu-id="0eeaf-125">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eeaf-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="0eeaf-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0eeaf-126">NOTES</span></span>
<span data-ttu-id="0eeaf-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="0eeaf-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="0eeaf-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-128">RELATED LINKS</span></span>

[<span data-ttu-id="0eeaf-129">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eeaf-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0eeaf-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eeaf-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0eeaf-131">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eeaf-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eeaf-132">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0eeaf-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0eeaf-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eeaf-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eeaf-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eeaf-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eeaf-135">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eeaf-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eeaf-136">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0eeaf-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0eeaf-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0eeaf-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0eeaf-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0eeaf-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0eeaf-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0eeaf-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0eeaf-140">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0eeaf-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
