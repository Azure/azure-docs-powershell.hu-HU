---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 2838d3d18aaa1cdf450eed184c5ebfe9a803c20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918530"
---
# <span data-ttu-id="8fdea-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8fdea-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="8fdea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fdea-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdea-103">Leállítja a csomagrögzítési műveletet egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="8fdea-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="8fdea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fdea-104">SYNTAX</span></span>

### <span data-ttu-id="8fdea-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fdea-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8fdea-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fdea-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdea-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fdea-108">DESCRIPTION</span></span>
<span data-ttu-id="8fdea-109">Leállítja a csomagrögzítési műveletet egy virtuális hálózati átjárón, és feltölti az eredményt az adott SasUrl tárolón.</span><span class="sxs-lookup"><span data-stu-id="8fdea-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="8fdea-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fdea-110">EXAMPLES</span></span>

### <span data-ttu-id="8fdea-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8fdea-111">Example 1</span></span>
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

### <span data-ttu-id="8fdea-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8fdea-112">Example 2</span></span>
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

## <span data-ttu-id="8fdea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fdea-113">PARAMETERS</span></span>

### <span data-ttu-id="8fdea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fdea-114">-AsJob</span></span>
<span data-ttu-id="8fdea-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8fdea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fdea-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fdea-116">-Confirm</span></span>
<span data-ttu-id="8fdea-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8fdea-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fdea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdea-118">-DefaultProfile</span></span>
<span data-ttu-id="8fdea-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fdea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fdea-120">-InputObject</span></span>
<span data-ttu-id="8fdea-121">A virtuális hálózati átjáró objektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="8fdea-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="8fdea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8fdea-122">-Name</span></span>
<span data-ttu-id="8fdea-123">A virtuális hálózati átjáró neve, ahol a csomagok rögzítését el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="8fdea-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="8fdea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fdea-124">-ResourceGroupName</span></span>
<span data-ttu-id="8fdea-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fdea-125">The resource group name.</span></span>

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

### <span data-ttu-id="8fdea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fdea-126">-ResourceId</span></span>
<span data-ttu-id="8fdea-127">A VirtualNetworkGateway Azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="8fdea-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="8fdea-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="8fdea-128">-SasUrl</span></span>
<span data-ttu-id="8fdea-129">AZ SAS URL-csomagrögzítése a virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="8fdea-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="8fdea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdea-130">-WhatIf</span></span>
<span data-ttu-id="8fdea-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8fdea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fdea-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fdea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fdea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdea-133">CommonParameters</span></span>
<span data-ttu-id="8fdea-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdea-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fdea-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdea-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fdea-136">INPUTS</span></span>

### <span data-ttu-id="8fdea-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8fdea-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8fdea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8fdea-138">System.String</span></span>

## <span data-ttu-id="8fdea-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fdea-139">OUTPUTS</span></span>

### <span data-ttu-id="8fdea-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8fdea-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="8fdea-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fdea-141">NOTES</span></span>

## <span data-ttu-id="8fdea-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fdea-142">RELATED LINKS</span></span>
[<span data-ttu-id="8fdea-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8fdea-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
