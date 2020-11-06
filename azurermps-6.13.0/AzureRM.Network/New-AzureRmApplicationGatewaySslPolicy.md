---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 140bfd84d2758badc45a902e4ed14e027c5bca3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505352"
---
# <span data-ttu-id="cc410-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="cc410-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="cc410-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc410-102">SYNOPSIS</span></span>
<span data-ttu-id="cc410-103">SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cc410-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc410-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc410-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc410-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc410-105">DESCRIPTION</span></span>
<span data-ttu-id="cc410-106">A **New-AzureRmApplicationGatewaySslPolicy** parancsmag SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cc410-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="cc410-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc410-107">EXAMPLES</span></span>

### <span data-ttu-id="cc410-108">1:</span><span class="sxs-lookup"><span data-stu-id="cc410-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="cc410-109">Ez a parancs létrehoz egy egyéni házirendet.</span><span class="sxs-lookup"><span data-stu-id="cc410-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="cc410-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc410-110">PARAMETERS</span></span>

### <span data-ttu-id="cc410-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="cc410-111">-CipherSuite</span></span>
<span data-ttu-id="cc410-112">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="cc410-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc410-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc410-113">-DefaultProfile</span></span>
<span data-ttu-id="cc410-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc410-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc410-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="cc410-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="cc410-116">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="cc410-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="cc410-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cc410-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc410-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="cc410-118">TLSv1_0</span></span> 
- <span data-ttu-id="cc410-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="cc410-119">TLSv1_1</span></span> 
- <span data-ttu-id="cc410-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="cc410-120">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc410-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="cc410-121">-MinProtocolVersion</span></span>
<span data-ttu-id="cc410-122">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="cc410-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="cc410-123">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="cc410-123">-PolicyName</span></span>
<span data-ttu-id="cc410-124">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="cc410-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="cc410-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="cc410-125">-PolicyType</span></span>
<span data-ttu-id="cc410-126">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="cc410-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="cc410-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc410-127">-Confirm</span></span>
<span data-ttu-id="cc410-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc410-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc410-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc410-129">-WhatIf</span></span>
<span data-ttu-id="cc410-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc410-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc410-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc410-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc410-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc410-132">CommonParameters</span></span>
<span data-ttu-id="cc410-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc410-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc410-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc410-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc410-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc410-135">INPUTS</span></span>

### <span data-ttu-id="cc410-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc410-136">None</span></span>

## <span data-ttu-id="cc410-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc410-137">OUTPUTS</span></span>

### <span data-ttu-id="cc410-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="cc410-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="cc410-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc410-139">NOTES</span></span>
* <span data-ttu-id="cc410-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="cc410-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cc410-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc410-141">RELATED LINKS</span></span>

[<span data-ttu-id="cc410-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="cc410-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="cc410-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="cc410-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


