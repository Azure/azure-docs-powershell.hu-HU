---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144243"
---
# <span data-ttu-id="eba24-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="eba24-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="eba24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eba24-102">SYNOPSIS</span></span>
<span data-ttu-id="eba24-103">Törli a megadott Azure dedikált HSM-et.</span><span class="sxs-lookup"><span data-stu-id="eba24-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="eba24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eba24-104">SYNTAX</span></span>

### <span data-ttu-id="eba24-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eba24-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eba24-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eba24-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eba24-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eba24-107">DESCRIPTION</span></span>
<span data-ttu-id="eba24-108">Törli a megadott Azure dedikált HSM-et.</span><span class="sxs-lookup"><span data-stu-id="eba24-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="eba24-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eba24-109">EXAMPLES</span></span>

### <span data-ttu-id="eba24-110">1. példa: Dedikált HSM eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="eba24-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="eba24-111">Ez a commnad név szerint eltávolítja a hardveres biztonsági modulokat.</span><span class="sxs-lookup"><span data-stu-id="eba24-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="eba24-112">2. példa: Dedikált HSM eltávolítása objektumról</span><span class="sxs-lookup"><span data-stu-id="eba24-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="eba24-113">Ez a commnad objektumról eltávolítja a dedikált HSM-et.</span><span class="sxs-lookup"><span data-stu-id="eba24-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="eba24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eba24-114">PARAMETERS</span></span>

### <span data-ttu-id="eba24-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba24-115">-AsJob</span></span>
<span data-ttu-id="eba24-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="eba24-116">Run the command as a job</span></span>

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

### <span data-ttu-id="eba24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba24-117">-DefaultProfile</span></span>
<span data-ttu-id="eba24-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eba24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eba24-119">-InputObject</span></span>
<span data-ttu-id="eba24-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="eba24-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eba24-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eba24-121">-Name</span></span>
<span data-ttu-id="eba24-122">A törlésre kijelölt HSM neve</span><span class="sxs-lookup"><span data-stu-id="eba24-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="eba24-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eba24-123">-NoWait</span></span>
<span data-ttu-id="eba24-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="eba24-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eba24-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eba24-125">-PassThru</span></span>
<span data-ttu-id="eba24-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="eba24-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eba24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba24-127">-ResourceGroupName</span></span>
<span data-ttu-id="eba24-128">Annak az erőforráscsoportnak a neve, amelyhez a dedikált HSM tartozik.</span><span class="sxs-lookup"><span data-stu-id="eba24-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="eba24-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eba24-129">-SubscriptionId</span></span>
<span data-ttu-id="eba24-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="eba24-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eba24-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="eba24-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eba24-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eba24-132">-Confirm</span></span>
<span data-ttu-id="eba24-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eba24-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba24-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba24-134">-WhatIf</span></span>
<span data-ttu-id="eba24-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eba24-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba24-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eba24-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba24-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba24-137">CommonParameters</span></span>
<span data-ttu-id="eba24-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba24-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba24-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eba24-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba24-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eba24-140">INPUTS</span></span>

### <span data-ttu-id="eba24-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="eba24-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="eba24-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eba24-142">OUTPUTS</span></span>

### <span data-ttu-id="eba24-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eba24-143">System.Boolean</span></span>

## <span data-ttu-id="eba24-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eba24-144">NOTES</span></span>

<span data-ttu-id="eba24-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eba24-145">ALIASES</span></span>

<span data-ttu-id="eba24-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="eba24-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eba24-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="eba24-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eba24-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eba24-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eba24-149">INPUTOBJECT: <IDedicatedHsmIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="eba24-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eba24-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="eba24-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eba24-151">`[Name <String>]`: A dedikált Hsm neve</span><span class="sxs-lookup"><span data-stu-id="eba24-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="eba24-152">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="eba24-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="eba24-153">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="eba24-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eba24-154">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="eba24-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eba24-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eba24-155">RELATED LINKS</span></span>

