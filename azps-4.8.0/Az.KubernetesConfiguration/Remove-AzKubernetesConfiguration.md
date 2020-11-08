---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181865"
---
# <span data-ttu-id="2252c-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="2252c-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="2252c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2252c-102">SYNOPSIS</span></span>
<span data-ttu-id="2252c-103">Ezzel törli a verziókövetés konfigurációjának beállításához használt YAML-fájlt, így a jövőbeli szinkronizálás megmarad a repóból.</span><span class="sxs-lookup"><span data-stu-id="2252c-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="2252c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2252c-104">SYNTAX</span></span>

### <span data-ttu-id="2252c-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2252c-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2252c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2252c-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2252c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2252c-107">DESCRIPTION</span></span>
<span data-ttu-id="2252c-108">Ezzel törli a verziókövetés konfigurációjának beállításához használt YAML-fájlt, így a jövőbeli szinkronizálás megmarad a repóból.</span><span class="sxs-lookup"><span data-stu-id="2252c-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="2252c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2252c-109">EXAMPLES</span></span>

### <span data-ttu-id="2252c-110">Példa 1: kubernetes-configuation eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="2252c-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="2252c-111">Ez a parancs eltávolítja a configuation kubernetes-fürtöt név szerint.</span><span class="sxs-lookup"><span data-stu-id="2252c-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="2252c-112">2. példa: kubernetes-configuation eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="2252c-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="2252c-113">Ez a parancs eltávolítja az objektum configuation kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2252c-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="2252c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2252c-114">PARAMETERS</span></span>

### <span data-ttu-id="2252c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2252c-115">-AsJob</span></span>
<span data-ttu-id="2252c-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="2252c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2252c-117">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="2252c-117">-ClusterName</span></span>
<span data-ttu-id="2252c-118">A kubernetes-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2252c-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="2252c-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2252c-119">-ClusterType</span></span>
<span data-ttu-id="2252c-120">A Kubernetes-fürterőforrás neve – managedClusters (ak-fürtök esetében) vagy connectedClusters (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="2252c-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="2252c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2252c-121">-DefaultProfile</span></span>
<span data-ttu-id="2252c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2252c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2252c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2252c-123">-InputObject</span></span>
<span data-ttu-id="2252c-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2252c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2252c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2252c-125">-Name</span></span>
<span data-ttu-id="2252c-126">A verziókövetés konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="2252c-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="2252c-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="2252c-127">-NoWait</span></span>
<span data-ttu-id="2252c-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="2252c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2252c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2252c-129">-PassThru</span></span>
<span data-ttu-id="2252c-130">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="2252c-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2252c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2252c-131">-ResourceGroupName</span></span>
<span data-ttu-id="2252c-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2252c-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="2252c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2252c-133">-SubscriptionId</span></span>
<span data-ttu-id="2252c-134">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2252c-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="2252c-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2252c-135">-Confirm</span></span>
<span data-ttu-id="2252c-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2252c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2252c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2252c-137">-WhatIf</span></span>
<span data-ttu-id="2252c-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2252c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2252c-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2252c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2252c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2252c-140">CommonParameters</span></span>
<span data-ttu-id="2252c-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2252c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2252c-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2252c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2252c-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2252c-143">INPUTS</span></span>

### <span data-ttu-id="2252c-144">Microsoft. Azure. PowerShell. parancsmagok. KubernetesConfiguration. models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="2252c-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="2252c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2252c-145">OUTPUTS</span></span>

### <span data-ttu-id="2252c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2252c-146">System.Boolean</span></span>

## <span data-ttu-id="2252c-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2252c-147">NOTES</span></span>

<span data-ttu-id="2252c-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2252c-148">ALIASES</span></span>

<span data-ttu-id="2252c-149">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="2252c-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2252c-150">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2252c-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2252c-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="2252c-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2252c-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="2252c-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2252c-153">`[ClusterName <String>]`: A kubernetes-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2252c-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="2252c-154">`[ClusterResourceName <String>]`: A Kubernetes-fürterőforrás neve – managedClusters (ak-fürtök esetében) vagy connectedClusters (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="2252c-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="2252c-155">`[ClusterRp <String>]`: A Kubernetes-as cluster RP-Microsoft. ContainerService (ak-fürtök esetében) vagy Microsoft. Kubernetes (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="2252c-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="2252c-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2252c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2252c-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2252c-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2252c-158">`[SourceControlConfigurationName <String>]`: A verziókövetés konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="2252c-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="2252c-159">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2252c-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2252c-160">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="2252c-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2252c-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2252c-161">RELATED LINKS</span></span>

