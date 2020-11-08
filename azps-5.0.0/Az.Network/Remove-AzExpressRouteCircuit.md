---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195354"
---
# <span data-ttu-id="65085-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65085-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="65085-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65085-102">SYNOPSIS</span></span>
<span data-ttu-id="65085-103">ExpressRoute-áramkör eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="65085-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="65085-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65085-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65085-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65085-105">DESCRIPTION</span></span>
<span data-ttu-id="65085-106">A **Remove-AzExpressRouteCircuit** parancsmag eltávolítja a ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="65085-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="65085-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65085-107">EXAMPLES</span></span>

### <span data-ttu-id="65085-108">Példa 1: ExpressRoute-áramkör törlése</span><span class="sxs-lookup"><span data-stu-id="65085-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="65085-109">2. példa: ExpressRoute-áramkör törlése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="65085-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="65085-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65085-110">PARAMETERS</span></span>

### <span data-ttu-id="65085-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65085-111">-AsJob</span></span>
<span data-ttu-id="65085-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65085-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65085-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65085-113">-DefaultProfile</span></span>
<span data-ttu-id="65085-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65085-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65085-115">-Force</span><span class="sxs-lookup"><span data-stu-id="65085-115">-Force</span></span>
<span data-ttu-id="65085-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="65085-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65085-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65085-117">-Name</span></span>
<span data-ttu-id="65085-118">Az eltávolítandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="65085-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="65085-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65085-119">-PassThru</span></span>
<span data-ttu-id="65085-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="65085-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="65085-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="65085-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="65085-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65085-122">-ResourceGroupName</span></span>
<span data-ttu-id="65085-123">Annak az erőforráscsoportnek a neve, amelyhez a ExpressRoute-áramkör tartozik.</span><span class="sxs-lookup"><span data-stu-id="65085-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="65085-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65085-124">-Confirm</span></span>
<span data-ttu-id="65085-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65085-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65085-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65085-126">-WhatIf</span></span>
<span data-ttu-id="65085-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65085-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65085-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65085-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65085-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65085-129">CommonParameters</span></span>
<span data-ttu-id="65085-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65085-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65085-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65085-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65085-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65085-132">INPUTS</span></span>

### <span data-ttu-id="65085-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65085-133">System.String</span></span>

## <span data-ttu-id="65085-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65085-134">OUTPUTS</span></span>

### <span data-ttu-id="65085-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65085-135">System.Boolean</span></span>

## <span data-ttu-id="65085-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65085-136">NOTES</span></span>

## <span data-ttu-id="65085-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65085-137">RELATED LINKS</span></span>

[<span data-ttu-id="65085-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65085-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="65085-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65085-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="65085-140">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65085-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="65085-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65085-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
