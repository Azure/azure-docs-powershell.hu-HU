---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843597"
---
# <span data-ttu-id="2e31e-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e31e-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2e31e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e31e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e31e-103">Frissítheti a kapcsolat monitorát.</span><span class="sxs-lookup"><span data-stu-id="2e31e-103">Update a connection monitor.</span></span>

## <span data-ttu-id="2e31e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e31e-104">SYNTAX</span></span>

### <span data-ttu-id="2e31e-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e31e-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e31e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2e31e-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e31e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2e31e-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e31e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e31e-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e31e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e31e-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2e31e-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e31e-110">DESCRIPTION</span></span>
<span data-ttu-id="2e31e-111">A Set-AzNetworkWatcherConnectionMonitor parancsmag frissíti a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="2e31e-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="2e31e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2e31e-112">EXAMPLES</span></span>

### <span data-ttu-id="2e31e-113">---------------Példa 1: a kapcsolat monitorának frissítése---------------</span><span class="sxs-lookup"><span data-stu-id="2e31e-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="2e31e-114">Ebben a példában frissítjük a meglévő kapcsolati monitort a destinationAddress módosításával és a címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="2e31e-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="2e31e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e31e-115">PARAMETERS</span></span>

### <span data-ttu-id="2e31e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e31e-116">-AsJob</span></span>
<span data-ttu-id="2e31e-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2e31e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e31e-118">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="2e31e-118">-AutoStart</span></span>
<span data-ttu-id="2e31e-119">Automatikus indítás gombra.</span><span class="sxs-lookup"><span data-stu-id="2e31e-119">Auto start.</span></span>

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

### <span data-ttu-id="2e31e-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e31e-120">-Confirm</span></span>
<span data-ttu-id="2e31e-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e31e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e31e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e31e-122">-DefaultProfile</span></span>
<span data-ttu-id="2e31e-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e31e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e31e-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2e31e-124">-DestinationAddress</span></span>
<span data-ttu-id="2e31e-125">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="2e31e-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="2e31e-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2e31e-126">-DestinationPort</span></span>
<span data-ttu-id="2e31e-127">Célport.</span><span class="sxs-lookup"><span data-stu-id="2e31e-127">Destination port.</span></span>

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

### <span data-ttu-id="2e31e-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="2e31e-128">-DestinationResourceId</span></span>
<span data-ttu-id="2e31e-129">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e31e-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="2e31e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="2e31e-130">-Force</span></span>
<span data-ttu-id="2e31e-131">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e31e-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2e31e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e31e-132">-InputObject</span></span>
<span data-ttu-id="2e31e-133">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="2e31e-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="2e31e-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="2e31e-134">-Location</span></span>
<span data-ttu-id="2e31e-135">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="2e31e-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2e31e-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2e31e-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="2e31e-137">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="2e31e-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="2e31e-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e31e-138">-Name</span></span>
<span data-ttu-id="2e31e-139">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="2e31e-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="2e31e-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e31e-140">-NetworkWatcher</span></span>
<span data-ttu-id="2e31e-141">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="2e31e-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="2e31e-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2e31e-142">-NetworkWatcherName</span></span>
<span data-ttu-id="2e31e-143">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="2e31e-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="2e31e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e31e-144">-ResourceGroupName</span></span>
<span data-ttu-id="2e31e-145">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e31e-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2e31e-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e31e-146">-ResourceId</span></span>
<span data-ttu-id="2e31e-147">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2e31e-147">Resource ID.</span></span>

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

### <span data-ttu-id="2e31e-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2e31e-148">-SourcePort</span></span>
<span data-ttu-id="2e31e-149">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="2e31e-149">Source port.</span></span>

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

### <span data-ttu-id="2e31e-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2e31e-150">-SourceResourceId</span></span>
<span data-ttu-id="2e31e-151">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e31e-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="2e31e-152">-Címke</span><span class="sxs-lookup"><span data-stu-id="2e31e-152">-Tag</span></span>
<span data-ttu-id="2e31e-153">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2e31e-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2e31e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e31e-154">-WhatIf</span></span>
<span data-ttu-id="2e31e-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e31e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e31e-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e31e-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2e31e-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e31e-157">INPUTS</span></span>

### <span data-ttu-id="2e31e-158">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e31e-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2e31e-159">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2e31e-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="2e31e-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e31e-160">OUTPUTS</span></span>

### <span data-ttu-id="2e31e-161">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2e31e-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="2e31e-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e31e-162">NOTES</span></span>
<span data-ttu-id="2e31e-163">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="2e31e-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2e31e-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e31e-164">RELATED LINKS</span></span>
<span data-ttu-id="2e31e-165">[Új – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="2e31e-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="2e31e-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="2e31e-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="2e31e-167">[Új – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Új – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="2e31e-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="2e31e-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="2e31e-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

