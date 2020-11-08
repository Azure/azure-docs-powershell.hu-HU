---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186537"
---
# <span data-ttu-id="e3522-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e3522-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="e3522-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3522-102">SYNOPSIS</span></span>
<span data-ttu-id="e3522-103">Új csomópont típusú erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e3522-103">Create new node type resource.</span></span>

## <span data-ttu-id="e3522-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3522-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3522-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3522-105">DESCRIPTION</span></span>
<span data-ttu-id="e3522-106">Új csomópont típusú erőforrás létrehozása adott fürtökhöz.</span><span class="sxs-lookup"><span data-stu-id="e3522-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="e3522-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3522-107">EXAMPLES</span></span>

### <span data-ttu-id="e3522-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3522-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="e3522-109">Elsődleges csomópont-típus létrehozása 3 csomóponttal</span><span class="sxs-lookup"><span data-stu-id="e3522-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="e3522-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="e3522-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="e3522-111">Az elsődleges csomópontot 5 csomóponttal hozza létre, és adja meg az elhelyezési tulajdonságokat, a kapacitásokat, az alkalmazást és az ideiglenes portokat.</span><span class="sxs-lookup"><span data-stu-id="e3522-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="e3522-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3522-112">PARAMETERS</span></span>

### <span data-ttu-id="e3522-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="e3522-113">-ApplicationEndPort</span></span>
<span data-ttu-id="e3522-114">Egy porttartomány alkalmazás-végpontja.</span><span class="sxs-lookup"><span data-stu-id="e3522-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="e3522-115">-ApplicationStartPort</span></span>
<span data-ttu-id="e3522-116">Egy porttartomány alkalmazás-indítási portja.</span><span class="sxs-lookup"><span data-stu-id="e3522-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3522-117">-AsJob</span></span>
<span data-ttu-id="e3522-118">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e3522-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e3522-119">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="e3522-119">-Capacity</span></span>
<span data-ttu-id="e3522-120">A csomópont típusú csomópontokban kulcs/érték párokként alkalmazott kapacitások címkéi: a cluster resource Manager ezeket a címkéket fogja használni annak megértéséhez, hogy mennyi erőforrást tartalmaz a csomópont.</span><span class="sxs-lookup"><span data-stu-id="e3522-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="e3522-121">Frissítés: felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="e3522-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-122">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e3522-122">-ClusterName</span></span>
<span data-ttu-id="e3522-123">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="e3522-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e3522-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3522-124">-DefaultProfile</span></span>
<span data-ttu-id="e3522-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3522-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3522-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="e3522-126">-DiskSize</span></span>
<span data-ttu-id="e3522-127">A csomópont típusa GB-ban</span><span class="sxs-lookup"><span data-stu-id="e3522-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="e3522-128">Alapértelmezett 100.</span><span class="sxs-lookup"><span data-stu-id="e3522-128">Default 100.</span></span>

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

### <span data-ttu-id="e3522-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="e3522-129">-EphemeralEndPort</span></span>
<span data-ttu-id="e3522-130">Egy porttartomány időszakos végpontja.</span><span class="sxs-lookup"><span data-stu-id="e3522-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="e3522-131">-EphemeralStartPort</span></span>
<span data-ttu-id="e3522-132">Egy porttartomány ideiglenes indítási portja.</span><span class="sxs-lookup"><span data-stu-id="e3522-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e3522-133">-InstanceCount</span></span>
<span data-ttu-id="e3522-134">A csomópont-típus csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="e3522-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3522-135">-Name</span></span>
<span data-ttu-id="e3522-136">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="e3522-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="e3522-137">-PlacementProperty</span></span>
<span data-ttu-id="e3522-138">Az elhelyezési címkék a csomópontok típusában kulcs/érték párokként alkalmazhatók, amelyek azt jelzik, hogy egyes szolgáltatások (munkaterhelés) futása milyen módon történjen.</span><span class="sxs-lookup"><span data-stu-id="e3522-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="e3522-139">Frissítés: felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="e3522-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-140">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="e3522-140">-Primary</span></span>
<span data-ttu-id="e3522-141">Adja meg, hogy a csomópont típusa elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="e3522-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="e3522-142">A csomópont típusa a rendszerszolgáltatásokat fogja futtatni.</span><span class="sxs-lookup"><span data-stu-id="e3522-142">On this node type will run system services.</span></span>
<span data-ttu-id="e3522-143">Csak egy csomópontot kell megjelölni elsődlegesként.</span><span class="sxs-lookup"><span data-stu-id="e3522-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="e3522-144">Az elsődleges csomópont típusa nem törölhető, illetve nem módosítható a meglévő fürtök esetében.</span><span class="sxs-lookup"><span data-stu-id="e3522-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="e3522-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3522-145">-ResourceGroupName</span></span>
<span data-ttu-id="e3522-146">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="e3522-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e3522-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="e3522-147">-VmImageOffer</span></span>
<span data-ttu-id="e3522-148">Az Azure Virtual Machines piactér-kép ajánlati típusa.</span><span class="sxs-lookup"><span data-stu-id="e3522-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e3522-149">Alapértelmezett: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="e3522-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e3522-150">-VmImagePublisher</span></span>
<span data-ttu-id="e3522-151">Az Azure Virtual Machines piactér képének kiadója</span><span class="sxs-lookup"><span data-stu-id="e3522-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e3522-152">Alapértelmezett: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="e3522-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="e3522-153">-VmImageSku</span></span>
<span data-ttu-id="e3522-154">Az Azure Virtual Machines piactér képe.</span><span class="sxs-lookup"><span data-stu-id="e3522-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e3522-155">Alapértelmezett: 2019-adatközpont.</span><span class="sxs-lookup"><span data-stu-id="e3522-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="e3522-156">-VmImageVersion</span></span>
<span data-ttu-id="e3522-157">Az Azure Virtual Machines piactéren elérhető kép verziója.</span><span class="sxs-lookup"><span data-stu-id="e3522-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e3522-158">Alapértelmezett: legújabb.</span><span class="sxs-lookup"><span data-stu-id="e3522-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="e3522-159">-VmSize</span></span>
<span data-ttu-id="e3522-160">A virtuális gépek mérete a készletben.</span><span class="sxs-lookup"><span data-stu-id="e3522-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="e3522-161">A készlet minden virtuális számítógépe azonos méretű.</span><span class="sxs-lookup"><span data-stu-id="e3522-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="e3522-162">Alapértelmezett: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="e3522-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3522-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3522-163">-Confirm</span></span>
<span data-ttu-id="e3522-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3522-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3522-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3522-165">-WhatIf</span></span>
<span data-ttu-id="e3522-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3522-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3522-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3522-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3522-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3522-168">CommonParameters</span></span>
<span data-ttu-id="e3522-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3522-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3522-170">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3522-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3522-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3522-171">INPUTS</span></span>

### <span data-ttu-id="e3522-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e3522-172">System.String</span></span>

## <span data-ttu-id="e3522-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3522-173">OUTPUTS</span></span>

### <span data-ttu-id="e3522-174">Microsoft. Azure. Command. ServiceFabric. models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e3522-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e3522-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3522-175">NOTES</span></span>

## <span data-ttu-id="e3522-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3522-176">RELATED LINKS</span></span>
