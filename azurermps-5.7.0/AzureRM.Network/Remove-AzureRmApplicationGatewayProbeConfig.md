---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 14d1aea928923d9da4eee089ae1e95c75289eb3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680413"
---
# <span data-ttu-id="bbb7d-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bbb7d-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="bbb7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb7d-103">Egy meglévő alkalmazás-átjárótól eltávolítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="bbb7d-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbb7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbb7d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbb7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbb7d-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb7d-106">A Remove-AzureRmApplicationGatewayProbeConfig parancsmag eltávolítja a Heath-szondát egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="bbb7d-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="bbb7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bbb7d-107">EXAMPLES</span></span>

### <span data-ttu-id="bbb7d-108">1. példa: biztonságiállapot-szonda eltávolítása meglévő alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="bbb7d-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="bbb7d-109">Ez a parancs eltávolítja a Probe04 nevű biztonságiállapot-szondat az átjáró nevű alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="bbb7d-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="bbb7d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbb7d-110">PARAMETERS</span></span>

### <span data-ttu-id="bbb7d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbb7d-111">-ApplicationGateway</span></span>
<span data-ttu-id="bbb7d-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja a szondát.</span><span class="sxs-lookup"><span data-stu-id="bbb7d-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb7d-113">-DefaultProfile</span></span>
<span data-ttu-id="bbb7d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbb7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bbb7d-115">-Name</span></span>
<span data-ttu-id="bbb7d-116">Annak a szondanak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="bbb7d-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb7d-117">CommonParameters</span></span>
<span data-ttu-id="bbb7d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbb7d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb7d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb7d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb7d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbb7d-120">INPUTS</span></span>

### <span data-ttu-id="bbb7d-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbb7d-121">PSApplicationGateway</span></span>
<span data-ttu-id="bbb7d-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bbb7d-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="bbb7d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbb7d-123">OUTPUTS</span></span>

### <span data-ttu-id="bbb7d-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbb7d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbb7d-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbb7d-125">NOTES</span></span>

## <span data-ttu-id="bbb7d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbb7d-126">RELATED LINKS</span></span>

[<span data-ttu-id="bbb7d-127">Szonda eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="bbb7d-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="bbb7d-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bbb7d-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bbb7d-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bbb7d-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bbb7d-130">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bbb7d-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bbb7d-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bbb7d-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

