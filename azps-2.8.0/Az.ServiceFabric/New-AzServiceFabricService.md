---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 5a17b7197399ac51afccfbc5b00a77e0d2bca727
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838003"
---
# <span data-ttu-id="bd29c-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bd29c-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="bd29c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd29c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd29c-103">Új szolgáltatási anyag szolgáltatás létrehozása a megadott alkalmazásban és fürtben.</span><span class="sxs-lookup"><span data-stu-id="bd29c-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="bd29c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd29c-104">SYNTAX</span></span>

### <span data-ttu-id="bd29c-105">Stateless-Singleton (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd29c-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd29c-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="bd29c-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd29c-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="bd29c-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd29c-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="bd29c-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd29c-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="bd29c-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd29c-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="bd29c-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd29c-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd29c-111">DESCRIPTION</span></span>
<span data-ttu-id="bd29c-112">Ez a parancsmag lehetővé teszi a megadott alkalmazásban a hontalan vagy állapot-nyilvántartó szolgáltatások létrehozását.</span><span class="sxs-lookup"><span data-stu-id="bd29c-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="bd29c-113">A szolgáltatásnak ki kell lépnie az alkalmazás jegyzékfájljában, és a típusnak meg kell egyeznie a jegyzékfájl egyikével.</span><span class="sxs-lookup"><span data-stu-id="bd29c-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="bd29c-114">Az alkalmazás nevének a szolgáltatás nevének előtagjának kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bd29c-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="bd29c-115">Példák</span><span class="sxs-lookup"><span data-stu-id="bd29c-115">EXAMPLES</span></span>

### <span data-ttu-id="bd29c-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd29c-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="bd29c-117">Ez a példa létrehoz egy új, hontalan szolgáltatást "testApp ~ testService1", amelyben a Count-1 (az összes csomóponton) szerepel.</span><span class="sxs-lookup"><span data-stu-id="bd29c-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="bd29c-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="bd29c-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="bd29c-119">Az alábbi példa egy új, "testApp ~ testService2" szolgáltatót hoz létre 5 csomópontból álló céllal.</span><span class="sxs-lookup"><span data-stu-id="bd29c-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="bd29c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd29c-120">PARAMETERS</span></span>

### <span data-ttu-id="bd29c-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="bd29c-121">-ApplicationName</span></span>
<span data-ttu-id="bd29c-122">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="bd29c-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="bd29c-123">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="bd29c-123">-ClusterName</span></span>
<span data-ttu-id="bd29c-124">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="bd29c-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bd29c-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="bd29c-125">-DefaultMoveCost</span></span>
<span data-ttu-id="bd29c-126">Adja meg az áthelyezés alapértelmezett költségét.</span><span class="sxs-lookup"><span data-stu-id="bd29c-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="bd29c-127">A magasabb költségek miatt kevésbé valószínű, hogy a cluster resource Manager áthelyezi a replikát a fürt kiegyensúlyozásakor.</span><span class="sxs-lookup"><span data-stu-id="bd29c-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

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

### <span data-ttu-id="bd29c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd29c-128">-DefaultProfile</span></span>
<span data-ttu-id="bd29c-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd29c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd29c-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="bd29c-130">-InstanceCount</span></span>
<span data-ttu-id="bd29c-131">A szolgáltatáshoz tartozó példányok számának megadása</span><span class="sxs-lookup"><span data-stu-id="bd29c-131">Specify the instance count for the service</span></span>

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

### <span data-ttu-id="bd29c-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="bd29c-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="bd29c-133">A szolgáltatás min-kópiakészlet-méretének megadása</span><span class="sxs-lookup"><span data-stu-id="bd29c-133">Specify the min replica set size for the service</span></span>

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

### <span data-ttu-id="bd29c-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd29c-134">-Name</span></span>
<span data-ttu-id="bd29c-135">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="bd29c-135">Specify the name of the service.</span></span>

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

### <span data-ttu-id="bd29c-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="bd29c-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="bd29c-137">Azt jelzi, hogy a szolgáltatás a névvel ellátott partíciót használja.</span><span class="sxs-lookup"><span data-stu-id="bd29c-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="bd29c-138">Az e modellt használó szolgáltatások általában egy rögzített halmazban tárolható adatgyűjtők lehetnek.</span><span class="sxs-lookup"><span data-stu-id="bd29c-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="bd29c-139">A névvel ellátott lemezpartíció által használt adatmezők néhány gyakori példája: régiók, postai kódok, vevőcsoportok vagy más üzleti határvonalak.</span><span class="sxs-lookup"><span data-stu-id="bd29c-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

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

### <span data-ttu-id="bd29c-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="bd29c-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="bd29c-141">Azt jelzi, hogy a szolgáltatás az egyedi partíciót használja.</span><span class="sxs-lookup"><span data-stu-id="bd29c-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="bd29c-142">Az egyedi partíciókat általában akkor használják, ha a szolgáltatás nem igényel további művelettervet.</span><span class="sxs-lookup"><span data-stu-id="bd29c-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

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

### <span data-ttu-id="bd29c-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="bd29c-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="bd29c-144">Azt jelzi, hogy a szolgáltatás a UniformInt64-partíciót használja.</span><span class="sxs-lookup"><span data-stu-id="bd29c-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="bd29c-145">Ez azt jelenti, hogy minden partíciót egy Int64-kulcs birtokában kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bd29c-145">This means that each partition owns a range of int64 keys.</span></span>

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

### <span data-ttu-id="bd29c-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="bd29c-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="bd29c-147">A szolgáltatáshoz tartozó kvórum-elvesztési idő megadása</span><span class="sxs-lookup"><span data-stu-id="bd29c-147">Specify the quorum loss wait duration for the service</span></span>

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

### <span data-ttu-id="bd29c-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="bd29c-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="bd29c-149">A replika újraindítási várakozási időtartamának megadása a szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="bd29c-149">Specify the replica restart wait duration for the service</span></span>

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

### <span data-ttu-id="bd29c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd29c-150">-ResourceGroupName</span></span>
<span data-ttu-id="bd29c-151">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="bd29c-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bd29c-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="bd29c-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="bd29c-153">Adja meg a szolgáltatáshoz tartozó állást a replika időtartamával.</span><span class="sxs-lookup"><span data-stu-id="bd29c-153">Specify the stand by replica duration for the service</span></span>

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

### <span data-ttu-id="bd29c-154">-Állapotú</span><span class="sxs-lookup"><span data-stu-id="bd29c-154">-Stateful</span></span>
<span data-ttu-id="bd29c-155">Az állapot-nyilvántartó szolgáltatás használata</span><span class="sxs-lookup"><span data-stu-id="bd29c-155">Use for stateful service</span></span>

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

### <span data-ttu-id="bd29c-156">-Hontalan</span><span class="sxs-lookup"><span data-stu-id="bd29c-156">-Stateless</span></span>
<span data-ttu-id="bd29c-157">A hontalan szolgáltatás használata</span><span class="sxs-lookup"><span data-stu-id="bd29c-157">Use for stateless service</span></span>

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

### <span data-ttu-id="bd29c-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="bd29c-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="bd29c-159">A szolgáltatáshoz tartozó replikakészlet-készlet méretének meghatározása</span><span class="sxs-lookup"><span data-stu-id="bd29c-159">Specify the target replica set size for the service</span></span>

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

### <span data-ttu-id="bd29c-160">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="bd29c-160">-Type</span></span>
<span data-ttu-id="bd29c-161">Adja meg az alkalmazás szolgáltatás-típusának nevét az alkalmazás jegyzékfájljában.</span><span class="sxs-lookup"><span data-stu-id="bd29c-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

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

### <span data-ttu-id="bd29c-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd29c-162">-Confirm</span></span>
<span data-ttu-id="bd29c-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd29c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd29c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd29c-164">-WhatIf</span></span>
<span data-ttu-id="bd29c-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd29c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd29c-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd29c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd29c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd29c-167">CommonParameters</span></span>
<span data-ttu-id="bd29c-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd29c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd29c-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd29c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd29c-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd29c-170">INPUTS</span></span>

### <span data-ttu-id="bd29c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="bd29c-171">System.String</span></span>

## <span data-ttu-id="bd29c-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd29c-172">OUTPUTS</span></span>

### <span data-ttu-id="bd29c-173">Microsoft. Azure. Command. ServiceFabric. models. PSService</span><span class="sxs-lookup"><span data-stu-id="bd29c-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="bd29c-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd29c-174">NOTES</span></span>

## <span data-ttu-id="bd29c-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd29c-175">RELATED LINKS</span></span>
