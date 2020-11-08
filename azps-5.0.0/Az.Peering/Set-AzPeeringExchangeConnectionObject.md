---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188229"
---
# <span data-ttu-id="b13b9-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b13b9-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="b13b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b13b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b13b9-103">Az Exchange-kapcsolat adatait állítja be vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="b13b9-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="b13b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b13b9-104">SYNTAX</span></span>

### <span data-ttu-id="b13b9-105">IPv4Address (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b13b9-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b13b9-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="b13b9-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b13b9-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="b13b9-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b13b9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b13b9-108">DESCRIPTION</span></span>
<span data-ttu-id="b13b9-109">Az Update-AzPeering együtt használva ez a memória-művelet, és csak akkor szűnik meg `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="b13b9-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="b13b9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b13b9-110">EXAMPLES</span></span>

### <span data-ttu-id="b13b9-111">Az Md5-üzenetkivonat frissítése</span><span class="sxs-lookup"><span data-stu-id="b13b9-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="b13b9-112">Frissíti az Md5-ujjlenyomatot a társközi objektum első kapcsolatához a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b13b9-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b13b9-113">A BGP-munkameneti cím frissítése</span><span class="sxs-lookup"><span data-stu-id="b13b9-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="b13b9-114">Frissíti a társközi objektum első kapcsolatának a kapcsolati címét a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b13b9-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="b13b9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b13b9-115">PARAMETERS</span></span>

### <span data-ttu-id="b13b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13b9-116">-DefaultProfile</span></span>
<span data-ttu-id="b13b9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b13b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b13b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b13b9-118">-InputObject</span></span>
<span data-ttu-id="b13b9-119">Az Exchange-kapcsolat objektum</span><span class="sxs-lookup"><span data-stu-id="b13b9-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13b9-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b13b9-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b13b9-121">A hirdetett IPv4 maximális száma</span><span class="sxs-lookup"><span data-stu-id="b13b9-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13b9-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b13b9-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b13b9-123">A hirdetett maximális IPv6-érték</span><span class="sxs-lookup"><span data-stu-id="b13b9-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13b9-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b13b9-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b13b9-125">Az MD5 hitelesítési kulcs a munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="b13b9-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="b13b9-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b13b9-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="b13b9-127">A társközi munkamenet IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="b13b9-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13b9-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b13b9-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="b13b9-129">A társközi munkamenet IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="b13b9-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13b9-130">CommonParameters</span></span>
<span data-ttu-id="b13b9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b13b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13b9-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b13b9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13b9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b13b9-133">INPUTS</span></span>

### <span data-ttu-id="b13b9-134">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b13b9-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b13b9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b13b9-135">OUTPUTS</span></span>

### <span data-ttu-id="b13b9-136">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b13b9-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b13b9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b13b9-137">NOTES</span></span>

## <span data-ttu-id="b13b9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b13b9-138">RELATED LINKS</span></span>
