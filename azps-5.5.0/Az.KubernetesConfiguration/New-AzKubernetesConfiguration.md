---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 425a2f2fcc145b360ea981a4d78113d6053c90e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152571"
---
# <span data-ttu-id="62c52-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="62c52-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="62c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c52-102">SYNOPSIS</span></span>
<span data-ttu-id="62c52-103">Hozzon létre egy új Kubanetes-forrásvezérlő-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="62c52-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="62c52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62c52-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62c52-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62c52-105">DESCRIPTION</span></span>
<span data-ttu-id="62c52-106">Hozzon létre egy új Kubanetes-forrásvezérlő-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="62c52-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="62c52-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62c52-107">EXAMPLES</span></span>

### <span data-ttu-id="62c52-108">1. példa: Konfiguráció létrehozása a rendszerhálózati fürthöz</span><span class="sxs-lookup"><span data-stu-id="62c52-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="62c52-109">Ez a parancs konfigurációt hoz létre a kubernetes fürthöz.</span><span class="sxs-lookup"><span data-stu-id="62c52-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="62c52-110">1. példa: Konfigurálás létrehozása a következő paramétert megadásával: operátorNevespace</span><span class="sxs-lookup"><span data-stu-id="62c52-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="62c52-111">Ez a parancs konfigurációt hoz létre az új operátor névterében a kubernetes fürthöz.</span><span class="sxs-lookup"><span data-stu-id="62c52-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="62c52-112">Megjegyzés: Nem lehet konfigurációt létrehozni egy meglévő operátor névterében.</span><span class="sxs-lookup"><span data-stu-id="62c52-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="62c52-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62c52-113">PARAMETERS</span></span>

### <span data-ttu-id="62c52-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="62c52-114">-ClusterName</span></span>
<span data-ttu-id="62c52-115">A kubernetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="62c52-115">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="62c52-116">-ClusterScoped</span></span>
<span data-ttu-id="62c52-117">Ha a beállításnak megfelelő tartományt ad meg, a konfiguráció hatókörét fürtre állíthatja (az alapértelmezett névTér.</span><span class="sxs-lookup"><span data-stu-id="62c52-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="62c52-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="62c52-118">-ClusterType</span></span>
<span data-ttu-id="62c52-119">A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="62c52-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c52-120">-DefaultProfile</span></span>
<span data-ttu-id="62c52-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62c52-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c52-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="62c52-122">-EnableHelmOperator</span></span>
<span data-ttu-id="62c52-123">Option to enable Fogék operátor for this git configuration.</span><span class="sxs-lookup"><span data-stu-id="62c52-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="62c52-124">-FogarasoperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="62c52-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="62c52-125">Values override for the operator Chart.</span><span class="sxs-lookup"><span data-stu-id="62c52-125">Values override for the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-126">-KatonaOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="62c52-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="62c52-127">A Chart operátor verziója.</span><span class="sxs-lookup"><span data-stu-id="62c52-127">Version of the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-128">-Name</span><span class="sxs-lookup"><span data-stu-id="62c52-128">-Name</span></span>
<span data-ttu-id="62c52-129">A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="62c52-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="62c52-130">-OperatorInstanceName</span></span>
<span data-ttu-id="62c52-131">Az operátor példányneve – az adott konfiguráció azonosítása.</span><span class="sxs-lookup"><span data-stu-id="62c52-131">Instance name of the operator - identifying the specific configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="62c52-132">-OperatorNamespace</span></span>
<span data-ttu-id="62c52-133">Az a névtér, amelyre az operátor telepítve van.</span><span class="sxs-lookup"><span data-stu-id="62c52-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="62c52-134">Legfeljebb 253 kisbetűs alfanumerikus karakter, kötőjel és pont.</span><span class="sxs-lookup"><span data-stu-id="62c52-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="62c52-135">-OperatorParameters</span></span>
<span data-ttu-id="62c52-136">Az Operátor példány bármely paramétere karakterlánc formátumban.</span><span class="sxs-lookup"><span data-stu-id="62c52-136">Any Parameters for the Operator instance in string format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="62c52-137">-RepositoryUrl</span></span>
<span data-ttu-id="62c52-138">A SourceControl adattár URL-címe.</span><span class="sxs-lookup"><span data-stu-id="62c52-138">Url of the SourceControl Repository.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c52-139">-ResourceGroupName</span></span>
<span data-ttu-id="62c52-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="62c52-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62c52-141">-SubscriptionId</span></span>
<span data-ttu-id="62c52-142">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62c52-142">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c52-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62c52-143">-Confirm</span></span>
<span data-ttu-id="62c52-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62c52-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c52-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c52-145">-WhatIf</span></span>
<span data-ttu-id="62c52-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62c52-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c52-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62c52-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c52-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c52-148">CommonParameters</span></span>
<span data-ttu-id="62c52-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c52-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c52-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62c52-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c52-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62c52-151">INPUTS</span></span>

## <span data-ttu-id="62c52-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c52-152">OUTPUTS</span></span>

### <span data-ttu-id="62c52-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.iSourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="62c52-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="62c52-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62c52-154">NOTES</span></span>

<span data-ttu-id="62c52-155">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="62c52-155">ALIASES</span></span>

## <span data-ttu-id="62c52-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62c52-156">RELATED LINKS</span></span>

