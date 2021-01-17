---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342113"
---
# <span data-ttu-id="e0226-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e0226-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="e0226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0226-102">SYNOPSIS</span></span>
<span data-ttu-id="e0226-103">Hozzon létre új szervizszolgáltatást a megadott alkalmazás és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="e0226-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="e0226-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0226-104">SYNTAX</span></span>

### <span data-ttu-id="e0226-105">Stateless-Singleton (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0226-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0226-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="e0226-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0226-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="e0226-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0226-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="e0226-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0226-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="e0226-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0226-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="e0226-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0226-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0226-111">DESCRIPTION</span></span>
<span data-ttu-id="e0226-112">Ez a parancsmag lehetővé teszi, hogy a megadott alkalmazás alatt állapot nélküli vagy állapotos szolgáltatásokat hozzon létre.</span><span class="sxs-lookup"><span data-stu-id="e0226-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="e0226-113">A szolgáltatásnak ki kell lépnie az alkalmazás jegyzékfájlból, és a típusnak meg kell egyednek lennie a jegyzékfájlban találhatóval.</span><span class="sxs-lookup"><span data-stu-id="e0226-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="e0226-114">Az alkalmazásnévnek a szolgáltatásnév előtagja kell, hogy legyen.</span><span class="sxs-lookup"><span data-stu-id="e0226-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="e0226-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0226-115">EXAMPLES</span></span>

### <span data-ttu-id="e0226-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0226-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="e0226-117">Ebben a példában létrehoz egy új állapot nélküli "testApp~testService1" szolgáltatást a példányszám -1 értékével (az összes csomóponton).</span><span class="sxs-lookup"><span data-stu-id="e0226-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="e0226-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="e0226-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="e0226-119">Ebben a példában egy új állapotos "testApp~testService2" szolgáltatást hozunk létre 5 csomópont célértékével.</span><span class="sxs-lookup"><span data-stu-id="e0226-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="e0226-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0226-120">PARAMETERS</span></span>

### <span data-ttu-id="e0226-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e0226-121">-ApplicationName</span></span>
<span data-ttu-id="e0226-122">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="e0226-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e0226-123">-ClusterName</span></span>
<span data-ttu-id="e0226-124">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="e0226-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e0226-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="e0226-125">-DefaultMoveCost</span></span>
<span data-ttu-id="e0226-126">Adja meg az áthelyezés alapértelmezett költségét.</span><span class="sxs-lookup"><span data-stu-id="e0226-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="e0226-127">A magasabb költségek miatt kevésbé valószínű, hogy a Fürterőforrás-kezelő áthelyezi a replikát a fürt kiegyensúlyozásakor.</span><span class="sxs-lookup"><span data-stu-id="e0226-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0226-128">-DefaultProfile</span></span>
<span data-ttu-id="e0226-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0226-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0226-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e0226-130">-InstanceCount</span></span>
<span data-ttu-id="e0226-131">A szolgáltatás példányszámának megadása</span><span class="sxs-lookup"><span data-stu-id="e0226-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="e0226-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="e0226-133">A szolgáltatás minimális replikakészletméretének megadása</span><span class="sxs-lookup"><span data-stu-id="e0226-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e0226-134">-Name</span></span>
<span data-ttu-id="e0226-135">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="e0226-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="e0226-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="e0226-137">Azt jelzi, hogy a szolgáltatás a megnevezett partíciós sémát használja.</span><span class="sxs-lookup"><span data-stu-id="e0226-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="e0226-138">Az ezt a modellt használó szolgáltatások általában olyan adatokat tartalmaznak, amelyek egy kötött halmazon belül gyűjtővel is gyűjtődnek.</span><span class="sxs-lookup"><span data-stu-id="e0226-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="e0226-139">Az elnevezett partíciókulcsként használt adatmezők közé tartozik például a régiók, az irányítószámok, az ügyfélcsoportok vagy más üzleti területek.</span><span class="sxs-lookup"><span data-stu-id="e0226-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="e0226-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="e0226-141">Azt jelzi, hogy a szolgáltatás az egytonos partíciós sémát használja.</span><span class="sxs-lookup"><span data-stu-id="e0226-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="e0226-142">Az egytonos partíciókat általában akkor használják, ha a szolgáltatás nem igényel további útválasztást.</span><span class="sxs-lookup"><span data-stu-id="e0226-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="e0226-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="e0226-144">Azt jelzi, hogy a szolgáltatás a UniformInt64 partíciós sémát használja.</span><span class="sxs-lookup"><span data-stu-id="e0226-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="e0226-145">Ez azt jelenti, hogy minden partíciónak van egy int64-es kulcstartománya.</span><span class="sxs-lookup"><span data-stu-id="e0226-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-146">-LossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="e0226-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="e0226-147">Adja meg a szolgáltatás veszteségveszteség-várakozási időtartamát</span><span class="sxs-lookup"><span data-stu-id="e0226-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="e0226-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="e0226-149">A replika újraindítási várakozási időtartamának megadása a szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="e0226-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0226-150">-ResourceGroupName</span></span>
<span data-ttu-id="e0226-151">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="e0226-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e0226-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="e0226-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="e0226-153">A szolgáltatás stand by replika-időtartamának megadása</span><span class="sxs-lookup"><span data-stu-id="e0226-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="e0226-154">-Stateful</span></span>
<span data-ttu-id="e0226-155">Állapotos szolgáltatáshoz használható</span><span class="sxs-lookup"><span data-stu-id="e0226-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-156">-Stateless</span><span class="sxs-lookup"><span data-stu-id="e0226-156">-Stateless</span></span>
<span data-ttu-id="e0226-157">Állapot nélküli szolgáltatáshoz használható</span><span class="sxs-lookup"><span data-stu-id="e0226-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="e0226-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="e0226-159">A célként megadott replikakészlet méretének megadása a szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="e0226-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-160">-Type</span><span class="sxs-lookup"><span data-stu-id="e0226-160">-Type</span></span>
<span data-ttu-id="e0226-161">Adja meg az alkalmazás szolgáltatástípusának nevét, amely létezik az alkalmazás jegyzékfájlban.</span><span class="sxs-lookup"><span data-stu-id="e0226-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0226-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0226-162">-Confirm</span></span>
<span data-ttu-id="e0226-163">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e0226-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0226-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0226-164">-WhatIf</span></span>
<span data-ttu-id="e0226-165">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e0226-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0226-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0226-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0226-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0226-167">CommonParameters</span></span>
<span data-ttu-id="e0226-168">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0226-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0226-169">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0226-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0226-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0226-170">INPUTS</span></span>

### <span data-ttu-id="e0226-171">System.String</span><span class="sxs-lookup"><span data-stu-id="e0226-171">System.String</span></span>

## <span data-ttu-id="e0226-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0226-172">OUTPUTS</span></span>

### <span data-ttu-id="e0226-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="e0226-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="e0226-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0226-174">NOTES</span></span>

## <span data-ttu-id="e0226-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0226-175">RELATED LINKS</span></span>
