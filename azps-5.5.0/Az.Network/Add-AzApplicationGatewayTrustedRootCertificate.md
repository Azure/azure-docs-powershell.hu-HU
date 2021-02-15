---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159266"
---
# <span data-ttu-id="96288-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96288-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="96288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96288-102">SYNOPSIS</span></span>
<span data-ttu-id="96288-103">Hozzáad egy megbízható főtanúsítványt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="96288-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="96288-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96288-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96288-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96288-105">DESCRIPTION</span></span>
<span data-ttu-id="96288-106">Az **Add-AzApplicationGatewayTrustedRootCertificate** parancsmag hozzáad egy megbízható gyökértanúsítványt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="96288-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="96288-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96288-107">EXAMPLES</span></span>

### <span data-ttu-id="96288-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="96288-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="96288-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="96288-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="96288-110">A második parancs egy új megbízható főtanúsítványt ad hozzá az alkalmazás-átjáróhoz, amely a főtanúsítvány elérési útját adja meg bemenetként.</span><span class="sxs-lookup"><span data-stu-id="96288-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="96288-111">A harmadik parancs új háttér-http-beállítást hoz létre megbízható gyökértanúsítvány használatával a háttérkiszolgálói tanúsítvány hitelesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="96288-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="96288-112">A negyedik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="96288-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="96288-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96288-113">PARAMETERS</span></span>

### <span data-ttu-id="96288-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96288-114">-ApplicationGateway</span></span>
<span data-ttu-id="96288-115">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="96288-115">The applicationGateway</span></span>

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

### <span data-ttu-id="96288-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="96288-116">-CertificateFile</span></span>
<span data-ttu-id="96288-117">Tanúsítvány CER-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="96288-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="96288-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96288-118">-DefaultProfile</span></span>
<span data-ttu-id="96288-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96288-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96288-120">-Name</span><span class="sxs-lookup"><span data-stu-id="96288-120">-Name</span></span>
<span data-ttu-id="96288-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="96288-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="96288-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96288-122">-Confirm</span></span>
<span data-ttu-id="96288-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96288-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96288-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96288-124">-WhatIf</span></span>
<span data-ttu-id="96288-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96288-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96288-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96288-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96288-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96288-127">CommonParameters</span></span>
<span data-ttu-id="96288-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96288-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96288-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96288-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96288-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96288-130">INPUTS</span></span>

### <span data-ttu-id="96288-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96288-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96288-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96288-132">OUTPUTS</span></span>

### <span data-ttu-id="96288-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96288-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96288-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96288-134">NOTES</span></span>

## <span data-ttu-id="96288-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96288-135">RELATED LINKS</span></span>

[<span data-ttu-id="96288-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96288-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="96288-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96288-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="96288-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96288-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="96288-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96288-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
