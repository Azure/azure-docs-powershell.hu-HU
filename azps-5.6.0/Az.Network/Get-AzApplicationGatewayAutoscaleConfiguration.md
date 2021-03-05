---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 78a9623e5e65c93d302b356b64b5c30033697fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003669"
---
# <span data-ttu-id="30ae2-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="30ae2-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="30ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="30ae2-103">Az alkalmazás átjárójának automatikus méretezésű konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="30ae2-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="30ae2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30ae2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ae2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="30ae2-106">A **Get-AzApplicationGatewayAutoscaleConfiguration parancsmag** az alkalmazás-átjáró automatikus méretezésű konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="30ae2-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="30ae2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30ae2-107">EXAMPLES</span></span>

### <span data-ttu-id="30ae2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="30ae2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="30ae2-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="30ae2-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="30ae2-110">A második parancs kinyeri az automatikus skálás konfigurációt az alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="30ae2-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="30ae2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30ae2-111">PARAMETERS</span></span>

### <span data-ttu-id="30ae2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30ae2-112">-ApplicationGateway</span></span>
<span data-ttu-id="30ae2-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="30ae2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="30ae2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ae2-114">-DefaultProfile</span></span>
<span data-ttu-id="30ae2-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30ae2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ae2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ae2-116">CommonParameters</span></span>
<span data-ttu-id="30ae2-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ae2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ae2-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30ae2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ae2-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30ae2-119">INPUTS</span></span>

### <span data-ttu-id="30ae2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30ae2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30ae2-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ae2-121">OUTPUTS</span></span>

### <span data-ttu-id="30ae2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="30ae2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="30ae2-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30ae2-123">NOTES</span></span>

## <span data-ttu-id="30ae2-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30ae2-124">RELATED LINKS</span></span>

[<span data-ttu-id="30ae2-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="30ae2-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="30ae2-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="30ae2-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="30ae2-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="30ae2-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
