---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: b8b9eadd0beba6413b8b5919087a1c9081735ddf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015046"
---
# <span data-ttu-id="37a48-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="37a48-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="37a48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37a48-102">SYNOPSIS</span></span>
<span data-ttu-id="37a48-103">SSL-házirendet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="37a48-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="37a48-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37a48-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37a48-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37a48-105">DESCRIPTION</span></span>
<span data-ttu-id="37a48-106">A **New-AzApplicationGatewaySslPolicy** parancsmag ssl-házirendet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="37a48-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="37a48-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37a48-107">EXAMPLES</span></span>

### <span data-ttu-id="37a48-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="37a48-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="37a48-109">Ez a parancs egyéni házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="37a48-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="37a48-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37a48-110">PARAMETERS</span></span>

### <span data-ttu-id="37a48-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="37a48-111">-CipherSuite</span></span>
<span data-ttu-id="37a48-112">Ssl cipher suites to be enabled in the specified order to application gateway</span><span class="sxs-lookup"><span data-stu-id="37a48-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="37a48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a48-113">-DefaultProfile</span></span>
<span data-ttu-id="37a48-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37a48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37a48-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="37a48-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="37a48-116">Azt adja meg, hogy mely protokollok vannak letiltva.</span><span class="sxs-lookup"><span data-stu-id="37a48-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="37a48-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="37a48-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37a48-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="37a48-118">TLSv1_0</span></span> 
- <span data-ttu-id="37a48-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="37a48-119">TLSv1_1</span></span> 
- <span data-ttu-id="37a48-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="37a48-120">TLSv1_2</span></span>

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

### <span data-ttu-id="37a48-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="37a48-121">-MinProtocolVersion</span></span>
<span data-ttu-id="37a48-122">Az Ssl-protokoll minimális verziója, amelyet az alkalmazás-átjáró támogat</span><span class="sxs-lookup"><span data-stu-id="37a48-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="37a48-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="37a48-123">-PolicyName</span></span>
<span data-ttu-id="37a48-124">Az Ssl előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="37a48-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="37a48-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="37a48-125">-PolicyType</span></span>
<span data-ttu-id="37a48-126">Az Ssl-házirend típusa</span><span class="sxs-lookup"><span data-stu-id="37a48-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="37a48-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37a48-127">-Confirm</span></span>
<span data-ttu-id="37a48-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37a48-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a48-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37a48-129">-WhatIf</span></span>
<span data-ttu-id="37a48-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37a48-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37a48-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37a48-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a48-132">CommonParameters</span></span>
<span data-ttu-id="37a48-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a48-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a48-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a48-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37a48-135">INPUTS</span></span>

### <span data-ttu-id="37a48-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="37a48-136">None</span></span>

## <span data-ttu-id="37a48-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37a48-137">OUTPUTS</span></span>

### <span data-ttu-id="37a48-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="37a48-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="37a48-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37a48-139">NOTES</span></span>
* <span data-ttu-id="37a48-140">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="37a48-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="37a48-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37a48-141">RELATED LINKS</span></span>

[<span data-ttu-id="37a48-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="37a48-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="37a48-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="37a48-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


