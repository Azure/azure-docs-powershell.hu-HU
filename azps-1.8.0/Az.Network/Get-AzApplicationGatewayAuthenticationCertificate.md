---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670677"
---
# <span data-ttu-id="d81fa-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d81fa-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d81fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d81fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d81fa-103">Hitelesítési tanúsítvány kérése az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d81fa-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="d81fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d81fa-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d81fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d81fa-105">DESCRIPTION</span></span>
<span data-ttu-id="d81fa-106">A **Get-AzApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát kapja.</span><span class="sxs-lookup"><span data-stu-id="d81fa-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d81fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d81fa-107">EXAMPLES</span></span>

### <span data-ttu-id="d81fa-108">1. példa: meghatározott hitelesítési tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="d81fa-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="d81fa-109">Az első parancs a appGwName nevű alkalmazás-átjárót kapja meg, és a $appgw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d81fa-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="d81fa-110">A második parancs megkapja a pool01 nevű hitelesítési tanúsítványt, és a $pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d81fa-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="d81fa-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d81fa-111">PARAMETERS</span></span>

### <span data-ttu-id="d81fa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81fa-112">-ApplicationGateway</span></span>
<span data-ttu-id="d81fa-113">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag hitelesítő tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="d81fa-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="d81fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81fa-114">-DefaultProfile</span></span>
<span data-ttu-id="d81fa-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d81fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d81fa-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d81fa-116">-Name</span></span>
<span data-ttu-id="d81fa-117">Annak a hitelesítési tanúsítványnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d81fa-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d81fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81fa-118">CommonParameters</span></span>
<span data-ttu-id="d81fa-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d81fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81fa-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d81fa-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81fa-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d81fa-121">INPUTS</span></span>

### <span data-ttu-id="d81fa-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81fa-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d81fa-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d81fa-123">OUTPUTS</span></span>

### <span data-ttu-id="d81fa-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d81fa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d81fa-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d81fa-125">NOTES</span></span>
* <span data-ttu-id="d81fa-126">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="d81fa-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d81fa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d81fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="d81fa-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d81fa-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d81fa-129">Új – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d81fa-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d81fa-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d81fa-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d81fa-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d81fa-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


