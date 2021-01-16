---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360987"
---
# <span data-ttu-id="8d02b-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d02b-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8d02b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d02b-102">SYNOPSIS</span></span>
<span data-ttu-id="8d02b-103">Megbízható gyökértanúsítványt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8d02b-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="8d02b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d02b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d02b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d02b-105">DESCRIPTION</span></span>
<span data-ttu-id="8d02b-106">A **New-AzApplicationGatewayTrustedRootCertificate** parancsmag megbízható gyökértanúsítványt hoz létre egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8d02b-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8d02b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d02b-107">EXAMPLES</span></span>

### <span data-ttu-id="8d02b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d02b-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="8d02b-109">Ez a parancs létrehoz egy "trc1" nevű megbízható gyökértanúsítványt, és az eredményt a "Trc1" nevű változóban $trc.</span><span class="sxs-lookup"><span data-stu-id="8d02b-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="8d02b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d02b-110">PARAMETERS</span></span>

### <span data-ttu-id="8d02b-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8d02b-111">-CertificateFile</span></span>
<span data-ttu-id="8d02b-112">Tanúsítvány CER-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="8d02b-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="8d02b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d02b-113">-DefaultProfile</span></span>
<span data-ttu-id="8d02b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d02b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d02b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8d02b-115">-Name</span></span>
<span data-ttu-id="8d02b-116">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="8d02b-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="8d02b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d02b-117">-Confirm</span></span>
<span data-ttu-id="8d02b-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d02b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d02b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d02b-119">-WhatIf</span></span>
<span data-ttu-id="8d02b-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d02b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d02b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d02b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d02b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d02b-122">CommonParameters</span></span>
<span data-ttu-id="8d02b-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d02b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d02b-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d02b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d02b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d02b-125">INPUTS</span></span>

### <span data-ttu-id="8d02b-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d02b-126">None</span></span>

## <span data-ttu-id="8d02b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d02b-127">OUTPUTS</span></span>

### <span data-ttu-id="8d02b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d02b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8d02b-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d02b-129">NOTES</span></span>

## <span data-ttu-id="8d02b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d02b-130">RELATED LINKS</span></span>

[<span data-ttu-id="8d02b-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d02b-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8d02b-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d02b-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8d02b-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d02b-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8d02b-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d02b-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
