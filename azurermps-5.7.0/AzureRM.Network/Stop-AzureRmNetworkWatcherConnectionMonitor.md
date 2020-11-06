---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e49245fabd4387c48def797168e1d572a43d6bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494435"
---
# <span data-ttu-id="25baf-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25baf-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="25baf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25baf-102">SYNOPSIS</span></span>
<span data-ttu-id="25baf-103">A kapcsolat figyelésének leállítása</span><span class="sxs-lookup"><span data-stu-id="25baf-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25baf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25baf-104">SYNTAX</span></span>

### <span data-ttu-id="25baf-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25baf-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25baf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="25baf-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25baf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="25baf-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25baf-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="25baf-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25baf-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="25baf-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25baf-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="25baf-110">DESCRIPTION</span></span>
<span data-ttu-id="25baf-111">A Stop-AzureRmNetworkWatcherConnectionMonitor parancsmag leállítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="25baf-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="25baf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="25baf-112">EXAMPLES</span></span>

### <span data-ttu-id="25baf-113">Példa 1: a kapcsolat figyelésének leállítása</span><span class="sxs-lookup"><span data-stu-id="25baf-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="25baf-114">Ebben a példában a kapcsolati monitor neve és a Hálózatfigyelő beállítás van megadva</span><span class="sxs-lookup"><span data-stu-id="25baf-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="25baf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25baf-115">PARAMETERS</span></span>

### <span data-ttu-id="25baf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25baf-116">-AsJob</span></span>
<span data-ttu-id="25baf-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="25baf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25baf-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25baf-118">-Confirm</span></span>
<span data-ttu-id="25baf-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25baf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25baf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25baf-120">-DefaultProfile</span></span>
<span data-ttu-id="25baf-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25baf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25baf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25baf-122">-InputObject</span></span>
<span data-ttu-id="25baf-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="25baf-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="25baf-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="25baf-124">-Location</span></span>
<span data-ttu-id="25baf-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="25baf-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="25baf-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25baf-126">-Name</span></span>
<span data-ttu-id="25baf-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="25baf-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="25baf-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25baf-128">-NetworkWatcher</span></span>
<span data-ttu-id="25baf-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="25baf-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="25baf-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="25baf-130">-NetworkWatcherName</span></span>
<span data-ttu-id="25baf-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="25baf-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="25baf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25baf-132">-PassThru</span></span>
<span data-ttu-id="25baf-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="25baf-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="25baf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25baf-134">-ResourceGroupName</span></span>
<span data-ttu-id="25baf-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="25baf-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="25baf-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25baf-136">-ResourceId</span></span>
<span data-ttu-id="25baf-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="25baf-137">Resource ID.</span></span>

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

### <span data-ttu-id="25baf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25baf-138">-WhatIf</span></span>
<span data-ttu-id="25baf-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25baf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25baf-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25baf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25baf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25baf-141">CommonParameters</span></span>
<span data-ttu-id="25baf-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25baf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="25baf-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25baf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25baf-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25baf-144">INPUTS</span></span>

### <span data-ttu-id="25baf-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25baf-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="25baf-146">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="25baf-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="25baf-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25baf-147">OUTPUTS</span></span>

### <span data-ttu-id="25baf-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25baf-148">System.Boolean</span></span>

## <span data-ttu-id="25baf-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25baf-149">NOTES</span></span>
<span data-ttu-id="25baf-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="25baf-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="25baf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25baf-151">RELATED LINKS</span></span>

[<span data-ttu-id="25baf-152">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25baf-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="25baf-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25baf-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="25baf-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25baf-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="25baf-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="25baf-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="25baf-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="25baf-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="25baf-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="25baf-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="25baf-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="25baf-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="25baf-159">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25baf-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="25baf-160">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="25baf-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="25baf-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25baf-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="25baf-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25baf-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="25baf-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25baf-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="25baf-164">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25baf-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="25baf-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25baf-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="25baf-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="25baf-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="25baf-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25baf-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="25baf-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25baf-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="25baf-169">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25baf-169">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
