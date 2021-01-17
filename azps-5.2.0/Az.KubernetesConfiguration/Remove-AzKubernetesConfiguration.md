---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361646"
---
# <span data-ttu-id="9cc06-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cc06-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="9cc06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc06-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc06-103">Ezzel törli a forrásvezérlő konfigurációjának beállítását lehetővé telő YAML-fájlt, így leállítja a jövőbeli szinkronizálást a forrásfájlból.</span><span class="sxs-lookup"><span data-stu-id="9cc06-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="9cc06-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cc06-104">SYNTAX</span></span>

### <span data-ttu-id="9cc06-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cc06-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9cc06-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cc06-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cc06-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cc06-107">DESCRIPTION</span></span>
<span data-ttu-id="9cc06-108">Ezzel törli a forrásvezérlő konfigurációjának beállítását lehetővé telő YAML-fájlt, így leállítja a jövőbeli szinkronizálást a forrásfájlból.</span><span class="sxs-lookup"><span data-stu-id="9cc06-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="9cc06-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cc06-109">EXAMPLES</span></span>

### <span data-ttu-id="9cc06-110">1. példa: A kubanetes fürt nevének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9cc06-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="9cc06-111">Ez a parancs név szerint eltávolítja a kubernetes fürt konkguációját.</span><span class="sxs-lookup"><span data-stu-id="9cc06-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="9cc06-112">2. példa: A kubernetes fürtök konkguációinak eltávolítása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="9cc06-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="9cc06-113">Ez a parancs objektum szerint eltávolítja a parancssori hálózatok fürtjéhez használt konklguációt.</span><span class="sxs-lookup"><span data-stu-id="9cc06-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="9cc06-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cc06-114">PARAMETERS</span></span>

### <span data-ttu-id="9cc06-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cc06-115">-AsJob</span></span>
<span data-ttu-id="9cc06-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="9cc06-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9cc06-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9cc06-117">-ClusterName</span></span>
<span data-ttu-id="9cc06-118">A kubernetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="9cc06-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="9cc06-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="9cc06-119">-ClusterType</span></span>
<span data-ttu-id="9cc06-120">A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="9cc06-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="9cc06-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc06-121">-DefaultProfile</span></span>
<span data-ttu-id="9cc06-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cc06-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cc06-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cc06-123">-InputObject</span></span>
<span data-ttu-id="9cc06-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9cc06-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc06-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9cc06-125">-Name</span></span>
<span data-ttu-id="9cc06-126">A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="9cc06-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc06-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9cc06-127">-NoWait</span></span>
<span data-ttu-id="9cc06-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="9cc06-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cc06-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cc06-129">-PassThru</span></span>
<span data-ttu-id="9cc06-130">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="9cc06-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9cc06-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc06-131">-ResourceGroupName</span></span>
<span data-ttu-id="9cc06-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9cc06-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cc06-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cc06-133">-SubscriptionId</span></span>
<span data-ttu-id="9cc06-134">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9cc06-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="9cc06-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cc06-135">-Confirm</span></span>
<span data-ttu-id="9cc06-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9cc06-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc06-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc06-137">-WhatIf</span></span>
<span data-ttu-id="9cc06-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9cc06-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc06-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cc06-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc06-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc06-140">CommonParameters</span></span>
<span data-ttu-id="9cc06-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc06-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc06-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cc06-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc06-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cc06-143">INPUTS</span></span>

### <span data-ttu-id="9cc06-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="9cc06-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="9cc06-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc06-145">OUTPUTS</span></span>

### <span data-ttu-id="9cc06-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9cc06-146">System.Boolean</span></span>

## <span data-ttu-id="9cc06-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cc06-147">NOTES</span></span>

<span data-ttu-id="9cc06-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9cc06-148">ALIASES</span></span>

<span data-ttu-id="9cc06-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9cc06-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cc06-150">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9cc06-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cc06-151">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9cc06-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cc06-152">INPUTOBJECT: <IKubernetesConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9cc06-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cc06-153">`[ClusterName <String>]`: Anetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="9cc06-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="9cc06-154">`[ClusterResourceName <String>]`: A Kubernetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="9cc06-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="9cc06-155">`[ClusterRp <String>]`: A Kubanetes fürt RP - vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="9cc06-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="9cc06-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9cc06-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cc06-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9cc06-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9cc06-158">`[SourceControlConfigurationName <String>]`: A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="9cc06-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="9cc06-159">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9cc06-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="9cc06-160">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="9cc06-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="9cc06-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cc06-161">RELATED LINKS</span></span>

