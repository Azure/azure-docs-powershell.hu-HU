---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: daa058d1f3cc13e073d8533403341dad3db7c319
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152579"
---
# <span data-ttu-id="97863-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="97863-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="97863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97863-102">SYNOPSIS</span></span>
<span data-ttu-id="97863-103">A forrásvezérlő konfigurációjának részletei.</span><span class="sxs-lookup"><span data-stu-id="97863-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="97863-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97863-104">SYNTAX</span></span>

### <span data-ttu-id="97863-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97863-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97863-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="97863-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97863-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97863-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="97863-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97863-108">DESCRIPTION</span></span>
<span data-ttu-id="97863-109">A forrásvezérlő konfigurációjának részletei.</span><span class="sxs-lookup"><span data-stu-id="97863-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="97863-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97863-110">EXAMPLES</span></span>

### <span data-ttu-id="97863-111">1. példa: A rendszer a rendszerhálózati fürt összes konfigurációját beveszi</span><span class="sxs-lookup"><span data-stu-id="97863-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="97863-112">Ez a parancs lekérte a rendszer az összes beállítását.</span><span class="sxs-lookup"><span data-stu-id="97863-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="97863-113">2. példa: A kumernetes fürt konfigurációjának beállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="97863-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="97863-114">Ez a parancs név szerint konfigurálja a kubernetes fürtöt.</span><span class="sxs-lookup"><span data-stu-id="97863-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="97863-115">3. példa: A rendszer objektum szerint csoportosítva konfigurálja a rendszer a többhálózati hálózatokat.</span><span class="sxs-lookup"><span data-stu-id="97863-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="97863-116">Ez a parancs objektum szerint csoportosítva kapja meg a kubernetes fürt konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="97863-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="97863-117">4. példa: A rendszer a többhálózati fürt konfigurációját prognózis szerint konfigurálja</span><span class="sxs-lookup"><span data-stu-id="97863-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="97863-118">Ez a parancs a parancssori fürt konfigurációját kapja meg folyamat szerint.</span><span class="sxs-lookup"><span data-stu-id="97863-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="97863-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97863-119">PARAMETERS</span></span>

### <span data-ttu-id="97863-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="97863-120">-ClusterName</span></span>
<span data-ttu-id="97863-121">A kubernetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="97863-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="97863-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="97863-122">-ClusterRp</span></span>
<span data-ttu-id="97863-123">A Kubanetes-fürt RP- vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="97863-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="97863-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="97863-124">-ClusterType</span></span>
<span data-ttu-id="97863-125">A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="97863-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="97863-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97863-126">-DefaultProfile</span></span>
<span data-ttu-id="97863-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97863-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97863-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97863-128">-InputObject</span></span>
<span data-ttu-id="97863-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="97863-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97863-130">-Name</span><span class="sxs-lookup"><span data-stu-id="97863-130">-Name</span></span>
<span data-ttu-id="97863-131">A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="97863-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="97863-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97863-132">-ResourceGroupName</span></span>
<span data-ttu-id="97863-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="97863-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="97863-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97863-134">-SubscriptionId</span></span>
<span data-ttu-id="97863-135">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97863-135">The Azure subscription ID.</span></span>
<span data-ttu-id="97863-136">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-00000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="97863-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="97863-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97863-137">CommonParameters</span></span>
<span data-ttu-id="97863-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97863-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97863-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97863-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97863-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97863-140">INPUTS</span></span>

### <span data-ttu-id="97863-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="97863-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="97863-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97863-142">OUTPUTS</span></span>

### <span data-ttu-id="97863-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.iSourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="97863-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="97863-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97863-144">NOTES</span></span>

<span data-ttu-id="97863-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="97863-145">ALIASES</span></span>

<span data-ttu-id="97863-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="97863-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97863-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="97863-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97863-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97863-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97863-149">INPUTOBJECT: <IKubernetesConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="97863-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97863-150">`[ClusterName <String>]`: Anetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="97863-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="97863-151">`[ClusterResourceName <String>]`: A Kubernetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="97863-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="97863-152">`[ClusterRp <String>]`: A Kubanetes fürt RP - vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="97863-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="97863-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="97863-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97863-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="97863-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="97863-155">`[SourceControlConfigurationName <String>]`: A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="97863-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="97863-156">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97863-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="97863-157">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-00000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="97863-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="97863-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97863-158">RELATED LINKS</span></span>

