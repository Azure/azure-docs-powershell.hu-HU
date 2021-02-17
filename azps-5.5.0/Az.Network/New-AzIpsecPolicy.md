---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146930"
---
# <span data-ttu-id="75f6c-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="75f6c-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="75f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="75f6c-103">IPSec-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="75f6c-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="75f6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75f6c-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f6c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="75f6c-106">A New-AzIpsecPolicy parancsmag létrehoz egy IPSec-házirendjavaslatot, amely virtuális hálózati átjáró kapcsolaton keresztül használható.</span><span class="sxs-lookup"><span data-stu-id="75f6c-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="75f6c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75f6c-107">EXAMPLES</span></span>

### <span data-ttu-id="75f6c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="75f6c-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="75f6c-109">IpSec-házirend létrehozása egy új virtuális hálózati átjáró kapcsolatához.</span><span class="sxs-lookup"><span data-stu-id="75f6c-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="75f6c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f6c-110">PARAMETERS</span></span>

### <span data-ttu-id="75f6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f6c-111">-DefaultProfile</span></span>
<span data-ttu-id="75f6c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75f6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f6c-113">-Group</span><span class="sxs-lookup"><span data-stu-id="75f6c-113">-DhGroup</span></span>
<span data-ttu-id="75f6c-114">Az IKE 1. fázisában a kezdeti SA-hez használt.</span><span class="sxs-lookup"><span data-stu-id="75f6c-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f6c-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="75f6c-115">-IkeEncryption</span></span>
<span data-ttu-id="75f6c-116">Az IKE titkosítási algoritmus (IKE 1. fázis)</span><span class="sxs-lookup"><span data-stu-id="75f6c-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f6c-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="75f6c-117">-IkeIntegrity</span></span>
<span data-ttu-id="75f6c-118">Az IKE integritási algoritmus (IKE 1. fázis)</span><span class="sxs-lookup"><span data-stu-id="75f6c-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f6c-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="75f6c-119">-IpsecEncryption</span></span>
<span data-ttu-id="75f6c-120">AZ IPSec titkosítási algoritmus (IKE 2. fázis)</span><span class="sxs-lookup"><span data-stu-id="75f6c-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f6c-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="75f6c-121">-IpsecIntegrity</span></span>
<span data-ttu-id="75f6c-122">Az IPSec-integritási algoritmus (IKE 2. fázis)</span><span class="sxs-lookup"><span data-stu-id="75f6c-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f6c-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="75f6c-123">-PfsGroup</span></span>
<span data-ttu-id="75f6c-124">Az IKE 2. fázisában használt, új gyermek sa-hez használt.</span><span class="sxs-lookup"><span data-stu-id="75f6c-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f6c-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="75f6c-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="75f6c-126">Az IPSec biztonsági társítás (más néven gyors mód vagy 2. fázis) hasznos terhelési mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="75f6c-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="75f6c-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="75f6c-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="75f6c-128">Az IPSec biztonsági társítás (más néven gyors mód vagy 2. fázis) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="75f6c-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="75f6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f6c-129">CommonParameters</span></span>
<span data-ttu-id="75f6c-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f6c-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f6c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f6c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75f6c-132">INPUTS</span></span>

### <span data-ttu-id="75f6c-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="75f6c-133">None</span></span>

## <span data-ttu-id="75f6c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75f6c-134">OUTPUTS</span></span>

### <span data-ttu-id="75f6c-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="75f6c-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="75f6c-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75f6c-136">NOTES</span></span>

## <span data-ttu-id="75f6c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75f6c-137">RELATED LINKS</span></span>
