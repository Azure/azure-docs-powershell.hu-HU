---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194746"
---
# <span data-ttu-id="1c262-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c262-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="1c262-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c262-102">SYNOPSIS</span></span>
<span data-ttu-id="1c262-103">A verziókövetés konfigurációjának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1c262-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="1c262-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c262-104">SYNTAX</span></span>

### <span data-ttu-id="1c262-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c262-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c262-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1c262-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c262-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c262-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c262-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c262-108">DESCRIPTION</span></span>
<span data-ttu-id="1c262-109">A verziókövetés konfigurációjának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1c262-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="1c262-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1c262-110">EXAMPLES</span></span>

### <span data-ttu-id="1c262-111">Példa 1: a kubernetes-fürt összes konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="1c262-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="1c262-112">Ez a parancs beilleszti a kubernetes-fürt összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1c262-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="1c262-113">2. példa: kubernetes-fürt konfigurációjának beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="1c262-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="1c262-114">Ez a parancs a kubernetes-cluster konfigurációját név szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="1c262-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="1c262-115">Példa 3: kubernetes-fürt konfigurációjának beszerzése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="1c262-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="1c262-116">Ez a parancs a kubernetes-fürtök objektum szerinti konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1c262-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="1c262-117">Példa 4: a kubernetes-fürt konfigurációjának beszerzése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="1c262-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="1c262-118">Ez a parancs a kubernetes-fürt konfigurációját pipeline szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="1c262-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="1c262-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c262-119">PARAMETERS</span></span>

### <span data-ttu-id="1c262-120">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1c262-120">-ClusterName</span></span>
<span data-ttu-id="1c262-121">A kubernetes-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="1c262-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="1c262-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="1c262-122">-ClusterRp</span></span>
<span data-ttu-id="1c262-123">Az Kubernetes-as cluster RP-Microsoft. ContainerService (ak-fürtök esetében) vagy Microsoft. Kubernetes (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="1c262-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="1c262-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="1c262-124">-ClusterType</span></span>
<span data-ttu-id="1c262-125">A Kubernetes-fürterőforrás neve – managedClusters (ak-fürtök esetében) vagy connectedClusters (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="1c262-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="1c262-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c262-126">-DefaultProfile</span></span>
<span data-ttu-id="1c262-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c262-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c262-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c262-128">-InputObject</span></span>
<span data-ttu-id="1c262-129">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c262-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c262-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1c262-130">-Name</span></span>
<span data-ttu-id="1c262-131">A verziókövetés konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="1c262-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="1c262-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c262-132">-ResourceGroupName</span></span>
<span data-ttu-id="1c262-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c262-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c262-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c262-134">-SubscriptionId</span></span>
<span data-ttu-id="1c262-135">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c262-135">The Azure subscription ID.</span></span>
<span data-ttu-id="1c262-136">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1c262-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="1c262-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c262-137">CommonParameters</span></span>
<span data-ttu-id="1c262-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c262-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c262-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c262-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c262-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c262-140">INPUTS</span></span>

### <span data-ttu-id="1c262-141">Microsoft. Azure. PowerShell. parancsmagok. KubernetesConfiguration. models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="1c262-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="1c262-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c262-142">OUTPUTS</span></span>

### <span data-ttu-id="1c262-143">Microsoft. Azure. PowerShell. parancsmagok. KubernetesConfiguration. modellek. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c262-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="1c262-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c262-144">NOTES</span></span>

<span data-ttu-id="1c262-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1c262-145">ALIASES</span></span>

<span data-ttu-id="1c262-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1c262-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c262-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1c262-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c262-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1c262-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c262-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1c262-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c262-150">`[ClusterName <String>]`: A kubernetes-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="1c262-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="1c262-151">`[ClusterResourceName <String>]`: A Kubernetes-fürterőforrás neve – managedClusters (ak-fürtök esetében) vagy connectedClusters (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="1c262-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="1c262-152">`[ClusterRp <String>]`: A Kubernetes-as cluster RP-Microsoft. ContainerService (ak-fürtök esetében) vagy Microsoft. Kubernetes (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="1c262-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="1c262-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1c262-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c262-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c262-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1c262-155">`[SourceControlConfigurationName <String>]`: A verziókövetés konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="1c262-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="1c262-156">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c262-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="1c262-157">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1c262-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="1c262-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c262-158">RELATED LINKS</span></span>
