---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 2730e3ba1e85a876940492b4abfd4fbe5dbca956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501151"
---
# <span data-ttu-id="8ce6a-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8ce6a-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="8ce6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ce6a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce6a-103">A meglévő állapot-szonda konfigurációjának beolvasása egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ce6a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ce6a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ce6a-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce6a-106">A Get-AzureRmApplicationGatewayProbeConfig parancsmag meglévő állapot-szonda konfigurációt kap egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="8ce6a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8ce6a-107">EXAMPLES</span></span>

### <span data-ttu-id="8ce6a-108">Példa 1: meglévő szonda beszerzése egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="8ce6a-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="8ce6a-109">Ez a parancs beolvassa a Probe02 nevű biztonságiállapot-szonda az átjáró nevű alkalmazási átjáróból.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="8ce6a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ce6a-110">PARAMETERS</span></span>

### <span data-ttu-id="8ce6a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ce6a-111">-ApplicationGateway</span></span>
<span data-ttu-id="8ce6a-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a szonda konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="8ce6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce6a-113">-DefaultProfile</span></span>
<span data-ttu-id="8ce6a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce6a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ce6a-115">-Name</span></span>
<span data-ttu-id="8ce6a-116">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="8ce6a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce6a-117">CommonParameters</span></span>
<span data-ttu-id="8ce6a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ce6a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce6a-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce6a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce6a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce6a-120">INPUTS</span></span>

### <span data-ttu-id="8ce6a-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ce6a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8ce6a-122">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ce6a-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8ce6a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce6a-123">OUTPUTS</span></span>

### <span data-ttu-id="8ce6a-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="8ce6a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="8ce6a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ce6a-125">NOTES</span></span>

## <span data-ttu-id="8ce6a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ce6a-126">RELATED LINKS</span></span>

[<span data-ttu-id="8ce6a-127">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="8ce6a-127">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="8ce6a-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8ce6a-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="8ce6a-129">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8ce6a-129">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="8ce6a-130">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8ce6a-130">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="8ce6a-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8ce6a-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

