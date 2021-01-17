---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384773"
---
# <span data-ttu-id="5fad3-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="5fad3-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="5fad3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fad3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fad3-103">Létrehoz egy, a memóriában a társviszony létrehozásához vagy módosításához használható PSObject-et.</span><span class="sxs-lookup"><span data-stu-id="5fad3-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="5fad3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5fad3-104">SYNTAX</span></span>

### <span data-ttu-id="5fad3-105">IPv4Address (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5fad3-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fad3-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="5fad3-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fad3-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="5fad3-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fad3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5fad3-108">DESCRIPTION</span></span>
<span data-ttu-id="5fad3-109">PsObject-et hoz létre a memóriában</span><span class="sxs-lookup"><span data-stu-id="5fad3-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="5fad3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5fad3-110">EXAMPLES</span></span>

### <span data-ttu-id="5fad3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5fad3-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="5fad3-112">Helyi kapcsolatobjektum</span><span class="sxs-lookup"><span data-stu-id="5fad3-112">Local connection object</span></span>

## <span data-ttu-id="5fad3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fad3-113">PARAMETERS</span></span>

### <span data-ttu-id="5fad3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fad3-114">-DefaultProfile</span></span>
<span data-ttu-id="5fad3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fad3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fad3-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="5fad3-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="5fad3-117">A meghirdetett IPv4-es maximális érték</span><span class="sxs-lookup"><span data-stu-id="5fad3-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="5fad3-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="5fad3-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="5fad3-119">A meghirdetett IPv6 maximális mérete</span><span class="sxs-lookup"><span data-stu-id="5fad3-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="5fad3-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="5fad3-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="5fad3-121">A munkamenet MD5-hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="5fad3-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="5fad3-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="5fad3-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="5fad3-123">A társviszony-létesítés azonosítója https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="5fad3-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="5fad3-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="5fad3-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="5fad3-125">A társviszony IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="5fad3-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="5fad3-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="5fad3-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="5fad3-127">A társviszony IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="5fad3-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="5fad3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fad3-128">CommonParameters</span></span>
<span data-ttu-id="5fad3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fad3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fad3-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fad3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fad3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fad3-131">INPUTS</span></span>

### <span data-ttu-id="5fad3-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="5fad3-132">None</span></span>

## <span data-ttu-id="5fad3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fad3-133">OUTPUTS</span></span>

### <span data-ttu-id="5fad3-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="5fad3-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="5fad3-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5fad3-135">NOTES</span></span>

## <span data-ttu-id="5fad3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fad3-136">RELATED LINKS</span></span>
