---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481196"
---
# <span data-ttu-id="81636-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81636-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="81636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81636-102">SYNOPSIS</span></span>
<span data-ttu-id="81636-103">Eltávolít egy útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="81636-103">Removes a route filter.</span></span>

## <span data-ttu-id="81636-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81636-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81636-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81636-105">DESCRIPTION</span></span>
<span data-ttu-id="81636-106">Az **Remove-AzRouteFilter** parancsmag eltávolít egy útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="81636-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="81636-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81636-107">EXAMPLES</span></span>

### <span data-ttu-id="81636-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="81636-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="81636-109">A parancs eltávolítja a RouteFilter01 nevű útvonalszűrőt az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="81636-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="81636-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81636-110">PARAMETERS</span></span>

### <span data-ttu-id="81636-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81636-111">-DefaultProfile</span></span>
<span data-ttu-id="81636-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81636-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81636-113">-Force</span><span class="sxs-lookup"><span data-stu-id="81636-113">-Force</span></span>
<span data-ttu-id="81636-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81636-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="81636-115">-Name</span><span class="sxs-lookup"><span data-stu-id="81636-115">-Name</span></span>
<span data-ttu-id="81636-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="81636-116">The resource name.</span></span>

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

### <span data-ttu-id="81636-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81636-117">-PassThru</span></span>
<span data-ttu-id="81636-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="81636-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="81636-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81636-119">-ResourceGroupName</span></span>
<span data-ttu-id="81636-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81636-120">The resource group name.</span></span>

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

### <span data-ttu-id="81636-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81636-121">-Confirm</span></span>
<span data-ttu-id="81636-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="81636-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81636-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81636-123">-WhatIf</span></span>
<span data-ttu-id="81636-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="81636-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81636-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81636-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81636-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81636-126">CommonParameters</span></span>
<span data-ttu-id="81636-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81636-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81636-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81636-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81636-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81636-129">INPUTS</span></span>

### <span data-ttu-id="81636-130">System.String</span><span class="sxs-lookup"><span data-stu-id="81636-130">System.String</span></span>

## <span data-ttu-id="81636-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81636-131">OUTPUTS</span></span>

### <span data-ttu-id="81636-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81636-132">System.Boolean</span></span>

## <span data-ttu-id="81636-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81636-133">NOTES</span></span>

## <span data-ttu-id="81636-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81636-134">RELATED LINKS</span></span>

[<span data-ttu-id="81636-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81636-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="81636-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81636-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="81636-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81636-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="81636-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81636-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81636-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81636-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81636-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81636-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81636-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81636-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81636-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81636-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
