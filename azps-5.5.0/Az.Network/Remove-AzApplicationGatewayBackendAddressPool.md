---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206654"
---
# <span data-ttu-id="bda65-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bda65-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bda65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bda65-102">SYNOPSIS</span></span>
<span data-ttu-id="bda65-103">Eltávolít egy háttércímkészletet egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="bda65-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="bda65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bda65-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda65-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bda65-105">DESCRIPTION</span></span>
<span data-ttu-id="bda65-106">A **Remove-AzApplicationGatewayBackendAddressPool** parancsmag eltávolít egy háttércímkészletet egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="bda65-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="bda65-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bda65-107">EXAMPLES</span></span>

### <span data-ttu-id="bda65-108">1. példa: Háttércímkészlet eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="bda65-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="bda65-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoporthoz tartozó, és a $AppGw menti.</span><span class="sxs-lookup"><span data-stu-id="bda65-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="bda65-110">A második parancs eltávolítja a BackEndPool02 nevű háttércímkészletet az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="bda65-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="bda65-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bda65-111">PARAMETERS</span></span>

### <span data-ttu-id="bda65-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bda65-112">-ApplicationGateway</span></span>
<span data-ttu-id="bda65-113">Azt az alkalmazás-átjárót adja meg, amelyből a parancsmag eltávolítja a háttércímkészletet.</span><span class="sxs-lookup"><span data-stu-id="bda65-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="bda65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda65-114">-DefaultProfile</span></span>
<span data-ttu-id="bda65-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bda65-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bda65-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bda65-116">-Name</span></span>
<span data-ttu-id="bda65-117">Annak a háttércímkészletnek a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bda65-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bda65-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bda65-118">-Confirm</span></span>
<span data-ttu-id="bda65-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bda65-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda65-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda65-120">-WhatIf</span></span>
<span data-ttu-id="bda65-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bda65-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bda65-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bda65-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda65-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda65-123">CommonParameters</span></span>
<span data-ttu-id="bda65-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda65-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda65-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda65-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda65-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bda65-126">INPUTS</span></span>

### <span data-ttu-id="bda65-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bda65-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bda65-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bda65-128">OUTPUTS</span></span>

### <span data-ttu-id="bda65-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bda65-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bda65-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bda65-130">NOTES</span></span>

## <span data-ttu-id="bda65-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bda65-131">RELATED LINKS</span></span>

[<span data-ttu-id="bda65-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bda65-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bda65-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bda65-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bda65-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bda65-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bda65-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bda65-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


