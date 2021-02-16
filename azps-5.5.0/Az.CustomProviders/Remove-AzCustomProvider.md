---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148379"
---
# <span data-ttu-id="00806-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="00806-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="00806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00806-102">SYNOPSIS</span></span>
<span data-ttu-id="00806-103">Törli az egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="00806-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="00806-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00806-104">SYNTAX</span></span>

### <span data-ttu-id="00806-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00806-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00806-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="00806-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00806-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00806-107">DESCRIPTION</span></span>
<span data-ttu-id="00806-108">Törli az egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="00806-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="00806-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00806-109">EXAMPLES</span></span>

### <span data-ttu-id="00806-110">1. példa: Egyéni szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="00806-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="00806-111">Egyéni szolgáltató eltávolítása</span><span class="sxs-lookup"><span data-stu-id="00806-111">Remove a custom provider</span></span>

### <span data-ttu-id="00806-112">2. példa: Egyéni szolgáltató eltávolítása a PassThru szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="00806-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="00806-113">Távolítsa el az egyéni szolgáltatót a Sikeres vagy sikertelenség jelzésére a PassThru funkcióval.</span><span class="sxs-lookup"><span data-stu-id="00806-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="00806-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00806-114">PARAMETERS</span></span>

### <span data-ttu-id="00806-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00806-115">-AsJob</span></span>
<span data-ttu-id="00806-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="00806-116">Run the command as a job</span></span>

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

### <span data-ttu-id="00806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00806-117">-DefaultProfile</span></span>
<span data-ttu-id="00806-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00806-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00806-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00806-119">-InputObject</span></span>
<span data-ttu-id="00806-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="00806-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00806-121">-Name</span><span class="sxs-lookup"><span data-stu-id="00806-121">-Name</span></span>
<span data-ttu-id="00806-122">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="00806-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00806-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="00806-123">-NoWait</span></span>
<span data-ttu-id="00806-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="00806-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="00806-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00806-125">-PassThru</span></span>
<span data-ttu-id="00806-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="00806-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="00806-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00806-127">-ResourceGroupName</span></span>
<span data-ttu-id="00806-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00806-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="00806-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00806-129">-SubscriptionId</span></span>
<span data-ttu-id="00806-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00806-130">The Azure subscription ID.</span></span>
<span data-ttu-id="00806-131">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="00806-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="00806-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00806-132">-Confirm</span></span>
<span data-ttu-id="00806-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00806-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00806-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00806-134">-WhatIf</span></span>
<span data-ttu-id="00806-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00806-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00806-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00806-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00806-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00806-137">CommonParameters</span></span>
<span data-ttu-id="00806-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00806-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00806-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00806-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00806-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00806-140">INPUTS</span></span>

### <span data-ttu-id="00806-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="00806-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="00806-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00806-142">OUTPUTS</span></span>

### <span data-ttu-id="00806-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00806-143">System.Boolean</span></span>

## <span data-ttu-id="00806-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00806-144">NOTES</span></span>

<span data-ttu-id="00806-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="00806-145">ALIASES</span></span>

<span data-ttu-id="00806-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="00806-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00806-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="00806-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00806-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00806-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00806-149">INPUTOBJECT: <ICustomProvidersIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="00806-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00806-150">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="00806-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="00806-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="00806-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00806-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00806-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="00806-153">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="00806-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="00806-154">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="00806-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="00806-155">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00806-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="00806-156">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="00806-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="00806-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00806-157">RELATED LINKS</span></span>

