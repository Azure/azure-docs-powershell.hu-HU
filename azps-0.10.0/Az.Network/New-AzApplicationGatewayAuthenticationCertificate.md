---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841446"
---
# <span data-ttu-id="1172b-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1172b-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="1172b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1172b-102">SYNOPSIS</span></span>
<span data-ttu-id="1172b-103">Hitelesítési tanúsítványt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1172b-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="1172b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1172b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1172b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1172b-105">DESCRIPTION</span></span>
<span data-ttu-id="1172b-106">A **New-AzApplicationGatewayAuthenticationCertificate** parancsmag létrehoz egy hitelesítési tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="1172b-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="1172b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1172b-107">EXAMPLES</span></span>

### <span data-ttu-id="1172b-108">1:</span><span class="sxs-lookup"><span data-stu-id="1172b-108">1:</span></span>
```

```

## <span data-ttu-id="1172b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1172b-109">PARAMETERS</span></span>

### <span data-ttu-id="1172b-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1172b-110">-CertificateFile</span></span>
<span data-ttu-id="1172b-111">A hitelesítési tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1172b-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="1172b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1172b-112">-DefaultProfile</span></span>
<span data-ttu-id="1172b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1172b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1172b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1172b-114">-Name</span></span>
<span data-ttu-id="1172b-115">A hitelesítési tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1172b-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="1172b-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1172b-116">-Confirm</span></span>
<span data-ttu-id="1172b-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1172b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1172b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1172b-118">-WhatIf</span></span>
<span data-ttu-id="1172b-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1172b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1172b-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1172b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1172b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1172b-121">CommonParameters</span></span>
<span data-ttu-id="1172b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1172b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1172b-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1172b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1172b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1172b-124">INPUTS</span></span>

### <span data-ttu-id="1172b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1172b-125">System.String</span></span>

## <span data-ttu-id="1172b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1172b-126">OUTPUTS</span></span>

### <span data-ttu-id="1172b-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1172b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="1172b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1172b-128">NOTES</span></span>
* <span data-ttu-id="1172b-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="1172b-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1172b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1172b-130">RELATED LINKS</span></span>

[<span data-ttu-id="1172b-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1172b-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1172b-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1172b-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1172b-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1172b-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1172b-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1172b-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


