---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 62d58803f4b1c7cae39e41e5f903cbfaf022e632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837629"
---
# <span data-ttu-id="de5a7-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de5a7-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="de5a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="de5a7-103">A meglévő állapot-szonda konfigurációjának beolvasása egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="de5a7-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="de5a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de5a7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de5a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="de5a7-106">A Get-AzApplicationGatewayProbeConfig parancsmag meglévő állapot-szonda konfigurációt kap egy alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="de5a7-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="de5a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="de5a7-108">Példa 1: meglévő szonda beszerzése egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="de5a7-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="de5a7-109">Ez a parancs beolvassa a Probe02 nevű biztonságiállapot-szonda az átjáró nevű alkalmazási átjáróból.</span><span class="sxs-lookup"><span data-stu-id="de5a7-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="de5a7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de5a7-110">PARAMETERS</span></span>

### <span data-ttu-id="de5a7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de5a7-111">-ApplicationGateway</span></span>
<span data-ttu-id="de5a7-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a szonda konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="de5a7-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="de5a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5a7-113">-DefaultProfile</span></span>
<span data-ttu-id="de5a7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de5a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de5a7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de5a7-115">-Name</span></span>
<span data-ttu-id="de5a7-116">A szonda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de5a7-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="de5a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5a7-117">CommonParameters</span></span>
<span data-ttu-id="de5a7-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de5a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5a7-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de5a7-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5a7-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de5a7-120">INPUTS</span></span>

### <span data-ttu-id="de5a7-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de5a7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de5a7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de5a7-122">OUTPUTS</span></span>

### <span data-ttu-id="de5a7-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="de5a7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="de5a7-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de5a7-124">NOTES</span></span>

## <span data-ttu-id="de5a7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de5a7-125">RELATED LINKS</span></span>

[<span data-ttu-id="de5a7-126">Szonda hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="de5a7-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="de5a7-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de5a7-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="de5a7-128">Új – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de5a7-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="de5a7-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de5a7-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="de5a7-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de5a7-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

