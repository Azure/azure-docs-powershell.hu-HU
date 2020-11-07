---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850761"
---
# <span data-ttu-id="04b50-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04b50-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="04b50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04b50-102">SYNOPSIS</span></span>
<span data-ttu-id="04b50-103">Hitelesítési tanúsítvány kérése az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="04b50-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04b50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04b50-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04b50-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04b50-105">DESCRIPTION</span></span>
<span data-ttu-id="04b50-106">A **Get-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát kapja.</span><span class="sxs-lookup"><span data-stu-id="04b50-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="04b50-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04b50-107">EXAMPLES</span></span>

### <span data-ttu-id="04b50-108">1:</span><span class="sxs-lookup"><span data-stu-id="04b50-108">1:</span></span>
```

```

## <span data-ttu-id="04b50-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04b50-109">PARAMETERS</span></span>

### <span data-ttu-id="04b50-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04b50-110">-ApplicationGateway</span></span>
<span data-ttu-id="04b50-111">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag hitelesítő tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="04b50-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="04b50-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b50-112">-DefaultProfile</span></span>
<span data-ttu-id="04b50-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04b50-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04b50-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04b50-114">-Name</span></span>
<span data-ttu-id="04b50-115">Annak a hitelesítési tanúsítványnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="04b50-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="04b50-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b50-116">CommonParameters</span></span>
<span data-ttu-id="04b50-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04b50-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b50-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b50-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b50-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04b50-119">INPUTS</span></span>

### <span data-ttu-id="04b50-120">System. String</span><span class="sxs-lookup"><span data-stu-id="04b50-120">System.String</span></span>

## <span data-ttu-id="04b50-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04b50-121">OUTPUTS</span></span>

### <span data-ttu-id="04b50-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04b50-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="04b50-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04b50-123">NOTES</span></span>
* <span data-ttu-id="04b50-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="04b50-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="04b50-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04b50-125">RELATED LINKS</span></span>

[<span data-ttu-id="04b50-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04b50-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="04b50-127">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04b50-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="04b50-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04b50-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="04b50-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04b50-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


