---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 046a2ee4591eb345efd71163d27140799cb229e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849561"
---
# <span data-ttu-id="5ac2e-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ac2e-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="5ac2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ac2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac2e-103">A kapcsolat figyelésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="5ac2e-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ac2e-104">SYNTAX</span></span>

### <span data-ttu-id="5ac2e-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ac2e-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5ac2e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5ac2e-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5ac2e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5ac2e-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5ac2e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac2e-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5ac2e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ac2e-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5ac2e-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ac2e-110">DESCRIPTION</span></span>
<span data-ttu-id="5ac2e-111">A Remove-AzureRmNetworkWatcherConnectionMonitor parancsmag eltávolítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="5ac2e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5ac2e-112">EXAMPLES</span></span>

### <span data-ttu-id="5ac2e-113">---------------Példa 1: a megadott kapcsolat monitor eltávolítása---------------</span><span class="sxs-lookup"><span data-stu-id="5ac2e-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="5ac2e-114">Ebben a példában töröljük a kapcsolat monitor helyét és nevét.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="5ac2e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ac2e-115">PARAMETERS</span></span>

### <span data-ttu-id="5ac2e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ac2e-116">-AsJob</span></span>
<span data-ttu-id="5ac2e-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5ac2e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ac2e-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ac2e-118">-Confirm</span></span>
<span data-ttu-id="5ac2e-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac2e-120">-DefaultProfile</span></span>
<span data-ttu-id="5ac2e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac2e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ac2e-122">-InputObject</span></span>
<span data-ttu-id="5ac2e-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="5ac2e-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="5ac2e-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="5ac2e-124">-Location</span></span>
<span data-ttu-id="5ac2e-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5ac2e-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ac2e-126">-Name</span></span>
<span data-ttu-id="5ac2e-127">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="5ac2e-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ac2e-128">-NetworkWatcher</span></span>
<span data-ttu-id="5ac2e-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="5ac2e-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5ac2e-130">-NetworkWatcherName</span></span>
<span data-ttu-id="5ac2e-131">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="5ac2e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ac2e-132">-PassThru</span></span>
<span data-ttu-id="5ac2e-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ac2e-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ac2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="5ac2e-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5ac2e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac2e-136">-ResourceId</span></span>
<span data-ttu-id="5ac2e-137">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-137">Resource ID.</span></span>

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

### <span data-ttu-id="5ac2e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac2e-138">-WhatIf</span></span>
<span data-ttu-id="5ac2e-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac2e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ac2e-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="5ac2e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac2e-141">INPUTS</span></span>

### <span data-ttu-id="5ac2e-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ac2e-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5ac2e-143">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="5ac2e-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="5ac2e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac2e-144">OUTPUTS</span></span>

### <span data-ttu-id="5ac2e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ac2e-145">System.Boolean</span></span>


## <span data-ttu-id="5ac2e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ac2e-146">NOTES</span></span>
<span data-ttu-id="5ac2e-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="5ac2e-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="5ac2e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac2e-148">RELATED LINKS</span></span>
<span data-ttu-id="5ac2e-149">[Új – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="5ac2e-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="5ac2e-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="5ac2e-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="5ac2e-151">[Új – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Új – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="5ac2e-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="5ac2e-152">[Új – AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="5ac2e-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>

