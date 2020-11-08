---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185853"
---
# <span data-ttu-id="fa2b8-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fa2b8-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="fa2b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2b8-103">A csomópont típusától kezdve indítsa újra az adott csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="fa2b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa2b8-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa2b8-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2b8-106">A csomópont típusától kezdve indítsa újra az adott csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="fa2b8-107">A rendszer letiltotta a szolgáltatás szerkezetének csomópontját, mielőtt újra elindítja a VMS-et, és ismét engedélyezi őket, ha visszatérnek.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="fa2b8-108">Ha ez az elsődleges csomópont-típusokon végezhető el, eltarthat egy ideig, amíg az összes csomópontot nem indítja el egyszerre.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="fa2b8-109">A-ForceRestart akkor is kényszeríti a műveletet, ha a szolgáltatás nem tudja letiltani a csomópontokat, de óvatosan használja az adatvesztést, ha a csomóponton az állapotos terhelések futnak.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="fa2b8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fa2b8-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2b8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa2b8-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="fa2b8-112">A csomópont típusában indítsa újra a 0 és a 3 csomópontot.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="fa2b8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa2b8-113">PARAMETERS</span></span>

### <span data-ttu-id="fa2b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa2b8-114">-AsJob</span></span>
<span data-ttu-id="fa2b8-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fa2b8-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="fa2b8-116">-ClusterName</span></span>
<span data-ttu-id="fa2b8-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fa2b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2b8-118">-DefaultProfile</span></span>
<span data-ttu-id="fa2b8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa2b8-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="fa2b8-120">-ForceRestart</span></span>
<span data-ttu-id="fa2b8-121">Ezzel a jelölővel a csomópontot akkor is újra kell indítani, ha a szolgáltatás nem tudja letiltani a csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="fa2b8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa2b8-122">-Name</span></span>
<span data-ttu-id="fa2b8-123">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="fa2b8-124">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="fa2b8-124">-NodeName</span></span>
<span data-ttu-id="fa2b8-125">A művelet csomópont-neveinek listája.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="fa2b8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa2b8-126">-PassThru</span></span>
<span data-ttu-id="fa2b8-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fa2b8-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="fa2b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa2b8-129">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fa2b8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa2b8-130">-Confirm</span></span>
<span data-ttu-id="fa2b8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2b8-132">-WhatIf</span></span>
<span data-ttu-id="fa2b8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2b8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2b8-135">CommonParameters</span></span>
<span data-ttu-id="fa2b8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa2b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2b8-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa2b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2b8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa2b8-138">INPUTS</span></span>

### <span data-ttu-id="fa2b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa2b8-139">System.String</span></span>

## <span data-ttu-id="fa2b8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa2b8-140">OUTPUTS</span></span>

### <span data-ttu-id="fa2b8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa2b8-141">System.Boolean</span></span>

## <span data-ttu-id="fa2b8-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa2b8-142">NOTES</span></span>

## <span data-ttu-id="fa2b8-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa2b8-143">RELATED LINKS</span></span>