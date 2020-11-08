---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010902"
---
# <span data-ttu-id="f08e4-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f08e4-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f08e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f08e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f08e4-103">Egy alkalmazás-átjáró megbízható főtanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="f08e4-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="f08e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f08e4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f08e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f08e4-105">DESCRIPTION</span></span>
<span data-ttu-id="f08e4-106">A **set-AzApplicationGatewayTrustedRootCertificate** parancsmag módosította az alkalmazás-átjárók meglévő megbízható főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="f08e4-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="f08e4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f08e4-107">EXAMPLES</span></span>

### <span data-ttu-id="f08e4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f08e4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f08e4-109">A fenti példa szerint az esetek azt mutatják be, hogy miként frissíthet egy meglévő megbízható főtanúsítványt a főtanúsítvány bedobásakor.</span><span class="sxs-lookup"><span data-stu-id="f08e4-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="f08e4-110">Az első parancs beolvassa az Application Gatewayt, és a $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f08e4-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="f08e4-111">A második parancs módosította a meglévő megbízható főtanúsítványot egy új főtanúsítványsal.</span><span class="sxs-lookup"><span data-stu-id="f08e4-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="f08e4-112">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="f08e4-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f08e4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f08e4-113">PARAMETERS</span></span>

### <span data-ttu-id="f08e4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f08e4-114">-ApplicationGateway</span></span>
<span data-ttu-id="f08e4-115">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f08e4-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f08e4-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f08e4-116">-CertificateFile</span></span>
<span data-ttu-id="f08e4-117">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="f08e4-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="f08e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08e4-118">-DefaultProfile</span></span>
<span data-ttu-id="f08e4-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f08e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f08e4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f08e4-120">-Name</span></span>
<span data-ttu-id="f08e4-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="f08e4-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f08e4-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f08e4-122">-Confirm</span></span>
<span data-ttu-id="f08e4-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f08e4-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08e4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f08e4-124">-WhatIf</span></span>
<span data-ttu-id="f08e4-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f08e4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f08e4-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f08e4-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08e4-127">CommonParameters</span></span>
<span data-ttu-id="f08e4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f08e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08e4-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f08e4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08e4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f08e4-130">INPUTS</span></span>

### <span data-ttu-id="f08e4-131">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f08e4-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f08e4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f08e4-132">OUTPUTS</span></span>

### <span data-ttu-id="f08e4-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f08e4-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f08e4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f08e4-134">NOTES</span></span>

## <span data-ttu-id="f08e4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f08e4-135">RELATED LINKS</span></span>

[<span data-ttu-id="f08e4-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f08e4-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f08e4-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f08e4-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f08e4-138">Új – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f08e4-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f08e4-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f08e4-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
