---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172841"
---
# <span data-ttu-id="b5c20-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5c20-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="b5c20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5c20-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c20-103">A csomag rögzítési műveletének leállítása a VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="b5c20-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="b5c20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5c20-104">SYNTAX</span></span>

### <span data-ttu-id="b5c20-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5c20-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b5c20-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c20-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c20-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5c20-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c20-109">A csomag rögzítési műveletének leállítása a VPN-átjárón, és az eredmény feltöltése adott SasUrl-tárolóra.</span><span class="sxs-lookup"><span data-stu-id="b5c20-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="b5c20-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5c20-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c20-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b5c20-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="b5c20-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="b5c20-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="b5c20-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5c20-113">PARAMETERS</span></span>

### <span data-ttu-id="b5c20-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5c20-114">-AsJob</span></span>
<span data-ttu-id="b5c20-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5c20-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c20-116">-DefaultProfile</span></span>
<span data-ttu-id="b5c20-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5c20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5c20-118">-InputObject</span></span>
<span data-ttu-id="b5c20-119">A VPN-átjáró objektum, amelybe a csomag elindul.</span><span class="sxs-lookup"><span data-stu-id="b5c20-119">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5c20-120">-Name</span></span>
<span data-ttu-id="b5c20-121">Annak a VPN-átjárónak a neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="b5c20-121">The Vpn Gateway name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c20-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5c20-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b5c20-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c20-124">-ResourceId</span></span>
<span data-ttu-id="b5c20-125">Az Azure Resource ID a VpnGateway, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="b5c20-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="b5c20-126">-SasUrl</span></span>
<span data-ttu-id="b5c20-127">A SAS URL-csomag rögzítése a VPN-átjárón</span><span class="sxs-lookup"><span data-stu-id="b5c20-127">SAS URL packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5c20-128">-Confirm</span></span>
<span data-ttu-id="b5c20-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5c20-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c20-130">-WhatIf</span></span>
<span data-ttu-id="b5c20-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5c20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c20-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5c20-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c20-133">CommonParameters</span></span>
<span data-ttu-id="b5c20-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5c20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c20-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5c20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c20-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5c20-136">INPUTS</span></span>

### <span data-ttu-id="b5c20-137">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b5c20-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="b5c20-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c20-138">System.String</span></span>

## <span data-ttu-id="b5c20-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5c20-139">OUTPUTS</span></span>

### <span data-ttu-id="b5c20-140">Microsoft. Azure. commands. Network. models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="b5c20-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="b5c20-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5c20-141">NOTES</span></span>

## <span data-ttu-id="b5c20-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5c20-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5c20-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5c20-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)