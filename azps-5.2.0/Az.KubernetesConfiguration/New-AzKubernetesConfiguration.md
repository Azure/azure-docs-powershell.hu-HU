---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367722"
---
# <span data-ttu-id="de468-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="de468-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="de468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de468-102">SYNOPSIS</span></span>
<span data-ttu-id="de468-103">Hozzon létre egy új Kubanetes-forrásvezérlő-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="de468-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="de468-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de468-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de468-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de468-105">DESCRIPTION</span></span>
<span data-ttu-id="de468-106">Hozzon létre egy új Kubanetes-forrásvezérlő-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="de468-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="de468-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de468-107">EXAMPLES</span></span>

### <span data-ttu-id="de468-108">1. példa: Konfigurációs konfiguráció létrehozása a kubernetes fürthöz</span><span class="sxs-lookup"><span data-stu-id="de468-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="de468-109">Ezzel a paranccsal konkguguációt hoz létre a rendszer a parancssori hálózatok fürtjéhez.</span><span class="sxs-lookup"><span data-stu-id="de468-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="de468-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de468-110">PARAMETERS</span></span>

### <span data-ttu-id="de468-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="de468-111">-ClusterName</span></span>
<span data-ttu-id="de468-112">A kubernetes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="de468-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="de468-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="de468-113">-ClusterScoped</span></span>
<span data-ttu-id="de468-114">Ha a beállításnak megfelelő tartományt ad meg, a konfiguráció hatókörét fürtre állíthatja (az alapértelmezett névTér.</span><span class="sxs-lookup"><span data-stu-id="de468-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="de468-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="de468-115">-ClusterType</span></span>
<span data-ttu-id="de468-116">A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="de468-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="de468-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de468-117">-DefaultProfile</span></span>
<span data-ttu-id="de468-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de468-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de468-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="de468-119">-EnableHelmOperator</span></span>
<span data-ttu-id="de468-120">Option to enable Fogék operátor for this git configuration.</span><span class="sxs-lookup"><span data-stu-id="de468-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="de468-121">-MerteOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="de468-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="de468-122">Values override for the operator Chart.</span><span class="sxs-lookup"><span data-stu-id="de468-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="de468-123">-ÉkOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="de468-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="de468-124">A Chart operátor verziója.</span><span class="sxs-lookup"><span data-stu-id="de468-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="de468-125">-Name</span><span class="sxs-lookup"><span data-stu-id="de468-125">-Name</span></span>
<span data-ttu-id="de468-126">A forrásvezérlő-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="de468-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="de468-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="de468-127">-OperatorInstanceName</span></span>
<span data-ttu-id="de468-128">Az operátor példányneve – az adott konfiguráció azonosítása.</span><span class="sxs-lookup"><span data-stu-id="de468-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="de468-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="de468-129">-OperatorNamespace</span></span>
<span data-ttu-id="de468-130">Az a névtér, amelyre az operátor telepítve van.</span><span class="sxs-lookup"><span data-stu-id="de468-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="de468-131">Legfeljebb 253 kisbetűs alfanumerikus karakter, kötőjel és pont.</span><span class="sxs-lookup"><span data-stu-id="de468-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="de468-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="de468-132">-OperatorParameters</span></span>
<span data-ttu-id="de468-133">Az Operátor példány bármely paramétere karakterlánc formátumban.</span><span class="sxs-lookup"><span data-stu-id="de468-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="de468-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="de468-134">-RepositoryUrl</span></span>
<span data-ttu-id="de468-135">A SourceControl adattár URL-címe.</span><span class="sxs-lookup"><span data-stu-id="de468-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="de468-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de468-136">-ResourceGroupName</span></span>
<span data-ttu-id="de468-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de468-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="de468-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de468-138">-SubscriptionId</span></span>
<span data-ttu-id="de468-139">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="de468-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="de468-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de468-140">-Confirm</span></span>
<span data-ttu-id="de468-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="de468-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de468-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de468-142">-WhatIf</span></span>
<span data-ttu-id="de468-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="de468-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de468-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de468-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de468-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de468-145">CommonParameters</span></span>
<span data-ttu-id="de468-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de468-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de468-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de468-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de468-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de468-148">INPUTS</span></span>

## <span data-ttu-id="de468-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de468-149">OUTPUTS</span></span>

### <span data-ttu-id="de468-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="de468-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="de468-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de468-151">NOTES</span></span>

<span data-ttu-id="de468-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="de468-152">ALIASES</span></span>

## <span data-ttu-id="de468-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de468-153">RELATED LINKS</span></span>

