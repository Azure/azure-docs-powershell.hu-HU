---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499479"
---
# <span data-ttu-id="c3c03-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c03-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c3c03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3c03-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c03-103">Az alkalmazás-átjárók automatikus méretarányos konfigurációjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="c3c03-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3c03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3c03-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3c03-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3c03-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c03-106">A **set-AzureRmApplicationGatewayAutoscaleConfiguration** parancsmag módosította az alkalmazás-átjárók meglévő automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c3c03-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="c3c03-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3c03-107">EXAMPLES</span></span>

### <span data-ttu-id="c3c03-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3c03-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c3c03-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c3c03-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c3c03-110">A második parancs frissíti az automatikus méretezés konfigurációját az applicationg-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="c3c03-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="c3c03-111">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="c3c03-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c3c03-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3c03-112">PARAMETERS</span></span>

### <span data-ttu-id="c3c03-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3c03-113">-ApplicationGateway</span></span>
<span data-ttu-id="c3c03-114">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3c03-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c3c03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c03-115">-DefaultProfile</span></span>
<span data-ttu-id="c3c03-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3c03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c03-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="c3c03-117">-MinCapacity</span></span>
<span data-ttu-id="c3c03-118">Az capcity minimális értékének beállítása.</span><span class="sxs-lookup"><span data-stu-id="c3c03-118">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="c3c03-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3c03-119">-Confirm</span></span>
<span data-ttu-id="c3c03-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3c03-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3c03-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3c03-121">-WhatIf</span></span>
<span data-ttu-id="c3c03-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3c03-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3c03-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3c03-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3c03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c03-124">CommonParameters</span></span>
<span data-ttu-id="c3c03-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3c03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c03-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c03-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c03-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3c03-127">INPUTS</span></span>

### <span data-ttu-id="c3c03-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3c03-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3c03-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3c03-129">OUTPUTS</span></span>

### <span data-ttu-id="c3c03-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3c03-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3c03-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3c03-131">NOTES</span></span>

## <span data-ttu-id="c3c03-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3c03-132">RELATED LINKS</span></span>
