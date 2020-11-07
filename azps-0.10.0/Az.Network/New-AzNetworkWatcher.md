---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841297"
---
# <span data-ttu-id="4975f-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4975f-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="4975f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4975f-102">SYNOPSIS</span></span>
<span data-ttu-id="4975f-103">Új Hálózatfigyelő-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4975f-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="4975f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4975f-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4975f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4975f-105">DESCRIPTION</span></span>
<span data-ttu-id="4975f-106">Az New-AzNetworkWatcher parancsmag új Hálózatfigyelő-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4975f-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="4975f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4975f-107">EXAMPLES</span></span>

### <span data-ttu-id="4975f-108">Példa 1: Hálózatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="4975f-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="4975f-109">Ebben a példában egy új hálózati figyelőt hoz létre egy újonnan létrehozott erőforráscsoport belsejében.</span><span class="sxs-lookup"><span data-stu-id="4975f-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="4975f-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="4975f-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="4975f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4975f-111">PARAMETERS</span></span>

### <span data-ttu-id="4975f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4975f-112">-DefaultProfile</span></span>
<span data-ttu-id="4975f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4975f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4975f-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="4975f-114">-Location</span></span>
<span data-ttu-id="4975f-115">Helyre.</span><span class="sxs-lookup"><span data-stu-id="4975f-115">Location.</span></span>

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

### <span data-ttu-id="4975f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4975f-116">-Name</span></span>
<span data-ttu-id="4975f-117">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="4975f-117">The network watcher name.</span></span>

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

### <span data-ttu-id="4975f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4975f-118">-ResourceGroupName</span></span>
<span data-ttu-id="4975f-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4975f-119">The resource group name.</span></span>

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

### <span data-ttu-id="4975f-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="4975f-120">-Tag</span></span>
<span data-ttu-id="4975f-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4975f-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4975f-122">Példa:</span><span class="sxs-lookup"><span data-stu-id="4975f-122">For example:</span></span>

<span data-ttu-id="4975f-123">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="4975f-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4975f-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4975f-124">-Confirm</span></span>
<span data-ttu-id="4975f-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4975f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4975f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4975f-126">-WhatIf</span></span>
<span data-ttu-id="4975f-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4975f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4975f-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4975f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4975f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4975f-129">CommonParameters</span></span>
<span data-ttu-id="4975f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4975f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4975f-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4975f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4975f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4975f-132">INPUTS</span></span>

### <span data-ttu-id="4975f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4975f-133">System.String</span></span>
<span data-ttu-id="4975f-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4975f-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4975f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4975f-135">OUTPUTS</span></span>

### <span data-ttu-id="4975f-136">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4975f-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="4975f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4975f-137">NOTES</span></span>
<span data-ttu-id="4975f-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="4975f-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="4975f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4975f-139">RELATED LINKS</span></span>

[<span data-ttu-id="4975f-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4975f-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4975f-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4975f-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4975f-142">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4975f-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4975f-143">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4975f-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4975f-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4975f-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4975f-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4975f-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4975f-146">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4975f-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4975f-147">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4975f-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4975f-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4975f-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4975f-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4975f-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4975f-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4975f-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4975f-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4975f-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
