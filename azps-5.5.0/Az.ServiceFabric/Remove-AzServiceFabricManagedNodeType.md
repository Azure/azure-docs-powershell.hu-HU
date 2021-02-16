---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150698"
---
# <span data-ttu-id="755d0-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="755d0-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="755d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755d0-102">SYNOPSIS</span></span>
<span data-ttu-id="755d0-103">Távolítsa el a csomóponttípust vagy a csomóponttípus adott csomópontját.</span><span class="sxs-lookup"><span data-stu-id="755d0-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="755d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="755d0-104">SYNTAX</span></span>

### <span data-ttu-id="755d0-105">DeleteNodeTypeByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="755d0-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755d0-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="755d0-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755d0-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="755d0-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755d0-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="755d0-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="755d0-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="755d0-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755d0-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="755d0-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755d0-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="755d0-111">DESCRIPTION</span></span>
<span data-ttu-id="755d0-112">Távolítsa el a csomóponttípust vagy a csomóponttípus adott csomópontját.</span><span class="sxs-lookup"><span data-stu-id="755d0-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="755d0-113">Ha a paremter -NodeName paramétert használja, akkor csak a megadott csomópontok lesznek eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="755d0-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="755d0-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="755d0-114">EXAMPLES</span></span>

### <span data-ttu-id="755d0-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="755d0-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="755d0-116">Távolítsa el a csomóponttípust.</span><span class="sxs-lookup"><span data-stu-id="755d0-116">Remove node type.</span></span>

### <span data-ttu-id="755d0-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="755d0-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="755d0-118">Távolítsa el a csomóponttípust pipázással.</span><span class="sxs-lookup"><span data-stu-id="755d0-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="755d0-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="755d0-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="755d0-120">Távolítson el 2 csomópontot a csomóponttípusból.</span><span class="sxs-lookup"><span data-stu-id="755d0-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="755d0-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="755d0-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="755d0-122">Távolítson el 2 csomópontot a csomóponttípusból pipázással.</span><span class="sxs-lookup"><span data-stu-id="755d0-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="755d0-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="755d0-123">PARAMETERS</span></span>

### <span data-ttu-id="755d0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="755d0-124">-AsJob</span></span>
<span data-ttu-id="755d0-125">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="755d0-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="755d0-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="755d0-126">-ClusterName</span></span>
<span data-ttu-id="755d0-127">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="755d0-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="755d0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755d0-128">-DefaultProfile</span></span>
<span data-ttu-id="755d0-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="755d0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755d0-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="755d0-130">-ForceRemoveNode</span></span>
<span data-ttu-id="755d0-131">Ezzel a jelzővel akkor is kényszerítheti az eltávolítást, ha a szolgáltatási anyag nem tudja letiltani a csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="755d0-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="755d0-132">Legyen óvatos, mert ez adatvesztést okozhat, ha állapotos munkaterhelések futnak a csomópontokon, vagy lefelé hozhatja a fürtöt, ha a művelet után nem áll rendelkezésre elegendő magcsomópont.</span><span class="sxs-lookup"><span data-stu-id="755d0-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="755d0-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="755d0-133">-InputObject</span></span>
<span data-ttu-id="755d0-134">Node type resource</span><span class="sxs-lookup"><span data-stu-id="755d0-134">Node type resource</span></span>

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

### <span data-ttu-id="755d0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="755d0-135">-Name</span></span>
<span data-ttu-id="755d0-136">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="755d0-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="755d0-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="755d0-137">-NodeName</span></span>
<span data-ttu-id="755d0-138">A művelet csomópontnevének listája.</span><span class="sxs-lookup"><span data-stu-id="755d0-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="755d0-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="755d0-139">-PassThru</span></span>
<span data-ttu-id="755d0-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="755d0-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="755d0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755d0-141">-ResourceGroupName</span></span>
<span data-ttu-id="755d0-142">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="755d0-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="755d0-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="755d0-143">-ResourceId</span></span>
<span data-ttu-id="755d0-144">Node type resource id</span><span class="sxs-lookup"><span data-stu-id="755d0-144">Node type resource id</span></span>

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

### <span data-ttu-id="755d0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="755d0-145">-Confirm</span></span>
<span data-ttu-id="755d0-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="755d0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755d0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755d0-147">-WhatIf</span></span>
<span data-ttu-id="755d0-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="755d0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755d0-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="755d0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755d0-150">CommonParameters</span></span>
<span data-ttu-id="755d0-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755d0-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="755d0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755d0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="755d0-153">INPUTS</span></span>

### <span data-ttu-id="755d0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="755d0-154">System.String</span></span>

## <span data-ttu-id="755d0-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="755d0-155">OUTPUTS</span></span>

### <span data-ttu-id="755d0-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="755d0-156">System.Boolean</span></span>

## <span data-ttu-id="755d0-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="755d0-157">NOTES</span></span>

## <span data-ttu-id="755d0-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="755d0-158">RELATED LINKS</span></span>
