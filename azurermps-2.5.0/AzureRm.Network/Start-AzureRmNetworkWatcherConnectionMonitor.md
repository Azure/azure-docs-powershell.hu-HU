---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848697"
---
# <span data-ttu-id="5f37a-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f37a-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="5f37a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f37a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f37a-103">Kapcsolati monitor indítása</span><span class="sxs-lookup"><span data-stu-id="5f37a-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f37a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f37a-104">SYNTAX</span></span>

### <span data-ttu-id="5f37a-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f37a-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5f37a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5f37a-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5f37a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5f37a-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5f37a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f37a-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5f37a-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f37a-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5f37a-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f37a-110">DESCRIPTION</span></span>
<span data-ttu-id="5f37a-111">A Start-AzureRmNetworkWatcherConnectionMonitor parancsmag elindítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="5f37a-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="5f37a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5f37a-112">EXAMPLES</span></span>

### <span data-ttu-id="5f37a-113">---------------Példa 1: kapcsolat monitorjának indítása---------------</span><span class="sxs-lookup"><span data-stu-id="5f37a-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="5f37a-114">Ebben a példában a kapcsolat monitort a név és a Hálózatfigyelő paranccsal indíthatja el.</span><span class="sxs-lookup"><span data-stu-id="5f37a-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="5f37a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f37a-115">PARAMETERS</span></span>

### <span data-ttu-id="5f37a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f37a-116">-AsJob</span></span>
<span data-ttu-id="5f37a-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5f37a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f37a-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f37a-118">-Confirm</span></span>
<span data-ttu-id="5f37a-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f37a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f37a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f37a-120">-DefaultProfile</span></span>
<span data-ttu-id="5f37a-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f37a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f37a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f37a-122">-InputObject</span></span>
<span data-ttu-id="5f37a-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="5f37a-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="5f37a-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="5f37a-124">-Location</span></span>
<span data-ttu-id="5f37a-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="5f37a-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5f37a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f37a-126">-Name</span></span>
<span data-ttu-id="5f37a-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="5f37a-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="5f37a-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f37a-128">-NetworkWatcher</span></span>
<span data-ttu-id="5f37a-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="5f37a-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="5f37a-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5f37a-130">-NetworkWatcherName</span></span>
<span data-ttu-id="5f37a-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="5f37a-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="5f37a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f37a-132">-PassThru</span></span>
<span data-ttu-id="5f37a-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5f37a-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5f37a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f37a-134">-ResourceGroupName</span></span>
<span data-ttu-id="5f37a-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5f37a-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5f37a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f37a-136">-ResourceId</span></span>
<span data-ttu-id="5f37a-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5f37a-137">Resource ID.</span></span>

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

### <span data-ttu-id="5f37a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f37a-138">-WhatIf</span></span>
<span data-ttu-id="5f37a-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f37a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f37a-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f37a-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="5f37a-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f37a-141">INPUTS</span></span>

### <span data-ttu-id="5f37a-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f37a-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5f37a-143">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="5f37a-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="5f37a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f37a-144">OUTPUTS</span></span>

### <span data-ttu-id="5f37a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f37a-145">System.Boolean</span></span>


## <span data-ttu-id="5f37a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f37a-146">NOTES</span></span>
<span data-ttu-id="5f37a-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="5f37a-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="5f37a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f37a-148">RELATED LINKS</span></span>
<span data-ttu-id="5f37a-149">[Új – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="5f37a-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="5f37a-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="5f37a-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="5f37a-151">[Új – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Új – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="5f37a-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="5f37a-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="5f37a-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
