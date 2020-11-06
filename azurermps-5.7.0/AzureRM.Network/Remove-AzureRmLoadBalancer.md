---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 13ece8d5bb6ec42e59f6a44910d3a3d46dd9d844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493730"
---
# <span data-ttu-id="fb518-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb518-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="fb518-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb518-102">SYNOPSIS</span></span>
<span data-ttu-id="fb518-103">A terheléselosztó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="fb518-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb518-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb518-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb518-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb518-105">DESCRIPTION</span></span>
<span data-ttu-id="fb518-106">A **Remove-AzureRmLoadBalancer** parancsmag eltávolítja az Azure terheléselosztó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="fb518-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="fb518-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb518-107">EXAMPLES</span></span>

### <span data-ttu-id="fb518-108">1. példa: terheléselosztó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fb518-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fb518-109">Ez a parancs törli a MyLoadBalancer nevű terheléselosztó nevű MyResourceGroup a nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="fb518-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fb518-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb518-110">PARAMETERS</span></span>

### <span data-ttu-id="fb518-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb518-111">-AsJob</span></span>
<span data-ttu-id="fb518-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fb518-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb518-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb518-113">-DefaultProfile</span></span>
<span data-ttu-id="fb518-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb518-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb518-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb518-115">-Force</span></span>
<span data-ttu-id="fb518-116">Azt jelzi, hogy ez a parancsmag eltávolítja a terheléselosztást függetlenül attól, hogy az erőforrásokat rendelte-e hozzá.</span><span class="sxs-lookup"><span data-stu-id="fb518-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="fb518-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb518-117">-Name</span></span>
<span data-ttu-id="fb518-118">Az eltávolítandó terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb518-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="fb518-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb518-119">-PassThru</span></span>
<span data-ttu-id="fb518-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fb518-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb518-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fb518-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb518-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb518-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb518-123">Annak a csoportnak a nevét adja meg, amely az eltávolítandó terheléselosztót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fb518-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="fb518-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb518-124">-Confirm</span></span>
<span data-ttu-id="fb518-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb518-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb518-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb518-126">-WhatIf</span></span>
<span data-ttu-id="fb518-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb518-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb518-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb518-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb518-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb518-129">CommonParameters</span></span>
<span data-ttu-id="fb518-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb518-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb518-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb518-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb518-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb518-132">INPUTS</span></span>

### <span data-ttu-id="fb518-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb518-133">None</span></span>
<span data-ttu-id="fb518-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fb518-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb518-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb518-135">OUTPUTS</span></span>

## <span data-ttu-id="fb518-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb518-136">NOTES</span></span>

## <span data-ttu-id="fb518-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb518-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb518-138">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb518-138">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fb518-139">Új – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb518-139">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="fb518-140">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb518-140">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


