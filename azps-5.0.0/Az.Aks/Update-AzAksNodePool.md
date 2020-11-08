---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187893"
---
# <span data-ttu-id="16f83-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="16f83-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="16f83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16f83-102">SYNOPSIS</span></span>
<span data-ttu-id="16f83-103">Csomópont-készlet frissítése a felügyelt fürtökben.</span><span class="sxs-lookup"><span data-stu-id="16f83-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="16f83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16f83-104">SYNTAX</span></span>

### <span data-ttu-id="16f83-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16f83-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f83-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16f83-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f83-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16f83-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f83-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16f83-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16f83-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="16f83-109">DESCRIPTION</span></span>
<span data-ttu-id="16f83-110">Csomópont-készlet frissítése a felügyelt fürtökben.</span><span class="sxs-lookup"><span data-stu-id="16f83-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="16f83-111">Példák</span><span class="sxs-lookup"><span data-stu-id="16f83-111">EXAMPLES</span></span>

### <span data-ttu-id="16f83-112">Minimum számának módosítása 5 értékre megadott csomópont-készletre</span><span class="sxs-lookup"><span data-stu-id="16f83-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="16f83-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16f83-113">PARAMETERS</span></span>

### <span data-ttu-id="16f83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16f83-114">-AsJob</span></span>
<span data-ttu-id="16f83-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="16f83-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16f83-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="16f83-116">-ClusterName</span></span>
<span data-ttu-id="16f83-117">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="16f83-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="16f83-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="16f83-118">-ClusterObject</span></span>
<span data-ttu-id="16f83-119">A cluster objektum</span><span class="sxs-lookup"><span data-stu-id="16f83-119">The cluster object</span></span>

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

### <span data-ttu-id="16f83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f83-120">-DefaultProfile</span></span>
<span data-ttu-id="16f83-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16f83-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16f83-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="16f83-122">-EnableAutoScaling</span></span>
<span data-ttu-id="16f83-123">Szeretné-e engedélyezni az automatikus méretezést?</span><span class="sxs-lookup"><span data-stu-id="16f83-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="16f83-124">-Force</span><span class="sxs-lookup"><span data-stu-id="16f83-124">-Force</span></span>
<span data-ttu-id="16f83-125">Csomópont-készlet frissítése kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="16f83-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="16f83-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="16f83-126">-Id</span></span>
<span data-ttu-id="16f83-127">Node-készlet azonosítója a felügyelt Kubernetes-fürtben</span><span class="sxs-lookup"><span data-stu-id="16f83-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="16f83-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16f83-128">-InputObject</span></span>
<span data-ttu-id="16f83-129">Egy PSAgentPool objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="16f83-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="16f83-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="16f83-130">-KubernetesVersion</span></span>
<span data-ttu-id="16f83-131">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="16f83-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="16f83-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16f83-132">-MaxCount</span></span>
<span data-ttu-id="16f83-133">Csomópontok maximális száma automatikus méretezéshez</span><span class="sxs-lookup"><span data-stu-id="16f83-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="16f83-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="16f83-134">-MinCount</span></span>
<span data-ttu-id="16f83-135">Az automatikus méretezéshez szükséges csomópontok minimális száma</span><span class="sxs-lookup"><span data-stu-id="16f83-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="16f83-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16f83-136">-Name</span></span>
<span data-ttu-id="16f83-137">A csomópont-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="16f83-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="16f83-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f83-138">-ResourceGroupName</span></span>
<span data-ttu-id="16f83-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="16f83-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="16f83-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16f83-140">-Confirm</span></span>
<span data-ttu-id="16f83-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16f83-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f83-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f83-142">-WhatIf</span></span>
<span data-ttu-id="16f83-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16f83-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f83-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16f83-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f83-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f83-145">CommonParameters</span></span>
<span data-ttu-id="16f83-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16f83-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f83-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="16f83-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f83-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16f83-148">INPUTS</span></span>

### <span data-ttu-id="16f83-149">Microsoft. Azure. Command. AK. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="16f83-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="16f83-150">System. String</span><span class="sxs-lookup"><span data-stu-id="16f83-150">System.String</span></span>

## <span data-ttu-id="16f83-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16f83-151">OUTPUTS</span></span>

### <span data-ttu-id="16f83-152">Microsoft. Azure. Command. AK. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="16f83-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="16f83-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16f83-153">NOTES</span></span>

## <span data-ttu-id="16f83-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16f83-154">RELATED LINKS</span></span>