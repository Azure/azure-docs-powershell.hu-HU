---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: c482f3e4e7882f32db3415a36aab0a0313c0085a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491909"
---
# <span data-ttu-id="f24f2-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f24f2-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f24f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f24f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f24f2-103">Módosítja egy alkalmazás-átjáró SSL-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="f24f2-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f24f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f24f2-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f24f2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f24f2-105">DESCRIPTION</span></span>
<span data-ttu-id="f24f2-106">A **set-AzureRmApplicationGatewaySslPolicy** parancsmag az alkalmazás-ÁTJÁRÓk SSL-házirendjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="f24f2-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="f24f2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f24f2-107">EXAMPLES</span></span>

### <span data-ttu-id="f24f2-108">1:</span><span class="sxs-lookup"><span data-stu-id="f24f2-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="f24f2-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f24f2-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f24f2-110">Ez a második parancs az SSL-házirendet az előre definiált és a házirend neve AppGwSslPolicy20170401 módosította.</span><span class="sxs-lookup"><span data-stu-id="f24f2-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="f24f2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f24f2-111">PARAMETERS</span></span>

### <span data-ttu-id="f24f2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f24f2-112">-ApplicationGateway</span></span>
<span data-ttu-id="f24f2-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f24f2-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f24f2-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="f24f2-114">-CipherSuite</span></span>
<span data-ttu-id="f24f2-115">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="f24f2-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="f24f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24f2-116">-DefaultProfile</span></span>
<span data-ttu-id="f24f2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f24f2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f24f2-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="f24f2-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="f24f2-119">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="f24f2-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="f24f2-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f24f2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f24f2-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="f24f2-121">TLSv1_0</span></span> 
- <span data-ttu-id="f24f2-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="f24f2-122">TLSv1_1</span></span> 
- <span data-ttu-id="f24f2-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="f24f2-123">TLSv1_2</span></span>

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

### <span data-ttu-id="f24f2-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="f24f2-124">-MinProtocolVersion</span></span>
<span data-ttu-id="f24f2-125">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="f24f2-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="f24f2-126">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="f24f2-126">-PolicyName</span></span>
<span data-ttu-id="f24f2-127">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="f24f2-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="f24f2-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="f24f2-128">-PolicyType</span></span>
<span data-ttu-id="f24f2-129">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="f24f2-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="f24f2-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f24f2-130">-Confirm</span></span>
<span data-ttu-id="f24f2-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f24f2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24f2-132">-WhatIf</span></span>
<span data-ttu-id="f24f2-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f24f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24f2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f24f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24f2-135">CommonParameters</span></span>
<span data-ttu-id="f24f2-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f24f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24f2-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f24f2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24f2-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f24f2-138">INPUTS</span></span>

### <span data-ttu-id="f24f2-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f24f2-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f24f2-140">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f24f2-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f24f2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f24f2-141">OUTPUTS</span></span>

### <span data-ttu-id="f24f2-142">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f24f2-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f24f2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f24f2-143">NOTES</span></span>
* <span data-ttu-id="f24f2-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="f24f2-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f24f2-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f24f2-145">RELATED LINKS</span></span>

[<span data-ttu-id="f24f2-146">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f24f2-146">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="f24f2-147">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f24f2-147">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


