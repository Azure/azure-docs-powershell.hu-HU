---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848129"
---
# <span data-ttu-id="da31d-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="da31d-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="da31d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da31d-102">SYNOPSIS</span></span>
<span data-ttu-id="da31d-103">ExpressRoute-áramkör eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="da31d-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da31d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da31d-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da31d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da31d-105">DESCRIPTION</span></span>
<span data-ttu-id="da31d-106">A **Remove-AzureRmExpressRouteCircuit** parancsmag eltávolítja a ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="da31d-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="da31d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da31d-107">EXAMPLES</span></span>

### <span data-ttu-id="da31d-108">Példa 1: ExpressRoute-áramkör törlése</span><span class="sxs-lookup"><span data-stu-id="da31d-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="da31d-109">2. példa: ExpressRoute-áramkör törlése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="da31d-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="da31d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da31d-110">PARAMETERS</span></span>

### <span data-ttu-id="da31d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da31d-111">-AsJob</span></span>
<span data-ttu-id="da31d-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da31d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da31d-113">-DefaultProfile</span></span>
<span data-ttu-id="da31d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da31d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="da31d-115">-Force</span></span>
<span data-ttu-id="da31d-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="da31d-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da31d-117">-Name</span></span>
<span data-ttu-id="da31d-118">Az eltávolítandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="da31d-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da31d-119">-PassThru</span></span>
<span data-ttu-id="da31d-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="da31d-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="da31d-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="da31d-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da31d-122">-ResourceGroupName</span></span>
<span data-ttu-id="da31d-123">Annak az erőforráscsoportnek a neve, amelyhez a ExpressRoute-áramkör tartozik.</span><span class="sxs-lookup"><span data-stu-id="da31d-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da31d-124">-Confirm</span></span>
<span data-ttu-id="da31d-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da31d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da31d-126">-WhatIf</span></span>
<span data-ttu-id="da31d-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da31d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da31d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da31d-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da31d-129">CommonParameters</span></span>
<span data-ttu-id="da31d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da31d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da31d-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da31d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da31d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da31d-132">INPUTS</span></span>

## <span data-ttu-id="da31d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da31d-133">OUTPUTS</span></span>

## <span data-ttu-id="da31d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da31d-134">NOTES</span></span>

## <span data-ttu-id="da31d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da31d-135">RELATED LINKS</span></span>

[<span data-ttu-id="da31d-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="da31d-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="da31d-137">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="da31d-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="da31d-138">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="da31d-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="da31d-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="da31d-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
