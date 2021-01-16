---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363437"
---
# <span data-ttu-id="82764-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82764-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="82764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82764-102">SYNOPSIS</span></span>
<span data-ttu-id="82764-103">A csomagok rögzítésének leállítja a műveletet virtuális hálózati átjáró kapcsolatán</span><span class="sxs-lookup"><span data-stu-id="82764-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="82764-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82764-104">SYNTAX</span></span>

### <span data-ttu-id="82764-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82764-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82764-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="82764-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82764-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82764-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82764-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82764-108">DESCRIPTION</span></span>
<span data-ttu-id="82764-109">Leállítja a csomagrögzítési műveletet egy virtuális hálózati átjáró kapcsolatán, és feltölti az eredményt az adott SasUrl tárolón.</span><span class="sxs-lookup"><span data-stu-id="82764-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="82764-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82764-110">EXAMPLES</span></span>

### <span data-ttu-id="82764-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="82764-111">Example 1</span></span>
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

### <span data-ttu-id="82764-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="82764-112">Example 2</span></span>
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

## <span data-ttu-id="82764-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82764-113">PARAMETERS</span></span>

### <span data-ttu-id="82764-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82764-114">-AsJob</span></span>
<span data-ttu-id="82764-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="82764-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82764-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82764-116">-Confirm</span></span>
<span data-ttu-id="82764-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82764-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82764-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82764-118">-DefaultProfile</span></span>
<span data-ttu-id="82764-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82764-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82764-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82764-120">-InputObject</span></span>
<span data-ttu-id="82764-121">A virtuális hálózati átjáró csatlakozási objektuma, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="82764-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="82764-122">-Name</span><span class="sxs-lookup"><span data-stu-id="82764-122">-Name</span></span>
<span data-ttu-id="82764-123">A virtuális hálózati átjáró kapcsolatának neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="82764-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="82764-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82764-124">-ResourceGroupName</span></span>
<span data-ttu-id="82764-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="82764-125">The resource group name.</span></span>

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

### <span data-ttu-id="82764-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82764-126">-ResourceId</span></span>
<span data-ttu-id="82764-127">A VirtualNetworkGatewayConnection azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="82764-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="82764-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="82764-128">-SasUrl</span></span>
<span data-ttu-id="82764-129">A csomagok rögzítésének a virtuális hálózati átjárón való leállításához használható SAS URL-címe.</span><span class="sxs-lookup"><span data-stu-id="82764-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="82764-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82764-130">-WhatIf</span></span>
<span data-ttu-id="82764-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82764-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82764-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82764-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82764-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82764-133">CommonParameters</span></span>
<span data-ttu-id="82764-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82764-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82764-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82764-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82764-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82764-136">INPUTS</span></span>

### <span data-ttu-id="82764-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="82764-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="82764-138">System.String</span><span class="sxs-lookup"><span data-stu-id="82764-138">System.String</span></span>

## <span data-ttu-id="82764-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82764-139">OUTPUTS</span></span>

### <span data-ttu-id="82764-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="82764-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="82764-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82764-141">NOTES</span></span>

## <span data-ttu-id="82764-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82764-142">RELATED LINKS</span></span>
[<span data-ttu-id="82764-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82764-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)