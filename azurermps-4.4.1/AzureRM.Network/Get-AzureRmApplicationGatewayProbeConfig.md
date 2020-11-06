---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493441"
---
# <span data-ttu-id="b38c5-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b38c5-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b38c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b38c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b38c5-103">A meglévő állapot-szonda konfigurációjának beolvasása egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="b38c5-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b38c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b38c5-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b38c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b38c5-105">DESCRIPTION</span></span>
<span data-ttu-id="b38c5-106">A Get-AzureRmApplicationGatewayProbeConfig parancsmag meglévő állapot-szonda konfigurációt kap egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="b38c5-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="b38c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b38c5-107">EXAMPLES</span></span>

### <span data-ttu-id="b38c5-108">Példa 1: meglévő szonda beszerzése egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="b38c5-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="b38c5-109">Ez a parancs beolvassa a Probe02 nevű biztonságiállapot-szonda az átjáró nevű alkalmazási átjáróból.</span><span class="sxs-lookup"><span data-stu-id="b38c5-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="b38c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b38c5-110">PARAMETERS</span></span>

### <span data-ttu-id="b38c5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b38c5-111">-ApplicationGateway</span></span>
<span data-ttu-id="b38c5-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a szonda konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="b38c5-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="b38c5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b38c5-113">-Name</span></span>
<span data-ttu-id="b38c5-114">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b38c5-114">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="b38c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38c5-115">-DefaultProfile</span></span>
<span data-ttu-id="b38c5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b38c5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b38c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38c5-117">CommonParameters</span></span>
<span data-ttu-id="b38c5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b38c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38c5-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38c5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38c5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b38c5-120">INPUTS</span></span>

### <span data-ttu-id="b38c5-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b38c5-121">PSApplicationGateway</span></span>
<span data-ttu-id="b38c5-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b38c5-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b38c5-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b38c5-123">OUTPUTS</span></span>

### <span data-ttu-id="b38c5-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="b38c5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="b38c5-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="b38c5-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="b38c5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b38c5-126">NOTES</span></span>

## <span data-ttu-id="b38c5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b38c5-127">RELATED LINKS</span></span>

[<span data-ttu-id="b38c5-128">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="b38c5-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="b38c5-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b38c5-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b38c5-130">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b38c5-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b38c5-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b38c5-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b38c5-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b38c5-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

