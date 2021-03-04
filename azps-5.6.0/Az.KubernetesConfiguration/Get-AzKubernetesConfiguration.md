---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 8cbf938917f26b1229b5c18d25448da4df3bb5b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931033"
---
# <span data-ttu-id="58381-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="58381-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="58381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58381-102">SYNOPSIS</span></span>
<span data-ttu-id="58381-103">A forrásvezérlő konfigurációjának részletei.</span><span class="sxs-lookup"><span data-stu-id="58381-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="58381-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58381-104">SYNTAX</span></span>

### <span data-ttu-id="58381-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58381-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58381-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="58381-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58381-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="58381-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="58381-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58381-108">DESCRIPTION</span></span>
<span data-ttu-id="58381-109">A forrásvezérlő konfigurációjának részletei.</span><span class="sxs-lookup"><span data-stu-id="58381-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="58381-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58381-110">EXAMPLES</span></span>

### <span data-ttu-id="58381-111">1. példa: A rendszer az összes konfigurációt beveszi a rendszer által használt rendszercsoportba.</span><span class="sxs-lookup"><span data-stu-id="58381-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="58381-112">Ez a parancs a parancssori fürt összes konfigurációját beveszi.</span><span class="sxs-lookup"><span data-stu-id="58381-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="58381-113">2. példa: A rendszer név szerint konfigurálja a rendszer a többhálózati fürtöt</span><span class="sxs-lookup"><span data-stu-id="58381-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="58381-114">Ez a parancs név szerint konfigurálja a kubernetes fürtöt.</span><span class="sxs-lookup"><span data-stu-id="58381-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="58381-115">3. példa: A rendszer objektum szerint csoportosítva konfigurálja a rendszer a többhálózati hálózatokat.</span><span class="sxs-lookup"><span data-stu-id="58381-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="58381-116">Ez a parancs objektum szerint csoportosítva kapja meg a kubernetes fürt konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="58381-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="58381-117">4. példa: A rendszer a többhálózati fürt konfigurációját prognózis szerint konfigurálja</span><span class="sxs-lookup"><span data-stu-id="58381-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="58381-118">Ez a parancs a parancssori fürt konfigurációját kapja meg folyamat szerint.</span><span class="sxs-lookup"><span data-stu-id="58381-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="58381-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58381-119">PARAMETERS</span></span>

### <span data-ttu-id="58381-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="58381-120">-ClusterName</span></span>
<span data-ttu-id="58381-121">A kubernetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="58381-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="58381-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="58381-122">-ClusterRp</span></span>
<span data-ttu-id="58381-123">A Kubernetes-fürt RP- vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="58381-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="58381-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="58381-124">-ClusterType</span></span>
<span data-ttu-id="58381-125">A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="58381-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="58381-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58381-126">-DefaultProfile</span></span>
<span data-ttu-id="58381-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58381-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58381-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58381-128">-InputObject</span></span>
<span data-ttu-id="58381-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="58381-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58381-130">-Name</span><span class="sxs-lookup"><span data-stu-id="58381-130">-Name</span></span>
<span data-ttu-id="58381-131">A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="58381-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58381-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58381-132">-ResourceGroupName</span></span>
<span data-ttu-id="58381-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58381-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="58381-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58381-134">-SubscriptionId</span></span>
<span data-ttu-id="58381-135">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="58381-135">The Azure subscription ID.</span></span>
<span data-ttu-id="58381-136">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="58381-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="58381-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58381-137">CommonParameters</span></span>
<span data-ttu-id="58381-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58381-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58381-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58381-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58381-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58381-140">INPUTS</span></span>

### <span data-ttu-id="58381-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="58381-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="58381-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58381-142">OUTPUTS</span></span>

### <span data-ttu-id="58381-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.iSourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="58381-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="58381-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58381-144">NOTES</span></span>

<span data-ttu-id="58381-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="58381-145">ALIASES</span></span>

<span data-ttu-id="58381-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="58381-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58381-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="58381-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58381-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="58381-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58381-149">INPUTOBJECT: <IKubernetesConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="58381-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58381-150">`[ClusterName <String>]`: Anetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="58381-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="58381-151">`[ClusterResourceName <String>]`: A Kubernetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="58381-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="58381-152">`[ClusterRp <String>]`: A Kubanetes fürt RP - vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="58381-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="58381-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="58381-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58381-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58381-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="58381-155">`[SourceControlConfigurationName <String>]`: A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="58381-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="58381-156">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="58381-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="58381-157">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="58381-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="58381-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58381-158">RELATED LINKS</span></span>

