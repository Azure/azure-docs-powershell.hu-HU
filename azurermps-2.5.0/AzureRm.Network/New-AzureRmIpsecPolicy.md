---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
ms.openlocfilehash: 642284e7e1aa732983ee660ea323707be030b640
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849134"
---
# <span data-ttu-id="90737-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="90737-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="90737-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90737-102">SYNOPSIS</span></span>
<span data-ttu-id="90737-103">IPSec-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="90737-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90737-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90737-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90737-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90737-105">DESCRIPTION</span></span>
<span data-ttu-id="90737-106">Az New-AzureRmIpsecPolicy parancsmag létrehoz egy olyan IPSec-házirend-javaslatot, amelyet a virtuális hálózati átjáró-kapcsolathoz kell használni.</span><span class="sxs-lookup"><span data-stu-id="90737-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="90737-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90737-107">EXAMPLES</span></span>

### <span data-ttu-id="90737-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="90737-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="90737-109">Új virtuális hálózati átjáró-kapcsolathoz használandó IPSec-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="90737-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="90737-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90737-110">PARAMETERS</span></span>

### <span data-ttu-id="90737-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90737-111">-DefaultProfile</span></span>
<span data-ttu-id="90737-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90737-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90737-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="90737-113">-DhGroup</span></span>
<span data-ttu-id="90737-114">A kezdeti biztonsági társításhoz az IKE-fázis 1-es verziójában használt DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="90737-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="90737-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="90737-115">-IkeEncryption</span></span>
<span data-ttu-id="90737-116">Az IKE titkosítási algoritmusa (IKE 2 fázis)</span><span class="sxs-lookup"><span data-stu-id="90737-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="90737-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="90737-117">-IkeIntegrity</span></span>
<span data-ttu-id="90737-118">Az IKE Integrity algoritmusa (IKE 2 fázis)</span><span class="sxs-lookup"><span data-stu-id="90737-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="90737-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="90737-119">-IpsecEncryption</span></span>
<span data-ttu-id="90737-120">Az IPSec titkosítási algoritmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="90737-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="90737-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="90737-121">-IpsecIntegrity</span></span>
<span data-ttu-id="90737-122">Az IPSec-integritási algoritmus (IKE-fázis 1)</span><span class="sxs-lookup"><span data-stu-id="90737-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="90737-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="90737-123">-PfsGroup</span></span>
<span data-ttu-id="90737-124">Az IKE Phase 2 for New Child SA által használt DH-csoportok</span><span class="sxs-lookup"><span data-stu-id="90737-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="90737-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="90737-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="90737-126">Az IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) hasznos tárterülete KB-ban</span><span class="sxs-lookup"><span data-stu-id="90737-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="90737-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="90737-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="90737-128">Az IPSec biztonsági társítás (más néven Quick Mode vagy Phase 2 SA) élettartama másodpercben</span><span class="sxs-lookup"><span data-stu-id="90737-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="90737-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90737-129">CommonParameters</span></span>
<span data-ttu-id="90737-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90737-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90737-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90737-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90737-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90737-132">INPUTS</span></span>

### <span data-ttu-id="90737-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="90737-133">None</span></span>

## <span data-ttu-id="90737-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90737-134">OUTPUTS</span></span>

### <span data-ttu-id="90737-135">Microsoft. Azure. commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="90737-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="90737-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90737-136">NOTES</span></span>

## <span data-ttu-id="90737-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90737-137">RELATED LINKS</span></span>

