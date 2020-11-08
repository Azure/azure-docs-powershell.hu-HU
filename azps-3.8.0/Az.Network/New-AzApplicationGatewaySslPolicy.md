---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 758dddc18e029aadd1e3d548d613a07abd7fd565
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014776"
---
# <span data-ttu-id="06e86-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="06e86-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="06e86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06e86-102">SYNOPSIS</span></span>
<span data-ttu-id="06e86-103">SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="06e86-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="06e86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06e86-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e86-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06e86-105">DESCRIPTION</span></span>
<span data-ttu-id="06e86-106">A **New-AzApplicationGatewaySslPolicy** parancsmag SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="06e86-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="06e86-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06e86-107">EXAMPLES</span></span>

### <span data-ttu-id="06e86-108">1:</span><span class="sxs-lookup"><span data-stu-id="06e86-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="06e86-109">Ez a parancs létrehoz egy egyéni házirendet.</span><span class="sxs-lookup"><span data-stu-id="06e86-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="06e86-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06e86-110">PARAMETERS</span></span>

### <span data-ttu-id="06e86-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="06e86-111">-CipherSuite</span></span>
<span data-ttu-id="06e86-112">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="06e86-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="06e86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e86-113">-DefaultProfile</span></span>
<span data-ttu-id="06e86-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06e86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06e86-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="06e86-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="06e86-116">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="06e86-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="06e86-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="06e86-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06e86-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="06e86-118">TLSv1_0</span></span> 
- <span data-ttu-id="06e86-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="06e86-119">TLSv1_1</span></span> 
- <span data-ttu-id="06e86-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="06e86-120">TLSv1_2</span></span>

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

### <span data-ttu-id="06e86-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="06e86-121">-MinProtocolVersion</span></span>
<span data-ttu-id="06e86-122">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="06e86-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="06e86-123">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="06e86-123">-PolicyName</span></span>
<span data-ttu-id="06e86-124">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="06e86-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="06e86-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="06e86-125">-PolicyType</span></span>
<span data-ttu-id="06e86-126">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="06e86-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="06e86-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06e86-127">-Confirm</span></span>
<span data-ttu-id="06e86-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06e86-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e86-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e86-129">-WhatIf</span></span>
<span data-ttu-id="06e86-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06e86-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e86-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06e86-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e86-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e86-132">CommonParameters</span></span>
<span data-ttu-id="06e86-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06e86-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e86-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e86-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e86-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06e86-135">INPUTS</span></span>

### <span data-ttu-id="06e86-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="06e86-136">None</span></span>

## <span data-ttu-id="06e86-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06e86-137">OUTPUTS</span></span>

### <span data-ttu-id="06e86-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="06e86-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="06e86-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06e86-139">NOTES</span></span>
* <span data-ttu-id="06e86-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="06e86-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="06e86-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06e86-141">RELATED LINKS</span></span>

[<span data-ttu-id="06e86-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="06e86-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="06e86-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="06e86-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


