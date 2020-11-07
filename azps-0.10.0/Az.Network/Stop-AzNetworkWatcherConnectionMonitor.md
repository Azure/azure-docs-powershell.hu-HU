---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843522"
---
# <span data-ttu-id="4568f-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4568f-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4568f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4568f-102">SYNOPSIS</span></span>
<span data-ttu-id="4568f-103">A kapcsolat figyelésének leállítása</span><span class="sxs-lookup"><span data-stu-id="4568f-103">Stop a connection monitor</span></span>

## <span data-ttu-id="4568f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4568f-104">SYNTAX</span></span>

### <span data-ttu-id="4568f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4568f-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4568f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4568f-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4568f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4568f-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4568f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4568f-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4568f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4568f-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4568f-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="4568f-110">DESCRIPTION</span></span>
<span data-ttu-id="4568f-111">A Stop-AzNetworkWatcherConnectionMonitor parancsmag leállítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="4568f-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="4568f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4568f-112">EXAMPLES</span></span>

### <span data-ttu-id="4568f-113">---------------Példa 1: a kapcsolat figyelésének leállítása---------------</span><span class="sxs-lookup"><span data-stu-id="4568f-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="4568f-114">Ebben a példában a kapcsolati monitor neve és a Hálózatfigyelő beállítás van megadva</span><span class="sxs-lookup"><span data-stu-id="4568f-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="4568f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4568f-115">PARAMETERS</span></span>

### <span data-ttu-id="4568f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4568f-116">-AsJob</span></span>
<span data-ttu-id="4568f-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4568f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4568f-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4568f-118">-Confirm</span></span>
<span data-ttu-id="4568f-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4568f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4568f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4568f-120">-DefaultProfile</span></span>
<span data-ttu-id="4568f-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4568f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4568f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4568f-122">-InputObject</span></span>
<span data-ttu-id="4568f-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="4568f-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4568f-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="4568f-124">-Location</span></span>
<span data-ttu-id="4568f-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="4568f-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4568f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4568f-126">-Name</span></span>
<span data-ttu-id="4568f-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="4568f-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4568f-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4568f-128">-NetworkWatcher</span></span>
<span data-ttu-id="4568f-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="4568f-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="4568f-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4568f-130">-NetworkWatcherName</span></span>
<span data-ttu-id="4568f-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="4568f-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="4568f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4568f-132">-PassThru</span></span>
<span data-ttu-id="4568f-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4568f-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4568f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4568f-134">-ResourceGroupName</span></span>
<span data-ttu-id="4568f-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4568f-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4568f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4568f-136">-ResourceId</span></span>
<span data-ttu-id="4568f-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4568f-137">Resource ID.</span></span>

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

### <span data-ttu-id="4568f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4568f-138">-WhatIf</span></span>
<span data-ttu-id="4568f-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4568f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4568f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4568f-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="4568f-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4568f-141">INPUTS</span></span>

### <span data-ttu-id="4568f-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4568f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4568f-143">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4568f-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="4568f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4568f-144">OUTPUTS</span></span>

### <span data-ttu-id="4568f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4568f-145">System.Boolean</span></span>


## <span data-ttu-id="4568f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4568f-146">NOTES</span></span>
<span data-ttu-id="4568f-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="4568f-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4568f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4568f-148">RELATED LINKS</span></span>
<span data-ttu-id="4568f-149">[Új – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="4568f-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="4568f-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="4568f-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="4568f-151">[Új – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Új – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="4568f-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="4568f-152">[Új – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="4568f-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>