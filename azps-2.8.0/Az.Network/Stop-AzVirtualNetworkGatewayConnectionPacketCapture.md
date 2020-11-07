---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 791b6d74049aeec24e67ca29f5fae990f511908d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838281"
---
# <span data-ttu-id="9f15e-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f15e-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="9f15e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f15e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f15e-103">A csomag rögzítési műveletének leállítása virtuális hálózati átjáró-kapcsolaton</span><span class="sxs-lookup"><span data-stu-id="9f15e-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="9f15e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f15e-104">SYNTAX</span></span>

### <span data-ttu-id="9f15e-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f15e-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f15e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f15e-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f15e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f15e-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f15e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f15e-108">DESCRIPTION</span></span>
<span data-ttu-id="9f15e-109">A csomag rögzítési műveletének leállítása virtuális hálózati átjáró-kapcsolaton keresztül, és az eredmény feltöltése adott SasUrl-tárolóra.</span><span class="sxs-lookup"><span data-stu-id="9f15e-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="9f15e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9f15e-110">EXAMPLES</span></span>

### <span data-ttu-id="9f15e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9f15e-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="9f15e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9f15e-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="9f15e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f15e-113">PARAMETERS</span></span>

### <span data-ttu-id="9f15e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f15e-114">-AsJob</span></span>
<span data-ttu-id="9f15e-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9f15e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f15e-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f15e-116">-Confirm</span></span>
<span data-ttu-id="9f15e-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f15e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f15e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f15e-118">-DefaultProfile</span></span>
<span data-ttu-id="9f15e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f15e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f15e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f15e-120">-InputObject</span></span>
<span data-ttu-id="9f15e-121">A virtuális hálózati átjáró kapcsolat objektuma, ahol a csomag elindítható.</span><span class="sxs-lookup"><span data-stu-id="9f15e-121">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f15e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f15e-122">-Name</span></span>
<span data-ttu-id="9f15e-123">A virtuális hálózati átjáró kapcsolatának neve, amelybe a csomag-rögzítést el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="9f15e-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f15e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f15e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f15e-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f15e-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f15e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f15e-126">-ResourceId</span></span>
<span data-ttu-id="9f15e-127">Az Azure Resource ID a VirtualNetworkGatewayConnection, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="9f15e-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f15e-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="9f15e-128">-SasUrl</span></span>
<span data-ttu-id="9f15e-129">A virtuális hálózati átjárón a csomag rögzítésének leállítása a SAS URL-címe.</span><span class="sxs-lookup"><span data-stu-id="9f15e-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f15e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f15e-130">-WhatIf</span></span>
<span data-ttu-id="9f15e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f15e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f15e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f15e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f15e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f15e-133">CommonParameters</span></span>
<span data-ttu-id="9f15e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f15e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f15e-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f15e-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f15e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f15e-136">INPUTS</span></span>

### <span data-ttu-id="9f15e-137">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9f15e-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="9f15e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9f15e-138">System.String</span></span>

## <span data-ttu-id="9f15e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f15e-139">OUTPUTS</span></span>

### <span data-ttu-id="9f15e-140">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="9f15e-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="9f15e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f15e-141">NOTES</span></span>

## <span data-ttu-id="9f15e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f15e-142">RELATED LINKS</span></span>
[<span data-ttu-id="9f15e-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f15e-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)