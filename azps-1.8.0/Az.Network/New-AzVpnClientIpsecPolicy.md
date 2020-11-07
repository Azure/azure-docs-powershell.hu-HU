---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: a97379fb3cf59658c3f0822fc08fa65c0614021d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670245"
---
# <span data-ttu-id="cbdb3-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdb3-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="cbdb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdb3-103">Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van</span><span class="sxs-lookup"><span data-stu-id="cbdb3-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="cbdb3-104">Ez a parancs lehetővé teszik a kimenő objektum a VPN-alapú IPSec-házirend beállítását az új/exisitng átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="cbdb3-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="cbdb3-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbdb3-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdb3-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbdb3-106">DESCRIPTION</span></span>
<span data-ttu-id="cbdb3-107">Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van</span><span class="sxs-lookup"><span data-stu-id="cbdb3-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="cbdb3-108">Ez a parancs lehetővé teszik a kimenő objektum a VPN-alapú IPSec-házirend beállítását az új/exisitng átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="cbdb3-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="cbdb3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cbdb3-109">EXAMPLES</span></span>

### <span data-ttu-id="cbdb3-110">Virtuális magánhálózati IPSec-házirend-objektum meghatározása:</span><span class="sxs-lookup"><span data-stu-id="cbdb3-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="cbdb3-111">Ezzel a parancsmaggal létrehozhatja a virtuális magánhálózati IPSec-házirend objektumát az átadott egy vagy minden paraméter értékével, amelyet a felhasználó átadhat a param: VpnClientIpsecPolicy a PS parancs segítségével: New-AzVirtualNetworkGateway (új VPN-átjáró létrehozása)/Set-AzVirtualNetworkGateway (meglévő VPN-átjáró frissítése) a ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="cbdb3-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="cbdb3-112">Új virtuális hálózati átjáró létrehozása a VPN-alapú egyéni IPSec-házirend beállításával:</span><span class="sxs-lookup"><span data-stu-id="cbdb3-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="cbdb3-113">Ez a parancsmag a létrehozás után a virtuális hálózati átjáró objektum értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="cbdb3-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="cbdb3-114">Egyéni virtuális magánhálózati IPSec-házirend beállítása a meglévő virtuális hálózati átjárón:</span><span class="sxs-lookup"><span data-stu-id="cbdb3-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="cbdb3-115">Ez a parancsmag a virtuális hálózati átjáró objektumot a virtuális magánhálózati IPSec-házirend beállítása után ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="cbdb3-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="cbdb3-116">Virtuális hálózati átjáró beszerzése annak megállapításához, hogy helyesen van-e beállítva a VPN-házirend:</span><span class="sxs-lookup"><span data-stu-id="cbdb3-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="cbdb3-117">Ez a parancsmag a virtuális hálózati átjáró objektum értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="cbdb3-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="cbdb3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbdb3-118">PARAMETERS</span></span>

### <span data-ttu-id="cbdb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdb3-119">-DefaultProfile</span></span>
<span data-ttu-id="cbdb3-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbdb3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdb3-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="cbdb3-121">-DhGroup</span></span>
<span data-ttu-id="cbdb3-122">Az IKE-fázis 1-es verziójában az első biztonsági társításhoz használt vpnclient DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="cbdb3-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="cbdb3-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="cbdb3-123">-IkeEncryption</span></span>
<span data-ttu-id="cbdb3-124">A vpnclient IKE titkosítási algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="cbdb3-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="cbdb3-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="cbdb3-125">-IkeIntegrity</span></span>
<span data-ttu-id="cbdb3-126">A vpnclient IKE Integrity algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="cbdb3-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="cbdb3-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="cbdb3-127">-IpsecEncryption</span></span>
<span data-ttu-id="cbdb3-128">Az vpnclient IPSec titkosítási algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="cbdb3-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="cbdb3-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="cbdb3-129">-IpsecIntegrity</span></span>
<span data-ttu-id="cbdb3-130">A vpnclient IPSec Integrity algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="cbdb3-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="cbdb3-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="cbdb3-131">-PfsGroup</span></span>
<span data-ttu-id="cbdb3-132">A vpnclient PFS-csoportok az IKE Phase 2 for New Child SA alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="cbdb3-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="cbdb3-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="cbdb3-133">-SADataSize</span></span>
<span data-ttu-id="cbdb3-134">A vpnclient IPSec biztonsági társítása (más néven gyorsmódú vagy Phase 2 SA) terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="cbdb3-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="cbdb3-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="cbdb3-135">-SALifeTime</span></span>
<span data-ttu-id="cbdb3-136">A vpnclient IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="cbdb3-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="cbdb3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdb3-137">CommonParameters</span></span>
<span data-ttu-id="cbdb3-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbdb3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdb3-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdb3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdb3-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdb3-140">INPUTS</span></span>

### <span data-ttu-id="cbdb3-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="cbdb3-141">None</span></span>

## <span data-ttu-id="cbdb3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdb3-142">OUTPUTS</span></span>

### <span data-ttu-id="cbdb3-143">Microsoft. Azure. commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdb3-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="cbdb3-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbdb3-144">NOTES</span></span>

## <span data-ttu-id="cbdb3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbdb3-145">RELATED LINKS</span></span>
