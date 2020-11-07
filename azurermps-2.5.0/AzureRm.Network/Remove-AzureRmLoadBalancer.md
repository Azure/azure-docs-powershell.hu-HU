---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 96f6acdda93de63486f117c99572b4680fb025e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848122"
---
# <span data-ttu-id="70363-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70363-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="70363-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70363-102">SYNOPSIS</span></span>
<span data-ttu-id="70363-103">A terheléselosztó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="70363-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70363-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70363-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70363-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70363-105">DESCRIPTION</span></span>
<span data-ttu-id="70363-106">A **Remove-AzureRmLoadBalancer** parancsmag eltávolítja az Azure terheléselosztó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="70363-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="70363-107">Példák</span><span class="sxs-lookup"><span data-stu-id="70363-107">EXAMPLES</span></span>

### <span data-ttu-id="70363-108">1. példa: terheléselosztó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70363-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="70363-109">Ez a parancs törli a MyLoadBalancer nevű terheléselosztó nevű MyResourceGroup a nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="70363-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="70363-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70363-110">PARAMETERS</span></span>

### <span data-ttu-id="70363-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70363-111">-AsJob</span></span>
<span data-ttu-id="70363-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70363-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70363-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70363-113">-DefaultProfile</span></span>
<span data-ttu-id="70363-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70363-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70363-115">-Force</span><span class="sxs-lookup"><span data-stu-id="70363-115">-Force</span></span>
<span data-ttu-id="70363-116">Azt jelzi, hogy ez a parancsmag eltávolítja a terheléselosztást függetlenül attól, hogy az erőforrásokat rendelte-e hozzá.</span><span class="sxs-lookup"><span data-stu-id="70363-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70363-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70363-117">-Name</span></span>
<span data-ttu-id="70363-118">Az eltávolítandó terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70363-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="70363-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70363-119">-PassThru</span></span>
<span data-ttu-id="70363-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="70363-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="70363-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="70363-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70363-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70363-122">-ResourceGroupName</span></span>
<span data-ttu-id="70363-123">Annak a csoportnak a nevét adja meg, amely az eltávolítandó terheléselosztót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="70363-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="70363-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70363-124">-Confirm</span></span>
<span data-ttu-id="70363-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70363-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70363-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70363-126">-WhatIf</span></span>
<span data-ttu-id="70363-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70363-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70363-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70363-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70363-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70363-129">CommonParameters</span></span>
<span data-ttu-id="70363-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70363-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70363-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70363-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70363-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70363-132">INPUTS</span></span>

## <span data-ttu-id="70363-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70363-133">OUTPUTS</span></span>

## <span data-ttu-id="70363-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70363-134">NOTES</span></span>

## <span data-ttu-id="70363-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70363-135">RELATED LINKS</span></span>

[<span data-ttu-id="70363-136">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70363-136">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="70363-137">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70363-137">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="70363-138">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70363-138">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


