---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153579"
---
# <span data-ttu-id="8fa0f-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8fa0f-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="8fa0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa0f-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa0f-103">Eltávolít egy erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-103">Removes a resource group.</span></span>

## <span data-ttu-id="8fa0f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fa0f-104">SYNTAX</span></span>

### <span data-ttu-id="8fa0f-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fa0f-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fa0f-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8fa0f-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fa0f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fa0f-107">DESCRIPTION</span></span>
<span data-ttu-id="8fa0f-108">A **Remove-AzResourceGroup** parancsmag eltávolít egy Azure-erőforráscsoportot és annak erőforrásait az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="8fa0f-109">Ha törölni szeretne egy erőforrást, de ki szeretne hagyni az erőforráscsoportból, használja a Remove-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="8fa0f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fa0f-110">EXAMPLES</span></span>

### <span data-ttu-id="8fa0f-111">1. példa: Erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fa0f-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="8fa0f-112">Ez a parancs eltávolítja a ContosoRG01 erőforráscsoportot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="8fa0f-113">A parancsmag megerősítést kér, és nem ad vissza kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="8fa0f-114">2. példa: Erőforráscsoport eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="8fa0f-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="8fa0f-115">Ez a parancs a Get-AzResourceGroup parancsmag segítségével begyűjte a ContosoRG01 erőforráscsoportot, majd átadja a **Remove-AzResourceGroup** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="8fa0f-116">Az *Kényszerítés* paraméter elrejti a megerősítési kérést.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="8fa0f-117">3. példa: Az összes erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fa0f-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="8fa0f-118">Ez a parancs a **Get-AzResourceGroup** parancsmag segítségével begyűjte az összes erőforráscsoportot, majd a pipeline operátorral átadja őket a **Remove-AzResourceGroup** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="8fa0f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fa0f-119">PARAMETERS</span></span>

### <span data-ttu-id="8fa0f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8fa0f-120">-ApiVersion</span></span>
<span data-ttu-id="8fa0f-121">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8fa0f-122">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa0f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fa0f-123">-AsJob</span></span>
<span data-ttu-id="8fa0f-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8fa0f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fa0f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa0f-125">-DefaultProfile</span></span>
<span data-ttu-id="8fa0f-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8fa0f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fa0f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8fa0f-127">-Force</span></span>
<span data-ttu-id="8fa0f-128">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fa0f-129">-Id</span><span class="sxs-lookup"><span data-stu-id="8fa0f-129">-Id</span></span>
<span data-ttu-id="8fa0f-130">Az eltávolítható erőforráscsoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="8fa0f-131">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa0f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8fa0f-132">-Name</span></span>
<span data-ttu-id="8fa0f-133">Az eltávolítható erőforráscsoportok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="8fa0f-134">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa0f-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8fa0f-135">-Pre</span></span>
<span data-ttu-id="8fa0f-136">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8fa0f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fa0f-137">-Confirm</span></span>
<span data-ttu-id="8fa0f-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa0f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa0f-139">-WhatIf</span></span>
<span data-ttu-id="8fa0f-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fa0f-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fa0f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa0f-142">CommonParameters</span></span>
<span data-ttu-id="8fa0f-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa0f-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fa0f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa0f-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fa0f-145">INPUTS</span></span>

### <span data-ttu-id="8fa0f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8fa0f-146">System.String</span></span>

## <span data-ttu-id="8fa0f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fa0f-147">OUTPUTS</span></span>

### <span data-ttu-id="8fa0f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8fa0f-148">System.Boolean</span></span>

## <span data-ttu-id="8fa0f-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fa0f-149">NOTES</span></span>

## <span data-ttu-id="8fa0f-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fa0f-150">RELATED LINKS</span></span>

[<span data-ttu-id="8fa0f-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8fa0f-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="8fa0f-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8fa0f-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="8fa0f-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8fa0f-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


