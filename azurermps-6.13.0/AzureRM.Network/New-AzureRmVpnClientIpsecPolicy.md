---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504328"
---
# <span data-ttu-id="d64c4-101">New-AzureRmVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d64c4-101">New-AzureRmVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="d64c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d64c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d64c4-103">Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van</span><span class="sxs-lookup"><span data-stu-id="d64c4-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="d64c4-104">Ez a parancs lehetővé teszik a kimenő objektum a VPN-alapú IPSec-házirend beállítását az új/exisitng átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="d64c4-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d64c4-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d64c4-105">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d64c4-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="d64c4-106">DESCRIPTION</span></span>
<span data-ttu-id="d64c4-107">Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van</span><span class="sxs-lookup"><span data-stu-id="d64c4-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="d64c4-108">Ez a parancs lehetővé teszik a kimenő objektum a VPN-alapú IPSec-házirend beállítását az új/exisitng átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="d64c4-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="d64c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d64c4-109">EXAMPLES</span></span>

### <span data-ttu-id="d64c4-110">Virtuális magánhálózati IPSec-házirend-objektum meghatározása:</span><span class="sxs-lookup"><span data-stu-id="d64c4-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="d64c4-111">Ezzel a parancsmaggal létrehozhatja a virtuális magánhálózati IPSec-házirend objektumát az átadott egy vagy minden paraméter értékével, amelyet a felhasználó átadhat a param: VpnClientIpsecPolicy a PS parancs segítségével: New-AzureRmVirtualNetworkGateway (új VPN-átjáró létrehozása)/Set-AzureRmVirtualNetworkGateway (meglévő VPN-átjáró frissítése) a ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="d64c4-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (New VPN Gateway creation) / Set-AzureRmVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="d64c4-112">Új virtuális hálózati átjáró létrehozása a VPN-alapú egyéni IPSec-házirend beállításával:</span><span class="sxs-lookup"><span data-stu-id="d64c4-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="d64c4-113">Ez a parancsmag a létrehozás után a virtuális hálózati átjáró objektum értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d64c4-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="d64c4-114">Egyéni virtuális magánhálózati IPSec-házirend beállítása a meglévő virtuális hálózati átjárón:</span><span class="sxs-lookup"><span data-stu-id="d64c4-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="d64c4-115">Ez a parancsmag a virtuális hálózati átjáró objektumot a virtuális magánhálózati IPSec-házirend beállítása után ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d64c4-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="d64c4-116">Virtuális hálózati átjáró beszerzése annak megállapításához, hogy helyesen van-e beállítva a VPN-házirend:</span><span class="sxs-lookup"><span data-stu-id="d64c4-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="d64c4-117">Ez a parancsmag a virtuális hálózati átjáró objektum értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d64c4-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="d64c4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d64c4-118">PARAMETERS</span></span>

### <span data-ttu-id="d64c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64c4-119">-DefaultProfile</span></span>
<span data-ttu-id="d64c4-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d64c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64c4-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="d64c4-121">-DhGroup</span></span>
<span data-ttu-id="d64c4-122">Az IKE-fázis 1-es verziójában az első biztonsági társításhoz használt vpnclient DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="d64c4-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="d64c4-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="d64c4-123">-IkeEncryption</span></span>
<span data-ttu-id="d64c4-124">A vpnclient IKE titkosítási algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="d64c4-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="d64c4-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="d64c4-125">-IkeIntegrity</span></span>
<span data-ttu-id="d64c4-126">A vpnclient IKE Integrity algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="d64c4-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="d64c4-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="d64c4-127">-IpsecEncryption</span></span>
<span data-ttu-id="d64c4-128">Az vpnclient IPSec titkosítási algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="d64c4-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="d64c4-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="d64c4-129">-IpsecIntegrity</span></span>
<span data-ttu-id="d64c4-130">A vpnclient IPSec Integrity algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="d64c4-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="d64c4-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="d64c4-131">-PfsGroup</span></span>
<span data-ttu-id="d64c4-132">A vpnclient PFS-csoportok az IKE Phase 2 for New Child SA alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="d64c4-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="d64c4-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="d64c4-133">-SADataSize</span></span>
<span data-ttu-id="d64c4-134">A vpnclient IPSec biztonsági társítása (más néven gyorsmódú vagy Phase 2 SA) terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="d64c4-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="d64c4-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="d64c4-135">-SALifeTime</span></span>
<span data-ttu-id="d64c4-136">A vpnclient IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="d64c4-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="d64c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64c4-137">CommonParameters</span></span>
<span data-ttu-id="d64c4-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d64c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64c4-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64c4-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d64c4-140">INPUTS</span></span>

### <span data-ttu-id="d64c4-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="d64c4-141">None</span></span>

## <span data-ttu-id="d64c4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d64c4-142">OUTPUTS</span></span>

### <span data-ttu-id="d64c4-143">Microsoft. Azure. commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d64c4-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="d64c4-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d64c4-144">NOTES</span></span>

## <span data-ttu-id="d64c4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d64c4-145">RELATED LINKS</span></span>
