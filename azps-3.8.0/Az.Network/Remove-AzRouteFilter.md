---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013988"
---
# <span data-ttu-id="21106-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21106-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="21106-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21106-102">SYNOPSIS</span></span>
<span data-ttu-id="21106-103">Az útvonal-szűrő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="21106-103">Removes a route filter.</span></span>

## <span data-ttu-id="21106-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21106-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21106-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21106-105">DESCRIPTION</span></span>
<span data-ttu-id="21106-106">A **Remove-AzRouteFilter** parancsmag eltávolít egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="21106-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="21106-107">Példák</span><span class="sxs-lookup"><span data-stu-id="21106-107">EXAMPLES</span></span>

### <span data-ttu-id="21106-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21106-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="21106-109">A parancs eltávolítja a RouteFilter01 nevű útvonal-szűrőt a ResourceGroup01 nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="21106-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="21106-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21106-110">PARAMETERS</span></span>

### <span data-ttu-id="21106-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21106-111">-DefaultProfile</span></span>
<span data-ttu-id="21106-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21106-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21106-113">-Force</span><span class="sxs-lookup"><span data-stu-id="21106-113">-Force</span></span>
<span data-ttu-id="21106-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21106-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="21106-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21106-115">-Name</span></span>
<span data-ttu-id="21106-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="21106-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21106-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21106-117">-PassThru</span></span>
<span data-ttu-id="21106-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="21106-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="21106-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21106-119">-ResourceGroupName</span></span>
<span data-ttu-id="21106-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="21106-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21106-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21106-121">-Confirm</span></span>
<span data-ttu-id="21106-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21106-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21106-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21106-123">-WhatIf</span></span>
<span data-ttu-id="21106-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21106-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21106-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21106-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21106-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21106-126">CommonParameters</span></span>
<span data-ttu-id="21106-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21106-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21106-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21106-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21106-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21106-129">INPUTS</span></span>

### <span data-ttu-id="21106-130">System. String</span><span class="sxs-lookup"><span data-stu-id="21106-130">System.String</span></span>

## <span data-ttu-id="21106-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21106-131">OUTPUTS</span></span>

### <span data-ttu-id="21106-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21106-132">System.Boolean</span></span>

## <span data-ttu-id="21106-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21106-133">NOTES</span></span>

## <span data-ttu-id="21106-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21106-134">RELATED LINKS</span></span>

[<span data-ttu-id="21106-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21106-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="21106-136">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21106-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="21106-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21106-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="21106-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21106-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21106-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21106-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21106-140">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21106-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21106-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21106-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21106-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21106-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
