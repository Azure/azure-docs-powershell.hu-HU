---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: ab5697091cf36018601bb2417e42e74f763a5d8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670629"
---
# <span data-ttu-id="ec750-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec750-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ec750-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec750-102">SYNOPSIS</span></span>
<span data-ttu-id="ec750-103">SSL-tanúsítványt kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ec750-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="ec750-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec750-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec750-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec750-105">DESCRIPTION</span></span>
<span data-ttu-id="ec750-106">A **Get-AzApplicationGatewaySslCertificate** parancsmag SSL-tanúsítványt kap az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ec750-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="ec750-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec750-107">EXAMPLES</span></span>

### <span data-ttu-id="ec750-108">1. példa: adott SSL-tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="ec750-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="ec750-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ec750-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="ec750-110">A második parancs a Cert01 nevű SSL-tanúsítványt kapja meg az $AppGW nevű változóban tárolt alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="ec750-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="ec750-111">A parancs a $Cert nevű változóban tárolja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="ec750-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="ec750-112">2. példa: az SSL-tanúsítványok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ec750-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="ec750-113">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ec750-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="ec750-114">Ez a második parancs a $AppGW nevű változóban tárolt alkalmazás-átjáróból kapja meg az SSL-tanúsítványok listáját.</span><span class="sxs-lookup"><span data-stu-id="ec750-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="ec750-115">A parancs ezután a $Certs nevű változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="ec750-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="ec750-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec750-116">PARAMETERS</span></span>

### <span data-ttu-id="ec750-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec750-117">-ApplicationGateway</span></span>
<span data-ttu-id="ec750-118">Az SSL-tanúsítványt tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="ec750-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="ec750-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec750-119">-DefaultProfile</span></span>
<span data-ttu-id="ec750-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec750-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec750-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec750-121">-Name</span></span>
<span data-ttu-id="ec750-122">Annak az SSL-tanúsítványtárolónak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="ec750-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ec750-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec750-123">CommonParameters</span></span>
<span data-ttu-id="ec750-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec750-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec750-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec750-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec750-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec750-126">INPUTS</span></span>

### <span data-ttu-id="ec750-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec750-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec750-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec750-128">OUTPUTS</span></span>

### <span data-ttu-id="ec750-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec750-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ec750-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec750-130">NOTES</span></span>

## <span data-ttu-id="ec750-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec750-131">RELATED LINKS</span></span>

[<span data-ttu-id="ec750-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec750-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ec750-133">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec750-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ec750-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec750-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ec750-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec750-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


