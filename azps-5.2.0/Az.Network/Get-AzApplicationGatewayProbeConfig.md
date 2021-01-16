---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326686"
---
# <span data-ttu-id="6f757-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f757-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6f757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f757-102">SYNOPSIS</span></span>
<span data-ttu-id="6f757-103">Egy meglévő állapotkonfigurációt kap egy alkalmazás átjárótól.</span><span class="sxs-lookup"><span data-stu-id="6f757-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="6f757-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f757-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f757-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f757-105">DESCRIPTION</span></span>
<span data-ttu-id="6f757-106">A Get-AzApplicationGatewayProbeConfig parancsmag egy meglévő állapotkonfigurációt kap egy alkalmazás-átjárótól.</span><span class="sxs-lookup"><span data-stu-id="6f757-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="6f757-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f757-107">EXAMPLES</span></span>

### <span data-ttu-id="6f757-108">1. példa: Meglévő átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="6f757-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="6f757-109">Ez a parancs az Átjáró nevű alkalmazás-átjáróból bekérte az "111" nevű Állapot2 nevű nevet.</span><span class="sxs-lookup"><span data-stu-id="6f757-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="6f757-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f757-110">PARAMETERS</span></span>

### <span data-ttu-id="6f757-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f757-111">-ApplicationGateway</span></span>
<span data-ttu-id="6f757-112">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="6f757-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="6f757-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f757-113">-DefaultProfile</span></span>
<span data-ttu-id="6f757-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f757-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f757-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6f757-115">-Name</span></span>
<span data-ttu-id="6f757-116">A vizsgálat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f757-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="6f757-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f757-117">CommonParameters</span></span>
<span data-ttu-id="6f757-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f757-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f757-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f757-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f757-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f757-120">INPUTS</span></span>

### <span data-ttu-id="6f757-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f757-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f757-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f757-122">OUTPUTS</span></span>

### <span data-ttu-id="6f757-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="6f757-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="6f757-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f757-124">NOTES</span></span>

## <span data-ttu-id="6f757-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f757-125">RELATED LINKS</span></span>

[<span data-ttu-id="6f757-126">Bővítmény hozzáadása meglévő alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="6f757-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="6f757-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f757-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6f757-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f757-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6f757-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f757-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6f757-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f757-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

