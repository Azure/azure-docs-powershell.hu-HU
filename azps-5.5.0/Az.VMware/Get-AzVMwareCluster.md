---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 51a889abe0d1842f66a0ed9b17f3b07acd85a54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208902"
---
# <span data-ttu-id="3b204-101">Get-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="3b204-101">Get-AzVMwareCluster</span></span>

## <span data-ttu-id="3b204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b204-102">SYNOPSIS</span></span>
<span data-ttu-id="3b204-103">Fürt létrehozása név szerint egy privát felhőben</span><span class="sxs-lookup"><span data-stu-id="3b204-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="3b204-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b204-104">SYNTAX</span></span>

### <span data-ttu-id="3b204-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b204-105">List (Default)</span></span>
```
Get-AzVMwareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b204-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="3b204-106">Get</span></span>
```
Get-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b204-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3b204-107">GetViaIdentity</span></span>
```
Get-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3b204-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b204-108">DESCRIPTION</span></span>
<span data-ttu-id="3b204-109">Fürt létrehozása név szerint egy privát felhőben</span><span class="sxs-lookup"><span data-stu-id="3b204-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="3b204-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b204-110">EXAMPLES</span></span>

### <span data-ttu-id="3b204-111">1. példa: Fürt lekérte</span><span class="sxs-lookup"><span data-stu-id="3b204-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="3b204-112">Fürt lekérte</span><span class="sxs-lookup"><span data-stu-id="3b204-112">Get cluster</span></span>

### <span data-ttu-id="3b204-113">2. példa: Listacsoportok</span><span class="sxs-lookup"><span data-stu-id="3b204-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="3b204-114">Lista fürtök</span><span class="sxs-lookup"><span data-stu-id="3b204-114">List clusters</span></span>

## <span data-ttu-id="3b204-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b204-115">PARAMETERS</span></span>

### <span data-ttu-id="3b204-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b204-116">-DefaultProfile</span></span>
<span data-ttu-id="3b204-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b204-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b204-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b204-118">-InputObject</span></span>
<span data-ttu-id="3b204-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3b204-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b204-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3b204-120">-Name</span></span>
<span data-ttu-id="3b204-121">A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="3b204-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="3b204-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="3b204-122">-PrivateCloudName</span></span>
<span data-ttu-id="3b204-123">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="3b204-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="3b204-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b204-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b204-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b204-125">The name of the resource group.</span></span>
<span data-ttu-id="3b204-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="3b204-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3b204-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b204-127">-SubscriptionId</span></span>
<span data-ttu-id="3b204-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3b204-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3b204-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b204-129">CommonParameters</span></span>
<span data-ttu-id="3b204-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b204-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b204-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b204-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b204-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b204-132">INPUTS</span></span>

### <span data-ttu-id="3b204-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="3b204-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="3b204-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b204-134">OUTPUTS</span></span>

### <span data-ttu-id="3b204-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="3b204-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="3b204-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b204-136">NOTES</span></span>

<span data-ttu-id="3b204-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3b204-137">ALIASES</span></span>

<span data-ttu-id="3b204-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3b204-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b204-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="3b204-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b204-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b204-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b204-141">INPUTOBJECT: <IVMwareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3b204-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b204-142">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="3b204-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="3b204-143">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="3b204-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="3b204-144">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="3b204-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="3b204-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3b204-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b204-146">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="3b204-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="3b204-147">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="3b204-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="3b204-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b204-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3b204-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="3b204-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3b204-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3b204-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="3b204-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b204-151">RELATED LINKS</span></span>

