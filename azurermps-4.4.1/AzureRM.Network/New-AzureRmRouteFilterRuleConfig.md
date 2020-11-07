---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3c3e20762bcf8e48fc3f01d750419493a81ca8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672435"
---
# <span data-ttu-id="19167-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19167-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="19167-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19167-102">SYNOPSIS</span></span>
<span data-ttu-id="19167-103">Az útvonaltervezés szabályait hozza létre az útvonal-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="19167-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19167-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19167-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19167-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19167-105">DESCRIPTION</span></span>
<span data-ttu-id="19167-106">Az New-AzureRmRouteFilterRuleConfig parancsmag létrehoz egy útvonal-szűrési szabályt az Azure Route-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="19167-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="19167-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19167-107">EXAMPLES</span></span>

### <span data-ttu-id="19167-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19167-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="19167-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="19167-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="19167-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19167-110">PARAMETERS</span></span>

### <span data-ttu-id="19167-111">-Access</span><span class="sxs-lookup"><span data-stu-id="19167-111">-Access</span></span>
<span data-ttu-id="19167-112">Hozzáférés az útvonal-szűrő szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="19167-112">Access for route filter rule.</span></span>
<span data-ttu-id="19167-113">Az érvényes értékek: Allow vagy deny.</span><span class="sxs-lookup"><span data-stu-id="19167-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19167-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="19167-114">-CommunityList</span></span>
<span data-ttu-id="19167-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="19167-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19167-116">-Force</span><span class="sxs-lookup"><span data-stu-id="19167-116">-Force</span></span>
<span data-ttu-id="19167-117">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="19167-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="19167-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19167-118">-Name</span></span>
<span data-ttu-id="19167-119">Az útvonal-szűrő szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19167-119">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="19167-120">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="19167-120">-RouteFilterRuleType</span></span>
<span data-ttu-id="19167-121">Az útvonal szűrési szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="19167-121">Route Filter Rule Type.</span></span>
<span data-ttu-id="19167-122">Az érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="19167-122">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19167-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19167-123">-Confirm</span></span>
<span data-ttu-id="19167-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19167-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19167-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19167-125">-WhatIf</span></span>
<span data-ttu-id="19167-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19167-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19167-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19167-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19167-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19167-128">-DefaultProfile</span></span>
<span data-ttu-id="19167-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19167-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19167-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19167-130">CommonParameters</span></span>
<span data-ttu-id="19167-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19167-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19167-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19167-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19167-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19167-133">INPUTS</span></span>

## <span data-ttu-id="19167-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19167-134">OUTPUTS</span></span>

### <span data-ttu-id="19167-135">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="19167-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="19167-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19167-136">NOTES</span></span>
<span data-ttu-id="19167-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="19167-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="19167-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19167-138">RELATED LINKS</span></span>

[<span data-ttu-id="19167-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19167-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="19167-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19167-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="19167-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19167-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="19167-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="19167-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

