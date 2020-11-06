---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: 10cc869bf6e0ac194ce5e2e77c69885a8e0a0d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494840"
---
# <span data-ttu-id="95988-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95988-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="95988-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95988-102">SYNOPSIS</span></span>
<span data-ttu-id="95988-103">Új Hálózatfigyelő-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="95988-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95988-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95988-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95988-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95988-105">DESCRIPTION</span></span>
<span data-ttu-id="95988-106">Az New-AzureRmNetworkWatcher parancsmag új Hálózatfigyelő-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="95988-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="95988-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95988-107">EXAMPLES</span></span>

### <span data-ttu-id="95988-108">Példa 1: Hálózatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="95988-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="95988-109">Ebben a példában egy új hálózati figyelőt hoz létre egy újonnan létrehozott erőforráscsoport belsejében.</span><span class="sxs-lookup"><span data-stu-id="95988-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="95988-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="95988-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="95988-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95988-111">PARAMETERS</span></span>

### <span data-ttu-id="95988-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="95988-112">-Location</span></span>
<span data-ttu-id="95988-113">Helyre.</span><span class="sxs-lookup"><span data-stu-id="95988-113">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95988-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95988-114">-Name</span></span>
<span data-ttu-id="95988-115">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="95988-115">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95988-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95988-116">-ResourceGroupName</span></span>
<span data-ttu-id="95988-117">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="95988-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95988-118">-Címke</span><span class="sxs-lookup"><span data-stu-id="95988-118">-Tag</span></span>
<span data-ttu-id="95988-119">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="95988-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="95988-120">Példa:</span><span class="sxs-lookup"><span data-stu-id="95988-120">For example:</span></span>

<span data-ttu-id="95988-121">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="95988-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95988-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95988-122">-Confirm</span></span>
<span data-ttu-id="95988-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95988-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95988-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95988-124">-WhatIf</span></span>
<span data-ttu-id="95988-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95988-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95988-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95988-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95988-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95988-127">-DefaultProfile</span></span>
<span data-ttu-id="95988-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95988-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95988-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95988-129">CommonParameters</span></span>
<span data-ttu-id="95988-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95988-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95988-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95988-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95988-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95988-132">INPUTS</span></span>

### <span data-ttu-id="95988-133">System. String</span><span class="sxs-lookup"><span data-stu-id="95988-133">System.String</span></span>
<span data-ttu-id="95988-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="95988-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="95988-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95988-135">OUTPUTS</span></span>

### <span data-ttu-id="95988-136">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95988-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="95988-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95988-137">NOTES</span></span>
<span data-ttu-id="95988-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="95988-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="95988-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95988-139">RELATED LINKS</span></span>

[<span data-ttu-id="95988-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95988-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="95988-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95988-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="95988-142">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95988-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95988-143">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="95988-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="95988-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95988-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95988-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95988-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95988-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95988-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95988-147">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="95988-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="95988-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="95988-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="95988-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="95988-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="95988-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="95988-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="95988-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="95988-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
