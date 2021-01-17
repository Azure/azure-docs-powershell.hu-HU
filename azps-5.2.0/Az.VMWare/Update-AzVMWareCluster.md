---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326616"
---
# <span data-ttu-id="06f25-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="06f25-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="06f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f25-102">SYNOPSIS</span></span>
<span data-ttu-id="06f25-103">Fürt frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="06f25-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="06f25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06f25-104">SYNTAX</span></span>

### <span data-ttu-id="06f25-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06f25-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06f25-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="06f25-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06f25-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06f25-107">DESCRIPTION</span></span>
<span data-ttu-id="06f25-108">Fürt frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="06f25-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="06f25-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06f25-109">EXAMPLES</span></span>

### <span data-ttu-id="06f25-110">1. példa: A fürt méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="06f25-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="06f25-111">A fürt méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="06f25-111">Update cluster size by name</span></span>

### <span data-ttu-id="06f25-112">2. példa: A fürt méretének frissítése bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="06f25-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="06f25-113">A fürt méretének frissítése bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="06f25-113">Update cluster size by input object</span></span>

## <span data-ttu-id="06f25-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06f25-114">PARAMETERS</span></span>

### <span data-ttu-id="06f25-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06f25-115">-AsJob</span></span>
<span data-ttu-id="06f25-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="06f25-116">Run the command as a job</span></span>

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

### <span data-ttu-id="06f25-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="06f25-117">-ClusterSize</span></span>
<span data-ttu-id="06f25-118">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="06f25-118">The cluster size</span></span>

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

### <span data-ttu-id="06f25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f25-119">-DefaultProfile</span></span>
<span data-ttu-id="06f25-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06f25-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f25-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06f25-121">-InputObject</span></span>
<span data-ttu-id="06f25-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="06f25-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06f25-123">-Name</span><span class="sxs-lookup"><span data-stu-id="06f25-123">-Name</span></span>
<span data-ttu-id="06f25-124">A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="06f25-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="06f25-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06f25-125">-NoWait</span></span>
<span data-ttu-id="06f25-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="06f25-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06f25-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="06f25-127">-PrivateCloudName</span></span>
<span data-ttu-id="06f25-128">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="06f25-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="06f25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f25-129">-ResourceGroupName</span></span>
<span data-ttu-id="06f25-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06f25-130">The name of the resource group.</span></span>
<span data-ttu-id="06f25-131">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="06f25-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="06f25-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06f25-132">-SubscriptionId</span></span>
<span data-ttu-id="06f25-133">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="06f25-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="06f25-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06f25-134">-Confirm</span></span>
<span data-ttu-id="06f25-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06f25-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f25-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f25-136">-WhatIf</span></span>
<span data-ttu-id="06f25-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06f25-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f25-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06f25-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f25-139">CommonParameters</span></span>
<span data-ttu-id="06f25-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f25-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06f25-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f25-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06f25-142">INPUTS</span></span>

### <span data-ttu-id="06f25-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="06f25-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="06f25-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06f25-144">OUTPUTS</span></span>

### <span data-ttu-id="06f25-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="06f25-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="06f25-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06f25-146">NOTES</span></span>

<span data-ttu-id="06f25-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="06f25-147">ALIASES</span></span>

<span data-ttu-id="06f25-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="06f25-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06f25-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="06f25-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06f25-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06f25-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06f25-151">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="06f25-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06f25-152">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="06f25-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="06f25-153">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="06f25-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="06f25-154">`[HcxEnterpriseSiteName <String>]`: A HCX Nagyvállalati webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="06f25-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="06f25-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="06f25-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06f25-156">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="06f25-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="06f25-157">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="06f25-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="06f25-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06f25-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="06f25-159">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="06f25-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="06f25-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="06f25-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="06f25-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06f25-161">RELATED LINKS</span></span>

