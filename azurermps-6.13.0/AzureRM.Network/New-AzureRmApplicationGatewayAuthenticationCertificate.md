---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bdc2821c8499c5a95acd180c9bbfa28568cc5034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495049"
---
# <span data-ttu-id="cb2e7-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb2e7-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="cb2e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2e7-103">Hitelesítési tanúsítványt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb2e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb2e7-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb2e7-106">A **New-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag létrehoz egy hitelesítési tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cb2e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cb2e7-107">EXAMPLES</span></span>

## <span data-ttu-id="cb2e7-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-108">PARAMETERS</span></span>

### <span data-ttu-id="cb2e7-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cb2e7-109">-CertificateFile</span></span>
<span data-ttu-id="cb2e7-110">A hitelesítési tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="cb2e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2e7-111">-DefaultProfile</span></span>
<span data-ttu-id="cb2e7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb2e7-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb2e7-113">-Name</span></span>
<span data-ttu-id="cb2e7-114">A hitelesítési tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="cb2e7-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb2e7-115">-Confirm</span></span>
<span data-ttu-id="cb2e7-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2e7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2e7-117">-WhatIf</span></span>
<span data-ttu-id="cb2e7-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb2e7-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2e7-120">CommonParameters</span></span>
<span data-ttu-id="cb2e7-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb2e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2e7-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2e7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2e7-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-123">INPUTS</span></span>

### <span data-ttu-id="cb2e7-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="cb2e7-124">None</span></span>

## <span data-ttu-id="cb2e7-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-125">OUTPUTS</span></span>

### <span data-ttu-id="cb2e7-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb2e7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="cb2e7-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb2e7-127">NOTES</span></span>
* <span data-ttu-id="cb2e7-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="cb2e7-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cb2e7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb2e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="cb2e7-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb2e7-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="cb2e7-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb2e7-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="cb2e7-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb2e7-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="cb2e7-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cb2e7-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


