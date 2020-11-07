---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849574"
---
# <span data-ttu-id="a74b6-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a74b6-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a74b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a74b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a74b6-103">Létrehoz egy kapcsolat monitort.</span><span class="sxs-lookup"><span data-stu-id="a74b6-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a74b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a74b6-104">SYNTAX</span></span>

### <span data-ttu-id="a74b6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a74b6-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a74b6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a74b6-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a74b6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a74b6-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a74b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a74b6-108">DESCRIPTION</span></span>
<span data-ttu-id="a74b6-109">A New-AzureRmNetworkWatcherConnectionMonitor parancsmag a megadott forrás-és rcreates-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a74b6-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a74b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a74b6-110">EXAMPLES</span></span>

### <span data-ttu-id="a74b6-111">---------------Példa 1: kapcsolati monitor létrehozása VM-és internetes cél számára---------------</span><span class="sxs-lookup"><span data-stu-id="a74b6-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="a74b6-112">Az New-AzureRmNetworkWatcherConnectionMonitor parancsmag létrehoz egy kapcsolat monitort egy adott forráshoz és célhoz.</span><span class="sxs-lookup"><span data-stu-id="a74b6-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a74b6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a74b6-113">PARAMETERS</span></span>

### <span data-ttu-id="a74b6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a74b6-114">-AsJob</span></span>
<span data-ttu-id="a74b6-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a74b6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a74b6-116">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="a74b6-116">-AutoStart</span></span>
<span data-ttu-id="a74b6-117">Automatikus indítás gombra.</span><span class="sxs-lookup"><span data-stu-id="a74b6-117">Auto start.</span></span>

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

### <span data-ttu-id="a74b6-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a74b6-118">-Confirm</span></span>
<span data-ttu-id="a74b6-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a74b6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a74b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74b6-120">-DefaultProfile</span></span>
<span data-ttu-id="a74b6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a74b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a74b6-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a74b6-122">-DestinationAddress</span></span>
<span data-ttu-id="a74b6-123">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="a74b6-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a74b6-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a74b6-124">-DestinationPort</span></span>
<span data-ttu-id="a74b6-125">Célport.</span><span class="sxs-lookup"><span data-stu-id="a74b6-125">Destination port.</span></span>

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

### <span data-ttu-id="a74b6-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a74b6-126">-DestinationResourceId</span></span>
<span data-ttu-id="a74b6-127">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a74b6-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a74b6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a74b6-128">-Force</span></span>
<span data-ttu-id="a74b6-129">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a74b6-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a74b6-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="a74b6-130">-Location</span></span>
<span data-ttu-id="a74b6-131">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="a74b6-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a74b6-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a74b6-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a74b6-133">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="a74b6-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="a74b6-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a74b6-134">-Name</span></span>
<span data-ttu-id="a74b6-135">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="a74b6-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="a74b6-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a74b6-136">-NetworkWatcher</span></span>
<span data-ttu-id="a74b6-137">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a74b6-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="a74b6-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a74b6-138">-NetworkWatcherName</span></span>
<span data-ttu-id="a74b6-139">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="a74b6-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="a74b6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74b6-140">-ResourceGroupName</span></span>
<span data-ttu-id="a74b6-141">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a74b6-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a74b6-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a74b6-142">-SourcePort</span></span>
<span data-ttu-id="a74b6-143">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="a74b6-143">Source port.</span></span>

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

### <span data-ttu-id="a74b6-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a74b6-144">-SourceResourceId</span></span>
<span data-ttu-id="a74b6-145">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a74b6-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="a74b6-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="a74b6-146">-Tag</span></span>
<span data-ttu-id="a74b6-147">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a74b6-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a74b6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74b6-148">-WhatIf</span></span>
<span data-ttu-id="a74b6-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a74b6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a74b6-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a74b6-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a74b6-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a74b6-151">INPUTS</span></span>

### <span data-ttu-id="a74b6-152">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a74b6-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a74b6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a74b6-153">System.String</span></span>


## <span data-ttu-id="a74b6-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a74b6-154">OUTPUTS</span></span>

### <span data-ttu-id="a74b6-155">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a74b6-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="a74b6-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a74b6-156">NOTES</span></span>
<span data-ttu-id="a74b6-157">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="a74b6-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a74b6-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a74b6-158">RELATED LINKS</span></span>
<span data-ttu-id="a74b6-159">[Új – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a74b6-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="a74b6-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a74b6-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a74b6-161">[Új – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Új – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a74b6-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="a74b6-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="a74b6-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
