---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300290"
---
# <span data-ttu-id="950a4-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="950a4-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="950a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="950a4-102">SYNOPSIS</span></span>
<span data-ttu-id="950a4-103">A közvetlen kapcsolat adatait állítja be vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="950a4-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="950a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="950a4-104">SYNTAX</span></span>

### <span data-ttu-id="950a4-105">Sávszélesség (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="950a4-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="950a4-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="950a4-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="950a4-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="950a4-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="950a4-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="950a4-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="950a4-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="950a4-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="950a4-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="950a4-110">DESCRIPTION</span></span>
<span data-ttu-id="950a4-111">Az Update-AzPeering együtt használva ez a memória-művelet, és csak akkor szűnik meg `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="950a4-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="950a4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="950a4-112">EXAMPLES</span></span>

### <span data-ttu-id="950a4-113">Frissítés sávszélessége</span><span class="sxs-lookup"><span data-stu-id="950a4-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="950a4-114">A memóriában lévő társközi objektum első kapcsolata sávszélességének frissítése</span><span class="sxs-lookup"><span data-stu-id="950a4-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="950a4-115">A BGP-munkameneti cím frissítése</span><span class="sxs-lookup"><span data-stu-id="950a4-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="950a4-116">Frissíti a társközi objektum első kapcsolatának a kapcsolati címét a memóriában.</span><span class="sxs-lookup"><span data-stu-id="950a4-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="950a4-117">Frissítés a társas szolgáltatás használatához</span><span class="sxs-lookup"><span data-stu-id="950a4-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="950a4-118">A kapcsolat frissítése a társas szolgáltatással való használatra</span><span class="sxs-lookup"><span data-stu-id="950a4-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="950a4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="950a4-119">PARAMETERS</span></span>

### <span data-ttu-id="950a4-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="950a4-120">-BandwidthInMbps</span></span>
<span data-ttu-id="950a4-121">Az ezen a helyen a Mbps-ban ajánlott sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="950a4-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="950a4-122">-DefaultProfile</span></span>
<span data-ttu-id="950a4-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="950a4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="950a4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="950a4-124">-InputObject</span></span>
<span data-ttu-id="950a4-125">A közvetlen kapcsolat objektum</span><span class="sxs-lookup"><span data-stu-id="950a4-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="950a4-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="950a4-127">A hirdetett IPv4 maximális száma</span><span class="sxs-lookup"><span data-stu-id="950a4-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="950a4-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="950a4-129">A hirdetett maximális IPv6-érték</span><span class="sxs-lookup"><span data-stu-id="950a4-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="950a4-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="950a4-131">Az MD5 hitelesítési kulcs a munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="950a4-131">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="950a4-132">-SessionPrefixV4</span></span>
<span data-ttu-id="950a4-133">A társközi munkamenet IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="950a4-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="950a4-134">-SessionPrefixV6</span></span>
<span data-ttu-id="950a4-135">A társközi munkamenet IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="950a4-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="950a4-136">-UseForPeeringService</span></span>
<span data-ttu-id="950a4-137">Engedélyezés a Microsoft-társközi szolgáltatással (MPS) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="950a4-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="950a4-138">CommonParameters</span></span>
<span data-ttu-id="950a4-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="950a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="950a4-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="950a4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="950a4-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="950a4-141">INPUTS</span></span>

### <span data-ttu-id="950a4-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="950a4-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="950a4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="950a4-143">OUTPUTS</span></span>

### <span data-ttu-id="950a4-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="950a4-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="950a4-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="950a4-145">NOTES</span></span>

## <span data-ttu-id="950a4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="950a4-146">RELATED LINKS</span></span>
