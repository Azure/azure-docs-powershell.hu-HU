---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849217"
---
# <span data-ttu-id="65216-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="65216-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="65216-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65216-102">SYNOPSIS</span></span>
<span data-ttu-id="65216-103">A meglévő állapot-szonda konfigurációjának beolvasása egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="65216-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65216-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65216-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65216-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65216-105">DESCRIPTION</span></span>
<span data-ttu-id="65216-106">A Get-AzureRmApplicationGatewayProbeConfig parancsmag meglévő állapot-szonda konfigurációt kap egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="65216-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="65216-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65216-107">EXAMPLES</span></span>

### <span data-ttu-id="65216-108">Példa 1: meglévő szonda beszerzése egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="65216-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="65216-109">Ez a parancs beolvassa a Probe02 nevű biztonságiállapot-szonda az átjáró nevű alkalmazási átjáróból.</span><span class="sxs-lookup"><span data-stu-id="65216-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="65216-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65216-110">PARAMETERS</span></span>

### <span data-ttu-id="65216-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65216-111">-ApplicationGateway</span></span>
<span data-ttu-id="65216-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a szonda konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="65216-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="65216-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65216-113">-DefaultProfile</span></span>
<span data-ttu-id="65216-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65216-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65216-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65216-115">-Name</span></span>
<span data-ttu-id="65216-116">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65216-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65216-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65216-117">CommonParameters</span></span>
<span data-ttu-id="65216-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65216-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65216-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65216-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65216-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65216-120">INPUTS</span></span>

### <span data-ttu-id="65216-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65216-121">PSApplicationGateway</span></span>
<span data-ttu-id="65216-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="65216-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="65216-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65216-123">OUTPUTS</span></span>

### <span data-ttu-id="65216-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="65216-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="65216-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="65216-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="65216-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65216-126">NOTES</span></span>

## <span data-ttu-id="65216-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65216-127">RELATED LINKS</span></span>

[<span data-ttu-id="65216-128">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="65216-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="65216-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="65216-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="65216-130">Új – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="65216-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="65216-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="65216-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="65216-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="65216-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

