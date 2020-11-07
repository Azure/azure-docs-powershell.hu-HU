---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c8db96e9758e04a96f3f7b28c9fda9d8ac73a47e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837686"
---
# <span data-ttu-id="1ca4f-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1ca4f-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="1ca4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ca4f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca4f-103">Egy megbízható főtanúsítvány felvétele az alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="1ca4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ca4f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ca4f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ca4f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ca4f-106">Az **Add-AzApplicationGatewayTrustedRootCertificate** parancsmag egy megbízható legfelső szintű tanúsítványt ad egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="1ca4f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1ca4f-107">EXAMPLES</span></span>

### <span data-ttu-id="1ca4f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1ca4f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1ca4f-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="1ca4f-110">A második parancs hozzáadja az új megbízható főtanúsítványt az Application Gateway-hoz a főtanúsítvány elérési útjának beviteléhez.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="1ca4f-111">A harmadik parancs új backend http-beállítást hoz létre a megbízható főtanúsítvány használatával a backend-kiszolgáló tanúsítványának érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="1ca4f-112">A negyedik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="1ca4f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ca4f-113">PARAMETERS</span></span>

### <span data-ttu-id="1ca4f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca4f-114">-ApplicationGateway</span></span>
<span data-ttu-id="1ca4f-115">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca4f-115">The applicationGateway</span></span>

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

### <span data-ttu-id="1ca4f-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1ca4f-116">-CertificateFile</span></span>
<span data-ttu-id="1ca4f-117">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="1ca4f-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="1ca4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca4f-118">-DefaultProfile</span></span>
<span data-ttu-id="1ca4f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ca4f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ca4f-120">-Name</span></span>
<span data-ttu-id="1ca4f-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="1ca4f-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="1ca4f-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ca4f-122">-Confirm</span></span>
<span data-ttu-id="1ca4f-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca4f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca4f-124">-WhatIf</span></span>
<span data-ttu-id="1ca4f-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ca4f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca4f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca4f-127">CommonParameters</span></span>
<span data-ttu-id="1ca4f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ca4f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca4f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca4f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca4f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca4f-130">INPUTS</span></span>

### <span data-ttu-id="1ca4f-131">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca4f-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ca4f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca4f-132">OUTPUTS</span></span>

### <span data-ttu-id="1ca4f-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca4f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ca4f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ca4f-134">NOTES</span></span>

## <span data-ttu-id="1ca4f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ca4f-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ca4f-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1ca4f-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1ca4f-137">Új – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1ca4f-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1ca4f-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1ca4f-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1ca4f-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1ca4f-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
