---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146763"
---
# <span data-ttu-id="e8737-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8737-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e8737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8737-102">SYNOPSIS</span></span>
<span data-ttu-id="e8737-103">Eltávolít egy SSL-házirendet egy Azure-alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e8737-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e8737-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8737-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8737-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8737-105">DESCRIPTION</span></span>
<span data-ttu-id="e8737-106">A Remove-AzApplicationGatewaySslPolicy parancsmag eltávolítja az SSL-házirendet egy Azure-alkalmazásátjáróból.</span><span class="sxs-lookup"><span data-stu-id="e8737-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e8737-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8737-107">EXAMPLES</span></span>

### <span data-ttu-id="e8737-108">1. példa: SSL-házirend eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="e8737-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="e8737-109">Ez a parancs eltávolítja az SSL-házirendet az ApplicationGateway01 nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e8737-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="e8737-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8737-110">PARAMETERS</span></span>

### <span data-ttu-id="e8737-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8737-111">-ApplicationGateway</span></span>
<span data-ttu-id="e8737-112">Azt az alkalmazás-átjárót adja meg, amelyből a parancsmag eltávolítja az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="e8737-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="e8737-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8737-113">-DefaultProfile</span></span>
<span data-ttu-id="e8737-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8737-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8737-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8737-115">-Force</span></span>
<span data-ttu-id="e8737-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8737-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8737-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8737-117">-Confirm</span></span>
<span data-ttu-id="e8737-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e8737-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8737-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8737-119">-WhatIf</span></span>
<span data-ttu-id="e8737-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e8737-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8737-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8737-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8737-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8737-122">CommonParameters</span></span>
<span data-ttu-id="e8737-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8737-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8737-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8737-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8737-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8737-125">INPUTS</span></span>

### <span data-ttu-id="e8737-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8737-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8737-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8737-127">OUTPUTS</span></span>

### <span data-ttu-id="e8737-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8737-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8737-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8737-129">NOTES</span></span>
<span data-ttu-id="e8737-130">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="e8737-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e8737-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8737-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8737-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8737-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e8737-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8737-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e8737-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8737-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

