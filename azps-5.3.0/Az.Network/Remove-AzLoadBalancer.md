---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468929"
---
# <span data-ttu-id="7c70c-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c70c-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="7c70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c70c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c70c-103">Eltávolítja a terheléselosztást.</span><span class="sxs-lookup"><span data-stu-id="7c70c-103">Removes a load balancer.</span></span>

## <span data-ttu-id="7c70c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c70c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c70c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c70c-105">DESCRIPTION</span></span>
<span data-ttu-id="7c70c-106">A **Remove-AzLoadBalancer** parancsmag eltávolítja az Azure terheléselosztási eszközét.</span><span class="sxs-lookup"><span data-stu-id="7c70c-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="7c70c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c70c-107">EXAMPLES</span></span>

### <span data-ttu-id="7c70c-108">1. példa: Terheléselosztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7c70c-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7c70c-109">Ez a parancs törli a MyLoadBalancer nevű terheléselosztást a MyResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7c70c-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7c70c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c70c-110">PARAMETERS</span></span>

### <span data-ttu-id="7c70c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c70c-111">-AsJob</span></span>
<span data-ttu-id="7c70c-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7c70c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c70c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c70c-113">-DefaultProfile</span></span>
<span data-ttu-id="7c70c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c70c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c70c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7c70c-115">-Force</span></span>
<span data-ttu-id="7c70c-116">Azt jelzi, hogy ez a parancsmag eltávolítja a terheléselosztást, függetlenül attól, hogy erőforrások vannak-e hozzá rendelve.</span><span class="sxs-lookup"><span data-stu-id="7c70c-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="7c70c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7c70c-117">-Name</span></span>
<span data-ttu-id="7c70c-118">Az eltávolítható terheléselosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c70c-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="7c70c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c70c-119">-PassThru</span></span>
<span data-ttu-id="7c70c-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="7c70c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c70c-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7c70c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c70c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c70c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c70c-123">Annak az erőforráscsoportnak a neve, amely az eltávolítható terheléselosztást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7c70c-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="7c70c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c70c-124">-Confirm</span></span>
<span data-ttu-id="7c70c-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c70c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c70c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c70c-126">-WhatIf</span></span>
<span data-ttu-id="7c70c-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c70c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c70c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c70c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c70c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c70c-129">CommonParameters</span></span>
<span data-ttu-id="7c70c-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c70c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c70c-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c70c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c70c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c70c-132">INPUTS</span></span>

### <span data-ttu-id="7c70c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7c70c-133">System.String</span></span>

## <span data-ttu-id="7c70c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c70c-134">OUTPUTS</span></span>

### <span data-ttu-id="7c70c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c70c-135">System.Boolean</span></span>

## <span data-ttu-id="7c70c-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c70c-136">NOTES</span></span>

## <span data-ttu-id="7c70c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c70c-137">RELATED LINKS</span></span>

[<span data-ttu-id="7c70c-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c70c-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7c70c-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c70c-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="7c70c-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c70c-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


