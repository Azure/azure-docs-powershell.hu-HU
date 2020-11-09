---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301664"
---
# <span data-ttu-id="d88ef-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="d88ef-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="d88ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d88ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d88ef-103">Fürt frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d88ef-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="d88ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d88ef-104">SYNTAX</span></span>

### <span data-ttu-id="d88ef-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d88ef-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d88ef-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d88ef-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d88ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d88ef-107">DESCRIPTION</span></span>
<span data-ttu-id="d88ef-108">Fürt frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d88ef-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="d88ef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d88ef-109">EXAMPLES</span></span>

### <span data-ttu-id="d88ef-110">Példa 1: a szektorcsoport méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d88ef-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="d88ef-111">A szektorcsoport méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d88ef-111">Update cluster size by name</span></span>

### <span data-ttu-id="d88ef-112">2. példa: a szektorcsoport méretének frissítése beviteli objektum szerint</span><span class="sxs-lookup"><span data-stu-id="d88ef-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="d88ef-113">A szektorcsoport méretének frissítése beviteli objektum szerint</span><span class="sxs-lookup"><span data-stu-id="d88ef-113">Update cluster size by input object</span></span>

## <span data-ttu-id="d88ef-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d88ef-114">PARAMETERS</span></span>

### <span data-ttu-id="d88ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d88ef-115">-AsJob</span></span>
<span data-ttu-id="d88ef-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d88ef-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d88ef-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="d88ef-117">-ClusterSize</span></span>
<span data-ttu-id="d88ef-118">A szektorcsoport mérete</span><span class="sxs-lookup"><span data-stu-id="d88ef-118">The cluster size</span></span>

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

### <span data-ttu-id="d88ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88ef-119">-DefaultProfile</span></span>
<span data-ttu-id="d88ef-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d88ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d88ef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d88ef-121">-InputObject</span></span>
<span data-ttu-id="d88ef-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d88ef-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d88ef-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d88ef-123">-Name</span></span>
<span data-ttu-id="d88ef-124">A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d88ef-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="d88ef-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="d88ef-125">-NoWait</span></span>
<span data-ttu-id="d88ef-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d88ef-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d88ef-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d88ef-127">-PrivateCloudName</span></span>
<span data-ttu-id="d88ef-128">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d88ef-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="d88ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="d88ef-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d88ef-130">The name of the resource group.</span></span>
<span data-ttu-id="d88ef-131">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d88ef-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d88ef-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d88ef-132">-SubscriptionId</span></span>
<span data-ttu-id="d88ef-133">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d88ef-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d88ef-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d88ef-134">-Confirm</span></span>
<span data-ttu-id="d88ef-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d88ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d88ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88ef-136">-WhatIf</span></span>
<span data-ttu-id="d88ef-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d88ef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88ef-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d88ef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d88ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88ef-139">CommonParameters</span></span>
<span data-ttu-id="d88ef-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d88ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88ef-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d88ef-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88ef-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d88ef-142">INPUTS</span></span>

### <span data-ttu-id="d88ef-143">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="d88ef-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="d88ef-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d88ef-144">OUTPUTS</span></span>

### <span data-ttu-id="d88ef-145">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="d88ef-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="d88ef-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d88ef-146">NOTES</span></span>

<span data-ttu-id="d88ef-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d88ef-147">ALIASES</span></span>

<span data-ttu-id="d88ef-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d88ef-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d88ef-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d88ef-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d88ef-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d88ef-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d88ef-151">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d88ef-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d88ef-152">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d88ef-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d88ef-153">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d88ef-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d88ef-154">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d88ef-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d88ef-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d88ef-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d88ef-156">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="d88ef-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d88ef-157">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d88ef-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d88ef-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d88ef-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d88ef-159">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d88ef-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="d88ef-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d88ef-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d88ef-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d88ef-161">RELATED LINKS</span></span>

