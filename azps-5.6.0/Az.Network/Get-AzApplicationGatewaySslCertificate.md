---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: aa6dbacb85263d8f0169f913c07e56a9dbd1c7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940337"
---
# <span data-ttu-id="6ff4e-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ff4e-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6ff4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff4e-103">Ssl-tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6ff4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ff4e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff4e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ff4e-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff4e-106">A **Get-AzApplicationGatewaySslCertificate parancsmag** egy SSL-tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6ff4e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ff4e-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff4e-108">1. példa: Adott SSL-tanúsítvány lekérve</span><span class="sxs-lookup"><span data-stu-id="6ff4e-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6ff4e-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6ff4e-110">A második parancs a Cert01 nevű SSL-tanúsítványt az $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="6ff4e-111">A parancs a tanúsítványt a következő nevű változóban $Cert.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="6ff4e-112">2. példa: SSL-tanúsítványok listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="6ff4e-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="6ff4e-113">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6ff4e-114">Ez a második parancs lekérte az SSL-tanúsítványok listáját az $AppGW nevű változóban tárolt $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="6ff4e-115">A parancs ezután a találatokat a $Certs.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="6ff4e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ff4e-116">PARAMETERS</span></span>

### <span data-ttu-id="6ff4e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ff4e-117">-ApplicationGateway</span></span>
<span data-ttu-id="6ff4e-118">Az SSL-tanúsítványt tartalmazó alkalmazás-átjáróobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="6ff4e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff4e-119">-DefaultProfile</span></span>
<span data-ttu-id="6ff4e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff4e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6ff4e-121">-Name</span></span>
<span data-ttu-id="6ff4e-122">Annak az SSL-tanúsítványkészletnek a nevét adja meg, amelybe a parancsmag be fog jut.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6ff4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff4e-123">CommonParameters</span></span>
<span data-ttu-id="6ff4e-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff4e-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ff4e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff4e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ff4e-126">INPUTS</span></span>

### <span data-ttu-id="6ff4e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ff4e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ff4e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff4e-128">OUTPUTS</span></span>

### <span data-ttu-id="6ff4e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ff4e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6ff4e-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ff4e-130">NOTES</span></span>

## <span data-ttu-id="6ff4e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ff4e-131">RELATED LINKS</span></span>

[<span data-ttu-id="6ff4e-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ff4e-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6ff4e-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ff4e-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6ff4e-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ff4e-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6ff4e-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ff4e-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


