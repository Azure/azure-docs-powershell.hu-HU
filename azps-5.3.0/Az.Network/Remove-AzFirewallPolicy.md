---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468934"
---
# <span data-ttu-id="73c4f-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="73c4f-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="73c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="73c4f-103">Azure tűzfal-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="73c4f-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="73c4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73c4f-104">SYNTAX</span></span>

### <span data-ttu-id="73c4f-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73c4f-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c4f-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73c4f-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c4f-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73c4f-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c4f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="73c4f-109">A **Remove-AzFirewallPolicy** parancsmag eltávolítja az Azure tűzfal házirendet.</span><span class="sxs-lookup"><span data-stu-id="73c4f-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="73c4f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73c4f-110">EXAMPLES</span></span>

### <span data-ttu-id="73c4f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="73c4f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="73c4f-112">Ez a példa eltávolítja a "firewallpolicy" nevű tűzfal házirendet a "TestRg" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="73c4f-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="73c4f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="73c4f-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="73c4f-114">Ez a példa eltávolítja a tűzfal házirendet az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="73c4f-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="73c4f-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="73c4f-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="73c4f-116">Ez a példa eltávolítja a tűzfal házirend-$fp</span><span class="sxs-lookup"><span data-stu-id="73c4f-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="73c4f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73c4f-117">PARAMETERS</span></span>

### <span data-ttu-id="73c4f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73c4f-118">-AsJob</span></span>
<span data-ttu-id="73c4f-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73c4f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73c4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c4f-120">-DefaultProfile</span></span>
<span data-ttu-id="73c4f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73c4f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c4f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="73c4f-122">-Force</span></span>
<span data-ttu-id="73c4f-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73c4f-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="73c4f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73c4f-124">-InputObject</span></span>
<span data-ttu-id="73c4f-125">Az AzureFirewall házirend</span><span class="sxs-lookup"><span data-stu-id="73c4f-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73c4f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="73c4f-126">-Name</span></span>
<span data-ttu-id="73c4f-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="73c4f-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c4f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73c4f-128">-PassThru</span></span>
<span data-ttu-id="73c4f-129">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="73c4f-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="73c4f-130">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="73c4f-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="73c4f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c4f-131">-ResourceGroupName</span></span>
<span data-ttu-id="73c4f-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73c4f-132">The resource group name.</span></span>

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

### <span data-ttu-id="73c4f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73c4f-133">-ResourceId</span></span>
<span data-ttu-id="73c4f-134">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="73c4f-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c4f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73c4f-135">-Confirm</span></span>
<span data-ttu-id="73c4f-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="73c4f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c4f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c4f-137">-WhatIf</span></span>
<span data-ttu-id="73c4f-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="73c4f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c4f-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73c4f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c4f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c4f-140">CommonParameters</span></span>
<span data-ttu-id="73c4f-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c4f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c4f-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73c4f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c4f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73c4f-143">INPUTS</span></span>

### <span data-ttu-id="73c4f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="73c4f-144">System.String</span></span>

### <span data-ttu-id="73c4f-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="73c4f-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="73c4f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73c4f-146">OUTPUTS</span></span>

### <span data-ttu-id="73c4f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73c4f-147">System.Boolean</span></span>

## <span data-ttu-id="73c4f-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73c4f-148">NOTES</span></span>

## <span data-ttu-id="73c4f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73c4f-149">RELATED LINKS</span></span>
