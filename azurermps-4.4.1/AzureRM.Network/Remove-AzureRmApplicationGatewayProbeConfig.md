---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: df81af46023c1e28ecfe39cf880f45cd9b2319ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680256"
---
# <span data-ttu-id="d57fd-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d57fd-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="d57fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d57fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d57fd-103">Egy meglévő alkalmazás-átjárótól eltávolítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="d57fd-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d57fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d57fd-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d57fd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d57fd-105">DESCRIPTION</span></span>
<span data-ttu-id="d57fd-106">A Remove-AzureRmApplicationGatewayProbeConfig parancsmag eltávolítja a Heath-szondát egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="d57fd-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="d57fd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d57fd-107">EXAMPLES</span></span>

### <span data-ttu-id="d57fd-108">1. példa: biztonságiállapot-szonda eltávolítása meglévő alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="d57fd-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="d57fd-109">Ez a parancs eltávolítja a Probe04 nevű biztonságiállapot-szondat az átjáró nevű alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d57fd-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="d57fd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d57fd-110">PARAMETERS</span></span>

### <span data-ttu-id="d57fd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d57fd-111">-ApplicationGateway</span></span>
<span data-ttu-id="d57fd-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja a szondát.</span><span class="sxs-lookup"><span data-stu-id="d57fd-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="d57fd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d57fd-113">-Name</span></span>
<span data-ttu-id="d57fd-114">Annak a szondanak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="d57fd-114">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="d57fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57fd-115">-DefaultProfile</span></span>
<span data-ttu-id="d57fd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d57fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d57fd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57fd-117">CommonParameters</span></span>
<span data-ttu-id="d57fd-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d57fd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57fd-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57fd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57fd-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d57fd-120">INPUTS</span></span>

### <span data-ttu-id="d57fd-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d57fd-121">PSApplicationGateway</span></span>
<span data-ttu-id="d57fd-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d57fd-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d57fd-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d57fd-123">OUTPUTS</span></span>

### <span data-ttu-id="d57fd-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d57fd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d57fd-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d57fd-125">NOTES</span></span>

## <span data-ttu-id="d57fd-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d57fd-126">RELATED LINKS</span></span>

[<span data-ttu-id="d57fd-127">Szonda eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="d57fd-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="d57fd-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d57fd-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d57fd-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d57fd-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d57fd-130">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d57fd-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d57fd-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d57fd-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

