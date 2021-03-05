---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010421"
---
# <span data-ttu-id="7b129-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7b129-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7b129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b129-102">SYNOPSIS</span></span>
<span data-ttu-id="7b129-103">Hitelesítési tanúsítványt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7b129-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="7b129-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b129-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b129-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b129-105">DESCRIPTION</span></span>
<span data-ttu-id="7b129-106">A **New-AzApplicationGatewayAuthenticationCertificate parancsmag** létrehoz egy hitelesítési tanúsítványt egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7b129-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7b129-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b129-107">EXAMPLES</span></span>

### <span data-ttu-id="7b129-108">1. példa: Hitelesítési tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="7b129-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="7b129-109">Az első parancs a cert01 nevű hitelesítési tanúsítványt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7b129-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="7b129-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b129-110">PARAMETERS</span></span>

### <span data-ttu-id="7b129-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7b129-111">-CertificateFile</span></span>
<span data-ttu-id="7b129-112">A hitelesítési tanúsítvány elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b129-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="7b129-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b129-113">-DefaultProfile</span></span>
<span data-ttu-id="7b129-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b129-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b129-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7b129-115">-Name</span></span>
<span data-ttu-id="7b129-116">Megadja a hitelesítési tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="7b129-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="7b129-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b129-117">-Confirm</span></span>
<span data-ttu-id="7b129-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b129-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b129-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b129-119">-WhatIf</span></span>
<span data-ttu-id="7b129-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b129-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b129-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b129-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b129-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b129-122">CommonParameters</span></span>
<span data-ttu-id="7b129-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b129-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b129-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b129-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b129-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b129-125">INPUTS</span></span>

### <span data-ttu-id="7b129-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="7b129-126">None</span></span>

## <span data-ttu-id="7b129-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b129-127">OUTPUTS</span></span>

### <span data-ttu-id="7b129-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7b129-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7b129-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b129-129">NOTES</span></span>
* <span data-ttu-id="7b129-130">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7b129-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7b129-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b129-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b129-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7b129-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7b129-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7b129-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7b129-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7b129-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7b129-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7b129-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


