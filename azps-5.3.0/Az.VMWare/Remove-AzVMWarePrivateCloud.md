---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467055"
---
# <span data-ttu-id="f3b7f-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="f3b7f-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="f3b7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b7f-103">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="f3b7f-103">Delete a private cloud</span></span>

## <span data-ttu-id="f3b7f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3b7f-104">SYNTAX</span></span>

### <span data-ttu-id="f3b7f-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3b7f-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3b7f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3b7f-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3b7f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="f3b7f-108">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="f3b7f-108">Delete a private cloud</span></span>

## <span data-ttu-id="f3b7f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3b7f-109">EXAMPLES</span></span>

### <span data-ttu-id="f3b7f-110">1. példa: Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="f3b7f-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="f3b7f-111">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="f3b7f-111">Delete private cloud</span></span>

## <span data-ttu-id="f3b7f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3b7f-112">PARAMETERS</span></span>

### <span data-ttu-id="f3b7f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3b7f-113">-AsJob</span></span>
<span data-ttu-id="f3b7f-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f3b7f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f3b7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b7f-115">-DefaultProfile</span></span>
<span data-ttu-id="f3b7f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3b7f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3b7f-117">-InputObject</span></span>
<span data-ttu-id="f3b7f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3b7f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3b7f-119">-Name</span></span>
<span data-ttu-id="f3b7f-120">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="f3b7f-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="f3b7f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3b7f-121">-NoWait</span></span>
<span data-ttu-id="f3b7f-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f3b7f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3b7f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b7f-123">-PassThru</span></span>
<span data-ttu-id="f3b7f-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="f3b7f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3b7f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b7f-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3b7f-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-126">The name of the resource group.</span></span>
<span data-ttu-id="f3b7f-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f3b7f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f3b7f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3b7f-128">-SubscriptionId</span></span>
<span data-ttu-id="f3b7f-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f3b7f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3b7f-130">-Confirm</span></span>
<span data-ttu-id="f3b7f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b7f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b7f-132">-WhatIf</span></span>
<span data-ttu-id="f3b7f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3b7f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b7f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b7f-135">CommonParameters</span></span>
<span data-ttu-id="f3b7f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b7f-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3b7f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b7f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3b7f-138">INPUTS</span></span>

### <span data-ttu-id="f3b7f-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f3b7f-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f3b7f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3b7f-140">OUTPUTS</span></span>

### <span data-ttu-id="f3b7f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b7f-141">System.Boolean</span></span>

## <span data-ttu-id="f3b7f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3b7f-142">NOTES</span></span>

<span data-ttu-id="f3b7f-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f3b7f-143">ALIASES</span></span>

<span data-ttu-id="f3b7f-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f3b7f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3b7f-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3b7f-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3b7f-147">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f3b7f-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3b7f-148">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="f3b7f-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f3b7f-149">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="f3b7f-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f3b7f-150">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="f3b7f-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f3b7f-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f3b7f-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3b7f-152">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="f3b7f-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f3b7f-153">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="f3b7f-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f3b7f-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f3b7f-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f3b7f-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="f3b7f-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3b7f-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f3b7f-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3b7f-157">RELATED LINKS</span></span>

