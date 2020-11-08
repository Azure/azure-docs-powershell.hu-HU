---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184332"
---
# <span data-ttu-id="d1ade-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ade-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="d1ade-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1ade-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ade-103">Az alkalmazás-átjárók automatikus méretarányos konfigurációjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="d1ade-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="d1ade-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1ade-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ade-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1ade-105">DESCRIPTION</span></span>
<span data-ttu-id="d1ade-106">A **set-AzApplicationGatewayAutoscaleConfiguration** parancsmag módosította az alkalmazás-átjárók meglévő automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d1ade-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="d1ade-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1ade-107">EXAMPLES</span></span>

### <span data-ttu-id="d1ade-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d1ade-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d1ade-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d1ade-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d1ade-110">A második parancs az alkalmazás-átjáróról frissíti az automatikus méretezés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d1ade-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="d1ade-111">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="d1ade-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="d1ade-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1ade-112">PARAMETERS</span></span>

### <span data-ttu-id="d1ade-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ade-113">-ApplicationGateway</span></span>
<span data-ttu-id="d1ade-114">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ade-114">The applicationGateway</span></span>

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

### <span data-ttu-id="d1ade-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ade-115">-DefaultProfile</span></span>
<span data-ttu-id="d1ade-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1ade-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1ade-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="d1ade-117">-MaxCapacity</span></span>
<span data-ttu-id="d1ade-118">Az Application Gateway maximális kapacitása.</span><span class="sxs-lookup"><span data-stu-id="d1ade-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="d1ade-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="d1ade-119">-MinCapacity</span></span>
<span data-ttu-id="d1ade-120">Az Application Gateway minimális kapacitása.</span><span class="sxs-lookup"><span data-stu-id="d1ade-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="d1ade-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1ade-121">-Confirm</span></span>
<span data-ttu-id="d1ade-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1ade-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ade-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ade-123">-WhatIf</span></span>
<span data-ttu-id="d1ade-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1ade-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1ade-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1ade-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ade-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ade-126">CommonParameters</span></span>
<span data-ttu-id="d1ade-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1ade-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ade-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ade-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ade-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1ade-129">INPUTS</span></span>

### <span data-ttu-id="d1ade-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ade-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1ade-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1ade-131">OUTPUTS</span></span>

### <span data-ttu-id="d1ade-132">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ade-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1ade-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1ade-133">NOTES</span></span>

## <span data-ttu-id="d1ade-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1ade-134">RELATED LINKS</span></span>

[<span data-ttu-id="d1ade-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ade-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="d1ade-136">Új – AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ade-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="d1ade-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ade-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
