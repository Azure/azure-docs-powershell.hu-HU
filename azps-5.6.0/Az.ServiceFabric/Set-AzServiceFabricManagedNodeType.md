---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3f3f19f88ffdd37cbad009950c064e672e186b34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930785"
---
# <span data-ttu-id="c5d2f-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c5d2f-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="c5d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d2f-103">Beállítja a csomóponttípus erőforrástulajdonságokat, vagy reimage-műveleteket futtat a csomóponttípus -Reimage paraméterrel megadott ndes-ján.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="c5d2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5d2f-104">SYNTAX</span></span>

### <span data-ttu-id="c5d2f-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5d2f-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d2f-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="c5d2f-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5d2f-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="c5d2f-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d2f-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="c5d2f-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d2f-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="c5d2f-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d2f-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="c5d2f-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5d2f-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5d2f-111">DESCRIPTION</span></span>
<span data-ttu-id="c5d2f-112">Beállítja a csomóponttípus erőforrástulajdonságokat, vagy reimage-műveleteket futtat a csomóponttípus -Reimage paraméterrel megadott ndes-ján.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="c5d2f-113">A reimgae művelet során a szolgáltatás hálócsomópontjai le lesznek tiltva, mielőtt újra képbe kerülnek a virtuális gépeket, és ismét engedélyezték őket, miután visszatértek.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="c5d2f-114">Ha ez az elsődleges csomóponttípusokon történik, kis ideig is szükség lehet rá, mivel előfordulhat, hogy nem tudja egyszerre újraimálni az összes csomópontot.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="c5d2f-115">A -ForceReimage akkor is kényszeríti a műveletet, ha a szolgáltatás szövete nem tudja letiltani a csomópontokat, de legyen körültekintő, mivel ez adatvesztést okozhat, ha állapotos terhelések futnak a csomóponton.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="c5d2f-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5d2f-116">EXAMPLES</span></span>

### <span data-ttu-id="c5d2f-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5d2f-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="c5d2f-118">Frissítse a csomóponttípus példányszámát.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="c5d2f-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="c5d2f-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="c5d2f-120">Frissítse a csomóponttípus megfelelő helymegjelenítését.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-120">Update placement properites of the node type.</span></span> <span data-ttu-id="c5d2f-121">Ez felülírja a régebbi helymegjelenítési webhelyeket, ha vannak ilyenek.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="c5d2f-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="c5d2f-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="c5d2f-123">A 0-s és a 3-as csomópont újraimálása a csomóponttípuson.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="c5d2f-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="c5d2f-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="c5d2f-125">Frissítse a csomópont példányszámát pipázással.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="c5d2f-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5d2f-126">PARAMETERS</span></span>

### <span data-ttu-id="c5d2f-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="c5d2f-127">-ApplicationEndPort</span></span>
<span data-ttu-id="c5d2f-128">Porttartomány alkalmazásvégi portja.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="c5d2f-129">-ApplicationStartPort</span></span>
<span data-ttu-id="c5d2f-130">Egy porttartomány alkalmazás-indítási portja.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5d2f-131">-AsJob</span></span>
<span data-ttu-id="c5d2f-132">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c5d2f-133">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="c5d2f-133">-Capacity</span></span>
<span data-ttu-id="c5d2f-134">A csomóponttípus csomópontjaira kulcs-/értékpárokként alkalmazott kapacitáscímkék, a fürterőforrás-kezelő ezeket a címkéket használva tudja megérteni, hogy egy csomópont mennyi erőforrással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="c5d2f-135">A frissítés felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c5d2f-136">-ClusterName</span></span>
<span data-ttu-id="c5d2f-137">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d2f-138">-DefaultProfile</span></span>
<span data-ttu-id="c5d2f-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5d2f-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="c5d2f-140">-EphemeralEndPort</span></span>
<span data-ttu-id="c5d2f-141">Egy porttartomány áttűnő vég portja.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="c5d2f-142">-EphemeralStartPort</span></span>
<span data-ttu-id="c5d2f-143">Egy porttartomány kezdetű portja.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="c5d2f-144">-ForceReimage</span></span>
<span data-ttu-id="c5d2f-145">Ezzel a jelzővel akkor is kényszerítheti az eltávolítást, ha a szolgáltatási anyag nem tudja letiltani a csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="c5d2f-146">Legyen óvatos, mert ez adatvesztést okozhat, ha állapotos terhelések futnak a csomóponton.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5d2f-147">-InputObject</span></span>
<span data-ttu-id="c5d2f-148">Node type resource</span><span class="sxs-lookup"><span data-stu-id="c5d2f-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="c5d2f-149">-InstanceCount</span></span>
<span data-ttu-id="c5d2f-150">A csomóponttípus csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-151">-Name</span><span class="sxs-lookup"><span data-stu-id="c5d2f-151">-Name</span></span>
<span data-ttu-id="c5d2f-152">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c5d2f-153">-NodeName</span></span>
<span data-ttu-id="c5d2f-154">A művelet csomópontnevének listája.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5d2f-155">-PassThru</span></span>
<span data-ttu-id="c5d2f-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="c5d2f-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="c5d2f-157">-PlacementProperty</span></span>
<span data-ttu-id="c5d2f-158">A csomóponttípus csomópontjaira kulcs/érték párokként alkalmazott elhelyezési címkék, amelyek bizonyos szolgáltatások (munkaterhelés) futtatásának jelzésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="c5d2f-159">A frissítés felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="c5d2f-160">-Reimage</span></span>
<span data-ttu-id="c5d2f-161">Megadhatja, hogy a csomóponttípus csomópontjainak újraimálása történik-e.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d2f-162">-ResourceGroupName</span></span>
<span data-ttu-id="c5d2f-163">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5d2f-164">-ResourceId</span></span>
<span data-ttu-id="c5d2f-165">Node type resource id</span><span class="sxs-lookup"><span data-stu-id="c5d2f-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d2f-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5d2f-166">-Confirm</span></span>
<span data-ttu-id="c5d2f-167">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5d2f-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d2f-168">-WhatIf</span></span>
<span data-ttu-id="c5d2f-169">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d2f-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5d2f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d2f-171">CommonParameters</span></span>
<span data-ttu-id="c5d2f-172">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d2f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d2f-173">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5d2f-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d2f-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5d2f-174">INPUTS</span></span>

### <span data-ttu-id="c5d2f-175">System.String</span><span class="sxs-lookup"><span data-stu-id="c5d2f-175">System.String</span></span>

## <span data-ttu-id="c5d2f-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5d2f-176">OUTPUTS</span></span>

### <span data-ttu-id="c5d2f-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5d2f-177">System.Boolean</span></span>

## <span data-ttu-id="c5d2f-178">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5d2f-178">NOTES</span></span>

## <span data-ttu-id="c5d2f-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5d2f-179">RELATED LINKS</span></span>
