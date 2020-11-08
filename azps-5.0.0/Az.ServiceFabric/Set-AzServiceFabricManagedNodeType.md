---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186712"
---
# <span data-ttu-id="8d683-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="8d683-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="8d683-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d683-102">SYNOPSIS</span></span>
<span data-ttu-id="8d683-103">Beállítja a csomópont típusa erőforrás tulajdonságait, vagy ha a-Reimage paramétert tartalmazó csomópont típusának adott NDES a Reimage műveletet futtatja.</span><span class="sxs-lookup"><span data-stu-id="8d683-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="8d683-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d683-104">SYNTAX</span></span>

### <span data-ttu-id="8d683-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d683-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d683-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="8d683-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d683-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="8d683-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d683-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="8d683-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d683-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="8d683-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d683-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="8d683-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d683-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d683-111">DESCRIPTION</span></span>
<span data-ttu-id="8d683-112">Beállítja a csomópont típusa erőforrás tulajdonságait, vagy ha a-Reimage paramétert tartalmazó csomópont típusának adott NDES a Reimage műveletet futtatja.</span><span class="sxs-lookup"><span data-stu-id="8d683-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="8d683-113">A reimgae működéséhez a szolgáltatás szövet csomópontja le lesz tiltva a VMS-szolgáltatás visszaállítása előtt, és ismét engedélyezve van, miután visszajöttek.</span><span class="sxs-lookup"><span data-stu-id="8d683-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="8d683-114">Ha ez az elsődleges csomópont-típusokon végezhető el, akkor eltarthat egy ideig, amíg az összes csomópontot nem lehet egyszerre módosítani.</span><span class="sxs-lookup"><span data-stu-id="8d683-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="8d683-115">A-ForceReimage akkor is kényszeríti a műveletet, ha a szolgáltatás nem tudja letiltani a csomópontokat, de óvatosan használja az adatvesztést, ha a csomóponton az állapotos terhelések futnak.</span><span class="sxs-lookup"><span data-stu-id="8d683-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="8d683-116">Példák</span><span class="sxs-lookup"><span data-stu-id="8d683-116">EXAMPLES</span></span>

### <span data-ttu-id="8d683-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d683-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="8d683-118">Frissítse a csomópont típusának számát.</span><span class="sxs-lookup"><span data-stu-id="8d683-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="8d683-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d683-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="8d683-120">A csomópont-típus properites módosítása.</span><span class="sxs-lookup"><span data-stu-id="8d683-120">Update placement properites of the node type.</span></span> <span data-ttu-id="8d683-121">Ezzel felülírja a régebbi elhelyezési properites, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="8d683-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="8d683-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="8d683-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="8d683-123">A csomópont típusa a 0 és a 3 csomópontot ábrázolja.</span><span class="sxs-lookup"><span data-stu-id="8d683-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="8d683-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="8d683-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="8d683-125">Frissítse a csomópont típusának számát a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="8d683-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="8d683-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d683-126">PARAMETERS</span></span>

### <span data-ttu-id="8d683-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="8d683-127">-ApplicationEndPort</span></span>
<span data-ttu-id="8d683-128">Egy porttartomány alkalmazás-végpontja.</span><span class="sxs-lookup"><span data-stu-id="8d683-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="8d683-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="8d683-129">-ApplicationStartPort</span></span>
<span data-ttu-id="8d683-130">Egy porttartomány alkalmazás-indítási portja.</span><span class="sxs-lookup"><span data-stu-id="8d683-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="8d683-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d683-131">-AsJob</span></span>
<span data-ttu-id="8d683-132">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="8d683-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8d683-133">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="8d683-133">-Capacity</span></span>
<span data-ttu-id="8d683-134">A csomópont típusú csomópontokban kulcs/érték párokként alkalmazott kapacitások címkéi: a cluster resource Manager ezeket a címkéket fogja használni annak megértéséhez, hogy mennyi erőforrást tartalmaz a csomópont.</span><span class="sxs-lookup"><span data-stu-id="8d683-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="8d683-135">Frissítés: felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="8d683-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="8d683-136">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="8d683-136">-ClusterName</span></span>
<span data-ttu-id="8d683-137">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="8d683-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8d683-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d683-138">-DefaultProfile</span></span>
<span data-ttu-id="8d683-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d683-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d683-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="8d683-140">-EphemeralEndPort</span></span>
<span data-ttu-id="8d683-141">Egy porttartomány időszakos végpontja.</span><span class="sxs-lookup"><span data-stu-id="8d683-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="8d683-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="8d683-142">-EphemeralStartPort</span></span>
<span data-ttu-id="8d683-143">Egy porttartomány ideiglenes indítási portja.</span><span class="sxs-lookup"><span data-stu-id="8d683-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="8d683-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="8d683-144">-ForceReimage</span></span>
<span data-ttu-id="8d683-145">Az e jelző használatával akkor is kényszerítheti az eltávolítást, ha a szolgáltatás nem tudja letiltani a csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="8d683-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="8d683-146">Óvatosan használja az adatvesztést, ha az állapotos munkaterhelések a csomóponton futnak.</span><span class="sxs-lookup"><span data-stu-id="8d683-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="8d683-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d683-147">-InputObject</span></span>
<span data-ttu-id="8d683-148">Csomópont típusa erőforrás</span><span class="sxs-lookup"><span data-stu-id="8d683-148">Node type resource</span></span>

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

### <span data-ttu-id="8d683-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="8d683-149">-InstanceCount</span></span>
<span data-ttu-id="8d683-150">A csomópont-típus csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="8d683-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="8d683-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d683-151">-Name</span></span>
<span data-ttu-id="8d683-152">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="8d683-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="8d683-153">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="8d683-153">-NodeName</span></span>
<span data-ttu-id="8d683-154">A művelet csomópont-neveinek listája.</span><span class="sxs-lookup"><span data-stu-id="8d683-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="8d683-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d683-155">-PassThru</span></span>
<span data-ttu-id="8d683-156">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8d683-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8d683-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="8d683-157">-PlacementProperty</span></span>
<span data-ttu-id="8d683-158">Az elhelyezési címkék a csomópontok típusában kulcs/érték párokként alkalmazhatók, amelyek azt jelzik, hogy egyes szolgáltatások (munkaterhelés) futása milyen módon történjen.</span><span class="sxs-lookup"><span data-stu-id="8d683-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="8d683-159">Frissítés: felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="8d683-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="8d683-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="8d683-160">-Reimage</span></span>
<span data-ttu-id="8d683-161">A csomópontok típusának megadásához adja meg a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8d683-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="8d683-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d683-162">-ResourceGroupName</span></span>
<span data-ttu-id="8d683-163">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="8d683-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8d683-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d683-164">-ResourceId</span></span>
<span data-ttu-id="8d683-165">Csomópont típusa erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8d683-165">Node type resource id</span></span>

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

### <span data-ttu-id="8d683-166">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d683-166">-Confirm</span></span>
<span data-ttu-id="8d683-167">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d683-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d683-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d683-168">-WhatIf</span></span>
<span data-ttu-id="8d683-169">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d683-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d683-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d683-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d683-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d683-171">CommonParameters</span></span>
<span data-ttu-id="8d683-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d683-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d683-173">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d683-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d683-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d683-174">INPUTS</span></span>

### <span data-ttu-id="8d683-175">System. String</span><span class="sxs-lookup"><span data-stu-id="8d683-175">System.String</span></span>

## <span data-ttu-id="8d683-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d683-176">OUTPUTS</span></span>

### <span data-ttu-id="8d683-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d683-177">System.Boolean</span></span>

## <span data-ttu-id="8d683-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d683-178">NOTES</span></span>

## <span data-ttu-id="8d683-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d683-179">RELATED LINKS</span></span>
