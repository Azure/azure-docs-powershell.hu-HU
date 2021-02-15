---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143666"
---
# <span data-ttu-id="907ca-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="907ca-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="907ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="907ca-102">SYNOPSIS</span></span>
<span data-ttu-id="907ca-103">Diagramlekérdezés törlése</span><span class="sxs-lookup"><span data-stu-id="907ca-103">Delete a graph query.</span></span>

## <span data-ttu-id="907ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="907ca-104">SYNTAX</span></span>

### <span data-ttu-id="907ca-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="907ca-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="907ca-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="907ca-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="907ca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="907ca-107">DESCRIPTION</span></span>
<span data-ttu-id="907ca-108">Diagramlekérdezés törlése</span><span class="sxs-lookup"><span data-stu-id="907ca-108">Delete a graph query.</span></span>

## <span data-ttu-id="907ca-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="907ca-109">EXAMPLES</span></span>

### <span data-ttu-id="907ca-110">1. példa: Erőforrás-grafikon lekérdezés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="907ca-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="907ca-111">Ez a parancs név szerint eltávolítja az erőforrás-grafikon lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="907ca-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="907ca-112">2. példa: Erőforrás-grafikon lekérdezés eltávolítása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="907ca-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="907ca-113">Ez a parancs objektum szerint eltávolítja az erőforrás-grafikon lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="907ca-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="907ca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="907ca-114">PARAMETERS</span></span>

### <span data-ttu-id="907ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907ca-115">-DefaultProfile</span></span>
<span data-ttu-id="907ca-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="907ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907ca-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="907ca-117">-InputObject</span></span>
<span data-ttu-id="907ca-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="907ca-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="907ca-119">-Name</span><span class="sxs-lookup"><span data-stu-id="907ca-119">-Name</span></span>
<span data-ttu-id="907ca-120">A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="907ca-120">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907ca-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="907ca-121">-PassThru</span></span>
<span data-ttu-id="907ca-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="907ca-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="907ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="907ca-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="907ca-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907ca-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="907ca-125">-SubscriptionId</span></span>
<span data-ttu-id="907ca-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="907ca-126">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907ca-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="907ca-127">-Confirm</span></span>
<span data-ttu-id="907ca-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="907ca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907ca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907ca-129">-WhatIf</span></span>
<span data-ttu-id="907ca-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="907ca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="907ca-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="907ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="907ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907ca-132">CommonParameters</span></span>
<span data-ttu-id="907ca-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907ca-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="907ca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907ca-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="907ca-135">INPUTS</span></span>

### <span data-ttu-id="907ca-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="907ca-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="907ca-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="907ca-137">OUTPUTS</span></span>

### <span data-ttu-id="907ca-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="907ca-138">System.Boolean</span></span>

## <span data-ttu-id="907ca-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="907ca-139">NOTES</span></span>

<span data-ttu-id="907ca-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="907ca-140">ALIASES</span></span>

<span data-ttu-id="907ca-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="907ca-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="907ca-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="907ca-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="907ca-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="907ca-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="907ca-144">INPUTOBJECT: <IResourceGraphIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="907ca-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="907ca-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="907ca-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="907ca-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="907ca-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="907ca-147">`[ResourceName <String>]`: A Graph-lekérdezés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="907ca-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="907ca-148">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="907ca-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="907ca-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="907ca-149">RELATED LINKS</span></span>

