---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469109"
---
# <span data-ttu-id="a709d-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="a709d-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="a709d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a709d-102">SYNOPSIS</span></span>
<span data-ttu-id="a709d-103">Csomópontkészlet frissítése felügyelt fürtben</span><span class="sxs-lookup"><span data-stu-id="a709d-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="a709d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a709d-104">SYNTAX</span></span>

### <span data-ttu-id="a709d-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a709d-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a709d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a709d-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a709d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a709d-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a709d-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a709d-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a709d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a709d-109">DESCRIPTION</span></span>
<span data-ttu-id="a709d-110">Csomópontkészlet frissítése felügyelt fürtben</span><span class="sxs-lookup"><span data-stu-id="a709d-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="a709d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a709d-111">EXAMPLES</span></span>

### <span data-ttu-id="a709d-112">A minimunszám módosítása 5-re a megadott csomópontkészlethez</span><span class="sxs-lookup"><span data-stu-id="a709d-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="a709d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a709d-113">PARAMETERS</span></span>

### <span data-ttu-id="a709d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a709d-114">-AsJob</span></span>
<span data-ttu-id="a709d-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a709d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a709d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a709d-116">-ClusterName</span></span>
<span data-ttu-id="a709d-117">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a709d-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="a709d-118">-ClusterObject</span></span>
<span data-ttu-id="a709d-119">A fürtobjektum</span><span class="sxs-lookup"><span data-stu-id="a709d-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a709d-120">-DefaultProfile</span></span>
<span data-ttu-id="a709d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a709d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a709d-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="a709d-122">-EnableAutoScaling</span></span>
<span data-ttu-id="a709d-123">Az automatikus méretarányozó engedélyezése</span><span class="sxs-lookup"><span data-stu-id="a709d-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="a709d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a709d-124">-Force</span></span>
<span data-ttu-id="a709d-125">Csomópontkészlet frissítése kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="a709d-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="a709d-126">-Id</span><span class="sxs-lookup"><span data-stu-id="a709d-126">-Id</span></span>
<span data-ttu-id="a709d-127">A felügyelt Kubanetes-fürtben található csomópontkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="a709d-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a709d-128">-InputObject</span></span>
<span data-ttu-id="a709d-129">EGY PSAgentPool-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="a709d-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="a709d-130">-KubernetesVersion</span></span>
<span data-ttu-id="a709d-131">A fürt létrehozásához használt Kuternetes-verzió.</span><span class="sxs-lookup"><span data-stu-id="a709d-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="a709d-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a709d-132">-MaxCount</span></span>
<span data-ttu-id="a709d-133">Az automatikus méretezés csomópontjainak maximális száma</span><span class="sxs-lookup"><span data-stu-id="a709d-133">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="a709d-134">-MinCount</span></span>
<span data-ttu-id="a709d-135">Az automatikus méretezés csomópontjainak minimális száma.</span><span class="sxs-lookup"><span data-stu-id="a709d-135">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-136">-Name</span><span class="sxs-lookup"><span data-stu-id="a709d-136">-Name</span></span>
<span data-ttu-id="a709d-137">A csomópontkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="a709d-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a709d-138">-ResourceGroupName</span></span>
<span data-ttu-id="a709d-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a709d-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a709d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a709d-140">-Confirm</span></span>
<span data-ttu-id="a709d-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a709d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a709d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a709d-142">-WhatIf</span></span>
<span data-ttu-id="a709d-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a709d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a709d-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a709d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a709d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a709d-145">CommonParameters</span></span>
<span data-ttu-id="a709d-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a709d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a709d-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a709d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a709d-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a709d-148">INPUTS</span></span>

### <span data-ttu-id="a709d-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a709d-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="a709d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="a709d-150">System.String</span></span>

## <span data-ttu-id="a709d-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a709d-151">OUTPUTS</span></span>

### <span data-ttu-id="a709d-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a709d-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="a709d-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a709d-153">NOTES</span></span>

## <span data-ttu-id="a709d-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a709d-154">RELATED LINKS</span></span>
