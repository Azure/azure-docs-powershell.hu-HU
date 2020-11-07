---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841294"
---
# <span data-ttu-id="32046-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32046-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="32046-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32046-102">SYNOPSIS</span></span>
<span data-ttu-id="32046-103">Létrehoz egy kapcsolat monitort.</span><span class="sxs-lookup"><span data-stu-id="32046-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="32046-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32046-104">SYNTAX</span></span>

### <span data-ttu-id="32046-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32046-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="32046-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="32046-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="32046-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="32046-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="32046-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="32046-108">DESCRIPTION</span></span>
<span data-ttu-id="32046-109">A New-AzNetworkWatcherConnectionMonitor parancsmag a megadott forrás-és rcreates-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="32046-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="32046-110">Példák</span><span class="sxs-lookup"><span data-stu-id="32046-110">EXAMPLES</span></span>

### <span data-ttu-id="32046-111">---------------Példa 1: kapcsolati monitor létrehozása VM-és internetes cél számára---------------</span><span class="sxs-lookup"><span data-stu-id="32046-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="32046-112">Az New-AzNetworkWatcherConnectionMonitor parancsmag létrehoz egy kapcsolat monitort egy adott forráshoz és célhoz.</span><span class="sxs-lookup"><span data-stu-id="32046-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="32046-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32046-113">PARAMETERS</span></span>

### <span data-ttu-id="32046-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32046-114">-AsJob</span></span>
<span data-ttu-id="32046-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="32046-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32046-116">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="32046-116">-AutoStart</span></span>
<span data-ttu-id="32046-117">Automatikus indítás gombra.</span><span class="sxs-lookup"><span data-stu-id="32046-117">Auto start.</span></span>

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

### <span data-ttu-id="32046-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32046-118">-Confirm</span></span>
<span data-ttu-id="32046-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32046-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32046-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32046-120">-DefaultProfile</span></span>
<span data-ttu-id="32046-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32046-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32046-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="32046-122">-DestinationAddress</span></span>
<span data-ttu-id="32046-123">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="32046-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="32046-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="32046-124">-DestinationPort</span></span>
<span data-ttu-id="32046-125">Célport.</span><span class="sxs-lookup"><span data-stu-id="32046-125">Destination port.</span></span>

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

### <span data-ttu-id="32046-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="32046-126">-DestinationResourceId</span></span>
<span data-ttu-id="32046-127">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32046-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="32046-128">-Force</span><span class="sxs-lookup"><span data-stu-id="32046-128">-Force</span></span>
<span data-ttu-id="32046-129">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32046-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32046-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="32046-130">-Location</span></span>
<span data-ttu-id="32046-131">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="32046-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="32046-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="32046-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="32046-133">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="32046-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="32046-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32046-134">-Name</span></span>
<span data-ttu-id="32046-135">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="32046-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32046-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32046-136">-NetworkWatcher</span></span>
<span data-ttu-id="32046-137">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="32046-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="32046-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="32046-138">-NetworkWatcherName</span></span>
<span data-ttu-id="32046-139">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="32046-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="32046-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32046-140">-ResourceGroupName</span></span>
<span data-ttu-id="32046-141">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32046-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="32046-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="32046-142">-SourcePort</span></span>
<span data-ttu-id="32046-143">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="32046-143">Source port.</span></span>

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

### <span data-ttu-id="32046-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="32046-144">-SourceResourceId</span></span>
<span data-ttu-id="32046-145">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32046-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="32046-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="32046-146">-Tag</span></span>
<span data-ttu-id="32046-147">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="32046-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="32046-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32046-148">-WhatIf</span></span>
<span data-ttu-id="32046-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32046-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32046-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32046-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="32046-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32046-151">INPUTS</span></span>

### <span data-ttu-id="32046-152">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32046-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="32046-153">System. String</span><span class="sxs-lookup"><span data-stu-id="32046-153">System.String</span></span>


## <span data-ttu-id="32046-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32046-154">OUTPUTS</span></span>

### <span data-ttu-id="32046-155">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="32046-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="32046-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32046-156">NOTES</span></span>
<span data-ttu-id="32046-157">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="32046-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="32046-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32046-158">RELATED LINKS</span></span>
<span data-ttu-id="32046-159">[Új – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="32046-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="32046-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="32046-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="32046-161">[Új – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Új – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="32046-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="32046-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="32046-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
