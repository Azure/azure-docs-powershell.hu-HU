---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e6321125958b872d15f60bbe433819c4c6f1d7ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015014"
---
# <span data-ttu-id="a0c49-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c49-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a0c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c49-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c49-103">Eltávolítja az automatikus méretezésű konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a0c49-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="a0c49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0c49-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0c49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0c49-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c49-106">A **Remove-AzApplicationGatewayAutoscaleConfiguration parancsmag** eltávolítja az automatikus skálás konfigurációt egy meglévő alkalmazásátjáróból.</span><span class="sxs-lookup"><span data-stu-id="a0c49-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="a0c49-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0c49-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c49-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a0c49-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="a0c49-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="a0c49-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a0c49-110">A második parancs eltávolítja az automatikus skálázási konfigurációt az alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a0c49-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="a0c49-111">A harmadik parancs frissíti az alkalmazás-átjárót az Azure-on.</span><span class="sxs-lookup"><span data-stu-id="a0c49-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="a0c49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0c49-112">PARAMETERS</span></span>

### <span data-ttu-id="a0c49-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0c49-113">-ApplicationGateway</span></span>
<span data-ttu-id="a0c49-114">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0c49-114">The applicationGateway</span></span>

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

### <span data-ttu-id="a0c49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c49-115">-DefaultProfile</span></span>
<span data-ttu-id="a0c49-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0c49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c49-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a0c49-117">-Force</span></span>
<span data-ttu-id="a0c49-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0c49-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0c49-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0c49-119">-Confirm</span></span>
<span data-ttu-id="a0c49-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0c49-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0c49-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c49-121">-WhatIf</span></span>
<span data-ttu-id="a0c49-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a0c49-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0c49-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0c49-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0c49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c49-124">CommonParameters</span></span>
<span data-ttu-id="a0c49-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c49-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c49-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c49-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0c49-127">INPUTS</span></span>

### <span data-ttu-id="a0c49-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0c49-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0c49-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0c49-129">OUTPUTS</span></span>

### <span data-ttu-id="a0c49-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0c49-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0c49-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0c49-131">NOTES</span></span>

## <span data-ttu-id="a0c49-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0c49-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0c49-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c49-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a0c49-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c49-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a0c49-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c49-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
