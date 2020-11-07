---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848766"
---
# <span data-ttu-id="28929-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="28929-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="28929-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28929-102">SYNOPSIS</span></span>
<span data-ttu-id="28929-103">Hitelesítési tanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="28929-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28929-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28929-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28929-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28929-105">DESCRIPTION</span></span>
<span data-ttu-id="28929-106">A **Remove-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway-ből távolítja el a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="28929-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="28929-107">Példák</span><span class="sxs-lookup"><span data-stu-id="28929-107">EXAMPLES</span></span>

### <span data-ttu-id="28929-108">1:</span><span class="sxs-lookup"><span data-stu-id="28929-108">1:</span></span>
```

```

## <span data-ttu-id="28929-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28929-109">PARAMETERS</span></span>

### <span data-ttu-id="28929-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28929-110">-ApplicationGateway</span></span>
<span data-ttu-id="28929-111">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja a hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="28929-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="28929-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28929-112">-DefaultProfile</span></span>
<span data-ttu-id="28929-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28929-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28929-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28929-114">-Name</span></span>
<span data-ttu-id="28929-115">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="28929-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28929-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28929-116">-Confirm</span></span>
<span data-ttu-id="28929-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28929-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28929-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28929-118">-WhatIf</span></span>
<span data-ttu-id="28929-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28929-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28929-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28929-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28929-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28929-121">CommonParameters</span></span>
<span data-ttu-id="28929-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28929-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28929-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28929-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28929-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28929-124">INPUTS</span></span>

### <span data-ttu-id="28929-125">System. String</span><span class="sxs-lookup"><span data-stu-id="28929-125">System.String</span></span>

## <span data-ttu-id="28929-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28929-126">OUTPUTS</span></span>

### <span data-ttu-id="28929-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28929-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="28929-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28929-128">NOTES</span></span>
* <span data-ttu-id="28929-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="28929-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="28929-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28929-130">RELATED LINKS</span></span>

[<span data-ttu-id="28929-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="28929-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="28929-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="28929-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="28929-133">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="28929-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="28929-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="28929-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


