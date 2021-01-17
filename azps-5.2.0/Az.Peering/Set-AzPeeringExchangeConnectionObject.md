---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334841"
---
# <span data-ttu-id="4bc52-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4bc52-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="4bc52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bc52-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc52-103">Beállítja vagy frissíti az Exchange-kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="4bc52-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="4bc52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4bc52-104">SYNTAX</span></span>

### <span data-ttu-id="4bc52-105">IPv4Address (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bc52-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc52-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="4bc52-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc52-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="4bc52-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bc52-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4bc52-108">DESCRIPTION</span></span>
<span data-ttu-id="4bc52-109">Az Update-AzPeering frissítéssel együtt használva ez memóriaművelet, és csak a következővel marad `Update-AzPeering` meg: .</span><span class="sxs-lookup"><span data-stu-id="4bc52-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="4bc52-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4bc52-110">EXAMPLES</span></span>

### <span data-ttu-id="4bc52-111">Md5-kivonat frissítése</span><span class="sxs-lookup"><span data-stu-id="4bc52-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="4bc52-112">Frissíti a társviszony-objektum első kapcsolatának Md5-kivonatát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="4bc52-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="4bc52-113">Bgp-munkamenet címének frissítése</span><span class="sxs-lookup"><span data-stu-id="4bc52-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="4bc52-114">Frissíti a társviszony-létesítés címét a memóriában a Társviszony-objektum első kapcsolatához.</span><span class="sxs-lookup"><span data-stu-id="4bc52-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="4bc52-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bc52-115">PARAMETERS</span></span>

### <span data-ttu-id="4bc52-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc52-116">-DefaultProfile</span></span>
<span data-ttu-id="4bc52-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bc52-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc52-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bc52-118">-InputObject</span></span>
<span data-ttu-id="4bc52-119">Az exchange connection objektum</span><span class="sxs-lookup"><span data-stu-id="4bc52-119">The exchange connection object</span></span>

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

### <span data-ttu-id="4bc52-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="4bc52-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="4bc52-121">A meghirdetett IPv4-es maximális érték</span><span class="sxs-lookup"><span data-stu-id="4bc52-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="4bc52-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="4bc52-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="4bc52-123">A meghirdetett IPv6 maximális mérete</span><span class="sxs-lookup"><span data-stu-id="4bc52-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="4bc52-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="4bc52-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="4bc52-125">A munkamenet MD5-hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="4bc52-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="4bc52-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="4bc52-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="4bc52-127">A társviszony IPv4-címe</span><span class="sxs-lookup"><span data-stu-id="4bc52-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="4bc52-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="4bc52-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="4bc52-129">A társviszony IPv6-címe</span><span class="sxs-lookup"><span data-stu-id="4bc52-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="4bc52-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc52-130">CommonParameters</span></span>
<span data-ttu-id="4bc52-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc52-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc52-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bc52-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc52-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bc52-133">INPUTS</span></span>

### <span data-ttu-id="4bc52-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="4bc52-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="4bc52-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bc52-135">OUTPUTS</span></span>

### <span data-ttu-id="4bc52-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="4bc52-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="4bc52-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4bc52-137">NOTES</span></span>

## <span data-ttu-id="4bc52-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bc52-138">RELATED LINKS</span></span>
