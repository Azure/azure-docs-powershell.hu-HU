---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348857"
---
# <span data-ttu-id="d0952-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="d0952-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="d0952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0952-102">SYNOPSIS</span></span>
<span data-ttu-id="d0952-103">Csomópontkészlet frissítése felügyelt fürtben</span><span class="sxs-lookup"><span data-stu-id="d0952-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="d0952-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0952-104">SYNTAX</span></span>

### <span data-ttu-id="d0952-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0952-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0952-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0952-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0952-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0952-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0952-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0952-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0952-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0952-109">DESCRIPTION</span></span>
<span data-ttu-id="d0952-110">Csomópontkészlet frissítése felügyelt fürtben</span><span class="sxs-lookup"><span data-stu-id="d0952-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="d0952-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0952-111">EXAMPLES</span></span>

### <span data-ttu-id="d0952-112">A minimunszám módosítása 5-re a megadott csomópontkészlethez</span><span class="sxs-lookup"><span data-stu-id="d0952-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="d0952-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0952-113">PARAMETERS</span></span>

### <span data-ttu-id="d0952-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0952-114">-AsJob</span></span>
<span data-ttu-id="d0952-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d0952-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0952-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d0952-116">-ClusterName</span></span>
<span data-ttu-id="d0952-117">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d0952-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="d0952-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="d0952-118">-ClusterObject</span></span>
<span data-ttu-id="d0952-119">A fürtobjektum</span><span class="sxs-lookup"><span data-stu-id="d0952-119">The cluster object</span></span>

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

### <span data-ttu-id="d0952-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0952-120">-DefaultProfile</span></span>
<span data-ttu-id="d0952-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0952-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0952-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="d0952-122">-EnableAutoScaling</span></span>
<span data-ttu-id="d0952-123">Az automatikus méretarányozó engedélyezése</span><span class="sxs-lookup"><span data-stu-id="d0952-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="d0952-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d0952-124">-Force</span></span>
<span data-ttu-id="d0952-125">Csomópontkészlet frissítése kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="d0952-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="d0952-126">-Id</span><span class="sxs-lookup"><span data-stu-id="d0952-126">-Id</span></span>
<span data-ttu-id="d0952-127">A felügyelt Kubanetes-fürtben található csomópontkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="d0952-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="d0952-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0952-128">-InputObject</span></span>
<span data-ttu-id="d0952-129">EGY PSAgentPool-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="d0952-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="d0952-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d0952-130">-KubernetesVersion</span></span>
<span data-ttu-id="d0952-131">A fürt létrehozásához használt Kuternetes-verzió.</span><span class="sxs-lookup"><span data-stu-id="d0952-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="d0952-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d0952-132">-MaxCount</span></span>
<span data-ttu-id="d0952-133">Az automatikus méretezés csomópontjainak maximális száma</span><span class="sxs-lookup"><span data-stu-id="d0952-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="d0952-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="d0952-134">-MinCount</span></span>
<span data-ttu-id="d0952-135">Az automatikus méretezés csomópontjainak minimális száma.</span><span class="sxs-lookup"><span data-stu-id="d0952-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="d0952-136">-Name</span><span class="sxs-lookup"><span data-stu-id="d0952-136">-Name</span></span>
<span data-ttu-id="d0952-137">A csomópontkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="d0952-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="d0952-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0952-138">-ResourceGroupName</span></span>
<span data-ttu-id="d0952-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0952-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0952-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0952-140">-Confirm</span></span>
<span data-ttu-id="d0952-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0952-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0952-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0952-142">-WhatIf</span></span>
<span data-ttu-id="d0952-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0952-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0952-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0952-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0952-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0952-145">CommonParameters</span></span>
<span data-ttu-id="d0952-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0952-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0952-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0952-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0952-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0952-148">INPUTS</span></span>

### <span data-ttu-id="d0952-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="d0952-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="d0952-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d0952-150">System.String</span></span>

## <span data-ttu-id="d0952-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0952-151">OUTPUTS</span></span>

### <span data-ttu-id="d0952-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="d0952-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="d0952-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0952-153">NOTES</span></span>

## <span data-ttu-id="d0952-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0952-154">RELATED LINKS</span></span>
