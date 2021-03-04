---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930922"
---
# <span data-ttu-id="dcad9-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dcad9-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="dcad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcad9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcad9-103">Eltávolít egy útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="dcad9-103">Removes a route filter.</span></span>

## <span data-ttu-id="dcad9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcad9-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcad9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcad9-105">DESCRIPTION</span></span>
<span data-ttu-id="dcad9-106">Az **Remove-AzRouteFilter** parancsmag eltávolítja az útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="dcad9-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="dcad9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcad9-107">EXAMPLES</span></span>

### <span data-ttu-id="dcad9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="dcad9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dcad9-109">A parancs eltávolítja a RouteFilter01 nevű útvonalszűrőt az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="dcad9-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="dcad9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcad9-110">PARAMETERS</span></span>

### <span data-ttu-id="dcad9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcad9-111">-DefaultProfile</span></span>
<span data-ttu-id="dcad9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcad9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcad9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dcad9-113">-Force</span></span>
<span data-ttu-id="dcad9-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dcad9-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dcad9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dcad9-115">-Name</span></span>
<span data-ttu-id="dcad9-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dcad9-116">The resource name.</span></span>

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

### <span data-ttu-id="dcad9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcad9-117">-PassThru</span></span>
<span data-ttu-id="dcad9-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="dcad9-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="dcad9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcad9-119">-ResourceGroupName</span></span>
<span data-ttu-id="dcad9-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dcad9-120">The resource group name.</span></span>

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

### <span data-ttu-id="dcad9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcad9-121">-Confirm</span></span>
<span data-ttu-id="dcad9-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dcad9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcad9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcad9-123">-WhatIf</span></span>
<span data-ttu-id="dcad9-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dcad9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcad9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcad9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcad9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcad9-126">CommonParameters</span></span>
<span data-ttu-id="dcad9-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcad9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcad9-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcad9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcad9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcad9-129">INPUTS</span></span>

### <span data-ttu-id="dcad9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dcad9-130">System.String</span></span>

## <span data-ttu-id="dcad9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcad9-131">OUTPUTS</span></span>

### <span data-ttu-id="dcad9-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dcad9-132">System.Boolean</span></span>

## <span data-ttu-id="dcad9-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcad9-133">NOTES</span></span>

## <span data-ttu-id="dcad9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcad9-134">RELATED LINKS</span></span>

[<span data-ttu-id="dcad9-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dcad9-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="dcad9-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dcad9-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="dcad9-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dcad9-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="dcad9-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcad9-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dcad9-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcad9-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dcad9-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcad9-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dcad9-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcad9-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dcad9-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcad9-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
