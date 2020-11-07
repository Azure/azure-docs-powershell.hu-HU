---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: bcc0a4f39b2c5578213aeb3ea5087ce1cc21cc4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665751"
---
# <span data-ttu-id="e3741-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="e3741-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="e3741-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3741-102">SYNOPSIS</span></span>
<span data-ttu-id="e3741-103">Kubectl-konfiguráció importálása és egyesítése felügyelt Kubernetes-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e3741-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="e3741-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3741-104">SYNTAX</span></span>

### <span data-ttu-id="e3741-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3741-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3741-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3741-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3741-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3741-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3741-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3741-108">DESCRIPTION</span></span>
<span data-ttu-id="e3741-109">Kubectl-konfiguráció importálása és egyesítése felügyelt Kubernetes-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e3741-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="e3741-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e3741-110">EXAMPLES</span></span>

### <span data-ttu-id="e3741-111">A Kubectl-konfiguráció importálása és egyesítése</span><span class="sxs-lookup"><span data-stu-id="e3741-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e3741-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3741-112">PARAMETERS</span></span>

### <span data-ttu-id="e3741-113">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="e3741-113">-Admin</span></span>
<span data-ttu-id="e3741-114">Az alapértelmezett "clusterUser" helyett a "clusterAdmin' kubectl" konfigurációt kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="e3741-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="e3741-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="e3741-115">-ConfigPath</span></span>
<span data-ttu-id="e3741-116">A létrehozandó vagy frissítendő kubectl konfigurációs fájl.</span><span class="sxs-lookup"><span data-stu-id="e3741-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="e3741-117">A "-" YAML kinyomtatásához használja inkább az stdout-ot.</span><span class="sxs-lookup"><span data-stu-id="e3741-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="e3741-118">Alapértelmezett:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="e3741-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="e3741-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3741-119">-DefaultProfile</span></span>
<span data-ttu-id="e3741-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3741-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3741-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e3741-121">-Force</span></span>
<span data-ttu-id="e3741-122">Az Kubernetes-konfiguráció importálása akkor is, ha az alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="e3741-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="e3741-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e3741-123">-Id</span></span>
<span data-ttu-id="e3741-124">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="e3741-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3741-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3741-125">-InputObject</span></span>
<span data-ttu-id="e3741-126">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e3741-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3741-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3741-127">-Name</span></span>
<span data-ttu-id="e3741-128">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="e3741-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3741-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3741-129">-PassThru</span></span>
<span data-ttu-id="e3741-130">Eredménye igaz, ha az importálás sikeres</span><span class="sxs-lookup"><span data-stu-id="e3741-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="e3741-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3741-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3741-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e3741-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3741-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3741-133">-Confirm</span></span>
<span data-ttu-id="e3741-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3741-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3741-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3741-135">-WhatIf</span></span>
<span data-ttu-id="e3741-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3741-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3741-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3741-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3741-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3741-138">CommonParameters</span></span>
<span data-ttu-id="e3741-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3741-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3741-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3741-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3741-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3741-141">INPUTS</span></span>

### <span data-ttu-id="e3741-142">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e3741-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="e3741-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e3741-143">System.String</span></span>

## <span data-ttu-id="e3741-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3741-144">OUTPUTS</span></span>

### <span data-ttu-id="e3741-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e3741-145">System.String</span></span>

## <span data-ttu-id="e3741-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3741-146">NOTES</span></span>

## <span data-ttu-id="e3741-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3741-147">RELATED LINKS</span></span>
