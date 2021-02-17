---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 76ad6df6dbbd9b019e4c89fdbca55107264f0406
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207510"
---
# <span data-ttu-id="14dbe-101">Remove-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="14dbe-101">Remove-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="14dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="14dbe-103">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="14dbe-103">Delete a private cloud</span></span>

## <span data-ttu-id="14dbe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14dbe-104">SYNTAX</span></span>

### <span data-ttu-id="14dbe-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14dbe-105">Delete (Default)</span></span>
```
Remove-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14dbe-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14dbe-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14dbe-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14dbe-107">DESCRIPTION</span></span>
<span data-ttu-id="14dbe-108">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="14dbe-108">Delete a private cloud</span></span>

## <span data-ttu-id="14dbe-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14dbe-109">EXAMPLES</span></span>

### <span data-ttu-id="14dbe-110">1. példa: Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="14dbe-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="14dbe-111">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="14dbe-111">Delete private cloud</span></span>

## <span data-ttu-id="14dbe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14dbe-112">PARAMETERS</span></span>

### <span data-ttu-id="14dbe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14dbe-113">-AsJob</span></span>
<span data-ttu-id="14dbe-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="14dbe-114">Run the command as a job</span></span>

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

### <span data-ttu-id="14dbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14dbe-115">-DefaultProfile</span></span>
<span data-ttu-id="14dbe-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14dbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14dbe-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14dbe-117">-InputObject</span></span>
<span data-ttu-id="14dbe-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="14dbe-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14dbe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="14dbe-119">-Name</span></span>
<span data-ttu-id="14dbe-120">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="14dbe-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14dbe-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="14dbe-121">-NoWait</span></span>
<span data-ttu-id="14dbe-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="14dbe-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14dbe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14dbe-123">-PassThru</span></span>
<span data-ttu-id="14dbe-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="14dbe-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="14dbe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14dbe-125">-ResourceGroupName</span></span>
<span data-ttu-id="14dbe-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14dbe-126">The name of the resource group.</span></span>
<span data-ttu-id="14dbe-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="14dbe-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="14dbe-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14dbe-128">-SubscriptionId</span></span>
<span data-ttu-id="14dbe-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14dbe-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="14dbe-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14dbe-130">-Confirm</span></span>
<span data-ttu-id="14dbe-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="14dbe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14dbe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14dbe-132">-WhatIf</span></span>
<span data-ttu-id="14dbe-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="14dbe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14dbe-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14dbe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14dbe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14dbe-135">CommonParameters</span></span>
<span data-ttu-id="14dbe-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14dbe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14dbe-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14dbe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14dbe-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14dbe-138">INPUTS</span></span>

### <span data-ttu-id="14dbe-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="14dbe-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="14dbe-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14dbe-140">OUTPUTS</span></span>

### <span data-ttu-id="14dbe-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14dbe-141">System.Boolean</span></span>

## <span data-ttu-id="14dbe-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14dbe-142">NOTES</span></span>

<span data-ttu-id="14dbe-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="14dbe-143">ALIASES</span></span>

<span data-ttu-id="14dbe-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="14dbe-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14dbe-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="14dbe-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14dbe-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14dbe-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14dbe-147">INPUTOBJECT: <IVMwareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="14dbe-147">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14dbe-148">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="14dbe-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="14dbe-149">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="14dbe-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="14dbe-150">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="14dbe-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="14dbe-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="14dbe-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14dbe-152">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="14dbe-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="14dbe-153">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="14dbe-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="14dbe-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14dbe-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="14dbe-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="14dbe-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="14dbe-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14dbe-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="14dbe-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14dbe-157">RELATED LINKS</span></span>

