---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181858"
---
# <span data-ttu-id="b4fad-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4fad-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="b4fad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4fad-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fad-103">Hozzon létre egy új Kubernetes-vezérlő konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b4fad-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="b4fad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4fad-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4fad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4fad-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fad-106">Hozzon létre egy új Kubernetes-vezérlő konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b4fad-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="b4fad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4fad-107">EXAMPLES</span></span>

### <span data-ttu-id="b4fad-108">Példa 1: configuation létrehozása kubernetes-fürtökhöz</span><span class="sxs-lookup"><span data-stu-id="b4fad-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="b4fad-109">Ez a parancs létrehoz egy configuation a kubernetes-alapú fürtökhöz.</span><span class="sxs-lookup"><span data-stu-id="b4fad-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="b4fad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4fad-110">PARAMETERS</span></span>

### <span data-ttu-id="b4fad-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b4fad-111">-ClusterName</span></span>
<span data-ttu-id="b4fad-112">A kubernetes-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b4fad-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="b4fad-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="b4fad-113">-ClusterScoped</span></span>
<span data-ttu-id="b4fad-114">Ha a hágó értékre állítja a konfiguráció hatókörét a cluster értékre (az alapértelmezett névtér).</span><span class="sxs-lookup"><span data-stu-id="b4fad-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="b4fad-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="b4fad-115">-ClusterType</span></span>
<span data-ttu-id="b4fad-116">A Kubernetes-fürterőforrás neve – managedClusters (ak-fürtök esetében) vagy connectedClusters (helyi K8S-fürtök esetén).</span><span class="sxs-lookup"><span data-stu-id="b4fad-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="b4fad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fad-117">-DefaultProfile</span></span>
<span data-ttu-id="b4fad-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4fad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4fad-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="b4fad-119">-EnableHelmOperator</span></span>
<span data-ttu-id="b4fad-120">A sisak-operátor beállításának engedélyezése a git konfigurációban.</span><span class="sxs-lookup"><span data-stu-id="b4fad-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="b4fad-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="b4fad-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="b4fad-122">Az értékek felülbírálják az operátor Helm-diagramját.</span><span class="sxs-lookup"><span data-stu-id="b4fad-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="b4fad-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="b4fad-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="b4fad-124">Az operátor élén álló diagram verziója.</span><span class="sxs-lookup"><span data-stu-id="b4fad-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="b4fad-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4fad-125">-Name</span></span>
<span data-ttu-id="b4fad-126">A verziókövetés konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="b4fad-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="b4fad-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="b4fad-127">-OperatorInstanceName</span></span>
<span data-ttu-id="b4fad-128">Az operátor példányának neve – a konkrét konfiguráció azonosítása.</span><span class="sxs-lookup"><span data-stu-id="b4fad-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="b4fad-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="b4fad-129">-OperatorNamespace</span></span>
<span data-ttu-id="b4fad-130">Az a névtér, amelyre az operátor van telepítve.</span><span class="sxs-lookup"><span data-stu-id="b4fad-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="b4fad-131">Legfeljebb 253 (kisbetűs), kötőjel és pont.</span><span class="sxs-lookup"><span data-stu-id="b4fad-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="b4fad-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="b4fad-132">-OperatorParameters</span></span>
<span data-ttu-id="b4fad-133">Az operátori példány paraméterei karakterlánc formátumban.</span><span class="sxs-lookup"><span data-stu-id="b4fad-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="b4fad-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="b4fad-134">-RepositoryUrl</span></span>
<span data-ttu-id="b4fad-135">A SourceControl-tárház URL-címe.</span><span class="sxs-lookup"><span data-stu-id="b4fad-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="b4fad-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4fad-136">-ResourceGroupName</span></span>
<span data-ttu-id="b4fad-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b4fad-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4fad-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4fad-138">-SubscriptionId</span></span>
<span data-ttu-id="b4fad-139">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b4fad-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="b4fad-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4fad-140">-Confirm</span></span>
<span data-ttu-id="b4fad-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4fad-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4fad-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4fad-142">-WhatIf</span></span>
<span data-ttu-id="b4fad-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4fad-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4fad-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4fad-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4fad-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fad-145">CommonParameters</span></span>
<span data-ttu-id="b4fad-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4fad-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fad-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4fad-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fad-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4fad-148">INPUTS</span></span>

## <span data-ttu-id="b4fad-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4fad-149">OUTPUTS</span></span>

### <span data-ttu-id="b4fad-150">Microsoft. Azure. PowerShell. parancsmagok. KubernetesConfiguration. modellek. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4fad-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="b4fad-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4fad-151">NOTES</span></span>

<span data-ttu-id="b4fad-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b4fad-152">ALIASES</span></span>

## <span data-ttu-id="b4fad-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4fad-153">RELATED LINKS</span></span>

