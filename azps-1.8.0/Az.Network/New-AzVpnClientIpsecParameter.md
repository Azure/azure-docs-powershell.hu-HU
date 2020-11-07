---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: e547389518bce61c3c3654011bdc0107dc5a112f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670247"
---
# <span data-ttu-id="dd5b0-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd5b0-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="dd5b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5b0-103">Ez a parancs lehetővé teszi a felhasználóknak, hogy létrehozzák a virtuális magánhálózati IPSec-paramétereket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup a meglévő VPN-átjárón).</span><span class="sxs-lookup"><span data-stu-id="dd5b0-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="dd5b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd5b0-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd5b0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="dd5b0-106">Ez a parancs lehetővé teszi a felhasználóknak, hogy létrehozzák a virtuális magánhálózati IPSec-paramétereket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup a meglévő VPN-átjárón).</span><span class="sxs-lookup"><span data-stu-id="dd5b0-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="dd5b0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd5b0-107">EXAMPLES</span></span>

### <span data-ttu-id="dd5b0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd5b0-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="dd5b0-109">New-AzVpnClientIpsecParameter parancsmag segítségével létrehozhatja a virtuális magánhálózati IPSec-paramétereket tartalmazó objektumot az átadott egy vagy minden paraméter értékével, amelyet a felhasználó bármely meglévő virtuális hálózati átjáróhoz beállíthat a ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="dd5b0-110">Ez a létrehozott VpnClientIPsecParameters objektum átkerül Set-AzVpnClientIpsecParameter parancsra, hogy a megadott VPN-alapú IPSec-házirendet a virtuális hálózati átjárón állítsa be a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="dd5b0-111">Ez a parancs olyan VpnClientIPsecParameters-objektumot ad eredményül, amely a paraméterek beállítását jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="dd5b0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd5b0-112">PARAMETERS</span></span>

### <span data-ttu-id="dd5b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5b0-113">-DefaultProfile</span></span>
<span data-ttu-id="dd5b0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5b0-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="dd5b0-115">-DhGroup</span></span>
<span data-ttu-id="dd5b0-116">Az IKE-fázis első lépésben használt vpnclient DH-csoportjai.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="dd5b0-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="dd5b0-117">-IkeEncryption</span></span>
<span data-ttu-id="dd5b0-118">A vpnclient IKE titkosítási algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="dd5b0-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="dd5b0-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="dd5b0-119">-IkeIntegrity</span></span>
<span data-ttu-id="dd5b0-120">A vpnclient IKE Integrity algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="dd5b0-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="dd5b0-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="dd5b0-121">-IpsecEncryption</span></span>
<span data-ttu-id="dd5b0-122">Az vpnclient IPSec titkosítási algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="dd5b0-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="dd5b0-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="dd5b0-123">-IpsecIntegrity</span></span>
<span data-ttu-id="dd5b0-124">A vpnclient IPSec Integrity algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="dd5b0-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="dd5b0-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="dd5b0-125">-PfsGroup</span></span>
<span data-ttu-id="dd5b0-126">A vpnclient PFS-csoportok az IKE Phase 2 for New Child SA alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="dd5b0-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="dd5b0-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="dd5b0-127">-SADataSize</span></span>
<span data-ttu-id="dd5b0-128">A vpnclient IPSec biztonsági társítása (más néven gyorsmódú vagy Phase 2 SA) terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="dd5b0-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="dd5b0-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="dd5b0-129">-SALifeTime</span></span>
<span data-ttu-id="dd5b0-130">A vpnclient IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="dd5b0-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="dd5b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5b0-131">CommonParameters</span></span>
<span data-ttu-id="dd5b0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd5b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5b0-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5b0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5b0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd5b0-134">INPUTS</span></span>

### <span data-ttu-id="dd5b0-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="dd5b0-135">None</span></span>

## <span data-ttu-id="dd5b0-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd5b0-136">OUTPUTS</span></span>

### <span data-ttu-id="dd5b0-137">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="dd5b0-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="dd5b0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd5b0-138">NOTES</span></span>

## <span data-ttu-id="dd5b0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd5b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="dd5b0-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd5b0-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="dd5b0-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd5b0-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="dd5b0-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dd5b0-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
