---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847006"
---
# <span data-ttu-id="26b01-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="26b01-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="26b01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26b01-102">SYNOPSIS</span></span>
<span data-ttu-id="26b01-103">Létrehozza a PSObject létrehozásához vagy módosításához használandó a memória-adatkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="26b01-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="26b01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26b01-104">SYNTAX</span></span>

### <span data-ttu-id="26b01-105">IPv4PrefixIPv6Prefix (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26b01-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26b01-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="26b01-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26b01-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="26b01-107">DESCRIPTION</span></span>
<span data-ttu-id="26b01-108">A memória PSObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="26b01-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="26b01-109">Példák</span><span class="sxs-lookup"><span data-stu-id="26b01-109">EXAMPLES</span></span>

### <span data-ttu-id="26b01-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26b01-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="26b01-111">Új helyi kapcsolat</span><span class="sxs-lookup"><span data-stu-id="26b01-111">New local connection</span></span>

### <span data-ttu-id="26b01-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="26b01-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="26b01-113">Közvetlen kapcsolódási kapcsolat létrehozása a Microsoft-szolgáltatókkal való használathoz és a Microsoft által biztosított IP-címekhez</span><span class="sxs-lookup"><span data-stu-id="26b01-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="26b01-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="26b01-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="26b01-115">Közvetlen kapcsolódási kapcsolat létrehozása a felhasználó által engedélyezve lévő szolgáltatásokkal és a társközi IP-címekkel</span><span class="sxs-lookup"><span data-stu-id="26b01-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="26b01-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="26b01-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="26b01-117">Közvetlen kapcsolódási kapcsolat létrehozása BGP-munkamenetek IP-címei nélkül.</span><span class="sxs-lookup"><span data-stu-id="26b01-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="26b01-118">A munkatársnak be kell állítania az IP-címeket, mielőtt a BGP-munkamenetet be tudja állítani.</span><span class="sxs-lookup"><span data-stu-id="26b01-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="26b01-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26b01-119">PARAMETERS</span></span>

### <span data-ttu-id="26b01-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="26b01-120">-BandwidthInMbps</span></span>
<span data-ttu-id="26b01-121">Az ezen a helyen a Mbps-ban ajánlott sávszélesség.</span><span class="sxs-lookup"><span data-stu-id="26b01-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b01-122">-DefaultProfile</span></span>
<span data-ttu-id="26b01-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26b01-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26b01-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="26b01-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="26b01-125">A hirdetett IPv4 maximális száma</span><span class="sxs-lookup"><span data-stu-id="26b01-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="26b01-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="26b01-127">A hirdetett maximális IPv6-érték</span><span class="sxs-lookup"><span data-stu-id="26b01-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="26b01-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="26b01-129">Az MD5 hitelesítési kulcs a munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="26b01-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="26b01-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="26b01-131">Engedélyezze a Microsoftot a BGP-munkamenet címének megadásához.</span><span class="sxs-lookup"><span data-stu-id="26b01-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="26b01-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="26b01-133">A társközi létesítmény azonosítója https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="26b01-133">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="26b01-134">-SessionPrefixV4</span></span>
<span data-ttu-id="26b01-135">A társközi munkamenet IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="26b01-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="26b01-136">-SessionPrefixV6</span></span>
<span data-ttu-id="26b01-137">A társközi munkamenet IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="26b01-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b01-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="26b01-138">-UseForPeeringService</span></span>
<span data-ttu-id="26b01-139">Engedélyezés a Microsoft-társközi szolgáltatással (MPS) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="26b01-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="26b01-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b01-140">CommonParameters</span></span>
<span data-ttu-id="26b01-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26b01-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b01-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26b01-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b01-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26b01-143">INPUTS</span></span>

### <span data-ttu-id="26b01-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="26b01-144">None</span></span>

## <span data-ttu-id="26b01-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26b01-145">OUTPUTS</span></span>

### <span data-ttu-id="26b01-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="26b01-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="26b01-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26b01-147">NOTES</span></span>

## <span data-ttu-id="26b01-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26b01-148">RELATED LINKS</span></span>
