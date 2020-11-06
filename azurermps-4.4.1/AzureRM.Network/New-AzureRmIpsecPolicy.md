---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: 17b24668d497cd8d4405865d40f2969219ede719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502648"
---
# <span data-ttu-id="945b5-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="945b5-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="945b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="945b5-102">SYNOPSIS</span></span>
<span data-ttu-id="945b5-103">IPSec-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="945b5-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="945b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="945b5-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="945b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="945b5-105">DESCRIPTION</span></span>
<span data-ttu-id="945b5-106">Az New-AzureRmIpsecPolicy parancsmag létrehoz egy olyan IPSec-házirend-javaslatot, amelyet a virtuális hálózati átjáró-kapcsolathoz kell használni.</span><span class="sxs-lookup"><span data-stu-id="945b5-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="945b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="945b5-107">EXAMPLES</span></span>

### <span data-ttu-id="945b5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="945b5-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="945b5-109">Új virtuális hálózati átjáró-kapcsolathoz használandó IPSec-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="945b5-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="945b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="945b5-110">PARAMETERS</span></span>

### <span data-ttu-id="945b5-111">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="945b5-111">-DhGroup</span></span>
<span data-ttu-id="945b5-112">A kezdeti biztonsági társításhoz az IKE-fázis 1-es verziójában használt DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="945b5-112">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="945b5-113">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="945b5-113">-IkeEncryption</span></span>
<span data-ttu-id="945b5-114">Az IKE titkosítási algoritmusa (IKE 2 fázis)</span><span class="sxs-lookup"><span data-stu-id="945b5-114">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="945b5-115">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="945b5-115">-IkeIntegrity</span></span>
<span data-ttu-id="945b5-116">Az IKE Integrity algoritmusa (IKE 2 fázis)</span><span class="sxs-lookup"><span data-stu-id="945b5-116">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="945b5-117">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="945b5-117">-IpsecEncryption</span></span>
<span data-ttu-id="945b5-118">Az IPSec titkosítási algoritmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="945b5-118">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="945b5-119">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="945b5-119">-IpsecIntegrity</span></span>
<span data-ttu-id="945b5-120">Az IPSec-integritási algoritmus (IKE-fázis 1)</span><span class="sxs-lookup"><span data-stu-id="945b5-120">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="945b5-121">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="945b5-121">-PfsGroup</span></span>
<span data-ttu-id="945b5-122">Az IKE Phase 2 for New Child SA által használt DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="945b5-122">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="945b5-123">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="945b5-123">-SADataSizeKilobytes</span></span>
<span data-ttu-id="945b5-124">Az IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) hasznos tárterülete KB-ban</span><span class="sxs-lookup"><span data-stu-id="945b5-124">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="945b5-125">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="945b5-125">-SALifeTimeSeconds</span></span>
<span data-ttu-id="945b5-126">Az IPSec biztonsági társítás (más néven Quick Mode vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="945b5-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="945b5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945b5-127">-DefaultProfile</span></span>
<span data-ttu-id="945b5-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="945b5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="945b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945b5-129">CommonParameters</span></span>
<span data-ttu-id="945b5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="945b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945b5-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945b5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945b5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="945b5-132">INPUTS</span></span>

### <span data-ttu-id="945b5-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="945b5-133">None</span></span>

## <span data-ttu-id="945b5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="945b5-134">OUTPUTS</span></span>

### <span data-ttu-id="945b5-135">Microsoft. Azure. commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="945b5-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="945b5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="945b5-136">NOTES</span></span>

## <span data-ttu-id="945b5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="945b5-137">RELATED LINKS</span></span>

