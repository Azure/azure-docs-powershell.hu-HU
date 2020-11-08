---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185942"
---
# <span data-ttu-id="65b9a-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65b9a-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="65b9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="65b9a-103">A csomag rögzítési műveletének leállítása virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="65b9a-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="65b9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65b9a-104">SYNTAX</span></span>

### <span data-ttu-id="65b9a-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65b9a-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b9a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65b9a-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b9a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65b9a-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b9a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="65b9a-108">DESCRIPTION</span></span>
<span data-ttu-id="65b9a-109">Leállítja a csomag rögzítési műveletét egy virtuális hálózati átjárón, és feltölti az eredményt adott SasUrl-tárolóra.</span><span class="sxs-lookup"><span data-stu-id="65b9a-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="65b9a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="65b9a-110">EXAMPLES</span></span>

### <span data-ttu-id="65b9a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65b9a-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="65b9a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="65b9a-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="65b9a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65b9a-113">PARAMETERS</span></span>

### <span data-ttu-id="65b9a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65b9a-114">-AsJob</span></span>
<span data-ttu-id="65b9a-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65b9a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65b9a-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65b9a-116">-Confirm</span></span>
<span data-ttu-id="65b9a-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65b9a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b9a-118">-DefaultProfile</span></span>
<span data-ttu-id="65b9a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65b9a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b9a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65b9a-120">-InputObject</span></span>
<span data-ttu-id="65b9a-121">A virtuális hálózati átjáró objektum, amelyen a csomag elindítható.</span><span class="sxs-lookup"><span data-stu-id="65b9a-121">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b9a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65b9a-122">-Name</span></span>
<span data-ttu-id="65b9a-123">Annak a virtuális hálózati átjárónak a neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="65b9a-123">The virtual network gateway name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b9a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b9a-124">-ResourceGroupName</span></span>
<span data-ttu-id="65b9a-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="65b9a-125">The resource group name.</span></span>

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

### <span data-ttu-id="65b9a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65b9a-126">-ResourceId</span></span>
<span data-ttu-id="65b9a-127">Az Azure Resource ID a VirtualNetworkGateway, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="65b9a-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="65b9a-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="65b9a-128">-SasUrl</span></span>
<span data-ttu-id="65b9a-129">A SAS URL-csomag rögzítése a virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="65b9a-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="65b9a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b9a-130">-WhatIf</span></span>
<span data-ttu-id="65b9a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65b9a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b9a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65b9a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b9a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b9a-133">CommonParameters</span></span>
<span data-ttu-id="65b9a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65b9a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b9a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65b9a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b9a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b9a-136">INPUTS</span></span>

### <span data-ttu-id="65b9a-137">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65b9a-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="65b9a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="65b9a-138">System.String</span></span>

## <span data-ttu-id="65b9a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b9a-139">OUTPUTS</span></span>

### <span data-ttu-id="65b9a-140">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="65b9a-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="65b9a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65b9a-141">NOTES</span></span>

## <span data-ttu-id="65b9a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65b9a-142">RELATED LINKS</span></span>
[<span data-ttu-id="65b9a-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65b9a-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
