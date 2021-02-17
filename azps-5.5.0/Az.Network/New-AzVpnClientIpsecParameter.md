---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154234"
---
# <span data-ttu-id="0f366-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="0f366-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="0f366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f366-102">SYNOPSIS</span></span>
<span data-ttu-id="0f366-103">Ezzel a paranccsal a felhasználók létrehozhatják a Vpn ipsec paraméterobjektumot, amely egy vagy az összes értéket (ipsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,Group,PfsGroup) a meglévő VPN-átjárón állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="0f366-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="0f366-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f366-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f366-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f366-105">DESCRIPTION</span></span>
<span data-ttu-id="0f366-106">Ezzel a paranccsal a felhasználók létrehozhatják a Vpn ipsec paraméterobjektumot, amely egy vagy az összes értéket (ipsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,Group,PfsGroup) a meglévő VPN-átjárón állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="0f366-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="0f366-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f366-107">EXAMPLES</span></span>

### <span data-ttu-id="0f366-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0f366-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="0f366-109">New-AzVpnClientIpsecParameter a felhasználó által az ResourceGroup bármely meglévő virtuális hálózati átjárója számára beállítható, a megadott egy vagy több paraméter értékét használó VPN IPsec-paraméterek objektumának létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="0f366-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="0f366-110">Ez a létrehozott VpnClientIPsecParameters objektum át van adva egy Set-AzVpnClientIpsecParameter-parancsnak, amely a megadott Vpn ipsec egyéni házirendet virtuális hálózati átjárón adja meg a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="0f366-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="0f366-111">Ez a parancs a VpnClientIPsecParameters objektumát adja vissza, amely a beállított paramétereket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0f366-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="0f366-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f366-112">PARAMETERS</span></span>

### <span data-ttu-id="0f366-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f366-113">-DefaultProfile</span></span>
<span data-ttu-id="0f366-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f366-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f366-115">-Group</span><span class="sxs-lookup"><span data-stu-id="0f366-115">-DhGroup</span></span>
<span data-ttu-id="0f366-116">Az IKE 1. fázisában a kezdeti sa-hez használt VpnClient VPN-csoportok.</span><span class="sxs-lookup"><span data-stu-id="0f366-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="0f366-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="0f366-117">-IkeEncryption</span></span>
<span data-ttu-id="0f366-118">A VpnClient IKE titkosítási algoritmus (IKE 2. fázis)</span><span class="sxs-lookup"><span data-stu-id="0f366-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="0f366-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="0f366-119">-IkeIntegrity</span></span>
<span data-ttu-id="0f366-120">A VpnClient IKE integritási algoritmusa (IKE 2. fázis)</span><span class="sxs-lookup"><span data-stu-id="0f366-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="0f366-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="0f366-121">-IpsecEncryption</span></span>
<span data-ttu-id="0f366-122">A VpnClient IPSec titkosítási algoritmus (IKE 1. fázis)</span><span class="sxs-lookup"><span data-stu-id="0f366-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="0f366-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="0f366-123">-IpsecIntegrity</span></span>
<span data-ttu-id="0f366-124">A VpnClient IPSec integritási algoritmus (IKE 1. fázis)</span><span class="sxs-lookup"><span data-stu-id="0f366-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="0f366-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="0f366-125">-PfsGroup</span></span>
<span data-ttu-id="0f366-126">Az IKE 2. fázisában használt VpnClient PFS-csoportok új gyermek biztonsági társítása esetén</span><span class="sxs-lookup"><span data-stu-id="0f366-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="0f366-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="0f366-127">-SADataSize</span></span>
<span data-ttu-id="0f366-128">A VpnClient IPSec biztonsági társítás (más néven gyors mód vagy 2. fázis sa) hasznos terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="0f366-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="0f366-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="0f366-129">-SALifeTime</span></span>
<span data-ttu-id="0f366-130">A VpnClient IPSec biztonsági társítás (más néven gyorsmód vagy 2. fázis sa) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="0f366-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="0f366-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f366-131">CommonParameters</span></span>
<span data-ttu-id="0f366-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f366-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f366-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f366-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f366-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f366-134">INPUTS</span></span>

### <span data-ttu-id="0f366-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f366-135">None</span></span>

## <span data-ttu-id="0f366-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f366-136">OUTPUTS</span></span>

### <span data-ttu-id="0f366-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0f366-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="0f366-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f366-138">NOTES</span></span>

## <span data-ttu-id="0f366-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f366-139">RELATED LINKS</span></span>

[<span data-ttu-id="0f366-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="0f366-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="0f366-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="0f366-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="0f366-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="0f366-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
