---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011015"
---
# <span data-ttu-id="2a9bc-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2a9bc-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="2a9bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9bc-103">Azure VpnSiteLink objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="2a9bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a9bc-104">SYNTAX</span></span>

### <span data-ttu-id="2a9bc-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a9bc-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a9bc-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="2a9bc-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a9bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a9bc-107">DESCRIPTION</span></span>
<span data-ttu-id="2a9bc-108">Azure VpnSiteLink objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="2a9bc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2a9bc-109">EXAMPLES</span></span>

### <span data-ttu-id="2a9bc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2a9bc-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="2a9bc-111">A fentiekben létrehozunk egy erőforráscsoportot, egy virtuális WAN-csoportot és egy VpnSite, amelyben az Azure-ban az "testRG" erőforráscsoport az Amerikai Egyesült Államokban 1 VpnSiteLinks tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="2a9bc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a9bc-112">PARAMETERS</span></span>

### <span data-ttu-id="2a9bc-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="2a9bc-113">-BGPAsn</span></span>
<span data-ttu-id="2a9bc-114">A BGP ASN az ehhez a VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-114">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9bc-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2a9bc-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="2a9bc-116">A VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-116">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="2a9bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9bc-117">-DefaultProfile</span></span>
<span data-ttu-id="2a9bc-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a9bc-119">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2a9bc-119">-Fqdn</span></span>
<span data-ttu-id="2a9bc-120">A következő ugrás FQDN.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9bc-121">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="2a9bc-121">-IPAddress</span></span>
<span data-ttu-id="2a9bc-122">A következő ugrás az IP-címen.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9bc-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="2a9bc-123">-LinkProviderName</span></span>
<span data-ttu-id="2a9bc-124">Hivatkozás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-124">Link Provider Name.</span></span>

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

### <span data-ttu-id="2a9bc-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="2a9bc-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="2a9bc-126">A hivatkozás sebessége Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="2a9bc-126">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9bc-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a9bc-127">-Name</span></span>
<span data-ttu-id="2a9bc-128">név</span><span class="sxs-lookup"><span data-stu-id="2a9bc-128">Name</span></span>

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

### <span data-ttu-id="2a9bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9bc-129">CommonParameters</span></span>
<span data-ttu-id="2a9bc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a9bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9bc-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9bc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a9bc-132">INPUTS</span></span>

### <span data-ttu-id="2a9bc-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="2a9bc-133">None</span></span>

## <span data-ttu-id="2a9bc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a9bc-134">OUTPUTS</span></span>

### <span data-ttu-id="2a9bc-135">Microsoft. Azure. commands. Network. models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2a9bc-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="2a9bc-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a9bc-136">NOTES</span></span>

## <span data-ttu-id="2a9bc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a9bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="2a9bc-138">Új – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="2a9bc-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)