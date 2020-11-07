---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841717"
---
# <span data-ttu-id="5e9f8-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f8-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5e9f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9f8-103">SSL-tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="5e9f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e9f8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9f8-106">A **Get-AzApplicationGatewaySslCertificate** parancsmag SSL-tanúsítványt kap az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="5e9f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5e9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="5e9f8-108">1. példa: adott SSL-tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="5e9f8-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="5e9f8-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5e9f8-110">A második parancs a Cert01 nevű SSL-tanúsítványt kapja meg az $AppGW nevű változóban tárolt alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="5e9f8-111">A parancs a $Cert nevű változóban tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="5e9f8-112">2. példa: az SSL-tanúsítványok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5e9f8-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="5e9f8-113">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5e9f8-114">Ez a második parancs a $AppGW nevű változóban tárolt alkalmazás-átjáróból kapja meg az SSL-tanúsítványok listáját.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="5e9f8-115">A parancs ezután a $Certs nevű változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="5e9f8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e9f8-116">PARAMETERS</span></span>

### <span data-ttu-id="5e9f8-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e9f8-117">-ApplicationGateway</span></span>
<span data-ttu-id="5e9f8-118">Az SSL-tanúsítványt tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="5e9f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9f8-119">-DefaultProfile</span></span>
<span data-ttu-id="5e9f8-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9f8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e9f8-121">-Name</span></span>
<span data-ttu-id="5e9f8-122">Annak az SSL-tanúsítványtárolónak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="5e9f8-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5e9f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9f8-123">CommonParameters</span></span>
<span data-ttu-id="5e9f8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e9f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9f8-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9f8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9f8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e9f8-126">INPUTS</span></span>

### <span data-ttu-id="5e9f8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5e9f8-127">System.String</span></span>

## <span data-ttu-id="5e9f8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e9f8-128">OUTPUTS</span></span>

### <span data-ttu-id="5e9f8-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f8-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5e9f8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e9f8-130">NOTES</span></span>

## <span data-ttu-id="5e9f8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e9f8-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e9f8-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f8-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5e9f8-133">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f8-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5e9f8-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f8-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5e9f8-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f8-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


