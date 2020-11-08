---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014039"
---
# <span data-ttu-id="2879b-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2879b-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="2879b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2879b-102">SYNOPSIS</span></span>
<span data-ttu-id="2879b-103">A terheléselosztó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2879b-103">Removes a load balancer.</span></span>

## <span data-ttu-id="2879b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2879b-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2879b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2879b-105">DESCRIPTION</span></span>
<span data-ttu-id="2879b-106">A **Remove-AzLoadBalancer** parancsmag eltávolítja az Azure terheléselosztó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2879b-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="2879b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2879b-107">EXAMPLES</span></span>

### <span data-ttu-id="2879b-108">1. példa: terheléselosztó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2879b-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2879b-109">Ez a parancs törli a MyLoadBalancer nevű terheléselosztó nevű MyResourceGroup a nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="2879b-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2879b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2879b-110">PARAMETERS</span></span>

### <span data-ttu-id="2879b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2879b-111">-AsJob</span></span>
<span data-ttu-id="2879b-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2879b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2879b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2879b-113">-DefaultProfile</span></span>
<span data-ttu-id="2879b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2879b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2879b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2879b-115">-Force</span></span>
<span data-ttu-id="2879b-116">Azt jelzi, hogy ez a parancsmag eltávolítja a terheléselosztást függetlenül attól, hogy az erőforrásokat rendelte-e hozzá.</span><span class="sxs-lookup"><span data-stu-id="2879b-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="2879b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2879b-117">-Name</span></span>
<span data-ttu-id="2879b-118">Az eltávolítandó terheléselosztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2879b-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="2879b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2879b-119">-PassThru</span></span>
<span data-ttu-id="2879b-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2879b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2879b-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2879b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2879b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2879b-122">-ResourceGroupName</span></span>
<span data-ttu-id="2879b-123">Annak a csoportnak a nevét adja meg, amely az eltávolítandó terheléselosztót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2879b-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="2879b-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2879b-124">-Confirm</span></span>
<span data-ttu-id="2879b-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2879b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2879b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2879b-126">-WhatIf</span></span>
<span data-ttu-id="2879b-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2879b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2879b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2879b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2879b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2879b-129">CommonParameters</span></span>
<span data-ttu-id="2879b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2879b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2879b-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2879b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2879b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2879b-132">INPUTS</span></span>

### <span data-ttu-id="2879b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2879b-133">System.String</span></span>

## <span data-ttu-id="2879b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2879b-134">OUTPUTS</span></span>

### <span data-ttu-id="2879b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2879b-135">System.Boolean</span></span>

## <span data-ttu-id="2879b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2879b-136">NOTES</span></span>

## <span data-ttu-id="2879b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2879b-137">RELATED LINKS</span></span>

[<span data-ttu-id="2879b-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2879b-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2879b-139">Új – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2879b-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="2879b-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2879b-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


