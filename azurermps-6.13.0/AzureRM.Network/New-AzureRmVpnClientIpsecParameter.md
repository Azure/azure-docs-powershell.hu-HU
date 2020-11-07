---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680635"
---
# <span data-ttu-id="ea7b8-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ea7b8-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="ea7b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7b8-103">Ez a parancs lehetővé teszi a felhasználóknak, hogy létrehozzák a virtuális magánhálózati IPSec-paramétereket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup a meglévő VPN-átjárón).</span><span class="sxs-lookup"><span data-stu-id="ea7b8-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea7b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea7b8-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea7b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea7b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7b8-106">Ez a parancs lehetővé teszi a felhasználóknak, hogy létrehozzák a virtuális magánhálózati IPSec-paramétereket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup a meglévő VPN-átjárón).</span><span class="sxs-lookup"><span data-stu-id="ea7b8-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="ea7b8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ea7b8-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7b8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ea7b8-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="ea7b8-109">New-AzureRmVpnClientIpsecParameter parancsmag segítségével létrehozhatja a virtuális magánhálózati IPSec-paramétereket tartalmazó objektumot az átadott egy vagy minden paraméter értékével, amelyet a felhasználó bármely meglévő virtuális hálózati átjáróhoz beállíthat a ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="ea7b8-110">Ez a létrehozott VpnClientIPsecParameters objektum átkerül Set-AzureRmVpnClientIpsecParameter parancsra, hogy a megadott VPN-alapú IPSec-házirendet a virtuális hálózati átjárón állítsa be a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="ea7b8-111">Ez a parancs olyan VpnClientIPsecParameters-objektumot ad eredményül, amely a paraméterek beállítását jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="ea7b8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea7b8-112">PARAMETERS</span></span>

### <span data-ttu-id="ea7b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7b8-113">-DefaultProfile</span></span>
<span data-ttu-id="ea7b8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7b8-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="ea7b8-115">-DhGroup</span></span>
<span data-ttu-id="ea7b8-116">Az IKE-fázis első lépésben használt vpnclient DH-csoportjai.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="ea7b8-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="ea7b8-117">-IkeEncryption</span></span>
<span data-ttu-id="ea7b8-118">A vpnclient IKE titkosítási algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="ea7b8-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="ea7b8-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="ea7b8-119">-IkeIntegrity</span></span>
<span data-ttu-id="ea7b8-120">A vpnclient IKE Integrity algoritmusa (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="ea7b8-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="ea7b8-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="ea7b8-121">-IpsecEncryption</span></span>
<span data-ttu-id="ea7b8-122">Az vpnclient IPSec titkosítási algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="ea7b8-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="ea7b8-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="ea7b8-123">-IpsecIntegrity</span></span>
<span data-ttu-id="ea7b8-124">A vpnclient IPSec Integrity algoritmusa (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="ea7b8-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="ea7b8-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="ea7b8-125">-PfsGroup</span></span>
<span data-ttu-id="ea7b8-126">A vpnclient PFS-csoportok az IKE Phase 2 for New Child SA alkalmazásban</span><span class="sxs-lookup"><span data-stu-id="ea7b8-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="ea7b8-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="ea7b8-127">-SADataSize</span></span>
<span data-ttu-id="ea7b8-128">A vpnclient IPSec biztonsági társítása (más néven gyorsmódú vagy Phase 2 SA) terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="ea7b8-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="ea7b8-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="ea7b8-129">-SALifeTime</span></span>
<span data-ttu-id="ea7b8-130">A vpnclient IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="ea7b8-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="ea7b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7b8-131">CommonParameters</span></span>
<span data-ttu-id="ea7b8-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea7b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7b8-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7b8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7b8-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea7b8-134">INPUTS</span></span>

### <span data-ttu-id="ea7b8-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea7b8-135">None</span></span>

## <span data-ttu-id="ea7b8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea7b8-136">OUTPUTS</span></span>

### <span data-ttu-id="ea7b8-137">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ea7b8-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="ea7b8-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea7b8-138">NOTES</span></span>

## <span data-ttu-id="ea7b8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea7b8-139">RELATED LINKS</span></span>
