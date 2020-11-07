---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 61b23db6cfc634b318aa0070b5f784ad7067a234
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843537"
---
# <span data-ttu-id="e1040-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e1040-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e1040-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1040-102">SYNOPSIS</span></span>
<span data-ttu-id="e1040-103">Kapcsolati monitor indítása</span><span class="sxs-lookup"><span data-stu-id="e1040-103">Start a connection monitor</span></span>

## <span data-ttu-id="e1040-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1040-104">SYNTAX</span></span>

### <span data-ttu-id="e1040-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1040-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e1040-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e1040-106">SetByName</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e1040-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e1040-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e1040-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1040-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e1040-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e1040-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e1040-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1040-110">DESCRIPTION</span></span>
<span data-ttu-id="e1040-111">A Start-AzNetworkWatcherConnectionMonitor parancsmag elindítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="e1040-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="e1040-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e1040-112">EXAMPLES</span></span>

### <span data-ttu-id="e1040-113">---------------Példa 1: kapcsolat monitorjának indítása---------------</span><span class="sxs-lookup"><span data-stu-id="e1040-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="e1040-114">Ebben a példában a kapcsolat monitort a név és a Hálózatfigyelő paranccsal indíthatja el.</span><span class="sxs-lookup"><span data-stu-id="e1040-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="e1040-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1040-115">PARAMETERS</span></span>

### <span data-ttu-id="e1040-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1040-116">-AsJob</span></span>
<span data-ttu-id="e1040-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e1040-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1040-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1040-118">-Confirm</span></span>
<span data-ttu-id="e1040-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1040-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1040-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1040-120">-DefaultProfile</span></span>
<span data-ttu-id="e1040-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1040-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1040-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1040-122">-InputObject</span></span>
<span data-ttu-id="e1040-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="e1040-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="e1040-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="e1040-124">-Location</span></span>
<span data-ttu-id="e1040-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="e1040-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e1040-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1040-126">-Name</span></span>
<span data-ttu-id="e1040-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="e1040-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="e1040-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e1040-128">-NetworkWatcher</span></span>
<span data-ttu-id="e1040-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e1040-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="e1040-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e1040-130">-NetworkWatcherName</span></span>
<span data-ttu-id="e1040-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="e1040-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="e1040-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1040-132">-PassThru</span></span>
<span data-ttu-id="e1040-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e1040-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e1040-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1040-134">-ResourceGroupName</span></span>
<span data-ttu-id="e1040-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1040-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e1040-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1040-136">-ResourceId</span></span>
<span data-ttu-id="e1040-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e1040-137">Resource ID.</span></span>

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

### <span data-ttu-id="e1040-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1040-138">-WhatIf</span></span>
<span data-ttu-id="e1040-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1040-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1040-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1040-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="e1040-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1040-141">INPUTS</span></span>

### <span data-ttu-id="e1040-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e1040-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e1040-143">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e1040-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="e1040-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1040-144">OUTPUTS</span></span>

### <span data-ttu-id="e1040-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1040-145">System.Boolean</span></span>


## <span data-ttu-id="e1040-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1040-146">NOTES</span></span>
<span data-ttu-id="e1040-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="e1040-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e1040-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1040-148">RELATED LINKS</span></span>
<span data-ttu-id="e1040-149">[Új – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="e1040-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="e1040-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="e1040-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="e1040-151">[Új – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Új – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="e1040-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="e1040-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="e1040-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span></span>