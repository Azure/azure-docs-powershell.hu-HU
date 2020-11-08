---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025167"
---
# <span data-ttu-id="76556-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76556-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="76556-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76556-102">SYNOPSIS</span></span>
<span data-ttu-id="76556-103">Az automatikus méretezési konfiguráció eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="76556-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="76556-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76556-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76556-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76556-105">DESCRIPTION</span></span>
<span data-ttu-id="76556-106">A **Remove-AzApplicationGatewayAutoscaleConfiguration** parancsmag egy meglévő alkalmazás-átjáróból távolítja el az automatikus méretezés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="76556-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="76556-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76556-107">EXAMPLES</span></span>

### <span data-ttu-id="76556-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="76556-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="76556-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="76556-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="76556-110">A második parancs eltávolítja az automatikus méretezési konfigurációt az alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="76556-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="76556-111">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="76556-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="76556-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76556-112">PARAMETERS</span></span>

### <span data-ttu-id="76556-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76556-113">-ApplicationGateway</span></span>
<span data-ttu-id="76556-114">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="76556-114">The applicationGateway</span></span>

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

### <span data-ttu-id="76556-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76556-115">-DefaultProfile</span></span>
<span data-ttu-id="76556-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76556-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76556-117">-Force</span><span class="sxs-lookup"><span data-stu-id="76556-117">-Force</span></span>
<span data-ttu-id="76556-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76556-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="76556-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76556-119">-Confirm</span></span>
<span data-ttu-id="76556-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76556-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76556-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76556-121">-WhatIf</span></span>
<span data-ttu-id="76556-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76556-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76556-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76556-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76556-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76556-124">CommonParameters</span></span>
<span data-ttu-id="76556-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76556-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76556-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76556-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76556-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76556-127">INPUTS</span></span>

### <span data-ttu-id="76556-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76556-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76556-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76556-129">OUTPUTS</span></span>

### <span data-ttu-id="76556-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76556-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76556-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76556-131">NOTES</span></span>

## <span data-ttu-id="76556-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76556-132">RELATED LINKS</span></span>

[<span data-ttu-id="76556-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76556-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="76556-134">Új – AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76556-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="76556-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76556-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
