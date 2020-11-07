---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 2f2ca6c4b9174248074cb3863c7be7de45c170c6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843802"
---
# <span data-ttu-id="a6bf8-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6bf8-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a6bf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bf8-103">A kapcsolat figyelésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="a6bf8-103">Remove connection monitor.</span></span>

## <span data-ttu-id="a6bf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6bf8-104">SYNTAX</span></span>

### <span data-ttu-id="a6bf8-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6bf8-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a6bf8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a6bf8-106">SetByName</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a6bf8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a6bf8-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a6bf8-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6bf8-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a6bf8-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6bf8-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a6bf8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6bf8-110">DESCRIPTION</span></span>
<span data-ttu-id="a6bf8-111">A Remove-AzNetworkWatcherConnectionMonitor parancsmag eltávolítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="a6bf8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a6bf8-112">EXAMPLES</span></span>

### <span data-ttu-id="a6bf8-113">---------------Példa 1: a megadott kapcsolat monitor eltávolítása---------------</span><span class="sxs-lookup"><span data-stu-id="a6bf8-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="a6bf8-114">Ebben a példában töröljük a kapcsolat monitor helyét és nevét.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="a6bf8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6bf8-115">PARAMETERS</span></span>

### <span data-ttu-id="a6bf8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6bf8-116">-AsJob</span></span>
<span data-ttu-id="a6bf8-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a6bf8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6bf8-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6bf8-118">-Confirm</span></span>
<span data-ttu-id="a6bf8-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bf8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bf8-120">-DefaultProfile</span></span>
<span data-ttu-id="a6bf8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bf8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6bf8-122">-InputObject</span></span>
<span data-ttu-id="a6bf8-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="a6bf8-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="a6bf8-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="a6bf8-124">-Location</span></span>
<span data-ttu-id="a6bf8-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a6bf8-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6bf8-126">-Name</span></span>
<span data-ttu-id="a6bf8-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="a6bf8-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6bf8-128">-NetworkWatcher</span></span>
<span data-ttu-id="a6bf8-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="a6bf8-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a6bf8-130">-NetworkWatcherName</span></span>
<span data-ttu-id="a6bf8-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="a6bf8-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bf8-132">-PassThru</span></span>
<span data-ttu-id="a6bf8-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a6bf8-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a6bf8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bf8-134">-ResourceGroupName</span></span>
<span data-ttu-id="a6bf8-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a6bf8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6bf8-136">-ResourceId</span></span>
<span data-ttu-id="a6bf8-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-137">Resource ID.</span></span>

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

### <span data-ttu-id="a6bf8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bf8-138">-WhatIf</span></span>
<span data-ttu-id="a6bf8-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bf8-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a6bf8-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6bf8-141">INPUTS</span></span>

### <span data-ttu-id="a6bf8-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6bf8-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a6bf8-143">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a6bf8-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="a6bf8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6bf8-144">OUTPUTS</span></span>

### <span data-ttu-id="a6bf8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6bf8-145">System.Boolean</span></span>


## <span data-ttu-id="a6bf8-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6bf8-146">NOTES</span></span>
<span data-ttu-id="a6bf8-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="a6bf8-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a6bf8-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6bf8-148">RELATED LINKS</span></span>
<span data-ttu-id="a6bf8-149">[Új – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a6bf8-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="a6bf8-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a6bf8-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a6bf8-151">[Új – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Új – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a6bf8-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="a6bf8-152">[Új – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="a6bf8-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>

