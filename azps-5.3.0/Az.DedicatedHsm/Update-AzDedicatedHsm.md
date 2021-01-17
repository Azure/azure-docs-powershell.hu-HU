---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479257"
---
# <span data-ttu-id="6ceaf-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="6ceaf-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="6ceaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ceaf-102">SYNOPSIS</span></span>
<span data-ttu-id="6ceaf-103">Frissítsen egy dedikált HSM-et a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="6ceaf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ceaf-104">SYNTAX</span></span>

### <span data-ttu-id="6ceaf-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ceaf-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ceaf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6ceaf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ceaf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ceaf-107">DESCRIPTION</span></span>
<span data-ttu-id="6ceaf-108">Frissítsen egy dedikált HSM-et a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="6ceaf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ceaf-109">EXAMPLES</span></span>

### <span data-ttu-id="6ceaf-110">1. példa: A dedikált HSM paramétercímkének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="6ceaf-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="6ceaf-111">Ez a parancs név szerint frissíti a dedikált HSM paramétercímkét</span><span class="sxs-lookup"><span data-stu-id="6ceaf-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="6ceaf-112">2. példa: A dedikált HSM paramétercímke frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="6ceaf-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="6ceaf-113">Ez a parancs frissíti a dedikált HSM paramétercímkét objektum szerint</span><span class="sxs-lookup"><span data-stu-id="6ceaf-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="6ceaf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ceaf-114">PARAMETERS</span></span>

### <span data-ttu-id="6ceaf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ceaf-115">-AsJob</span></span>
<span data-ttu-id="6ceaf-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="6ceaf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6ceaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ceaf-117">-DefaultProfile</span></span>
<span data-ttu-id="6ceaf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ceaf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ceaf-119">-InputObject</span></span>
<span data-ttu-id="6ceaf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ceaf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6ceaf-121">-Name</span></span>
<span data-ttu-id="6ceaf-122">A dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="6ceaf-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceaf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6ceaf-123">-NoWait</span></span>
<span data-ttu-id="6ceaf-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="6ceaf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ceaf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ceaf-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ceaf-126">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceaf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ceaf-127">-SubscriptionId</span></span>
<span data-ttu-id="6ceaf-128">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ceaf-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceaf-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ceaf-130">-Tag</span></span>
<span data-ttu-id="6ceaf-131">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="6ceaf-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceaf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ceaf-132">-Confirm</span></span>
<span data-ttu-id="6ceaf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ceaf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ceaf-134">-WhatIf</span></span>
<span data-ttu-id="6ceaf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ceaf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ceaf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ceaf-137">CommonParameters</span></span>
<span data-ttu-id="6ceaf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ceaf-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ceaf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ceaf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ceaf-140">INPUTS</span></span>

### <span data-ttu-id="6ceaf-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="6ceaf-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="6ceaf-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ceaf-142">OUTPUTS</span></span>

### <span data-ttu-id="6ceaf-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="6ceaf-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="6ceaf-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ceaf-144">NOTES</span></span>

<span data-ttu-id="6ceaf-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6ceaf-145">ALIASES</span></span>

<span data-ttu-id="6ceaf-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6ceaf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ceaf-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ceaf-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ceaf-149">INPUTOBJECT: <IDedicatedHsmIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6ceaf-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ceaf-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6ceaf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ceaf-151">`[Name <String>]`: A dedikált Hsm neve</span><span class="sxs-lookup"><span data-stu-id="6ceaf-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="6ceaf-152">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="6ceaf-153">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6ceaf-154">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6ceaf-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6ceaf-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ceaf-155">RELATED LINKS</span></span>

