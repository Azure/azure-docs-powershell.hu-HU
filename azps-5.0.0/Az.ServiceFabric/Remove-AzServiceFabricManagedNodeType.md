---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185860"
---
# <span data-ttu-id="e14d6-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e14d6-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="e14d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e14d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e14d6-103">Távolítsa el a csomópont típusát vagy a csomópont típusának bizonyos csomópontját.</span><span class="sxs-lookup"><span data-stu-id="e14d6-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="e14d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e14d6-104">SYNTAX</span></span>

### <span data-ttu-id="e14d6-105">DeleteNodeTypeByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e14d6-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14d6-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="e14d6-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14d6-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="e14d6-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14d6-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="e14d6-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e14d6-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="e14d6-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14d6-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="e14d6-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e14d6-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="e14d6-111">DESCRIPTION</span></span>
<span data-ttu-id="e14d6-112">Távolítsa el a csomópont típusát vagy a csomópont típusának bizonyos csomópontját.</span><span class="sxs-lookup"><span data-stu-id="e14d6-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="e14d6-113">Ha a paremter – csomópontnév, akkor a program csak a megadott csomópontokat távolítja el.</span><span class="sxs-lookup"><span data-stu-id="e14d6-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="e14d6-114">Példák</span><span class="sxs-lookup"><span data-stu-id="e14d6-114">EXAMPLES</span></span>

### <span data-ttu-id="e14d6-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e14d6-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="e14d6-116">Csomópont-típus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e14d6-116">Remove node type.</span></span>

### <span data-ttu-id="e14d6-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="e14d6-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="e14d6-118">Csomópont-típus eltávolítása a csövekkel</span><span class="sxs-lookup"><span data-stu-id="e14d6-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="e14d6-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="e14d6-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="e14d6-120">Távolítsa el a két csomópontot a csomópont típusától.</span><span class="sxs-lookup"><span data-stu-id="e14d6-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="e14d6-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="e14d6-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="e14d6-122">Távolítsa el a két csomópontot a csomópont típusától, a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="e14d6-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="e14d6-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e14d6-123">PARAMETERS</span></span>

### <span data-ttu-id="e14d6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e14d6-124">-AsJob</span></span>
<span data-ttu-id="e14d6-125">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e14d6-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e14d6-126">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e14d6-126">-ClusterName</span></span>
<span data-ttu-id="e14d6-127">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="e14d6-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14d6-128">-DefaultProfile</span></span>
<span data-ttu-id="e14d6-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e14d6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14d6-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="e14d6-130">-ForceRemoveNode</span></span>
<span data-ttu-id="e14d6-131">Az e jelző használatával akkor is kényszerítheti az eltávolítást, ha a szolgáltatás nem tudja letiltani a csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="e14d6-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="e14d6-132">Óvatosan használja az adatvesztést, ha az adatvesztést okoz, ha az állapotos munkamennyiségek a csomópontokon futnak, vagy ha a opearion után nem áll rendelkezésre elegendő mag csomópont.</span><span class="sxs-lookup"><span data-stu-id="e14d6-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e14d6-133">-InputObject</span></span>
<span data-ttu-id="e14d6-134">Csomópont típusa erőforrás</span><span class="sxs-lookup"><span data-stu-id="e14d6-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e14d6-135">-Name</span></span>
<span data-ttu-id="e14d6-136">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="e14d6-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-137">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="e14d6-137">-NodeName</span></span>
<span data-ttu-id="e14d6-138">A művelet csomópont-neveinek listája.</span><span class="sxs-lookup"><span data-stu-id="e14d6-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e14d6-139">-PassThru</span></span>
<span data-ttu-id="e14d6-140">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e14d6-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e14d6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14d6-141">-ResourceGroupName</span></span>
<span data-ttu-id="e14d6-142">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="e14d6-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e14d6-143">-ResourceId</span></span>
<span data-ttu-id="e14d6-144">Csomópont típusa erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e14d6-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e14d6-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e14d6-145">-Confirm</span></span>
<span data-ttu-id="e14d6-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e14d6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e14d6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14d6-147">-WhatIf</span></span>
<span data-ttu-id="e14d6-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e14d6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e14d6-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e14d6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e14d6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14d6-150">CommonParameters</span></span>
<span data-ttu-id="e14d6-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e14d6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14d6-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e14d6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14d6-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e14d6-153">INPUTS</span></span>

### <span data-ttu-id="e14d6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e14d6-154">System.String</span></span>

## <span data-ttu-id="e14d6-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e14d6-155">OUTPUTS</span></span>

### <span data-ttu-id="e14d6-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e14d6-156">System.Boolean</span></span>

## <span data-ttu-id="e14d6-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e14d6-157">NOTES</span></span>

## <span data-ttu-id="e14d6-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e14d6-158">RELATED LINKS</span></span>
