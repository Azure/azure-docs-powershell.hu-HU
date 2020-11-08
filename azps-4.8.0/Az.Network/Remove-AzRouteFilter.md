---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181538"
---
# <span data-ttu-id="8c163-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8c163-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="8c163-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c163-102">SYNOPSIS</span></span>
<span data-ttu-id="8c163-103">Az útvonal-szűrő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8c163-103">Removes a route filter.</span></span>

## <span data-ttu-id="8c163-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c163-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c163-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c163-105">DESCRIPTION</span></span>
<span data-ttu-id="8c163-106">A **Remove-AzRouteFilter** parancsmag eltávolít egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="8c163-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="8c163-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c163-107">EXAMPLES</span></span>

### <span data-ttu-id="8c163-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8c163-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8c163-109">A parancs eltávolítja a RouteFilter01 nevű útvonal-szűrőt a ResourceGroup01 nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="8c163-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8c163-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c163-110">PARAMETERS</span></span>

### <span data-ttu-id="8c163-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c163-111">-DefaultProfile</span></span>
<span data-ttu-id="8c163-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c163-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c163-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8c163-113">-Force</span></span>
<span data-ttu-id="8c163-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c163-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8c163-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c163-115">-Name</span></span>
<span data-ttu-id="8c163-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8c163-116">The resource name.</span></span>

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

### <span data-ttu-id="8c163-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c163-117">-PassThru</span></span>
<span data-ttu-id="8c163-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8c163-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="8c163-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c163-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c163-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c163-120">The resource group name.</span></span>

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

### <span data-ttu-id="8c163-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c163-121">-Confirm</span></span>
<span data-ttu-id="8c163-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c163-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c163-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c163-123">-WhatIf</span></span>
<span data-ttu-id="8c163-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c163-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c163-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c163-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c163-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c163-126">CommonParameters</span></span>
<span data-ttu-id="8c163-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c163-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c163-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c163-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c163-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c163-129">INPUTS</span></span>

### <span data-ttu-id="8c163-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8c163-130">System.String</span></span>

## <span data-ttu-id="8c163-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c163-131">OUTPUTS</span></span>

### <span data-ttu-id="8c163-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c163-132">System.Boolean</span></span>

## <span data-ttu-id="8c163-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c163-133">NOTES</span></span>

## <span data-ttu-id="8c163-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c163-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c163-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8c163-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8c163-136">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8c163-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8c163-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8c163-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="8c163-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c163-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8c163-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c163-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8c163-140">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c163-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8c163-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c163-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8c163-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c163-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
