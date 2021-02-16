---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
ms.openlocfilehash: 39a6f251cd0cfb190ea8541f5b04c35d710de2c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164482"
---
# <span data-ttu-id="957ce-101">Remove-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="957ce-101">Remove-AzVMwareAuthorization</span></span>

## <span data-ttu-id="957ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957ce-102">SYNOPSIS</span></span>
<span data-ttu-id="957ce-103">ExpressRoute-kapcsolat kapcsolati engedély törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="957ce-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="957ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="957ce-104">SYNTAX</span></span>

### <span data-ttu-id="957ce-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="957ce-105">Delete (Default)</span></span>
```
Remove-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="957ce-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="957ce-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="957ce-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="957ce-107">DESCRIPTION</span></span>
<span data-ttu-id="957ce-108">ExpressRoute-kapcsolat kapcsolati engedély törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="957ce-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="957ce-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="957ce-109">EXAMPLES</span></span>

### <span data-ttu-id="957ce-110">1. példa: A privát felhő engedélyének törlése</span><span class="sxs-lookup"><span data-stu-id="957ce-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="957ce-111">A privát felhő engedélyének törlése</span><span class="sxs-lookup"><span data-stu-id="957ce-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="957ce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="957ce-112">PARAMETERS</span></span>

### <span data-ttu-id="957ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="957ce-113">-AsJob</span></span>
<span data-ttu-id="957ce-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="957ce-114">Run the command as a job</span></span>

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

### <span data-ttu-id="957ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957ce-115">-DefaultProfile</span></span>
<span data-ttu-id="957ce-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="957ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="957ce-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="957ce-117">-InputObject</span></span>
<span data-ttu-id="957ce-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="957ce-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="957ce-119">-Name</span><span class="sxs-lookup"><span data-stu-id="957ce-119">-Name</span></span>
<span data-ttu-id="957ce-120">Az ExpressRoute-kapcsolat kapcsolati engedélyének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="957ce-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="957ce-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="957ce-121">-NoWait</span></span>
<span data-ttu-id="957ce-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="957ce-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="957ce-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="957ce-123">-PassThru</span></span>
<span data-ttu-id="957ce-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="957ce-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="957ce-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="957ce-125">-PrivateCloudName</span></span>
<span data-ttu-id="957ce-126">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="957ce-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="957ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957ce-127">-ResourceGroupName</span></span>
<span data-ttu-id="957ce-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="957ce-128">The name of the resource group.</span></span>
<span data-ttu-id="957ce-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="957ce-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="957ce-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="957ce-130">-SubscriptionId</span></span>
<span data-ttu-id="957ce-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="957ce-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="957ce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="957ce-132">-Confirm</span></span>
<span data-ttu-id="957ce-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="957ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="957ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957ce-134">-WhatIf</span></span>
<span data-ttu-id="957ce-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="957ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="957ce-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="957ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="957ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957ce-137">CommonParameters</span></span>
<span data-ttu-id="957ce-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="957ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957ce-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="957ce-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957ce-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="957ce-140">INPUTS</span></span>

### <span data-ttu-id="957ce-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="957ce-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="957ce-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="957ce-142">OUTPUTS</span></span>

### <span data-ttu-id="957ce-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="957ce-143">System.Boolean</span></span>

## <span data-ttu-id="957ce-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="957ce-144">NOTES</span></span>

<span data-ttu-id="957ce-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="957ce-145">ALIASES</span></span>

<span data-ttu-id="957ce-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="957ce-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="957ce-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="957ce-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="957ce-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="957ce-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="957ce-149">INPUTOBJECT: <IVMwareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="957ce-149">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="957ce-150">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="957ce-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="957ce-151">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="957ce-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="957ce-152">`[HcxEnterpriseSiteName <String>]`: A HCX Nagyvállalati webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="957ce-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="957ce-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="957ce-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="957ce-154">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="957ce-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="957ce-155">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="957ce-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="957ce-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="957ce-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="957ce-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="957ce-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="957ce-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="957ce-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="957ce-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="957ce-159">RELATED LINKS</span></span>

