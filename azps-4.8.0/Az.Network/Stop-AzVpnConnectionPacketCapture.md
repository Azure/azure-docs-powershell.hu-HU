---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 88cbb5417e8a82ede25cc77274294a5dc4f64b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172843"
---
# <span data-ttu-id="1702c-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1702c-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="1702c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1702c-102">SYNOPSIS</span></span>
<span data-ttu-id="1702c-103">A csomag rögzítési műveletének leállítása VPN-kapcsolaton</span><span class="sxs-lookup"><span data-stu-id="1702c-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="1702c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1702c-104">SYNTAX</span></span>

### <span data-ttu-id="1702c-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1702c-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-LinkConnectionName <String>] -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1702c-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="1702c-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-LinkConnectionName <String>]
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1702c-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="1702c-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> [-LinkConnectionName <String>] -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1702c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1702c-108">DESCRIPTION</span></span>
<span data-ttu-id="1702c-109">A csomag rögzítési műveletének leállítása VPN-kapcsolaton, és az eredmény feltöltése adott SasUrl-tároló esetén</span><span class="sxs-lookup"><span data-stu-id="1702c-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="1702c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1702c-110">EXAMPLES</span></span>

### <span data-ttu-id="1702c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1702c-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="1702c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1702c-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="1702c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1702c-113">PARAMETERS</span></span>

### <span data-ttu-id="1702c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1702c-114">-AsJob</span></span>
<span data-ttu-id="1702c-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1702c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1702c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1702c-116">-DefaultProfile</span></span>
<span data-ttu-id="1702c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1702c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1702c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1702c-118">-InputObject</span></span>
<span data-ttu-id="1702c-119">A VPN-kapcsolat objektum, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="1702c-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1702c-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="1702c-120">-LinkConnectionName</span></span>
<span data-ttu-id="1702c-121">A SiteLinkConnection nevei.</span><span class="sxs-lookup"><span data-stu-id="1702c-121">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1702c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1702c-122">-Name</span></span>
<span data-ttu-id="1702c-123">Annak a virtuális magánhálózati kapcsolatnak a neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="1702c-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1702c-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="1702c-124">-ParentResourceName</span></span>
<span data-ttu-id="1702c-125">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1702c-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1702c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1702c-126">-ResourceGroupName</span></span>
<span data-ttu-id="1702c-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1702c-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1702c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1702c-128">-ResourceId</span></span>
<span data-ttu-id="1702c-129">Az Azure Resource ID a VpnConnection, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="1702c-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1702c-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="1702c-130">-SasUrl</span></span>
<span data-ttu-id="1702c-131">A SAS URL-címe a virtuális magánhálózati csomag rögzítésének leállítása céljából.</span><span class="sxs-lookup"><span data-stu-id="1702c-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="1702c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1702c-132">-Confirm</span></span>
<span data-ttu-id="1702c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1702c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1702c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1702c-134">-WhatIf</span></span>
<span data-ttu-id="1702c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1702c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1702c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1702c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1702c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1702c-137">CommonParameters</span></span>
<span data-ttu-id="1702c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1702c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1702c-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1702c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1702c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1702c-140">INPUTS</span></span>

### <span data-ttu-id="1702c-141">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1702c-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="1702c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1702c-142">System.String</span></span>

## <span data-ttu-id="1702c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1702c-143">OUTPUTS</span></span>

### <span data-ttu-id="1702c-144">Microsoft. Azure. commands. Network. models. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="1702c-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="1702c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1702c-145">NOTES</span></span>

## <span data-ttu-id="1702c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1702c-146">RELATED LINKS</span></span>

[<span data-ttu-id="1702c-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1702c-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)