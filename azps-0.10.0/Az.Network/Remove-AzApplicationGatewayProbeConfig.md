---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841197"
---
# <span data-ttu-id="abcba-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="abcba-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="abcba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abcba-102">SYNOPSIS</span></span>
<span data-ttu-id="abcba-103">Egy meglévő alkalmazás-átjárótól eltávolítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="abcba-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="abcba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abcba-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abcba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abcba-105">DESCRIPTION</span></span>
<span data-ttu-id="abcba-106">A Remove-AzApplicationGatewayProbeConfig parancsmag eltávolítja a Heath-szondát egy meglévő alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="abcba-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="abcba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abcba-107">EXAMPLES</span></span>

### <span data-ttu-id="abcba-108">1. példa: biztonságiállapot-szonda eltávolítása meglévő alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="abcba-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="abcba-109">Ez a parancs eltávolítja a Probe04 nevű biztonságiállapot-szondat az átjáró nevű alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="abcba-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="abcba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abcba-110">PARAMETERS</span></span>

### <span data-ttu-id="abcba-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abcba-111">-ApplicationGateway</span></span>
<span data-ttu-id="abcba-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja a szondát.</span><span class="sxs-lookup"><span data-stu-id="abcba-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="abcba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abcba-113">-DefaultProfile</span></span>
<span data-ttu-id="abcba-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abcba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abcba-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abcba-115">-Name</span></span>
<span data-ttu-id="abcba-116">Annak a szondanak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="abcba-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="abcba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcba-117">CommonParameters</span></span>
<span data-ttu-id="abcba-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abcba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcba-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcba-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcba-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcba-120">INPUTS</span></span>

### <span data-ttu-id="abcba-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abcba-121">PSApplicationGateway</span></span>
<span data-ttu-id="abcba-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="abcba-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="abcba-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcba-123">OUTPUTS</span></span>

### <span data-ttu-id="abcba-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abcba-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="abcba-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abcba-125">NOTES</span></span>

## <span data-ttu-id="abcba-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abcba-126">RELATED LINKS</span></span>

[<span data-ttu-id="abcba-127">Szonda eltávolítása meglévő alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="abcba-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="abcba-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="abcba-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="abcba-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="abcba-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="abcba-130">Új – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="abcba-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="abcba-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="abcba-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

