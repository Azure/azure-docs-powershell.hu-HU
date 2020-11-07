---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 8f48cf6fb5b3c4489a116ef0f7ee5a32649d96ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670125"
---
# <span data-ttu-id="39c16-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39c16-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="39c16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39c16-102">SYNOPSIS</span></span>
<span data-ttu-id="39c16-103">Az útvonal-szűrő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="39c16-103">Removes a route filter.</span></span>

## <span data-ttu-id="39c16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39c16-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39c16-105">DESCRIPTION</span></span>
<span data-ttu-id="39c16-106">A **Remove-AzRouteFilter** parancsmag eltávolít egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="39c16-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="39c16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="39c16-107">EXAMPLES</span></span>

### <span data-ttu-id="39c16-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39c16-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="39c16-109">A parancs eltávolítja a RouteFilter01 nevű útvonal-szűrőt a ResourceGroup01 nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="39c16-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="39c16-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39c16-110">PARAMETERS</span></span>

### <span data-ttu-id="39c16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c16-111">-DefaultProfile</span></span>
<span data-ttu-id="39c16-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39c16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c16-113">-Force</span><span class="sxs-lookup"><span data-stu-id="39c16-113">-Force</span></span>
<span data-ttu-id="39c16-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39c16-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="39c16-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39c16-115">-Name</span></span>
<span data-ttu-id="39c16-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="39c16-116">The resource name.</span></span>

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

### <span data-ttu-id="39c16-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39c16-117">-PassThru</span></span>
<span data-ttu-id="39c16-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="39c16-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="39c16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c16-119">-ResourceGroupName</span></span>
<span data-ttu-id="39c16-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="39c16-120">The resource group name.</span></span>

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

### <span data-ttu-id="39c16-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39c16-121">-Confirm</span></span>
<span data-ttu-id="39c16-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39c16-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c16-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c16-123">-WhatIf</span></span>
<span data-ttu-id="39c16-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39c16-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c16-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39c16-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c16-126">CommonParameters</span></span>
<span data-ttu-id="39c16-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39c16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c16-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c16-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39c16-129">INPUTS</span></span>

### <span data-ttu-id="39c16-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39c16-130">System.String</span></span>

## <span data-ttu-id="39c16-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39c16-131">OUTPUTS</span></span>

### <span data-ttu-id="39c16-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39c16-132">System.Boolean</span></span>

## <span data-ttu-id="39c16-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39c16-133">NOTES</span></span>

## <span data-ttu-id="39c16-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39c16-134">RELATED LINKS</span></span>

[<span data-ttu-id="39c16-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39c16-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="39c16-136">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39c16-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="39c16-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39c16-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="39c16-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c16-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39c16-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c16-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39c16-140">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c16-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39c16-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c16-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39c16-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c16-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
