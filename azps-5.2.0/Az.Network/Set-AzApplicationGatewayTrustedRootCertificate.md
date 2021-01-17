---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351054"
---
# <span data-ttu-id="bbd27-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd27-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="bbd27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd27-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd27-103">Frissíti egy alkalmazás-átjáró megbízható gyökértanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="bbd27-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="bbd27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bbd27-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bbd27-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd27-106">A **Set-AzApplicationGatewayTrustedRootCertificate** parancsmag módosítja egy alkalmazás átjáró meglévő megbízható gyökértanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="bbd27-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="bbd27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bbd27-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd27-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bbd27-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="bbd27-109">A fenti példa azt mutatja be, hogy miként frissíthet egy meglévő megbízható főtanúsítványt a gyökértanúsítványok telepítésekor.</span><span class="sxs-lookup"><span data-stu-id="bbd27-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="bbd27-110">Az első parancs egy alkalmazás-átjárót kap, és a $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="bbd27-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="bbd27-111">A második parancs egy új főtanúsítványsal módosítja a meglévő megbízható gyökértanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="bbd27-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="bbd27-112">A harmadik parancs frissíti az alkalmazás-átjárót az Azure-on.</span><span class="sxs-lookup"><span data-stu-id="bbd27-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="bbd27-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd27-113">PARAMETERS</span></span>

### <span data-ttu-id="bbd27-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbd27-114">-ApplicationGateway</span></span>
<span data-ttu-id="bbd27-115">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbd27-115">The applicationGateway</span></span>

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

### <span data-ttu-id="bbd27-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bbd27-116">-CertificateFile</span></span>
<span data-ttu-id="bbd27-117">Tanúsítvány CER-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="bbd27-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="bbd27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd27-118">-DefaultProfile</span></span>
<span data-ttu-id="bbd27-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbd27-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd27-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bbd27-120">-Name</span></span>
<span data-ttu-id="bbd27-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="bbd27-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="bbd27-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbd27-122">-Confirm</span></span>
<span data-ttu-id="bbd27-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bbd27-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd27-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd27-124">-WhatIf</span></span>
<span data-ttu-id="bbd27-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bbd27-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd27-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbd27-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd27-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd27-127">CommonParameters</span></span>
<span data-ttu-id="bbd27-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd27-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd27-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd27-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd27-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbd27-130">INPUTS</span></span>

### <span data-ttu-id="bbd27-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbd27-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbd27-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd27-132">OUTPUTS</span></span>

### <span data-ttu-id="bbd27-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbd27-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbd27-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bbd27-134">NOTES</span></span>

## <span data-ttu-id="bbd27-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbd27-135">RELATED LINKS</span></span>

[<span data-ttu-id="bbd27-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd27-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="bbd27-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd27-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="bbd27-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd27-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="bbd27-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd27-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
