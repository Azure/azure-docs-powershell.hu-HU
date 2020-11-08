---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184881"
---
# <span data-ttu-id="9d7a4-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d7a4-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9d7a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7a4-103">Hitelesítési tanúsítványt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="9d7a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d7a4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d7a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d7a4-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7a4-106">A **New-AzApplicationGatewayAuthenticationCertificate** parancsmag létrehoz egy hitelesítési tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="9d7a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d7a4-107">EXAMPLES</span></span>

### <span data-ttu-id="9d7a4-108">Példa 1: hitelesítési tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="9d7a4-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="9d7a4-109">Az első parancs létrehozza a cert01 nevű hitelesítési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="9d7a4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d7a4-110">PARAMETERS</span></span>

### <span data-ttu-id="9d7a4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9d7a4-111">-CertificateFile</span></span>
<span data-ttu-id="9d7a4-112">A hitelesítési tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-112">Specifies the path of the authentication certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7a4-113">-DefaultProfile</span></span>
<span data-ttu-id="9d7a4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d7a4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d7a4-115">-Name</span></span>
<span data-ttu-id="9d7a4-116">A hitelesítési tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-116">Specifies a name for the authentication certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d7a4-117">-Confirm</span></span>
<span data-ttu-id="9d7a4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d7a4-119">-WhatIf</span></span>
<span data-ttu-id="9d7a4-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d7a4-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7a4-122">CommonParameters</span></span>
<span data-ttu-id="9d7a4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d7a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7a4-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7a4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7a4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d7a4-125">INPUTS</span></span>

### <span data-ttu-id="9d7a4-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9d7a4-126">None</span></span>

## <span data-ttu-id="9d7a4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d7a4-127">OUTPUTS</span></span>

### <span data-ttu-id="9d7a4-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d7a4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9d7a4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d7a4-129">NOTES</span></span>
* <span data-ttu-id="9d7a4-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="9d7a4-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9d7a4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d7a4-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d7a4-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d7a4-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9d7a4-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d7a4-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9d7a4-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d7a4-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9d7a4-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9d7a4-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)

