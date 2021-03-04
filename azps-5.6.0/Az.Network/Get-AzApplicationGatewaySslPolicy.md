---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940329"
---
# <span data-ttu-id="4a3dc-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3dc-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4a3dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3dc-103">Egy alkalmazás-átjáró SSL-házirendét használja.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="4a3dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4a3dc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a3dc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4a3dc-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3dc-106">A **Get-AzApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjére érvényes.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="4a3dc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4a3dc-107">EXAMPLES</span></span>

### <span data-ttu-id="4a3dc-108">1:</span><span class="sxs-lookup"><span data-stu-id="4a3dc-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="4a3dc-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4a3dc-110">A második parancs az ssl-házirendet a következő nevű változóban tárolt alkalmazás-átjáróból $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="4a3dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a3dc-111">PARAMETERS</span></span>

### <span data-ttu-id="4a3dc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a3dc-112">-ApplicationGateway</span></span>
<span data-ttu-id="4a3dc-113">A parancsmag által lekért SSL-házirend alkalmazás-átjáróját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4a3dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3dc-114">-DefaultProfile</span></span>
<span data-ttu-id="4a3dc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3dc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3dc-116">CommonParameters</span></span>
<span data-ttu-id="4a3dc-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3dc-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a3dc-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3dc-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a3dc-119">INPUTS</span></span>

### <span data-ttu-id="4a3dc-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a3dc-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a3dc-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3dc-121">OUTPUTS</span></span>

### <span data-ttu-id="4a3dc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3dc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4a3dc-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4a3dc-123">NOTES</span></span>
* <span data-ttu-id="4a3dc-124">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="4a3dc-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4a3dc-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a3dc-125">RELATED LINKS</span></span>

[<span data-ttu-id="4a3dc-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3dc-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4a3dc-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3dc-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


