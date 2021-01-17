---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467057"
---
# <span data-ttu-id="55b39-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="55b39-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="55b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b39-102">SYNOPSIS</span></span>
<span data-ttu-id="55b39-103">ExpressRoute-kapcsolat kapcsolati engedély törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="55b39-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="55b39-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55b39-104">SYNTAX</span></span>

### <span data-ttu-id="55b39-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55b39-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55b39-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55b39-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55b39-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55b39-107">DESCRIPTION</span></span>
<span data-ttu-id="55b39-108">ExpressRoute-kapcsolat kapcsolati engedély törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="55b39-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="55b39-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55b39-109">EXAMPLES</span></span>

### <span data-ttu-id="55b39-110">1. példa: A privát felhő engedélyének törlése</span><span class="sxs-lookup"><span data-stu-id="55b39-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="55b39-111">A privát felhő engedélyének törlése</span><span class="sxs-lookup"><span data-stu-id="55b39-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="55b39-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55b39-112">PARAMETERS</span></span>

### <span data-ttu-id="55b39-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b39-113">-AsJob</span></span>
<span data-ttu-id="55b39-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="55b39-114">Run the command as a job</span></span>

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

### <span data-ttu-id="55b39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b39-115">-DefaultProfile</span></span>
<span data-ttu-id="55b39-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55b39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b39-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55b39-117">-InputObject</span></span>
<span data-ttu-id="55b39-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="55b39-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55b39-119">-Name</span><span class="sxs-lookup"><span data-stu-id="55b39-119">-Name</span></span>
<span data-ttu-id="55b39-120">Az ExpressRoute-kapcsolat kapcsolati engedélyének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="55b39-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55b39-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55b39-121">-NoWait</span></span>
<span data-ttu-id="55b39-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="55b39-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55b39-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55b39-123">-PassThru</span></span>
<span data-ttu-id="55b39-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="55b39-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="55b39-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="55b39-125">-PrivateCloudName</span></span>
<span data-ttu-id="55b39-126">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="55b39-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="55b39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b39-127">-ResourceGroupName</span></span>
<span data-ttu-id="55b39-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55b39-128">The name of the resource group.</span></span>
<span data-ttu-id="55b39-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="55b39-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="55b39-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55b39-130">-SubscriptionId</span></span>
<span data-ttu-id="55b39-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55b39-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="55b39-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55b39-132">-Confirm</span></span>
<span data-ttu-id="55b39-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55b39-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b39-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b39-134">-WhatIf</span></span>
<span data-ttu-id="55b39-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55b39-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b39-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55b39-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b39-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b39-137">CommonParameters</span></span>
<span data-ttu-id="55b39-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b39-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b39-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55b39-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b39-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55b39-140">INPUTS</span></span>

### <span data-ttu-id="55b39-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="55b39-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="55b39-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55b39-142">OUTPUTS</span></span>

### <span data-ttu-id="55b39-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55b39-143">System.Boolean</span></span>

## <span data-ttu-id="55b39-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55b39-144">NOTES</span></span>

<span data-ttu-id="55b39-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="55b39-145">ALIASES</span></span>

<span data-ttu-id="55b39-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="55b39-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55b39-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="55b39-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55b39-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55b39-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55b39-149">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="55b39-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55b39-150">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="55b39-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="55b39-151">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="55b39-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="55b39-152">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="55b39-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="55b39-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="55b39-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55b39-154">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="55b39-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="55b39-155">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="55b39-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="55b39-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55b39-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="55b39-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="55b39-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="55b39-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55b39-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="55b39-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55b39-159">RELATED LINKS</span></span>

