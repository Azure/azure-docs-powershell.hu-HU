---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362653"
---
# <span data-ttu-id="4c9e6-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4c9e6-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="4c9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9e6-103">Beállítja vagy frissíti a közvetlen kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="4c9e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c9e6-104">SYNTAX</span></span>

### <span data-ttu-id="4c9e6-105">Sávszélesség (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c9e6-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9e6-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="4c9e6-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9e6-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="4c9e6-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9e6-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="4c9e6-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9e6-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="4c9e6-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c9e6-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c9e6-110">DESCRIPTION</span></span>
<span data-ttu-id="4c9e6-111">Az Update-AzPeering frissítéssel együtt használva ez memóriaművelet, és csak a következővel marad `Update-AzPeering` meg: .</span><span class="sxs-lookup"><span data-stu-id="4c9e6-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="4c9e6-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c9e6-112">EXAMPLES</span></span>

### <span data-ttu-id="4c9e6-113">Frissítés sávszélessége</span><span class="sxs-lookup"><span data-stu-id="4c9e6-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="4c9e6-114">A társviszony-objektum első kapcsolatának sávszélességét frissíti a memóriában.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="4c9e6-115">Bgp-munkamenet címének frissítése</span><span class="sxs-lookup"><span data-stu-id="4c9e6-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="4c9e6-116">Frissíti a társviszony-létesítés címét a memóriában a Társviszony-objektum első kapcsolatához.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="4c9e6-117">Társviszony-szolgáltatás használatának frissítése</span><span class="sxs-lookup"><span data-stu-id="4c9e6-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="4c9e6-118">A társviszony-létesítés szolgáltatáshoz használható kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="4c9e6-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="4c9e6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c9e6-119">PARAMETERS</span></span>

### <span data-ttu-id="4c9e6-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="4c9e6-120">-BandwidthInMbps</span></span>
<span data-ttu-id="4c9e6-121">Az ezen a helyen mbit/s-ként kínált sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="4c9e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9e6-122">-DefaultProfile</span></span>
<span data-ttu-id="4c9e6-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c9e6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9e6-124">-InputObject</span></span>
<span data-ttu-id="4c9e6-125">A közvetlen kapcsolat objektum</span><span class="sxs-lookup"><span data-stu-id="4c9e6-125">The direct connection Object</span></span>

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

### <span data-ttu-id="4c9e6-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="4c9e6-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="4c9e6-127">A meghirdetett IPv4-es maximális érték</span><span class="sxs-lookup"><span data-stu-id="4c9e6-127">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="4c9e6-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="4c9e6-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="4c9e6-129">A meghirdetett IPv6 maximális mérete</span><span class="sxs-lookup"><span data-stu-id="4c9e6-129">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="4c9e6-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="4c9e6-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="4c9e6-131">A munkamenet MD5-hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="4c9e6-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="4c9e6-132">-SessionPrefixV4</span></span>
<span data-ttu-id="4c9e6-133">A társviszony IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="4c9e6-133">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="4c9e6-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="4c9e6-134">-SessionPrefixV6</span></span>
<span data-ttu-id="4c9e6-135">A társviszony IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="4c9e6-135">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="4c9e6-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="4c9e6-136">-UseForPeeringService</span></span>
<span data-ttu-id="4c9e6-137">Használat engedélyezése a Microsoft társviszony-létesítő szolgáltatásával (MPS).</span><span class="sxs-lookup"><span data-stu-id="4c9e6-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="4c9e6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9e6-138">CommonParameters</span></span>
<span data-ttu-id="4c9e6-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9e6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9e6-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c9e6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9e6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c9e6-141">INPUTS</span></span>

### <span data-ttu-id="4c9e6-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="4c9e6-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="4c9e6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c9e6-143">OUTPUTS</span></span>

### <span data-ttu-id="4c9e6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="4c9e6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="4c9e6-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c9e6-145">NOTES</span></span>

## <span data-ttu-id="4c9e6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c9e6-146">RELATED LINKS</span></span>
