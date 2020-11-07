---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: df9d22c7b6097251e0237f500de837cbf89cdea1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841357"
---
# <span data-ttu-id="50f42-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="50f42-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="50f42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50f42-102">SYNOPSIS</span></span>
<span data-ttu-id="50f42-103">IPSec-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="50f42-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="50f42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50f42-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50f42-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50f42-105">DESCRIPTION</span></span>
<span data-ttu-id="50f42-106">Az New-AzIpsecPolicy parancsmag létrehoz egy olyan IPSec-házirend-javaslatot, amelyet a virtuális hálózati átjáró-kapcsolathoz kell használni.</span><span class="sxs-lookup"><span data-stu-id="50f42-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="50f42-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50f42-107">EXAMPLES</span></span>

### <span data-ttu-id="50f42-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="50f42-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="50f42-109">Új virtuális hálózati átjáró-kapcsolathoz használandó IPSec-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="50f42-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="50f42-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50f42-110">PARAMETERS</span></span>

### <span data-ttu-id="50f42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f42-111">-DefaultProfile</span></span>
<span data-ttu-id="50f42-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50f42-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="50f42-113">-DhGroup</span></span>
<span data-ttu-id="50f42-114">A kezdeti biztonsági társításhoz az IKE-fázis 1-es verziójában használt DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="50f42-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="50f42-115">-IkeEncryption</span></span>
<span data-ttu-id="50f42-116">Az IKE titkosítási algoritmusa (IKE 2 fázis)</span><span class="sxs-lookup"><span data-stu-id="50f42-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="50f42-117">-IkeIntegrity</span></span>
<span data-ttu-id="50f42-118">Az IKE Integrity algoritmusa (IKE 2 fázis)</span><span class="sxs-lookup"><span data-stu-id="50f42-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="50f42-119">-IpsecEncryption</span></span>
<span data-ttu-id="50f42-120">Az IPSec titkosítási algoritmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="50f42-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="50f42-121">-IpsecIntegrity</span></span>
<span data-ttu-id="50f42-122">Az IPSec-integritási algoritmus (IKE-fázis 1)</span><span class="sxs-lookup"><span data-stu-id="50f42-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="50f42-123">-PfsGroup</span></span>
<span data-ttu-id="50f42-124">Az IKE Phase 2 for New Child SA által használt DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="50f42-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="50f42-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="50f42-126">Az IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) hasznos tárterülete KB-ban</span><span class="sxs-lookup"><span data-stu-id="50f42-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="50f42-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="50f42-128">Az IPSec biztonsági társítás (más néven Quick Mode vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="50f42-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f42-129">CommonParameters</span></span>
<span data-ttu-id="50f42-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50f42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f42-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f42-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f42-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50f42-132">INPUTS</span></span>

### <span data-ttu-id="50f42-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="50f42-133">None</span></span>

## <span data-ttu-id="50f42-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50f42-134">OUTPUTS</span></span>

### <span data-ttu-id="50f42-135">Microsoft. Azure. commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="50f42-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="50f42-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50f42-136">NOTES</span></span>

## <span data-ttu-id="50f42-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50f42-137">RELATED LINKS</span></span>

