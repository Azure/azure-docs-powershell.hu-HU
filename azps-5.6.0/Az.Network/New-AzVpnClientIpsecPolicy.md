---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924673"
---
# <span data-ttu-id="1fc7d-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1fc7d-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="1fc7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fc7d-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc7d-103">Ezzel a paranccsal a felhasználók létrehozhatják a Vpn ipsec házirendobjektumot, amely megadja az ipsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,Group,PfsGroup értéket a VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="1fc7d-104">Ezzel a paranccsal a kimeneti objektum vpn ipsec-házirendet állíthat be az új/ meglévő átjárókhoz is.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="1fc7d-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1fc7d-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc7d-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1fc7d-106">DESCRIPTION</span></span>
<span data-ttu-id="1fc7d-107">Ezzel a paranccsal a felhasználók létrehozhatják a Vpn ipsec házirendobjektumot, amely megadja az ipsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,Group,PfsGroup értéket a VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="1fc7d-108">Ezzel a paranccsal a kimeneti objektum vpn ipsec-házirendet állíthat be az új/ meglévő átjárókhoz is.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="1fc7d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1fc7d-109">EXAMPLES</span></span>

### <span data-ttu-id="1fc7d-110">1. példa: Vpn ipsec-házirendobjektum definiálása:</span><span class="sxs-lookup"><span data-stu-id="1fc7d-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="1fc7d-111">Ezzel a parancsmaggal hozhatja létre a vpn ipsec házirendobjektumot a felhasználó által a paraméter:VpnClientIpsecPolicy of PS parancs által át lehet adni: New-AzVirtualNetworkGateway (Új VPN-átjáró létrehozása) / Set-AzVirtualNetworkGateway (meglévő VPN-átjáró frissítése) az ResourceGroupban:</span><span class="sxs-lookup"><span data-stu-id="1fc7d-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="1fc7d-112">2. példa: Új virtuális hálózati átjáró létrehozása egyéni IPsec-házirend beállításával:</span><span class="sxs-lookup"><span data-stu-id="1fc7d-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="1fc7d-113">Ez a parancsmag a létrehozás után virtuális hálózati átjáróobjektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="1fc7d-114">3. példa: Egyéni vpn ipsec-házirend beállítása meglévő virtuális hálózati átjárón:</span><span class="sxs-lookup"><span data-stu-id="1fc7d-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="1fc7d-115">Ez a parancsmag virtuális hálózati átjáróobjektumot ad vissza a vpn egyéni ipsec-házirend beállítása után.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="1fc7d-116">4. példa: Virtuális hálózati átjárót beállítva láthatja, hogy megfelelően van-e beállítva a vpn egyéni házirend:</span><span class="sxs-lookup"><span data-stu-id="1fc7d-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="1fc7d-117">Ez a parancsmag virtuális hálózati átjáróobjektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="1fc7d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fc7d-118">PARAMETERS</span></span>

### <span data-ttu-id="1fc7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc7d-119">-DefaultProfile</span></span>
<span data-ttu-id="1fc7d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fc7d-121">-Group</span><span class="sxs-lookup"><span data-stu-id="1fc7d-121">-DhGroup</span></span>
<span data-ttu-id="1fc7d-122">Az IKE 1. fázisában használt VpnClient VPN-csoportok a kezdeti SA-hez</span><span class="sxs-lookup"><span data-stu-id="1fc7d-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="1fc7d-123">-IkeEncryption</span></span>
<span data-ttu-id="1fc7d-124">A VpnClient IKE titkosítási algoritmus (IKE 2. fázis)</span><span class="sxs-lookup"><span data-stu-id="1fc7d-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="1fc7d-125">-IkeIntegrity</span></span>
<span data-ttu-id="1fc7d-126">A VpnClient IKE integritási algoritmusa (IKE 2. fázis)</span><span class="sxs-lookup"><span data-stu-id="1fc7d-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="1fc7d-127">-IpsecEncryption</span></span>
<span data-ttu-id="1fc7d-128">A VpnClient IPSec titkosítási algoritmus (IKE 1. fázis)</span><span class="sxs-lookup"><span data-stu-id="1fc7d-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="1fc7d-129">-IpsecIntegrity</span></span>
<span data-ttu-id="1fc7d-130">A VpnClient IPSec integritási algoritmus (IKE 1. fázis)</span><span class="sxs-lookup"><span data-stu-id="1fc7d-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="1fc7d-131">-PfsGroup</span></span>
<span data-ttu-id="1fc7d-132">Az IKE 2. fázisában használt VpnClient PFS-csoportok új gyermek biztonsági társítása esetén</span><span class="sxs-lookup"><span data-stu-id="1fc7d-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="1fc7d-133">-SADataSize</span></span>
<span data-ttu-id="1fc7d-134">A VpnClient IPSec biztonsági társítás (más néven gyors mód vagy 2. fázis sa) terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="1fc7d-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="1fc7d-135">-SALifeTime</span></span>
<span data-ttu-id="1fc7d-136">A VpnClient IPSec biztonsági társítás (más néven gyorsmód vagy 2. fázis sa) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="1fc7d-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc7d-137">CommonParameters</span></span>
<span data-ttu-id="1fc7d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc7d-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc7d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc7d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fc7d-140">INPUTS</span></span>

### <span data-ttu-id="1fc7d-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="1fc7d-141">None</span></span>

## <span data-ttu-id="1fc7d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fc7d-142">OUTPUTS</span></span>

### <span data-ttu-id="1fc7d-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1fc7d-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="1fc7d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1fc7d-144">NOTES</span></span>

## <span data-ttu-id="1fc7d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fc7d-145">RELATED LINKS</span></span>
