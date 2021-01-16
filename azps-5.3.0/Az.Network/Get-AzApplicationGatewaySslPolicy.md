---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468173"
---
# <span data-ttu-id="789c2-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="789c2-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="789c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="789c2-102">SYNOPSIS</span></span>
<span data-ttu-id="789c2-103">Egy alkalmazás-átjáró SSL-házirendét használja.</span><span class="sxs-lookup"><span data-stu-id="789c2-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="789c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="789c2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="789c2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="789c2-105">DESCRIPTION</span></span>
<span data-ttu-id="789c2-106">A **Get-AzApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjére érvényes.</span><span class="sxs-lookup"><span data-stu-id="789c2-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="789c2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="789c2-107">EXAMPLES</span></span>

### <span data-ttu-id="789c2-108">1:</span><span class="sxs-lookup"><span data-stu-id="789c2-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="789c2-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="789c2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="789c2-110">A második parancs az ssl-házirendet a következő nevű változóban tárolt alkalmazás-átjáróból $AppGW.</span><span class="sxs-lookup"><span data-stu-id="789c2-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="789c2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="789c2-111">PARAMETERS</span></span>

### <span data-ttu-id="789c2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="789c2-112">-ApplicationGateway</span></span>
<span data-ttu-id="789c2-113">A parancsmag által lekért SSL-házirend alkalmazás-átjáróját adja meg.</span><span class="sxs-lookup"><span data-stu-id="789c2-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="789c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789c2-114">-DefaultProfile</span></span>
<span data-ttu-id="789c2-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="789c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="789c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789c2-116">CommonParameters</span></span>
<span data-ttu-id="789c2-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789c2-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="789c2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789c2-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="789c2-119">INPUTS</span></span>

### <span data-ttu-id="789c2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="789c2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="789c2-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="789c2-121">OUTPUTS</span></span>

### <span data-ttu-id="789c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="789c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="789c2-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="789c2-123">NOTES</span></span>
* <span data-ttu-id="789c2-124">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="789c2-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="789c2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="789c2-125">RELATED LINKS</span></span>

[<span data-ttu-id="789c2-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="789c2-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="789c2-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="789c2-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


