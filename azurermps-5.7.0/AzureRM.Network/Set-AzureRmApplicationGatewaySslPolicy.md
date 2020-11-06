---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 7ab968539cb57568540a0e1c60f59b36d6de79ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493725"
---
# <span data-ttu-id="e5a18-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a18-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e5a18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5a18-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a18-103">Módosítja egy alkalmazás-átjáró SSL-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="e5a18-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5a18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5a18-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5a18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5a18-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a18-106">A **set-AzureRmApplicationGatewaySslPolicy** parancsmag az alkalmazás-ÁTJÁRÓk SSL-házirendjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="e5a18-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e5a18-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5a18-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a18-108">1:</span><span class="sxs-lookup"><span data-stu-id="e5a18-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="e5a18-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5a18-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e5a18-110">Ez a második parancs az SSL-házirendet az előre definiált és a házirend neve AppGwSslPolicy20170401 módosította.</span><span class="sxs-lookup"><span data-stu-id="e5a18-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="e5a18-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5a18-111">PARAMETERS</span></span>

### <span data-ttu-id="e5a18-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-112">-ApplicationGateway</span></span>
<span data-ttu-id="e5a18-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="e5a18-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a18-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="e5a18-114">-CipherSuite</span></span>
<span data-ttu-id="e5a18-115">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="e5a18-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="e5a18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a18-116">-DefaultProfile</span></span>
<span data-ttu-id="e5a18-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5a18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5a18-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="e5a18-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="e5a18-119">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="e5a18-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="e5a18-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e5a18-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5a18-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="e5a18-121">TLSv1_0</span></span> 
- <span data-ttu-id="e5a18-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="e5a18-122">TLSv1_1</span></span> 
- <span data-ttu-id="e5a18-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="e5a18-123">TLSv1_2</span></span>

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

### <span data-ttu-id="e5a18-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="e5a18-124">-MinProtocolVersion</span></span>
<span data-ttu-id="e5a18-125">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="e5a18-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="e5a18-126">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="e5a18-126">-PolicyName</span></span>
<span data-ttu-id="e5a18-127">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="e5a18-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="e5a18-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="e5a18-128">-PolicyType</span></span>
<span data-ttu-id="e5a18-129">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="e5a18-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="e5a18-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5a18-130">-Confirm</span></span>
<span data-ttu-id="e5a18-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5a18-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a18-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a18-132">-WhatIf</span></span>
<span data-ttu-id="e5a18-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5a18-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a18-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5a18-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a18-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a18-135">CommonParameters</span></span>
<span data-ttu-id="e5a18-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5a18-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a18-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a18-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a18-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5a18-138">INPUTS</span></span>

### <span data-ttu-id="e5a18-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a18-139">System.String</span></span>

## <span data-ttu-id="e5a18-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5a18-140">OUTPUTS</span></span>

### <span data-ttu-id="e5a18-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5a18-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5a18-142">NOTES</span></span>
* <span data-ttu-id="e5a18-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="e5a18-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e5a18-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5a18-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5a18-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a18-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e5a18-146">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a18-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


