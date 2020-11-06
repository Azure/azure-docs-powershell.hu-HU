---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3887f8cdbc4256d39e76fc6b86ff9e9113385519
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506020"
---
# <span data-ttu-id="77b5c-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="77b5c-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="77b5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="77b5c-103">SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="77b5c-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77b5c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77b5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="77b5c-106">A **New-AzureRmApplicationGatewaySslPolicy** parancsmag SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="77b5c-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="77b5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="77b5c-107">EXAMPLES</span></span>

### <span data-ttu-id="77b5c-108">1:</span><span class="sxs-lookup"><span data-stu-id="77b5c-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="77b5c-109">Ez a parancs létrehoz egy egyéni házirendet.</span><span class="sxs-lookup"><span data-stu-id="77b5c-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="77b5c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77b5c-110">PARAMETERS</span></span>

### <span data-ttu-id="77b5c-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="77b5c-111">-CipherSuite</span></span>
<span data-ttu-id="77b5c-112">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="77b5c-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="77b5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b5c-113">-DefaultProfile</span></span>
<span data-ttu-id="77b5c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77b5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77b5c-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="77b5c-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="77b5c-116">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="77b5c-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="77b5c-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="77b5c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77b5c-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="77b5c-118">TLSv1_0</span></span> 
- <span data-ttu-id="77b5c-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="77b5c-119">TLSv1_1</span></span> 
- <span data-ttu-id="77b5c-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="77b5c-120">TLSv1_2</span></span>

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

### <span data-ttu-id="77b5c-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="77b5c-121">-MinProtocolVersion</span></span>
<span data-ttu-id="77b5c-122">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="77b5c-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5c-123">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="77b5c-123">-PolicyName</span></span>
<span data-ttu-id="77b5c-124">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="77b5c-124">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5c-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="77b5c-125">-PolicyType</span></span>
<span data-ttu-id="77b5c-126">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="77b5c-126">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77b5c-127">-Confirm</span></span>
<span data-ttu-id="77b5c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77b5c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b5c-129">-WhatIf</span></span>
<span data-ttu-id="77b5c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77b5c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77b5c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77b5c-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b5c-132">CommonParameters</span></span>
<span data-ttu-id="77b5c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77b5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b5c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b5c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b5c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77b5c-135">INPUTS</span></span>

### <span data-ttu-id="77b5c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="77b5c-136">System.String</span></span>

## <span data-ttu-id="77b5c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77b5c-137">OUTPUTS</span></span>

### <span data-ttu-id="77b5c-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="77b5c-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="77b5c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77b5c-139">NOTES</span></span>
* <span data-ttu-id="77b5c-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="77b5c-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="77b5c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77b5c-141">RELATED LINKS</span></span>

[<span data-ttu-id="77b5c-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="77b5c-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="77b5c-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="77b5c-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


