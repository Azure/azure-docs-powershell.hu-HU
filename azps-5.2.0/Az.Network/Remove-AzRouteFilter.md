---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344789"
---
# <span data-ttu-id="6feb5-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6feb5-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="6feb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6feb5-102">SYNOPSIS</span></span>
<span data-ttu-id="6feb5-103">Eltávolít egy útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="6feb5-103">Removes a route filter.</span></span>

## <span data-ttu-id="6feb5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6feb5-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6feb5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6feb5-105">DESCRIPTION</span></span>
<span data-ttu-id="6feb5-106">Az **Remove-AzRouteFilter** parancsmag eltávolít egy útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="6feb5-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="6feb5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6feb5-107">EXAMPLES</span></span>

### <span data-ttu-id="6feb5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6feb5-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6feb5-109">A parancs eltávolítja a RouteFilter01 nevű útvonalszűrőt az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6feb5-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6feb5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6feb5-110">PARAMETERS</span></span>

### <span data-ttu-id="6feb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6feb5-111">-DefaultProfile</span></span>
<span data-ttu-id="6feb5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6feb5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6feb5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6feb5-113">-Force</span></span>
<span data-ttu-id="6feb5-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6feb5-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6feb5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6feb5-115">-Name</span></span>
<span data-ttu-id="6feb5-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6feb5-116">The resource name.</span></span>

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

### <span data-ttu-id="6feb5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6feb5-117">-PassThru</span></span>
<span data-ttu-id="6feb5-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="6feb5-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="6feb5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6feb5-119">-ResourceGroupName</span></span>
<span data-ttu-id="6feb5-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6feb5-120">The resource group name.</span></span>

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

### <span data-ttu-id="6feb5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6feb5-121">-Confirm</span></span>
<span data-ttu-id="6feb5-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6feb5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6feb5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6feb5-123">-WhatIf</span></span>
<span data-ttu-id="6feb5-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6feb5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6feb5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6feb5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6feb5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6feb5-126">CommonParameters</span></span>
<span data-ttu-id="6feb5-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6feb5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6feb5-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6feb5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6feb5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6feb5-129">INPUTS</span></span>

### <span data-ttu-id="6feb5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6feb5-130">System.String</span></span>

## <span data-ttu-id="6feb5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6feb5-131">OUTPUTS</span></span>

### <span data-ttu-id="6feb5-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6feb5-132">System.Boolean</span></span>

## <span data-ttu-id="6feb5-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6feb5-133">NOTES</span></span>

## <span data-ttu-id="6feb5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6feb5-134">RELATED LINKS</span></span>

[<span data-ttu-id="6feb5-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6feb5-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6feb5-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6feb5-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="6feb5-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6feb5-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="6feb5-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6feb5-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6feb5-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6feb5-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6feb5-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6feb5-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6feb5-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6feb5-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6feb5-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6feb5-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
