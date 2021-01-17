---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468833"
---
# <span data-ttu-id="e6e07-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6e07-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="e6e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e07-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e07-103">Frissíti egy alkalmazás-átjáró automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e6e07-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="e6e07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6e07-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e07-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6e07-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e07-106">A **Set-AzApplicationGatewayAutoscaleConfiguration parancsmag** módosítja az alkalmazásátjárók meglévő automatikus skálás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e6e07-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="e6e07-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6e07-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e07-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6e07-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e6e07-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="e6e07-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="e6e07-110">A második parancs frissíti az automatikus skálázási konfigurációt az alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="e6e07-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="e6e07-111">A harmadik parancs frissíti az alkalmazás-átjárót az Azure-on.</span><span class="sxs-lookup"><span data-stu-id="e6e07-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e6e07-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6e07-112">PARAMETERS</span></span>

### <span data-ttu-id="e6e07-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6e07-113">-ApplicationGateway</span></span>
<span data-ttu-id="e6e07-114">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6e07-114">The applicationGateway</span></span>

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

### <span data-ttu-id="e6e07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e07-115">-DefaultProfile</span></span>
<span data-ttu-id="e6e07-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6e07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e07-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="e6e07-117">-MaxCapacity</span></span>
<span data-ttu-id="e6e07-118">Az alkalmazás-átjáró maximális kapacitása.</span><span class="sxs-lookup"><span data-stu-id="e6e07-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="e6e07-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="e6e07-119">-MinCapacity</span></span>
<span data-ttu-id="e6e07-120">Az alkalmazás-átjáró minimális kapacitása.</span><span class="sxs-lookup"><span data-stu-id="e6e07-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="e6e07-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6e07-121">-Confirm</span></span>
<span data-ttu-id="e6e07-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6e07-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e07-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e07-123">-WhatIf</span></span>
<span data-ttu-id="e6e07-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6e07-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e07-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6e07-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e07-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e07-126">CommonParameters</span></span>
<span data-ttu-id="e6e07-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e07-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e07-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e07-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e07-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6e07-129">INPUTS</span></span>

### <span data-ttu-id="e6e07-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6e07-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6e07-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6e07-131">OUTPUTS</span></span>

### <span data-ttu-id="e6e07-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6e07-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6e07-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6e07-133">NOTES</span></span>

## <span data-ttu-id="e6e07-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6e07-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6e07-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6e07-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="e6e07-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6e07-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="e6e07-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6e07-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
