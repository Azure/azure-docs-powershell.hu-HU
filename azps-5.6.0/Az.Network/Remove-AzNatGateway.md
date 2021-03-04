---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 430ea183d618779045aaf5d13554edac2ce98626
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941593"
---
# <span data-ttu-id="8439d-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8439d-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="8439d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8439d-102">SYNOPSIS</span></span>
<span data-ttu-id="8439d-103">Nat Gateway resource eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8439d-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="8439d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8439d-104">SYNTAX</span></span>

### <span data-ttu-id="8439d-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8439d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8439d-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8439d-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8439d-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8439d-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8439d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8439d-108">DESCRIPTION</span></span>
<span data-ttu-id="8439d-109">Nat Gateway Resource eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8439d-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="8439d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8439d-110">EXAMPLES</span></span>

### <span data-ttu-id="8439d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8439d-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="8439d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8439d-112">PARAMETERS</span></span>

### <span data-ttu-id="8439d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8439d-113">-AsJob</span></span>
<span data-ttu-id="8439d-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8439d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8439d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8439d-115">-DefaultProfile</span></span>
<span data-ttu-id="8439d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8439d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8439d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8439d-117">-Force</span></span>
<span data-ttu-id="8439d-118">Ha erőforrást szeretne törölni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8439d-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="8439d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8439d-119">-InputObject</span></span>
<span data-ttu-id="8439d-120">A Nat Gateway erőforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="8439d-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8439d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8439d-121">-Name</span></span>
<span data-ttu-id="8439d-122">A Nat Átjáró erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8439d-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8439d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8439d-123">-PassThru</span></span>
<span data-ttu-id="8439d-124">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8439d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8439d-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8439d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8439d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8439d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8439d-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8439d-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8439d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8439d-128">-ResourceId</span></span>
<span data-ttu-id="8439d-129">A Nat átjáróhoz társított erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8439d-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8439d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8439d-130">-Confirm</span></span>
<span data-ttu-id="8439d-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8439d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8439d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8439d-132">-WhatIf</span></span>
<span data-ttu-id="8439d-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8439d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8439d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8439d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8439d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8439d-135">CommonParameters</span></span>
<span data-ttu-id="8439d-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8439d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8439d-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8439d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8439d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8439d-138">INPUTS</span></span>

### <span data-ttu-id="8439d-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="8439d-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="8439d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8439d-140">System.String</span></span>

## <span data-ttu-id="8439d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8439d-141">OUTPUTS</span></span>

### <span data-ttu-id="8439d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8439d-142">System.Boolean</span></span>

## <span data-ttu-id="8439d-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8439d-143">NOTES</span></span>

## <span data-ttu-id="8439d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8439d-144">RELATED LINKS</span></span>
