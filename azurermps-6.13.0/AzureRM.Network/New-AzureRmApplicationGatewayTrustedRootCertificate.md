---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505351"
---
# <span data-ttu-id="27bba-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="27bba-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="27bba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27bba-102">SYNOPSIS</span></span>
<span data-ttu-id="27bba-103">Megbízható főtanúsítványot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="27bba-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27bba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27bba-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27bba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27bba-105">DESCRIPTION</span></span>
<span data-ttu-id="27bba-106">A **New-AzureRmApplicationGatewayTrustedRootCertificate** parancsmag megbízható főtanúsítványot hoz létre az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="27bba-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="27bba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27bba-107">EXAMPLES</span></span>

### <span data-ttu-id="27bba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27bba-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="27bba-109">A parancs létrehoz egy "trc1" nevű megbízható főtanúsítványt, és az eredményt az $trc nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="27bba-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="27bba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27bba-110">PARAMETERS</span></span>

### <span data-ttu-id="27bba-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="27bba-111">-CertificateFile</span></span>
<span data-ttu-id="27bba-112">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="27bba-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="27bba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bba-113">-DefaultProfile</span></span>
<span data-ttu-id="27bba-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27bba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27bba-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27bba-115">-Name</span></span>
<span data-ttu-id="27bba-116">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="27bba-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="27bba-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27bba-117">-Confirm</span></span>
<span data-ttu-id="27bba-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27bba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27bba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27bba-119">-WhatIf</span></span>
<span data-ttu-id="27bba-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27bba-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27bba-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27bba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27bba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bba-122">CommonParameters</span></span>
<span data-ttu-id="27bba-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27bba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bba-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27bba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bba-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27bba-125">INPUTS</span></span>

### <span data-ttu-id="27bba-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="27bba-126">None</span></span>

## <span data-ttu-id="27bba-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27bba-127">OUTPUTS</span></span>

### <span data-ttu-id="27bba-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="27bba-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="27bba-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27bba-129">NOTES</span></span>

## <span data-ttu-id="27bba-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27bba-130">RELATED LINKS</span></span>
