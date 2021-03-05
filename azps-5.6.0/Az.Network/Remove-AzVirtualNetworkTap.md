---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: a0188236a5ce0b4da29a61b38d7c1889bc909968
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005958"
---
# <span data-ttu-id="1f505-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1f505-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="1f505-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f505-102">SYNOPSIS</span></span>
<span data-ttu-id="1f505-103">Virtuális hálózati koppintás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1f505-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="1f505-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f505-104">SYNTAX</span></span>

### <span data-ttu-id="1f505-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f505-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f505-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f505-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f505-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f505-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f505-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f505-108">DESCRIPTION</span></span>
<span data-ttu-id="1f505-109">A **Remove-AzVirtualNetworkTap** parancsmag eltávolítja az Azure virtuális hálózatra való rákoppintást.</span><span class="sxs-lookup"><span data-stu-id="1f505-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="1f505-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f505-110">EXAMPLES</span></span>

### <span data-ttu-id="1f505-111">1. példa: Virtuális hálózatra való koppintás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1f505-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="1f505-112">Ez a parancs eltávolítja a VirtualNetworkTap1-et az Erőforráscsoport1 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="1f505-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1f505-113">Mivel a *Force* paramétert nem használja, a rendszer kérni fogja a felhasználótól a művelet megerősítését.</span><span class="sxs-lookup"><span data-stu-id="1f505-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="1f505-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f505-114">PARAMETERS</span></span>

### <span data-ttu-id="1f505-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f505-115">-AsJob</span></span>
<span data-ttu-id="1f505-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1f505-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f505-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f505-117">-DefaultProfile</span></span>
<span data-ttu-id="1f505-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f505-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f505-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1f505-119">-Force</span></span>
<span data-ttu-id="1f505-120">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="1f505-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="1f505-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f505-121">-InputObject</span></span>
<span data-ttu-id="1f505-122">Hivatkozás a VirtualNetworkTap erőforrásra</span><span class="sxs-lookup"><span data-stu-id="1f505-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f505-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f505-123">-Name</span></span>
<span data-ttu-id="1f505-124">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="1f505-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f505-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f505-125">-PassThru</span></span>
<span data-ttu-id="1f505-126">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="1f505-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f505-127">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1f505-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f505-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f505-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f505-129">A virtuális hálózat erőforráscsoportneve koppintás.</span><span class="sxs-lookup"><span data-stu-id="1f505-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f505-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f505-130">-ResourceId</span></span>
<span data-ttu-id="1f505-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="1f505-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f505-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f505-132">-Confirm</span></span>
<span data-ttu-id="1f505-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1f505-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f505-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f505-134">-WhatIf</span></span>
<span data-ttu-id="1f505-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1f505-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f505-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f505-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f505-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f505-137">CommonParameters</span></span>
<span data-ttu-id="1f505-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f505-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f505-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f505-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f505-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f505-140">INPUTS</span></span>

### <span data-ttu-id="1f505-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1f505-141">System.String</span></span>

### <span data-ttu-id="1f505-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1f505-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="1f505-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f505-143">OUTPUTS</span></span>

### <span data-ttu-id="1f505-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f505-144">System.Boolean</span></span>

## <span data-ttu-id="1f505-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f505-145">NOTES</span></span>

## <span data-ttu-id="1f505-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f505-146">RELATED LINKS</span></span>

[<span data-ttu-id="1f505-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1f505-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="1f505-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1f505-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="1f505-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1f505-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
