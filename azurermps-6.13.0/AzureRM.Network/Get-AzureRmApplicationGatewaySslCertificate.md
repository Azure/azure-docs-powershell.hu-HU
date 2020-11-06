---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: e957ef203d0bf90393e523cca41b949a9d99acc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501143"
---
# <span data-ttu-id="c8581-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8581-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c8581-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8581-102">SYNOPSIS</span></span>
<span data-ttu-id="c8581-103">SSL-tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c8581-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8581-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8581-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8581-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8581-105">DESCRIPTION</span></span>
<span data-ttu-id="c8581-106">A **Get-AzureRmApplicationGatewaySslCertificate** parancsmag SSL-tanúsítványt kap az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c8581-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="c8581-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8581-107">EXAMPLES</span></span>

### <span data-ttu-id="c8581-108">1. példa: adott SSL-tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="c8581-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c8581-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c8581-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c8581-110">A második parancs a Cert01 nevű SSL-tanúsítványt kapja meg az $AppGW nevű változóban tárolt alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="c8581-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="c8581-111">A parancs a $Cert nevű változóban tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c8581-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="c8581-112">2. példa: az SSL-tanúsítványok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c8581-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="c8581-113">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c8581-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c8581-114">Ez a második parancs a $AppGW nevű változóban tárolt alkalmazás-átjáróból kapja meg az SSL-tanúsítványok listáját.</span><span class="sxs-lookup"><span data-stu-id="c8581-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="c8581-115">A parancs ezután a $Certs nevű változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="c8581-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="c8581-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8581-116">PARAMETERS</span></span>

### <span data-ttu-id="c8581-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8581-117">-ApplicationGateway</span></span>
<span data-ttu-id="c8581-118">Az SSL-tanúsítványt tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="c8581-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="c8581-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8581-119">-DefaultProfile</span></span>
<span data-ttu-id="c8581-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8581-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8581-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8581-121">-Name</span></span>
<span data-ttu-id="c8581-122">Annak az SSL-tanúsítványtárolónak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="c8581-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8581-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8581-123">CommonParameters</span></span>
<span data-ttu-id="c8581-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8581-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8581-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8581-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8581-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8581-126">INPUTS</span></span>

### <span data-ttu-id="c8581-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8581-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="c8581-128">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8581-128">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="c8581-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8581-129">OUTPUTS</span></span>

### <span data-ttu-id="c8581-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8581-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c8581-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8581-131">NOTES</span></span>

## <span data-ttu-id="c8581-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8581-132">RELATED LINKS</span></span>

[<span data-ttu-id="c8581-133">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8581-133">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c8581-134">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8581-134">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c8581-135">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8581-135">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c8581-136">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8581-136">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


