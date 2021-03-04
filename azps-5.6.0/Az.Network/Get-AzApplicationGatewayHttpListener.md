---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941753"
---
# <span data-ttu-id="410be-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="410be-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="410be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410be-102">SYNOPSIS</span></span>
<span data-ttu-id="410be-103">Egy alkalmazás-átjáró HTTP- hallgatóját használja.</span><span class="sxs-lookup"><span data-stu-id="410be-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="410be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="410be-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="410be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="410be-105">DESCRIPTION</span></span>
<span data-ttu-id="410be-106">A **Get-AzApplicationGatewayHttpListener** parancsmag egy alkalmazás-átjáró HTTP- hallgatóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="410be-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="410be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="410be-107">EXAMPLES</span></span>

### <span data-ttu-id="410be-108">1. példa: Adott HTTP-hallgató le kérése</span><span class="sxs-lookup"><span data-stu-id="410be-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="410be-109">Ez a parancs egy Listener01 nevű HTTP-hallgatót kap.</span><span class="sxs-lookup"><span data-stu-id="410be-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="410be-110">2. példa: HTTP-hallgatói listájának le kérése</span><span class="sxs-lookup"><span data-stu-id="410be-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="410be-111">Ez a parancs a HTTP-hallgatók listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="410be-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="410be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="410be-112">PARAMETERS</span></span>

### <span data-ttu-id="410be-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="410be-113">-ApplicationGateway</span></span>
<span data-ttu-id="410be-114">A HTTP-et tartalmazó alkalmazás-átjáróobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="410be-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="410be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410be-115">-DefaultProfile</span></span>
<span data-ttu-id="410be-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="410be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="410be-117">-Name</span><span class="sxs-lookup"><span data-stu-id="410be-117">-Name</span></span>
<span data-ttu-id="410be-118">Annak a HTTP-hallgatónak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="410be-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="410be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410be-119">CommonParameters</span></span>
<span data-ttu-id="410be-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="410be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410be-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="410be-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410be-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="410be-122">INPUTS</span></span>

### <span data-ttu-id="410be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="410be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="410be-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="410be-124">OUTPUTS</span></span>

### <span data-ttu-id="410be-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="410be-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="410be-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="410be-126">NOTES</span></span>

## <span data-ttu-id="410be-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="410be-127">RELATED LINKS</span></span>

[<span data-ttu-id="410be-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="410be-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="410be-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="410be-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="410be-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="410be-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="410be-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="410be-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


