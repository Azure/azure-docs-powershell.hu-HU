---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: dc6dc0c201ebb8298805064e06af5bb6c63ceda8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495545"
---
# <span data-ttu-id="4c79d-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4c79d-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4c79d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c79d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c79d-103">SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4c79d-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c79d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c79d-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c79d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c79d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c79d-106">A **New-AzureRmApplicationGatewaySslPolicy** parancsmag SSL-házirendet hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4c79d-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="4c79d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4c79d-107">EXAMPLES</span></span>

### <span data-ttu-id="4c79d-108">1:</span><span class="sxs-lookup"><span data-stu-id="4c79d-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="4c79d-109">Ez a parancs létrehoz egy egyéni házirendet.</span><span class="sxs-lookup"><span data-stu-id="4c79d-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="4c79d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c79d-110">PARAMETERS</span></span>

### <span data-ttu-id="4c79d-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="4c79d-111">-CipherSuite</span></span>
<span data-ttu-id="4c79d-112">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="4c79d-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="4c79d-113">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="4c79d-113">-DisabledSslProtocols</span></span>
<span data-ttu-id="4c79d-114">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="4c79d-114">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="4c79d-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4c79d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c79d-116">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="4c79d-116">TLSv1_0</span></span> 
- <span data-ttu-id="4c79d-117">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="4c79d-117">TLSv1_1</span></span> 
- <span data-ttu-id="4c79d-118">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="4c79d-118">TLSv1_2</span></span>

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

### <span data-ttu-id="4c79d-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="4c79d-119">-MinProtocolVersion</span></span>
<span data-ttu-id="4c79d-120">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="4c79d-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="4c79d-121">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="4c79d-121">-PolicyName</span></span>
<span data-ttu-id="4c79d-122">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="4c79d-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="4c79d-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="4c79d-123">-PolicyType</span></span>
<span data-ttu-id="4c79d-124">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="4c79d-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="4c79d-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c79d-125">-Confirm</span></span>
<span data-ttu-id="4c79d-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c79d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c79d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c79d-127">-WhatIf</span></span>
<span data-ttu-id="4c79d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c79d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c79d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c79d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c79d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c79d-130">-DefaultProfile</span></span>
<span data-ttu-id="4c79d-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c79d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c79d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c79d-132">CommonParameters</span></span>
<span data-ttu-id="4c79d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c79d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c79d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c79d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c79d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c79d-135">INPUTS</span></span>

### <span data-ttu-id="4c79d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4c79d-136">System.String</span></span>

## <span data-ttu-id="4c79d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c79d-137">OUTPUTS</span></span>

### <span data-ttu-id="4c79d-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4c79d-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4c79d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c79d-139">NOTES</span></span>
* <span data-ttu-id="4c79d-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="4c79d-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4c79d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c79d-141">RELATED LINKS</span></span>

[<span data-ttu-id="4c79d-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4c79d-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4c79d-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4c79d-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


