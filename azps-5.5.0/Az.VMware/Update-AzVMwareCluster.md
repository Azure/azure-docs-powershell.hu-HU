---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149762"
---
# <span data-ttu-id="d4153-101">Update-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="d4153-101">Update-AzVMwareCluster</span></span>

## <span data-ttu-id="d4153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4153-102">SYNOPSIS</span></span>
<span data-ttu-id="d4153-103">Fürt frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d4153-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="d4153-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4153-104">SYNTAX</span></span>

### <span data-ttu-id="d4153-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4153-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4153-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d4153-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4153-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4153-107">DESCRIPTION</span></span>
<span data-ttu-id="d4153-108">Fürt frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d4153-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="d4153-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4153-109">EXAMPLES</span></span>

### <span data-ttu-id="d4153-110">1. példa: A fürt méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d4153-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="d4153-111">A fürt méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d4153-111">Update cluster size by name</span></span>

### <span data-ttu-id="d4153-112">2. példa: A fürt méretének frissítése bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="d4153-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="d4153-113">A fürt méretének frissítése bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="d4153-113">Update cluster size by input object</span></span>

## <span data-ttu-id="d4153-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4153-114">PARAMETERS</span></span>

### <span data-ttu-id="d4153-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4153-115">-AsJob</span></span>
<span data-ttu-id="d4153-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d4153-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d4153-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="d4153-117">-ClusterSize</span></span>
<span data-ttu-id="d4153-118">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="d4153-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4153-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4153-119">-DefaultProfile</span></span>
<span data-ttu-id="d4153-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4153-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4153-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4153-121">-InputObject</span></span>
<span data-ttu-id="d4153-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d4153-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4153-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d4153-123">-Name</span></span>
<span data-ttu-id="d4153-124">A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="d4153-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4153-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d4153-125">-NoWait</span></span>
<span data-ttu-id="d4153-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d4153-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d4153-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d4153-127">-PrivateCloudName</span></span>
<span data-ttu-id="d4153-128">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d4153-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="d4153-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4153-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4153-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4153-130">The name of the resource group.</span></span>
<span data-ttu-id="d4153-131">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d4153-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d4153-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4153-132">-SubscriptionId</span></span>
<span data-ttu-id="d4153-133">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4153-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d4153-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4153-134">-Confirm</span></span>
<span data-ttu-id="d4153-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4153-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4153-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4153-136">-WhatIf</span></span>
<span data-ttu-id="d4153-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4153-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4153-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4153-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4153-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4153-139">CommonParameters</span></span>
<span data-ttu-id="d4153-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4153-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4153-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4153-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4153-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4153-142">INPUTS</span></span>

### <span data-ttu-id="d4153-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="d4153-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="d4153-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4153-144">OUTPUTS</span></span>

### <span data-ttu-id="d4153-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="d4153-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="d4153-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4153-146">NOTES</span></span>

<span data-ttu-id="d4153-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d4153-147">ALIASES</span></span>

<span data-ttu-id="d4153-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d4153-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4153-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d4153-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4153-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4153-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4153-151">INPUTOBJECT: <IVMwareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d4153-151">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4153-152">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d4153-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d4153-153">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="d4153-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d4153-154">`[HcxEnterpriseSiteName <String>]`: A HCX Nagyvállalati webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d4153-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d4153-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d4153-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4153-156">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="d4153-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d4153-157">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d4153-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d4153-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4153-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d4153-159">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d4153-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="d4153-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4153-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d4153-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4153-161">RELATED LINKS</span></span>

