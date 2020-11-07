---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: b096c87e588c48b609fe0a55be7344b39df98c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849581"
---
# <span data-ttu-id="68e05-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68e05-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="68e05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68e05-102">SYNOPSIS</span></span>
<span data-ttu-id="68e05-103">Új Hálózatfigyelő-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="68e05-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68e05-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68e05-105">DESCRIPTION</span></span>
<span data-ttu-id="68e05-106">Az New-AzureRmNetworkWatcher parancsmag új Hálózatfigyelő-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="68e05-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="68e05-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68e05-107">EXAMPLES</span></span>

### <span data-ttu-id="68e05-108">Példa 1: Hálózatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="68e05-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="68e05-109">Ebben a példában egy új hálózati figyelőt hoz létre egy újonnan létrehozott erőforráscsoport belsejében.</span><span class="sxs-lookup"><span data-stu-id="68e05-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="68e05-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="68e05-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="68e05-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68e05-111">PARAMETERS</span></span>

### <span data-ttu-id="68e05-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e05-112">-DefaultProfile</span></span>
<span data-ttu-id="68e05-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68e05-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68e05-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="68e05-114">-Location</span></span>
<span data-ttu-id="68e05-115">Helyre.</span><span class="sxs-lookup"><span data-stu-id="68e05-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e05-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68e05-116">-Name</span></span>
<span data-ttu-id="68e05-117">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="68e05-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e05-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e05-118">-ResourceGroupName</span></span>
<span data-ttu-id="68e05-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="68e05-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e05-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="68e05-120">-Tag</span></span>
<span data-ttu-id="68e05-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="68e05-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="68e05-122">Példa:</span><span class="sxs-lookup"><span data-stu-id="68e05-122">For example:</span></span>

<span data-ttu-id="68e05-123">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="68e05-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e05-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68e05-124">-Confirm</span></span>
<span data-ttu-id="68e05-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68e05-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e05-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e05-126">-WhatIf</span></span>
<span data-ttu-id="68e05-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68e05-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e05-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68e05-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e05-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e05-129">CommonParameters</span></span>
<span data-ttu-id="68e05-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68e05-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e05-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e05-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e05-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68e05-132">INPUTS</span></span>

### <span data-ttu-id="68e05-133">System. String</span><span class="sxs-lookup"><span data-stu-id="68e05-133">System.String</span></span>
<span data-ttu-id="68e05-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="68e05-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="68e05-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68e05-135">OUTPUTS</span></span>

### <span data-ttu-id="68e05-136">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68e05-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="68e05-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68e05-137">NOTES</span></span>
<span data-ttu-id="68e05-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="68e05-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="68e05-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68e05-139">RELATED LINKS</span></span>

[<span data-ttu-id="68e05-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68e05-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="68e05-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68e05-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="68e05-142">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68e05-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68e05-143">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="68e05-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="68e05-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68e05-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68e05-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68e05-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68e05-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68e05-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68e05-147">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="68e05-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="68e05-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="68e05-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="68e05-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="68e05-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="68e05-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="68e05-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="68e05-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="68e05-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
