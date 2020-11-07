---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 10582a0e81fdb9c86902c7a2580ad31fe84f3bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679890"
---
# <span data-ttu-id="82ed8-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82ed8-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="82ed8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="82ed8-103">A kapcsolat figyelésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="82ed8-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ed8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82ed8-104">SYNTAX</span></span>

### <span data-ttu-id="82ed8-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82ed8-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82ed8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="82ed8-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ed8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="82ed8-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ed8-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="82ed8-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ed8-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="82ed8-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ed8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="82ed8-110">DESCRIPTION</span></span>
<span data-ttu-id="82ed8-111">A Remove-AzureRmNetworkWatcherConnectionMonitor parancsmag eltávolítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="82ed8-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="82ed8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="82ed8-112">EXAMPLES</span></span>

### <span data-ttu-id="82ed8-113">1. példa: a megadott kapcsolati monitor eltávolítása</span><span class="sxs-lookup"><span data-stu-id="82ed8-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="82ed8-114">Ebben a példában töröljük a kapcsolat monitor helyét és nevét.</span><span class="sxs-lookup"><span data-stu-id="82ed8-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="82ed8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82ed8-115">PARAMETERS</span></span>

### <span data-ttu-id="82ed8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82ed8-116">-AsJob</span></span>
<span data-ttu-id="82ed8-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="82ed8-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ed8-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82ed8-118">-Confirm</span></span>
<span data-ttu-id="82ed8-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82ed8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ed8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ed8-120">-DefaultProfile</span></span>
<span data-ttu-id="82ed8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82ed8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82ed8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82ed8-122">-InputObject</span></span>
<span data-ttu-id="82ed8-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="82ed8-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ed8-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="82ed8-124">-Location</span></span>
<span data-ttu-id="82ed8-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="82ed8-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="82ed8-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82ed8-126">-Name</span></span>
<span data-ttu-id="82ed8-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="82ed8-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ed8-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ed8-128">-NetworkWatcher</span></span>
<span data-ttu-id="82ed8-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="82ed8-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="82ed8-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="82ed8-130">-NetworkWatcherName</span></span>
<span data-ttu-id="82ed8-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="82ed8-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="82ed8-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82ed8-132">-PassThru</span></span>
<span data-ttu-id="82ed8-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="82ed8-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ed8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ed8-134">-ResourceGroupName</span></span>
<span data-ttu-id="82ed8-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="82ed8-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="82ed8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ed8-136">-ResourceId</span></span>
<span data-ttu-id="82ed8-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="82ed8-137">Resource ID.</span></span>

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

### <span data-ttu-id="82ed8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ed8-138">-WhatIf</span></span>
<span data-ttu-id="82ed8-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82ed8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ed8-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82ed8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ed8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ed8-141">CommonParameters</span></span>
<span data-ttu-id="82ed8-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82ed8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="82ed8-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ed8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ed8-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ed8-144">INPUTS</span></span>

### <span data-ttu-id="82ed8-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ed8-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="82ed8-146">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="82ed8-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="82ed8-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ed8-147">OUTPUTS</span></span>

### <span data-ttu-id="82ed8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82ed8-148">System.Boolean</span></span>

## <span data-ttu-id="82ed8-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82ed8-149">NOTES</span></span>
<span data-ttu-id="82ed8-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="82ed8-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="82ed8-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82ed8-151">RELATED LINKS</span></span>

[<span data-ttu-id="82ed8-152">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ed8-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="82ed8-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ed8-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="82ed8-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ed8-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="82ed8-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="82ed8-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="82ed8-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="82ed8-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="82ed8-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="82ed8-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="82ed8-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="82ed8-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="82ed8-159">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ed8-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="82ed8-160">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="82ed8-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="82ed8-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ed8-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="82ed8-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ed8-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="82ed8-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ed8-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="82ed8-164">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82ed8-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="82ed8-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82ed8-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="82ed8-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="82ed8-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

