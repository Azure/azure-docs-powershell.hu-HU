---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499780"
---
# <span data-ttu-id="6466f-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6466f-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="6466f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6466f-102">SYNOPSIS</span></span>
<span data-ttu-id="6466f-103">Hitelesítési tanúsítvány kérése az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6466f-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6466f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6466f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6466f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6466f-105">DESCRIPTION</span></span>
<span data-ttu-id="6466f-106">A **Get-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát kapja.</span><span class="sxs-lookup"><span data-stu-id="6466f-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="6466f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6466f-107">EXAMPLES</span></span>

## <span data-ttu-id="6466f-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6466f-108">PARAMETERS</span></span>

### <span data-ttu-id="6466f-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6466f-109">-ApplicationGateway</span></span>
<span data-ttu-id="6466f-110">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag hitelesítő tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="6466f-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="6466f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6466f-111">-DefaultProfile</span></span>
<span data-ttu-id="6466f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6466f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6466f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6466f-113">-Name</span></span>
<span data-ttu-id="6466f-114">Annak a hitelesítési tanúsítványnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="6466f-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6466f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6466f-115">CommonParameters</span></span>
<span data-ttu-id="6466f-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6466f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6466f-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6466f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6466f-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6466f-118">INPUTS</span></span>

### <span data-ttu-id="6466f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="6466f-119">System.String</span></span>

## <span data-ttu-id="6466f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6466f-120">OUTPUTS</span></span>

### <span data-ttu-id="6466f-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6466f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="6466f-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6466f-122">NOTES</span></span>
* <span data-ttu-id="6466f-123">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="6466f-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6466f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6466f-124">RELATED LINKS</span></span>

[<span data-ttu-id="6466f-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6466f-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6466f-126">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6466f-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6466f-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6466f-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6466f-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6466f-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


