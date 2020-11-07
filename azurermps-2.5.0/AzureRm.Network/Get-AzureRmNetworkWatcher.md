---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850698"
---
# <span data-ttu-id="f2cfc-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfc-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="f2cfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cfc-103">A Hálózatfigyelő tulajdonságait kapja meg</span><span class="sxs-lookup"><span data-stu-id="f2cfc-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2cfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2cfc-104">SYNTAX</span></span>

### <span data-ttu-id="f2cfc-105">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2cfc-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2cfc-106">Lista</span><span class="sxs-lookup"><span data-stu-id="f2cfc-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2cfc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2cfc-107">DESCRIPTION</span></span>
<span data-ttu-id="f2cfc-108">A Get-AzureRmNetworkWatcher parancsmag egy vagy több Azure Network Watcher-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="f2cfc-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="f2cfc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2cfc-109">EXAMPLES</span></span>

### <span data-ttu-id="f2cfc-110">--------------------------Példa 1: hálózati figyelő beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="f2cfc-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="f2cfc-111">A NetworkWatcher_westcentralus nevű Hálózatfigyelőt kapja az erőforráscsoport NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="f2cfc-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="f2cfc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2cfc-112">PARAMETERS</span></span>

### <span data-ttu-id="f2cfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cfc-113">-DefaultProfile</span></span>
<span data-ttu-id="f2cfc-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2cfc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2cfc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2cfc-115">-Name</span></span>
<span data-ttu-id="f2cfc-116">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfc-116">The network watcher name.</span></span>

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

### <span data-ttu-id="f2cfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2cfc-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfc-118">The resource group name.</span></span>

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

### <span data-ttu-id="f2cfc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cfc-119">CommonParameters</span></span>
<span data-ttu-id="f2cfc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2cfc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cfc-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cfc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cfc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2cfc-122">INPUTS</span></span>

### <span data-ttu-id="f2cfc-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="f2cfc-123">None</span></span>

## <span data-ttu-id="f2cfc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2cfc-124">OUTPUTS</span></span>

### <span data-ttu-id="f2cfc-125">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfc-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="f2cfc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2cfc-126">NOTES</span></span>
<span data-ttu-id="f2cfc-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="f2cfc-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="f2cfc-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2cfc-128">RELATED LINKS</span></span>

[<span data-ttu-id="f2cfc-129">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfc-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f2cfc-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfc-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f2cfc-131">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfc-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfc-132">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f2cfc-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f2cfc-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfc-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfc-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfc-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfc-135">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfc-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfc-136">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f2cfc-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f2cfc-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f2cfc-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f2cfc-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f2cfc-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f2cfc-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f2cfc-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f2cfc-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f2cfc-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
