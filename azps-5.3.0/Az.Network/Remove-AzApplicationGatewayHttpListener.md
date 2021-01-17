---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479976"
---
# <span data-ttu-id="fcc9e-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fcc9e-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fcc9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc9e-103">Eltávolít egy HTTP-hallgatót egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="fcc9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fcc9e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcc9e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fcc9e-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc9e-106">A **Remove-AzApplicationGatewayHttpListener** parancsmag eltávolítja a HTTP-szolgáltatásokat egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="fcc9e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fcc9e-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc9e-108">1. példa: Alkalmazás-átjáró HTTP-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fcc9e-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="fcc9e-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fcc9e-110">A második parancs eltávolítja a Listener02 nevű HTTP-hallgatót a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="fcc9e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcc9e-111">PARAMETERS</span></span>

### <span data-ttu-id="fcc9e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcc9e-112">-ApplicationGateway</span></span>
<span data-ttu-id="fcc9e-113">Azt az alkalmazás-átjárót adja meg, amelyről el szeretné távolítani a HTTP-et.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="fcc9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc9e-114">-DefaultProfile</span></span>
<span data-ttu-id="fcc9e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcc9e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fcc9e-116">-Name</span></span>
<span data-ttu-id="fcc9e-117">A parancsmag által eltávolított HTTP-hallgató nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcc9e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc9e-118">CommonParameters</span></span>
<span data-ttu-id="fcc9e-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc9e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc9e-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc9e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc9e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcc9e-121">INPUTS</span></span>

### <span data-ttu-id="fcc9e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcc9e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fcc9e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc9e-123">OUTPUTS</span></span>

### <span data-ttu-id="fcc9e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fcc9e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fcc9e-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fcc9e-125">NOTES</span></span>

## <span data-ttu-id="fcc9e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcc9e-126">RELATED LINKS</span></span>

[<span data-ttu-id="fcc9e-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fcc9e-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fcc9e-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fcc9e-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fcc9e-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fcc9e-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fcc9e-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fcc9e-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


