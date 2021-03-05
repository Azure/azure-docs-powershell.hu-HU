---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e849b109ba1f1fd43ca960d56581357729f5c344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010358"
---
# <span data-ttu-id="15942-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="15942-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="15942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15942-102">SYNOPSIS</span></span>
<span data-ttu-id="15942-103">Automatikus méretezésű konfigurációt hoz létre az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="15942-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="15942-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15942-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15942-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15942-105">DESCRIPTION</span></span>
<span data-ttu-id="15942-106">A **New-AzApplicationGatewayAutoscaleConfiguration parancsmag** létrehoz egy automatikus skálás konfigurációt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="15942-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="15942-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15942-107">EXAMPLES</span></span>

### <span data-ttu-id="15942-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="15942-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="15942-109">Az első parancs létrehoz egy 3-as kapacitású automatikus skálázási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="15942-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="15942-110">A második parancs létrehoz egy automatikus skálázási konfigurációval konfigurált alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="15942-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="15942-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15942-111">PARAMETERS</span></span>

### <span data-ttu-id="15942-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15942-112">-DefaultProfile</span></span>
<span data-ttu-id="15942-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15942-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15942-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="15942-114">-MaxCapacity</span></span>
<span data-ttu-id="15942-115">Az alkalmazás-átjáróhoz mindig rendelkezésre álló [és díjbeszámító] maximális kapacitásegységek.</span><span class="sxs-lookup"><span data-stu-id="15942-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15942-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="15942-116">-MinCapacity</span></span>
<span data-ttu-id="15942-117">Az alkalmazás-átjárókhoz mindig rendelkezésre álló [és díjbeszámító] minimális kapacitásegységek.</span><span class="sxs-lookup"><span data-stu-id="15942-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15942-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15942-118">-Confirm</span></span>
<span data-ttu-id="15942-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15942-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15942-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15942-120">-WhatIf</span></span>
<span data-ttu-id="15942-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15942-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15942-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15942-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15942-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15942-123">CommonParameters</span></span>
<span data-ttu-id="15942-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15942-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15942-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15942-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15942-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15942-126">INPUTS</span></span>

### <span data-ttu-id="15942-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="15942-127">None</span></span>

## <span data-ttu-id="15942-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15942-128">OUTPUTS</span></span>

### <span data-ttu-id="15942-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="15942-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="15942-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15942-130">NOTES</span></span>

## <span data-ttu-id="15942-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15942-131">RELATED LINKS</span></span>

[<span data-ttu-id="15942-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="15942-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="15942-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="15942-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="15942-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="15942-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
