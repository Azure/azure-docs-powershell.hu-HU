---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8d1918599832f5740515dc6334192bf9b4cc54ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926178"
---
# <span data-ttu-id="39ad6-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="39ad6-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="39ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="39ad6-103">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="39ad6-103">Delete a private cloud</span></span>

## <span data-ttu-id="39ad6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39ad6-104">SYNTAX</span></span>

### <span data-ttu-id="39ad6-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39ad6-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39ad6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39ad6-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39ad6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39ad6-107">DESCRIPTION</span></span>
<span data-ttu-id="39ad6-108">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="39ad6-108">Delete a private cloud</span></span>

## <span data-ttu-id="39ad6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39ad6-109">EXAMPLES</span></span>

### <span data-ttu-id="39ad6-110">1. példa: Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="39ad6-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="39ad6-111">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="39ad6-111">Delete private cloud</span></span>

## <span data-ttu-id="39ad6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="39ad6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39ad6-113">-AsJob</span></span>
<span data-ttu-id="39ad6-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="39ad6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="39ad6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ad6-115">-DefaultProfile</span></span>
<span data-ttu-id="39ad6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39ad6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39ad6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39ad6-117">-InputObject</span></span>
<span data-ttu-id="39ad6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="39ad6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39ad6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="39ad6-119">-Name</span></span>
<span data-ttu-id="39ad6-120">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="39ad6-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="39ad6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39ad6-121">-NoWait</span></span>
<span data-ttu-id="39ad6-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="39ad6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39ad6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39ad6-123">-PassThru</span></span>
<span data-ttu-id="39ad6-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="39ad6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39ad6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ad6-125">-ResourceGroupName</span></span>
<span data-ttu-id="39ad6-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39ad6-126">The name of the resource group.</span></span>
<span data-ttu-id="39ad6-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="39ad6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="39ad6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39ad6-128">-SubscriptionId</span></span>
<span data-ttu-id="39ad6-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="39ad6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="39ad6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39ad6-130">-Confirm</span></span>
<span data-ttu-id="39ad6-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="39ad6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ad6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ad6-132">-WhatIf</span></span>
<span data-ttu-id="39ad6-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="39ad6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ad6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39ad6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ad6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ad6-135">CommonParameters</span></span>
<span data-ttu-id="39ad6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39ad6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ad6-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39ad6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ad6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39ad6-138">INPUTS</span></span>

### <span data-ttu-id="39ad6-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="39ad6-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="39ad6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ad6-140">OUTPUTS</span></span>

### <span data-ttu-id="39ad6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39ad6-141">System.Boolean</span></span>

## <span data-ttu-id="39ad6-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39ad6-142">NOTES</span></span>

<span data-ttu-id="39ad6-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="39ad6-143">ALIASES</span></span>

<span data-ttu-id="39ad6-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="39ad6-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39ad6-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="39ad6-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39ad6-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39ad6-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39ad6-147">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="39ad6-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39ad6-148">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="39ad6-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="39ad6-149">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="39ad6-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="39ad6-150">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="39ad6-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="39ad6-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="39ad6-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39ad6-152">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="39ad6-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="39ad6-153">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="39ad6-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="39ad6-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39ad6-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="39ad6-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="39ad6-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="39ad6-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="39ad6-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="39ad6-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39ad6-157">RELATED LINKS</span></span>

