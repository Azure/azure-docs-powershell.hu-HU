---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: cf67e27a8f502a753cded74f0cb5bf48ceb2d4ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672366"
---
# <span data-ttu-id="ae99c-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae99c-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ae99c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae99c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae99c-103">Kapcsolati monitor indítása</span><span class="sxs-lookup"><span data-stu-id="ae99c-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae99c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae99c-104">SYNTAX</span></span>

### <span data-ttu-id="ae99c-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae99c-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae99c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ae99c-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae99c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ae99c-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae99c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae99c-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae99c-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ae99c-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae99c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae99c-110">DESCRIPTION</span></span>
<span data-ttu-id="ae99c-111">A Start-AzureRmNetworkWatcherConnectionMonitor parancsmag elindítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="ae99c-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="ae99c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ae99c-112">EXAMPLES</span></span>

### <span data-ttu-id="ae99c-113">1. példa: egy kapcsolat monitorjának indítása</span><span class="sxs-lookup"><span data-stu-id="ae99c-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="ae99c-114">Ebben a példában a kapcsolat monitort a név és a Hálózatfigyelő paranccsal indíthatja el.</span><span class="sxs-lookup"><span data-stu-id="ae99c-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="ae99c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae99c-115">PARAMETERS</span></span>

### <span data-ttu-id="ae99c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae99c-116">-AsJob</span></span>
<span data-ttu-id="ae99c-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ae99c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae99c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae99c-118">-Confirm</span></span>
<span data-ttu-id="ae99c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae99c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae99c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae99c-120">-DefaultProfile</span></span>
<span data-ttu-id="ae99c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae99c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae99c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae99c-122">-InputObject</span></span>
<span data-ttu-id="ae99c-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="ae99c-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="ae99c-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="ae99c-124">-Location</span></span>
<span data-ttu-id="ae99c-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="ae99c-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ae99c-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae99c-126">-Name</span></span>
<span data-ttu-id="ae99c-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="ae99c-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="ae99c-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae99c-128">-NetworkWatcher</span></span>
<span data-ttu-id="ae99c-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ae99c-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="ae99c-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ae99c-130">-NetworkWatcherName</span></span>
<span data-ttu-id="ae99c-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ae99c-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="ae99c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae99c-132">-PassThru</span></span>
<span data-ttu-id="ae99c-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ae99c-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ae99c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae99c-134">-ResourceGroupName</span></span>
<span data-ttu-id="ae99c-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ae99c-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ae99c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae99c-136">-ResourceId</span></span>
<span data-ttu-id="ae99c-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ae99c-137">Resource ID.</span></span>

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

### <span data-ttu-id="ae99c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae99c-138">-WhatIf</span></span>
<span data-ttu-id="ae99c-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae99c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae99c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae99c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae99c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae99c-141">CommonParameters</span></span>
<span data-ttu-id="ae99c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae99c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae99c-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae99c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae99c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae99c-144">INPUTS</span></span>

### <span data-ttu-id="ae99c-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae99c-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ae99c-146">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ae99c-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ae99c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae99c-147">OUTPUTS</span></span>

### <span data-ttu-id="ae99c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae99c-148">System.Boolean</span></span>

## <span data-ttu-id="ae99c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae99c-149">NOTES</span></span>
<span data-ttu-id="ae99c-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="ae99c-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ae99c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae99c-151">RELATED LINKS</span></span>

[<span data-ttu-id="ae99c-152">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae99c-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ae99c-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae99c-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ae99c-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae99c-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ae99c-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae99c-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="ae99c-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae99c-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="ae99c-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ae99c-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="ae99c-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ae99c-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="ae99c-159">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae99c-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ae99c-160">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae99c-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="ae99c-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae99c-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ae99c-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae99c-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ae99c-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae99c-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ae99c-164">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae99c-164">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ae99c-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ae99c-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="ae99c-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae99c-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ae99c-167">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae99c-167">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ae99c-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae99c-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ae99c-169">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae99c-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
