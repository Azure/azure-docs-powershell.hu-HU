---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330498"
---
# <span data-ttu-id="d616d-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d616d-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="d616d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d616d-102">SYNOPSIS</span></span>
<span data-ttu-id="d616d-103">Indítsa újra az egyes csomópontokat a csomóponttípusból.</span><span class="sxs-lookup"><span data-stu-id="d616d-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="d616d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d616d-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d616d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d616d-105">DESCRIPTION</span></span>
<span data-ttu-id="d616d-106">Indítsa újra az egyes csomópontokat a csomóponttípusból.</span><span class="sxs-lookup"><span data-stu-id="d616d-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="d616d-107">A rendszer a vms újraindítása előtt letiltja a szolgáltatás-anyagcsomópontokat, és a visszaérésük után ismét engedélyezi őket.</span><span class="sxs-lookup"><span data-stu-id="d616d-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="d616d-108">Ha ez az elsődleges csomóponttípusokon történik, kis ideig is előfordulhat, hogy nem indítja újra egyszerre az összes csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d616d-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="d616d-109">A -ForceRestart akkor is kényszeríti a műveletet, ha a szolgáltatás szövete nem tudja letiltani a csomópontokat, de legyen körültekintő, mivel ez adatvesztést okozhat, ha állapotos terhelések futnak a csomóponton.</span><span class="sxs-lookup"><span data-stu-id="d616d-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="d616d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d616d-110">EXAMPLES</span></span>

### <span data-ttu-id="d616d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d616d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="d616d-112">Indítsa újra a 0- és a 3-as csomópontot a csomóponttípuson.</span><span class="sxs-lookup"><span data-stu-id="d616d-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="d616d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d616d-113">PARAMETERS</span></span>

### <span data-ttu-id="d616d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d616d-114">-AsJob</span></span>
<span data-ttu-id="d616d-115">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d616d-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d616d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d616d-116">-ClusterName</span></span>
<span data-ttu-id="d616d-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="d616d-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d616d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d616d-118">-DefaultProfile</span></span>
<span data-ttu-id="d616d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d616d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d616d-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="d616d-120">-ForceRestart</span></span>
<span data-ttu-id="d616d-121">Ezzel a jelölővel a csomópontot akkor is újraindíthatja, ha a szolgáltatás szövete nem tudja letiltani a csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="d616d-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="d616d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d616d-122">-Name</span></span>
<span data-ttu-id="d616d-123">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="d616d-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d616d-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d616d-124">-NodeName</span></span>
<span data-ttu-id="d616d-125">A művelet csomópontnevének listája.</span><span class="sxs-lookup"><span data-stu-id="d616d-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d616d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d616d-126">-PassThru</span></span>
<span data-ttu-id="d616d-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d616d-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d616d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d616d-128">-ResourceGroupName</span></span>
<span data-ttu-id="d616d-129">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d616d-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d616d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d616d-130">-Confirm</span></span>
<span data-ttu-id="d616d-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d616d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d616d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d616d-132">-WhatIf</span></span>
<span data-ttu-id="d616d-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d616d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d616d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d616d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d616d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d616d-135">CommonParameters</span></span>
<span data-ttu-id="d616d-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d616d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d616d-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d616d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d616d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d616d-138">INPUTS</span></span>

### <span data-ttu-id="d616d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d616d-139">System.String</span></span>

## <span data-ttu-id="d616d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d616d-140">OUTPUTS</span></span>

### <span data-ttu-id="d616d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d616d-141">System.Boolean</span></span>

## <span data-ttu-id="d616d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d616d-142">NOTES</span></span>

## <span data-ttu-id="d616d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d616d-143">RELATED LINKS</span></span>
