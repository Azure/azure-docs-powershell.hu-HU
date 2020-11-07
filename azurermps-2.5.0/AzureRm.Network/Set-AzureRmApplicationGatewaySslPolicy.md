---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 1e0d5de8013bbb6fd5104c3af5bdb555b0317e75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848101"
---
# <span data-ttu-id="02131-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="02131-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="02131-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02131-102">SYNOPSIS</span></span>
<span data-ttu-id="02131-103">Módosítja egy alkalmazás-átjáró SSL-házirendjét.</span><span class="sxs-lookup"><span data-stu-id="02131-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02131-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02131-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02131-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02131-105">DESCRIPTION</span></span>
<span data-ttu-id="02131-106">A **set-AzureRmApplicationGatewaySslPolicy** parancsmag az alkalmazás-ÁTJÁRÓk SSL-házirendjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="02131-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="02131-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02131-107">EXAMPLES</span></span>

### <span data-ttu-id="02131-108">1:</span><span class="sxs-lookup"><span data-stu-id="02131-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="02131-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02131-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="02131-110">Ez a második parancs az SSL-házirendet az előre definiált és a házirend neve AppGwSslPolicy20170401 módosította.</span><span class="sxs-lookup"><span data-stu-id="02131-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="02131-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02131-111">PARAMETERS</span></span>

### <span data-ttu-id="02131-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02131-112">-ApplicationGateway</span></span>
<span data-ttu-id="02131-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="02131-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="02131-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="02131-114">-CipherSuite</span></span>
<span data-ttu-id="02131-115">Az SSL-titkosítási lakosztályok engedélyezve vannak a megadott sorrendben az Application Gateway számára</span><span class="sxs-lookup"><span data-stu-id="02131-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="02131-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02131-116">-DefaultProfile</span></span>
<span data-ttu-id="02131-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02131-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02131-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="02131-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="02131-119">Meghatározza, hogy mely protokollok le vannak tiltva.</span><span class="sxs-lookup"><span data-stu-id="02131-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="02131-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="02131-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02131-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="02131-121">TLSv1_0</span></span> 
- <span data-ttu-id="02131-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="02131-122">TLSv1_1</span></span> 
- <span data-ttu-id="02131-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="02131-123">TLSv1_2</span></span>

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

### <span data-ttu-id="02131-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="02131-124">-MinProtocolVersion</span></span>
<span data-ttu-id="02131-125">Az alkalmazás-átjáróban támogatott SSL-protokoll minimális verziója</span><span class="sxs-lookup"><span data-stu-id="02131-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="02131-126">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="02131-126">-PolicyName</span></span>
<span data-ttu-id="02131-127">Az SSL előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="02131-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="02131-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="02131-128">-PolicyType</span></span>
<span data-ttu-id="02131-129">Az SSL-házirendek típusa</span><span class="sxs-lookup"><span data-stu-id="02131-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="02131-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02131-130">-Confirm</span></span>
<span data-ttu-id="02131-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02131-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02131-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02131-132">-WhatIf</span></span>
<span data-ttu-id="02131-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02131-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02131-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02131-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02131-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02131-135">CommonParameters</span></span>
<span data-ttu-id="02131-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02131-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02131-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02131-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02131-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02131-138">INPUTS</span></span>

### <span data-ttu-id="02131-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02131-139">System.String</span></span>

## <span data-ttu-id="02131-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02131-140">OUTPUTS</span></span>

### <span data-ttu-id="02131-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02131-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02131-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02131-142">NOTES</span></span>
* <span data-ttu-id="02131-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="02131-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="02131-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02131-144">RELATED LINKS</span></span>

[<span data-ttu-id="02131-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="02131-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="02131-146">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="02131-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


