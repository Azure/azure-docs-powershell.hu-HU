---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014771"
---
# <span data-ttu-id="714b6-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="714b6-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="714b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="714b6-102">SYNOPSIS</span></span>
<span data-ttu-id="714b6-103">Megbízható főtanúsítványot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="714b6-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="714b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="714b6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="714b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="714b6-105">DESCRIPTION</span></span>
<span data-ttu-id="714b6-106">A **New-AzApplicationGatewayTrustedRootCertificate** parancsmag megbízható főtanúsítványot hoz létre az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="714b6-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="714b6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="714b6-107">EXAMPLES</span></span>

### <span data-ttu-id="714b6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="714b6-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="714b6-109">A parancs létrehoz egy "trc1" nevű megbízható főtanúsítványt, és az eredményt az $trc nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="714b6-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="714b6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="714b6-110">PARAMETERS</span></span>

### <span data-ttu-id="714b6-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="714b6-111">-CertificateFile</span></span>
<span data-ttu-id="714b6-112">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="714b6-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="714b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714b6-113">-DefaultProfile</span></span>
<span data-ttu-id="714b6-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="714b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="714b6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="714b6-115">-Name</span></span>
<span data-ttu-id="714b6-116">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="714b6-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="714b6-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="714b6-117">-Confirm</span></span>
<span data-ttu-id="714b6-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="714b6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="714b6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="714b6-119">-WhatIf</span></span>
<span data-ttu-id="714b6-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="714b6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="714b6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="714b6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="714b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714b6-122">CommonParameters</span></span>
<span data-ttu-id="714b6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="714b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714b6-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="714b6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714b6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="714b6-125">INPUTS</span></span>

### <span data-ttu-id="714b6-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="714b6-126">None</span></span>

## <span data-ttu-id="714b6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="714b6-127">OUTPUTS</span></span>

### <span data-ttu-id="714b6-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="714b6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="714b6-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="714b6-129">NOTES</span></span>

## <span data-ttu-id="714b6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="714b6-130">RELATED LINKS</span></span>

[<span data-ttu-id="714b6-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="714b6-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="714b6-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="714b6-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="714b6-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="714b6-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="714b6-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="714b6-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
