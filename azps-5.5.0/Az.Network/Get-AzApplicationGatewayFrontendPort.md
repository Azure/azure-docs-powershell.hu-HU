---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147139"
---
# <span data-ttu-id="7a7bc-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7bc-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7a7bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7bc-103">Egy alkalmazás átjárójának előlapi portját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="7a7bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a7bc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a7bc-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7bc-106">A **Get-AzApplicationGatewayFrontendPort** parancsmag egy alkalmazás-átjáró előtér-portját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="7a7bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a7bc-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7bc-108">1. példa: Adott előlapi port lekérte</span><span class="sxs-lookup"><span data-stu-id="7a7bc-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7a7bc-109">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7a7bc-110">A második parancs a FrontEndPort01 nevű előlapi portot $AppGw a $FrontEndPort tárolja.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="7a7bc-111">2. példa: Előlapi portok listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="7a7bc-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="7a7bc-112">Az első parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap az ResourceGroup01 nevű erőforráscsoportból, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7a7bc-113">A második parancs lekérte az előlapi portok listáját a $AppGw és tárolja a $FrontEndPorts változóban.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="7a7bc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a7bc-114">PARAMETERS</span></span>

### <span data-ttu-id="7a7bc-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a7bc-115">-ApplicationGateway</span></span>
<span data-ttu-id="7a7bc-116">Az előlapi portot tartalmazó alkalmazás-átjáróobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="7a7bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7bc-117">-DefaultProfile</span></span>
<span data-ttu-id="7a7bc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7bc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7a7bc-119">-Name</span></span>
<span data-ttu-id="7a7bc-120">A lekért előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="7a7bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7bc-121">CommonParameters</span></span>
<span data-ttu-id="7a7bc-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7bc-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a7bc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7bc-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a7bc-124">INPUTS</span></span>

### <span data-ttu-id="7a7bc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a7bc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a7bc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a7bc-126">OUTPUTS</span></span>

### <span data-ttu-id="7a7bc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7bc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7a7bc-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a7bc-128">NOTES</span></span>

## <span data-ttu-id="7a7bc-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a7bc-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a7bc-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7bc-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7a7bc-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7bc-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7a7bc-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7bc-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7a7bc-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7a7bc-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


