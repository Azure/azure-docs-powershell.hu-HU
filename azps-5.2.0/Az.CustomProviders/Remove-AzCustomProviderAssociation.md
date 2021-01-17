---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330749"
---
# <span data-ttu-id="0fa77-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="0fa77-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="0fa77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa77-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa77-103">Társítás törlése</span><span class="sxs-lookup"><span data-stu-id="0fa77-103">Delete an association.</span></span>

## <span data-ttu-id="0fa77-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fa77-104">SYNTAX</span></span>

### <span data-ttu-id="0fa77-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fa77-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0fa77-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fa77-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fa77-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fa77-107">DESCRIPTION</span></span>
<span data-ttu-id="0fa77-108">Társítás törlése</span><span class="sxs-lookup"><span data-stu-id="0fa77-108">Delete an association.</span></span>

## <span data-ttu-id="0fa77-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fa77-109">EXAMPLES</span></span>

### <span data-ttu-id="0fa77-110">1. példa: Egyéni szolgáltató társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0fa77-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="0fa77-111">Egyéni szolgáltató-társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0fa77-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="0fa77-112">2. példa: Egyéni szolgáltatói társítás eltávolítása a Piping szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="0fa77-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="0fa77-113">Távolítsa el az egyéni szolgáltató-társításokat a sikeresség vagy a sikertelenség jelzésére pipázás és a PassThru funkció használatával.</span><span class="sxs-lookup"><span data-stu-id="0fa77-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="0fa77-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fa77-114">PARAMETERS</span></span>

### <span data-ttu-id="0fa77-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fa77-115">-AsJob</span></span>
<span data-ttu-id="0fa77-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="0fa77-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0fa77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa77-117">-DefaultProfile</span></span>
<span data-ttu-id="0fa77-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fa77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa77-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa77-119">-InputObject</span></span>
<span data-ttu-id="0fa77-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0fa77-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0fa77-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0fa77-121">-Name</span></span>
<span data-ttu-id="0fa77-122">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="0fa77-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fa77-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0fa77-123">-NoWait</span></span>
<span data-ttu-id="0fa77-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="0fa77-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0fa77-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fa77-125">-PassThru</span></span>
<span data-ttu-id="0fa77-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="0fa77-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0fa77-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="0fa77-127">-Scope</span></span>
<span data-ttu-id="0fa77-128">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="0fa77-128">The scope of the association.</span></span>

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

### <span data-ttu-id="0fa77-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fa77-129">-Confirm</span></span>
<span data-ttu-id="0fa77-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0fa77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa77-131">-WhatIf</span></span>
<span data-ttu-id="0fa77-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0fa77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa77-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fa77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa77-134">CommonParameters</span></span>
<span data-ttu-id="0fa77-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa77-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fa77-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa77-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fa77-137">INPUTS</span></span>

### <span data-ttu-id="0fa77-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="0fa77-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="0fa77-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fa77-139">OUTPUTS</span></span>

### <span data-ttu-id="0fa77-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fa77-140">System.Boolean</span></span>

## <span data-ttu-id="0fa77-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fa77-141">NOTES</span></span>

<span data-ttu-id="0fa77-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0fa77-142">ALIASES</span></span>

<span data-ttu-id="0fa77-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0fa77-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fa77-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0fa77-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fa77-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fa77-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fa77-146">INPUTOBJECT: <ICustomProvidersIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0fa77-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fa77-147">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="0fa77-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="0fa77-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0fa77-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fa77-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fa77-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0fa77-150">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="0fa77-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="0fa77-151">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="0fa77-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="0fa77-152">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0fa77-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="0fa77-153">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="0fa77-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="0fa77-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fa77-154">RELATED LINKS</span></span>

