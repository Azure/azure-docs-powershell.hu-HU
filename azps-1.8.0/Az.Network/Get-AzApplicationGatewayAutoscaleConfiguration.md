---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 723d1aaab342673f16d37cfaa15406f3ab99566d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670675"
---
# <span data-ttu-id="a61c5-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a61c5-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a61c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a61c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a61c5-103">Az alkalmazás-átjáró automatikus méretarányos konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a61c5-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="a61c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a61c5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a61c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a61c5-105">DESCRIPTION</span></span>
<span data-ttu-id="a61c5-106">A **Get-AzApplicationGatewayAutoscaleConfiguration** parancsmag automatikus méretarányos konfigurációt kap az alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="a61c5-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="a61c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a61c5-107">EXAMPLES</span></span>

### <span data-ttu-id="a61c5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a61c5-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="a61c5-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a61c5-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a61c5-110">A második parancs kibontja az automatikus méretezés konfigurációját az applicationg-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a61c5-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="a61c5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a61c5-111">PARAMETERS</span></span>

### <span data-ttu-id="a61c5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a61c5-112">-ApplicationGateway</span></span>
<span data-ttu-id="a61c5-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a61c5-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a61c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61c5-114">-DefaultProfile</span></span>
<span data-ttu-id="a61c5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a61c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a61c5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61c5-116">CommonParameters</span></span>
<span data-ttu-id="a61c5-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a61c5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61c5-118">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a61c5-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61c5-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a61c5-119">INPUTS</span></span>

### <span data-ttu-id="a61c5-120">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a61c5-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a61c5-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a61c5-121">OUTPUTS</span></span>

### <span data-ttu-id="a61c5-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a61c5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a61c5-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a61c5-123">NOTES</span></span>

## <span data-ttu-id="a61c5-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a61c5-124">RELATED LINKS</span></span>

[<span data-ttu-id="a61c5-125">Új – AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a61c5-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a61c5-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a61c5-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a61c5-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a61c5-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
