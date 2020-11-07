---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 6e2dceadf11323eb1798435df426c063f4d58858
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850737"
---
# <span data-ttu-id="baf1d-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="baf1d-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="baf1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="baf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="baf1d-103">SSL-tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="baf1d-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baf1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="baf1d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baf1d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="baf1d-105">DESCRIPTION</span></span>
<span data-ttu-id="baf1d-106">A **Get-AzureRmApplicationGatewaySslCertificate** parancsmag SSL-tanúsítványt kap az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="baf1d-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="baf1d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="baf1d-107">EXAMPLES</span></span>

### <span data-ttu-id="baf1d-108">1. példa: adott SSL-tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="baf1d-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="baf1d-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="baf1d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="baf1d-110">A második parancs a Cert01 nevű SSL-tanúsítványt kapja meg az $AppGW nevű változóban tárolt alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="baf1d-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="baf1d-111">A parancs a $Cert nevű változóban tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="baf1d-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="baf1d-112">2. példa: az SSL-tanúsítványok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="baf1d-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="baf1d-113">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="baf1d-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="baf1d-114">Ez a második parancs a $AppGW nevű változóban tárolt alkalmazás-átjáróból kapja meg az SSL-tanúsítványok listáját.</span><span class="sxs-lookup"><span data-stu-id="baf1d-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="baf1d-115">A parancs ezután a $Certs nevű változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="baf1d-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="baf1d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="baf1d-116">PARAMETERS</span></span>

### <span data-ttu-id="baf1d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="baf1d-117">-ApplicationGateway</span></span>
<span data-ttu-id="baf1d-118">Az SSL-tanúsítványt tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="baf1d-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="baf1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf1d-119">-DefaultProfile</span></span>
<span data-ttu-id="baf1d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baf1d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf1d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="baf1d-121">-Name</span></span>
<span data-ttu-id="baf1d-122">Annak az SSL-tanúsítványtárolónak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="baf1d-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="baf1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf1d-123">CommonParameters</span></span>
<span data-ttu-id="baf1d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="baf1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf1d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf1d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf1d-126">INPUTS</span></span>

### <span data-ttu-id="baf1d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="baf1d-127">System.String</span></span>

## <span data-ttu-id="baf1d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf1d-128">OUTPUTS</span></span>

### <span data-ttu-id="baf1d-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="baf1d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="baf1d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="baf1d-130">NOTES</span></span>

## <span data-ttu-id="baf1d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baf1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="baf1d-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="baf1d-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="baf1d-133">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="baf1d-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="baf1d-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="baf1d-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="baf1d-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="baf1d-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


