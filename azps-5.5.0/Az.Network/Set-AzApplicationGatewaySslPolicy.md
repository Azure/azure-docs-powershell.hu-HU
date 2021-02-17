---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 06b8f7bdaea4ebf11ff901fbe53be94f74c9bba7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156762"
---
# <span data-ttu-id="80303-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="80303-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="80303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80303-102">SYNOPSIS</span></span>
<span data-ttu-id="80303-103">Módosítja egy alkalmazás-átjáró SSL-házirendét.</span><span class="sxs-lookup"><span data-stu-id="80303-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="80303-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80303-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80303-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80303-105">DESCRIPTION</span></span>
<span data-ttu-id="80303-106">A **Set-AzApplicationGatewaySslPolicy** parancsmag módosítja egy alkalmazás-átjáró SSL-házirendét.</span><span class="sxs-lookup"><span data-stu-id="80303-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="80303-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80303-107">EXAMPLES</span></span>

### <span data-ttu-id="80303-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="80303-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="80303-109">Az első parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="80303-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="80303-110">Ez a második parancs módosítja az ssl-házirendet egy Előre definiált és Az AppGwSslPolicy20170401 házirendnévre.</span><span class="sxs-lookup"><span data-stu-id="80303-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="80303-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80303-111">PARAMETERS</span></span>

### <span data-ttu-id="80303-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80303-112">-ApplicationGateway</span></span>
<span data-ttu-id="80303-113">Annak az SSL-házirendnek az alkalmazás-átjáróját adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="80303-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80303-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="80303-114">-CipherSuite</span></span>
<span data-ttu-id="80303-115">Ssl cipher suites to be enabled in the specified order to application gateway</span><span class="sxs-lookup"><span data-stu-id="80303-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="80303-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80303-116">-DefaultProfile</span></span>
<span data-ttu-id="80303-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80303-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80303-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="80303-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="80303-119">Meghatározza, hogy mely protokollok vannak letiltva.</span><span class="sxs-lookup"><span data-stu-id="80303-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="80303-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="80303-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80303-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="80303-121">TLSv1_0</span></span> 
- <span data-ttu-id="80303-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="80303-122">TLSv1_1</span></span> 
- <span data-ttu-id="80303-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="80303-123">TLSv1_2</span></span>

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

### <span data-ttu-id="80303-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="80303-124">-MinProtocolVersion</span></span>
<span data-ttu-id="80303-125">Az Ssl-protokoll minimális verziója, amelyet az alkalmazás-átjáró támogat</span><span class="sxs-lookup"><span data-stu-id="80303-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="80303-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="80303-126">-PolicyName</span></span>
<span data-ttu-id="80303-127">Az Ssl előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="80303-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="80303-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="80303-128">-PolicyType</span></span>
<span data-ttu-id="80303-129">Az Ssl-házirend típusa</span><span class="sxs-lookup"><span data-stu-id="80303-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="80303-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80303-130">-Confirm</span></span>
<span data-ttu-id="80303-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="80303-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80303-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80303-132">-WhatIf</span></span>
<span data-ttu-id="80303-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="80303-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80303-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80303-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80303-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80303-135">CommonParameters</span></span>
<span data-ttu-id="80303-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80303-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80303-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80303-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80303-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80303-138">INPUTS</span></span>

### <span data-ttu-id="80303-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80303-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80303-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80303-140">OUTPUTS</span></span>

### <span data-ttu-id="80303-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80303-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80303-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80303-142">NOTES</span></span>
* <span data-ttu-id="80303-143">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="80303-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="80303-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80303-144">RELATED LINKS</span></span>

[<span data-ttu-id="80303-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="80303-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="80303-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="80303-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


