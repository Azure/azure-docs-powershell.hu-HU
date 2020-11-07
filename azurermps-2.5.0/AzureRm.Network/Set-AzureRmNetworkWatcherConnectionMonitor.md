---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8ebbf4a554ef3dcb13726839ee8b7ebb330bad8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849077"
---
# <span data-ttu-id="f3789-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3789-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f3789-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3789-102">SYNOPSIS</span></span>
<span data-ttu-id="f3789-103">Frissítheti a kapcsolat monitorát.</span><span class="sxs-lookup"><span data-stu-id="f3789-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3789-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3789-104">SYNTAX</span></span>

### <span data-ttu-id="f3789-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3789-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3789-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f3789-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3789-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f3789-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3789-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3789-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3789-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3789-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f3789-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3789-110">DESCRIPTION</span></span>
<span data-ttu-id="f3789-111">A Set-AzureRmNetworkWatcherConnectionMonitor parancsmag frissíti a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="f3789-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="f3789-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f3789-112">EXAMPLES</span></span>

### <span data-ttu-id="f3789-113">---------------Példa 1: a kapcsolat monitorának frissítése---------------</span><span class="sxs-lookup"><span data-stu-id="f3789-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="f3789-114">Ebben a példában frissítjük a meglévő kapcsolati monitort a destinationAddress módosításával és a címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="f3789-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="f3789-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3789-115">PARAMETERS</span></span>

### <span data-ttu-id="f3789-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3789-116">-AsJob</span></span>
<span data-ttu-id="f3789-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f3789-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3789-118">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="f3789-118">-AutoStart</span></span>
<span data-ttu-id="f3789-119">Automatikus indítás gombra.</span><span class="sxs-lookup"><span data-stu-id="f3789-119">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3789-120">-Confirm</span></span>
<span data-ttu-id="f3789-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3789-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3789-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3789-122">-DefaultProfile</span></span>
<span data-ttu-id="f3789-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3789-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3789-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f3789-124">-DestinationAddress</span></span>
<span data-ttu-id="f3789-125">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="f3789-125">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f3789-126">-DestinationPort</span></span>
<span data-ttu-id="f3789-127">Célport.</span><span class="sxs-lookup"><span data-stu-id="f3789-127">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="f3789-128">-DestinationResourceId</span></span>
<span data-ttu-id="f3789-129">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3789-129">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f3789-130">-Force</span></span>
<span data-ttu-id="f3789-131">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3789-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f3789-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3789-132">-InputObject</span></span>
<span data-ttu-id="f3789-133">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="f3789-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="f3789-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="f3789-134">-Location</span></span>
<span data-ttu-id="f3789-135">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="f3789-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f3789-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3789-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="f3789-137">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="f3789-137">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3789-138">-Name</span></span>
<span data-ttu-id="f3789-139">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="f3789-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="f3789-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3789-140">-NetworkWatcher</span></span>
<span data-ttu-id="f3789-141">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f3789-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="f3789-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f3789-142">-NetworkWatcherName</span></span>
<span data-ttu-id="f3789-143">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="f3789-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="f3789-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3789-144">-ResourceGroupName</span></span>
<span data-ttu-id="f3789-145">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3789-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f3789-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3789-146">-ResourceId</span></span>
<span data-ttu-id="f3789-147">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f3789-147">Resource ID.</span></span>

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

### <span data-ttu-id="f3789-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="f3789-148">-SourcePort</span></span>
<span data-ttu-id="f3789-149">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="f3789-149">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f3789-150">-SourceResourceId</span></span>
<span data-ttu-id="f3789-151">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3789-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="f3789-152">-Címke</span><span class="sxs-lookup"><span data-stu-id="f3789-152">-Tag</span></span>
<span data-ttu-id="f3789-153">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f3789-153">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3789-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3789-154">-WhatIf</span></span>
<span data-ttu-id="f3789-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3789-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3789-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3789-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f3789-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3789-157">INPUTS</span></span>

### <span data-ttu-id="f3789-158">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3789-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f3789-159">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f3789-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="f3789-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3789-160">OUTPUTS</span></span>

### <span data-ttu-id="f3789-161">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f3789-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="f3789-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3789-162">NOTES</span></span>
<span data-ttu-id="f3789-163">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="f3789-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f3789-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3789-164">RELATED LINKS</span></span>
<span data-ttu-id="f3789-165">[Új – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="f3789-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="f3789-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="f3789-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="f3789-167">[Új – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Új – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="f3789-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="f3789-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="f3789-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>

