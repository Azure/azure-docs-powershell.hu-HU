---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302751"
---
# <span data-ttu-id="504b1-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="504b1-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="504b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="504b1-102">SYNOPSIS</span></span>
<span data-ttu-id="504b1-103">SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="504b1-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="504b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="504b1-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="504b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="504b1-105">DESCRIPTION</span></span>
<span data-ttu-id="504b1-106">A **New-AzApplicationGatewaySslPolicy** parancsmag SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="504b1-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="504b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="504b1-107">EXAMPLES</span></span>

### <span data-ttu-id="504b1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="504b1-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="504b1-109">Ez a parancs létrehoz egy egyéni házirendet.</span><span class="sxs-lookup"><span data-stu-id="504b1-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="504b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="504b1-110">PARAMETERS</span></span>

### <span data-ttu-id="504b1-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="504b1-111">-CipherSuite</span></span>
<span data-ttu-id="504b1-112">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="504b1-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504b1-113">-DefaultProfile</span></span>
<span data-ttu-id="504b1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="504b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="504b1-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="504b1-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="504b1-116">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="504b1-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="504b1-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="504b1-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="504b1-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="504b1-118">TLSv1_0</span></span> 
- <span data-ttu-id="504b1-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="504b1-119">TLSv1_1</span></span> 
- <span data-ttu-id="504b1-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="504b1-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="504b1-121">-MinProtocolVersion</span></span>
<span data-ttu-id="504b1-122">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="504b1-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-123">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="504b1-123">-PolicyName</span></span>
<span data-ttu-id="504b1-124">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="504b1-124">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="504b1-125">-PolicyType</span></span>
<span data-ttu-id="504b1-126">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="504b1-126">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="504b1-127">-Confirm</span></span>
<span data-ttu-id="504b1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="504b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="504b1-129">-WhatIf</span></span>
<span data-ttu-id="504b1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="504b1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="504b1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="504b1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504b1-132">CommonParameters</span></span>
<span data-ttu-id="504b1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="504b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504b1-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="504b1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504b1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="504b1-135">INPUTS</span></span>

### <span data-ttu-id="504b1-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="504b1-136">None</span></span>

## <span data-ttu-id="504b1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="504b1-137">OUTPUTS</span></span>

### <span data-ttu-id="504b1-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="504b1-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="504b1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="504b1-139">NOTES</span></span>
* <span data-ttu-id="504b1-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="504b1-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="504b1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="504b1-141">RELATED LINKS</span></span>

[<span data-ttu-id="504b1-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="504b1-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="504b1-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="504b1-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


