---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356689"
---
# <span data-ttu-id="a0560-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a0560-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a0560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0560-102">SYNOPSIS</span></span>
<span data-ttu-id="a0560-103">Eltávolít egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="a0560-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a0560-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0560-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0560-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0560-105">DESCRIPTION</span></span>
<span data-ttu-id="a0560-106">A **Remove-AzExpressRouteCircuit** parancsmag eltávolít egy ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="a0560-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a0560-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0560-107">EXAMPLES</span></span>

### <span data-ttu-id="a0560-108">1. példa: ExpressRoute-áramkör törlése</span><span class="sxs-lookup"><span data-stu-id="a0560-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="a0560-109">2. példa: ExpressRoute-áramkör törlése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="a0560-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="a0560-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0560-110">PARAMETERS</span></span>

### <span data-ttu-id="a0560-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0560-111">-AsJob</span></span>
<span data-ttu-id="a0560-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a0560-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0560-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0560-113">-DefaultProfile</span></span>
<span data-ttu-id="a0560-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0560-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0560-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0560-115">-Force</span></span>
<span data-ttu-id="a0560-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a0560-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0560-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a0560-117">-Name</span></span>
<span data-ttu-id="a0560-118">Az eltávolítható ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="a0560-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="a0560-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0560-119">-PassThru</span></span>
<span data-ttu-id="a0560-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="a0560-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a0560-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a0560-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0560-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0560-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0560-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az ExpressRoute-kapcsolatcsoport tartozik.</span><span class="sxs-lookup"><span data-stu-id="a0560-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="a0560-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0560-124">-Confirm</span></span>
<span data-ttu-id="a0560-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0560-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0560-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0560-126">-WhatIf</span></span>
<span data-ttu-id="a0560-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a0560-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0560-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0560-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0560-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0560-129">CommonParameters</span></span>
<span data-ttu-id="a0560-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0560-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0560-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0560-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0560-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0560-132">INPUTS</span></span>

### <span data-ttu-id="a0560-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a0560-133">System.String</span></span>

## <span data-ttu-id="a0560-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0560-134">OUTPUTS</span></span>

### <span data-ttu-id="a0560-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0560-135">System.Boolean</span></span>

## <span data-ttu-id="a0560-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0560-136">NOTES</span></span>

## <span data-ttu-id="a0560-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0560-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0560-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a0560-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a0560-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a0560-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a0560-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a0560-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a0560-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a0560-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
