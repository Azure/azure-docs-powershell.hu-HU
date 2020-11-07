---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679161"
---
# <span data-ttu-id="47b37-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47b37-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="47b37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47b37-102">SYNOPSIS</span></span>
<span data-ttu-id="47b37-103">A megbízható főtanúsítvány beolvasása az alkalmazás-átjáró konkrét nevével</span><span class="sxs-lookup"><span data-stu-id="47b37-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47b37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47b37-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47b37-105">DESCRIPTION</span></span>
<span data-ttu-id="47b37-106">A **Get-AzureRmApplicationGatewayTrustedRootCertificate** parancsmag megbízható főtanúsítványokat kap, az alkalmazás-átjáróban megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="47b37-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="47b37-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47b37-107">EXAMPLES</span></span>

### <span data-ttu-id="47b37-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47b37-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="47b37-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="47b37-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="47b37-110">A második parancs a megbízható főtanúsítványt az alkalmazás-átjáró megadott nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="47b37-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="47b37-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47b37-111">PARAMETERS</span></span>

### <span data-ttu-id="47b37-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47b37-112">-ApplicationGateway</span></span>
<span data-ttu-id="47b37-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="47b37-113">The applicationGateway</span></span>

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

### <span data-ttu-id="47b37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b37-114">-DefaultProfile</span></span>
<span data-ttu-id="47b37-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47b37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b37-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47b37-116">-Name</span></span>
<span data-ttu-id="47b37-117">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="47b37-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b37-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b37-118">CommonParameters</span></span>
<span data-ttu-id="47b37-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47b37-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b37-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b37-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b37-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b37-121">INPUTS</span></span>

### <span data-ttu-id="47b37-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47b37-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47b37-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b37-123">OUTPUTS</span></span>

### <span data-ttu-id="47b37-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47b37-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="47b37-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47b37-125">NOTES</span></span>

## <span data-ttu-id="47b37-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47b37-126">RELATED LINKS</span></span>
