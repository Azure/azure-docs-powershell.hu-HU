---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837140"
---
# <span data-ttu-id="3af67-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3af67-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="3af67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3af67-102">SYNOPSIS</span></span>
<span data-ttu-id="3af67-103">Azure VpnSiteLink objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3af67-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="3af67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3af67-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3af67-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3af67-105">DESCRIPTION</span></span>
<span data-ttu-id="3af67-106">Azure VpnSiteLink objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3af67-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="3af67-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3af67-107">EXAMPLES</span></span>

### <span data-ttu-id="3af67-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3af67-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="3af67-109">A fentiekben létrehozunk egy erőforráscsoportot, egy virtuális WAN-csoportot és egy VpnSite, amelyben az Azure-ban az "testRG" erőforráscsoport az Amerikai Egyesült Államokban 1 VpnSiteLinks tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3af67-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="3af67-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3af67-110">PARAMETERS</span></span>

### <span data-ttu-id="3af67-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="3af67-111">-BGPAsn</span></span>
<span data-ttu-id="3af67-112">A BGP ASN az ehhez a VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="3af67-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="3af67-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3af67-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="3af67-114">A VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="3af67-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="3af67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af67-115">-DefaultProfile</span></span>
<span data-ttu-id="3af67-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3af67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3af67-117">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="3af67-117">-IPAddress</span></span>
<span data-ttu-id="3af67-118">A következő ugrás az IP-címen.</span><span class="sxs-lookup"><span data-stu-id="3af67-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="3af67-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="3af67-119">-LinkProviderName</span></span>
<span data-ttu-id="3af67-120">Hivatkozás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="3af67-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="3af67-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="3af67-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="3af67-122">A hivatkozás sebessége Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="3af67-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="3af67-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3af67-123">-Name</span></span>
<span data-ttu-id="3af67-124">név</span><span class="sxs-lookup"><span data-stu-id="3af67-124">Name</span></span>

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

### <span data-ttu-id="3af67-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af67-125">CommonParameters</span></span>
<span data-ttu-id="3af67-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3af67-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af67-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3af67-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af67-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3af67-128">INPUTS</span></span>

### <span data-ttu-id="3af67-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="3af67-129">None</span></span>

## <span data-ttu-id="3af67-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3af67-130">OUTPUTS</span></span>

### <span data-ttu-id="3af67-131">Microsoft. Azure. commands. Network. models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3af67-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="3af67-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3af67-132">NOTES</span></span>

## <span data-ttu-id="3af67-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3af67-133">RELATED LINKS</span></span>

[<span data-ttu-id="3af67-134">Új – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3af67-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)