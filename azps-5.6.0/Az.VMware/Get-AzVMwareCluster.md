---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936417"
---
# <span data-ttu-id="4bfc6-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="4bfc6-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="4bfc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bfc6-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfc6-103">Fürt létrehozása név szerint egy privát felhőben</span><span class="sxs-lookup"><span data-stu-id="4bfc6-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="4bfc6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4bfc6-104">SYNTAX</span></span>

### <span data-ttu-id="4bfc6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bfc6-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4bfc6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="4bfc6-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4bfc6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4bfc6-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4bfc6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4bfc6-108">DESCRIPTION</span></span>
<span data-ttu-id="4bfc6-109">Fürt létrehozása név szerint egy privát felhőben</span><span class="sxs-lookup"><span data-stu-id="4bfc6-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="4bfc6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4bfc6-110">EXAMPLES</span></span>

### <span data-ttu-id="4bfc6-111">1. példa: Fürt lekérte</span><span class="sxs-lookup"><span data-stu-id="4bfc6-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="4bfc6-112">Fürt lekérte</span><span class="sxs-lookup"><span data-stu-id="4bfc6-112">Get cluster</span></span>

### <span data-ttu-id="4bfc6-113">2. példa: Listacsoportok</span><span class="sxs-lookup"><span data-stu-id="4bfc6-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="4bfc6-114">Lista fürtök</span><span class="sxs-lookup"><span data-stu-id="4bfc6-114">List clusters</span></span>

## <span data-ttu-id="4bfc6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bfc6-115">PARAMETERS</span></span>

### <span data-ttu-id="4bfc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bfc6-116">-DefaultProfile</span></span>
<span data-ttu-id="4bfc6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bfc6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bfc6-118">-InputObject</span></span>
<span data-ttu-id="4bfc6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4bfc6-120">-Name</span></span>
<span data-ttu-id="4bfc6-121">A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="4bfc6-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc6-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="4bfc6-122">-PrivateCloudName</span></span>
<span data-ttu-id="4bfc6-123">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="4bfc6-123">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bfc6-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bfc6-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-125">The name of the resource group.</span></span>
<span data-ttu-id="4bfc6-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4bfc6-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bfc6-127">-SubscriptionId</span></span>
<span data-ttu-id="4bfc6-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfc6-129">CommonParameters</span></span>
<span data-ttu-id="4bfc6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfc6-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bfc6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfc6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bfc6-132">INPUTS</span></span>

### <span data-ttu-id="4bfc6-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="4bfc6-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="4bfc6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bfc6-134">OUTPUTS</span></span>

### <span data-ttu-id="4bfc6-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="4bfc6-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="4bfc6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4bfc6-136">NOTES</span></span>

<span data-ttu-id="4bfc6-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4bfc6-137">ALIASES</span></span>

<span data-ttu-id="4bfc6-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4bfc6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bfc6-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bfc6-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bfc6-141">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4bfc6-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bfc6-142">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="4bfc6-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="4bfc6-143">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="4bfc6-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="4bfc6-144">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="4bfc6-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="4bfc6-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4bfc6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bfc6-146">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="4bfc6-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="4bfc6-147">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="4bfc6-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="4bfc6-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4bfc6-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4bfc6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="4bfc6-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4bfc6-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4bfc6-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bfc6-151">RELATED LINKS</span></span>

