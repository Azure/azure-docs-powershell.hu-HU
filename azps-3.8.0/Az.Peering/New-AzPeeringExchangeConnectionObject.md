---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014474"
---
# <span data-ttu-id="210cb-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="210cb-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="210cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="210cb-102">SYNOPSIS</span></span>
<span data-ttu-id="210cb-103">Létrehozza a PSObject létrehozásához vagy módosításához használandó a memória-adatkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="210cb-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="210cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="210cb-104">SYNTAX</span></span>

### <span data-ttu-id="210cb-105">IPv4Address (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="210cb-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210cb-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="210cb-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210cb-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="210cb-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="210cb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="210cb-108">DESCRIPTION</span></span>
<span data-ttu-id="210cb-109">A memória PSObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="210cb-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="210cb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="210cb-110">EXAMPLES</span></span>

### <span data-ttu-id="210cb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="210cb-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="210cb-112">Helyi kapcsolat objektum</span><span class="sxs-lookup"><span data-stu-id="210cb-112">Local connection object</span></span>

## <span data-ttu-id="210cb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="210cb-113">PARAMETERS</span></span>

### <span data-ttu-id="210cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210cb-114">-DefaultProfile</span></span>
<span data-ttu-id="210cb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="210cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="210cb-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="210cb-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="210cb-117">A hirdetett IPv4 maximális száma</span><span class="sxs-lookup"><span data-stu-id="210cb-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="210cb-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="210cb-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="210cb-119">A hirdetett maximális IPv6-érték</span><span class="sxs-lookup"><span data-stu-id="210cb-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="210cb-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="210cb-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="210cb-121">Az MD5 hitelesítési kulcs a munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="210cb-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="210cb-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="210cb-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="210cb-123">A társközi létesítmény azonosítója https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="210cb-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="210cb-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="210cb-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="210cb-125">A társközi munkamenet IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="210cb-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="210cb-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="210cb-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="210cb-127">A társközi munkamenet IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="210cb-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="210cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210cb-128">CommonParameters</span></span>
<span data-ttu-id="210cb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="210cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210cb-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="210cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210cb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="210cb-131">INPUTS</span></span>

### <span data-ttu-id="210cb-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="210cb-132">None</span></span>

## <span data-ttu-id="210cb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="210cb-133">OUTPUTS</span></span>

### <span data-ttu-id="210cb-134">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="210cb-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="210cb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="210cb-135">NOTES</span></span>

## <span data-ttu-id="210cb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="210cb-136">RELATED LINKS</span></span>
