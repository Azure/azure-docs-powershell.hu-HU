---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: d8f2fcb875503b6d6a8063007926690ef682bdc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503475"
---
# <span data-ttu-id="dba19-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dba19-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="dba19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dba19-102">SYNOPSIS</span></span>
<span data-ttu-id="dba19-103">Az alkalmazás-átjárók hitelesítési tanúsítványának frissítése</span><span class="sxs-lookup"><span data-stu-id="dba19-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dba19-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dba19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dba19-105">DESCRIPTION</span></span>
<span data-ttu-id="dba19-106">A **set-AzureRmApplicationGatewayAuthenticationCertificate** parancsmag az Azure Application Gateway hitelesítési tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="dba19-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="dba19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dba19-107">EXAMPLES</span></span>

## <span data-ttu-id="dba19-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dba19-108">PARAMETERS</span></span>

### <span data-ttu-id="dba19-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba19-109">-ApplicationGateway</span></span>
<span data-ttu-id="dba19-110">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag egy hitelesítési tanúsítványt frissít.</span><span class="sxs-lookup"><span data-stu-id="dba19-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="dba19-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="dba19-111">-CertificateFile</span></span>
<span data-ttu-id="dba19-112">Annak a hitelesítési tanúsítványnak az elérési útját adja meg, amelyen a parancsmag frissíti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="dba19-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="dba19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba19-113">-DefaultProfile</span></span>
<span data-ttu-id="dba19-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dba19-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba19-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dba19-115">-Name</span></span>
<span data-ttu-id="dba19-116">Annak a hitelesítési tanúsítványnak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="dba19-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="dba19-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dba19-117">-Confirm</span></span>
<span data-ttu-id="dba19-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dba19-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba19-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba19-119">-WhatIf</span></span>
<span data-ttu-id="dba19-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dba19-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba19-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dba19-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba19-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba19-122">CommonParameters</span></span>
<span data-ttu-id="dba19-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dba19-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba19-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba19-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba19-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba19-125">INPUTS</span></span>

### <span data-ttu-id="dba19-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba19-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="dba19-127">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dba19-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="dba19-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba19-128">OUTPUTS</span></span>

### <span data-ttu-id="dba19-129">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba19-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dba19-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dba19-130">NOTES</span></span>
* <span data-ttu-id="dba19-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="dba19-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dba19-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dba19-132">RELATED LINKS</span></span>

[<span data-ttu-id="dba19-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dba19-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dba19-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dba19-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dba19-135">Új – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dba19-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dba19-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dba19-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

