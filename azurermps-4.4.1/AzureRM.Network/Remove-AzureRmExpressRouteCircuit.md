---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497056"
---
# <span data-ttu-id="99cf8-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99cf8-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="99cf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="99cf8-103">ExpressRoute-áramkör eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="99cf8-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99cf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99cf8-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99cf8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="99cf8-106">A **Remove-AzureRmExpressRouteCircuit** parancsmag eltávolítja a ExpressRoute-áramkört.</span><span class="sxs-lookup"><span data-stu-id="99cf8-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="99cf8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="99cf8-108">Példa 1: ExpressRoute-áramkör törlése</span><span class="sxs-lookup"><span data-stu-id="99cf8-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="99cf8-109">2. példa: ExpressRoute-áramkör törlése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="99cf8-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="99cf8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="99cf8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="99cf8-111">-Force</span></span>
<span data-ttu-id="99cf8-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="99cf8-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99cf8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99cf8-113">-Name</span></span>
<span data-ttu-id="99cf8-114">Az eltávolítandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="99cf8-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="99cf8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99cf8-115">-PassThru</span></span>
<span data-ttu-id="99cf8-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="99cf8-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="99cf8-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="99cf8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99cf8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99cf8-118">-ResourceGroupName</span></span>
<span data-ttu-id="99cf8-119">Annak az erőforráscsoportnek a neve, amelyhez a ExpressRoute-áramkör tartozik.</span><span class="sxs-lookup"><span data-stu-id="99cf8-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="99cf8-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99cf8-120">-Confirm</span></span>
<span data-ttu-id="99cf8-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99cf8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99cf8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99cf8-122">-WhatIf</span></span>
<span data-ttu-id="99cf8-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99cf8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99cf8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99cf8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99cf8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cf8-125">-DefaultProfile</span></span>
<span data-ttu-id="99cf8-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99cf8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99cf8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cf8-127">CommonParameters</span></span>
<span data-ttu-id="99cf8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99cf8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cf8-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99cf8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cf8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99cf8-130">INPUTS</span></span>

## <span data-ttu-id="99cf8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99cf8-131">OUTPUTS</span></span>

## <span data-ttu-id="99cf8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99cf8-132">NOTES</span></span>

## <span data-ttu-id="99cf8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99cf8-133">RELATED LINKS</span></span>

[<span data-ttu-id="99cf8-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99cf8-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="99cf8-135">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99cf8-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="99cf8-136">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99cf8-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="99cf8-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99cf8-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
