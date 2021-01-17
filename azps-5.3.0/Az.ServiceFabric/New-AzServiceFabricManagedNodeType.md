---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479554"
---
# <span data-ttu-id="0fa7d-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0fa7d-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="0fa7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa7d-103">Új csomóponttípus-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0fa7d-103">Create new node type resource.</span></span>

## <span data-ttu-id="0fa7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fa7d-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa7d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fa7d-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa7d-106">Új csomóponttípus-erőforrás létrehozása egy adott fürthöz.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="0fa7d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fa7d-107">EXAMPLES</span></span>

### <span data-ttu-id="0fa7d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0fa7d-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="0fa7d-109">Hozzon létre elsődleges csomóponttípust 3 csomóponttal.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="0fa7d-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0fa7d-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="0fa7d-111">Hozza létre az elsődleges csomóponttípust 5 csomóponttal, és adja meg az elhelyezési tulajdonságokat, a kapacitásokat, az alkalmazás- és a félkommerikus portokat.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="0fa7d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fa7d-112">PARAMETERS</span></span>

### <span data-ttu-id="0fa7d-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="0fa7d-113">-ApplicationEndPort</span></span>
<span data-ttu-id="0fa7d-114">Porttartomány alkalmazásvégi portja.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="0fa7d-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="0fa7d-115">-ApplicationStartPort</span></span>
<span data-ttu-id="0fa7d-116">Egy porttartomány alkalmazás-indítási portja.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="0fa7d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fa7d-117">-AsJob</span></span>
<span data-ttu-id="0fa7d-118">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0fa7d-119">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="0fa7d-119">-Capacity</span></span>
<span data-ttu-id="0fa7d-120">A csomóponttípus csomópontjaira kulcs-/értékpárokként alkalmazott kapacitáscímkék, a fürterőforrás-kezelő ezeket a címkéket használva tudja megérteni, hogy egy csomópont mennyi erőforrással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="0fa7d-121">A frissítés felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="0fa7d-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0fa7d-122">-ClusterName</span></span>
<span data-ttu-id="0fa7d-123">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0fa7d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa7d-124">-DefaultProfile</span></span>
<span data-ttu-id="0fa7d-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa7d-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="0fa7d-126">-DiskSize</span></span>
<span data-ttu-id="0fa7d-127">A GBs csomóponttípusú egyes vmek lemezmérete.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="0fa7d-128">Alapértelmezett 100.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-128">Default 100.</span></span>

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

### <span data-ttu-id="0fa7d-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="0fa7d-129">-EphemeralEndPort</span></span>
<span data-ttu-id="0fa7d-130">Egy porttartomány áttűnő vég portja.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="0fa7d-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="0fa7d-131">-EphemeralStartPort</span></span>
<span data-ttu-id="0fa7d-132">Egy porttartomány kezdetű portja.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="0fa7d-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0fa7d-133">-InstanceCount</span></span>
<span data-ttu-id="0fa7d-134">A csomóponttípus csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="0fa7d-135">-Name</span><span class="sxs-lookup"><span data-stu-id="0fa7d-135">-Name</span></span>
<span data-ttu-id="0fa7d-136">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="0fa7d-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="0fa7d-137">-PlacementProperty</span></span>
<span data-ttu-id="0fa7d-138">A csomóponttípus csomópontjaira kulcs-/értékpárokként alkalmazott elhelyezési címkék, amelyek bizonyos szolgáltatások (munkaterhelés) futtatásának jelzésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="0fa7d-139">A frissítés felülírja az aktuális értékeket.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="0fa7d-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="0fa7d-140">-Primary</span></span>
<span data-ttu-id="0fa7d-141">Adja meg, hogy a csomópont típusa elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="0fa7d-142">Ezen a csomóponttípuson rendszerszolgáltatások fognak futni.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-142">On this node type will run system services.</span></span>
<span data-ttu-id="0fa7d-143">Csak egy csomóponttípust kell elsődlegesként megjelölni.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="0fa7d-144">Az elsődleges csomóponttípus nem törölhető és nem módosítható meglévő fürtök esetén.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="0fa7d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa7d-145">-ResourceGroupName</span></span>
<span data-ttu-id="0fa7d-146">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0fa7d-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="0fa7d-147">-VmImageOffer</span></span>
<span data-ttu-id="0fa7d-148">Az Azure Virtuális gépek piactéri lemezkép ajánlattípusa.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0fa7d-149">Alapértelmezett: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="0fa7d-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0fa7d-150">-VmImagePublisher</span></span>
<span data-ttu-id="0fa7d-151">The publisher of the Azure Virtual Machines Marketplace image.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0fa7d-152">Alapértelmezett: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="0fa7d-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="0fa7d-153">-VmImageSku</span></span>
<span data-ttu-id="0fa7d-154">The SKU of the Azure Virtual Machines Marketplace image.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0fa7d-155">Alapérték: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="0fa7d-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="0fa7d-156">-VmImageVersion</span></span>
<span data-ttu-id="0fa7d-157">Az Azure Virtuális gépek piactér képe.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0fa7d-158">Alapértelmezett: legújabb.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-158">Default: latest.</span></span>

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

### <span data-ttu-id="0fa7d-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="0fa7d-159">-VmSize</span></span>
<span data-ttu-id="0fa7d-160">A virtuális gépek mérete a készletben.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="0fa7d-161">A készlet összes virtuális gépe azonos méretű.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="0fa7d-162">Alapértelmezett: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="0fa7d-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fa7d-163">-Confirm</span></span>
<span data-ttu-id="0fa7d-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa7d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa7d-165">-WhatIf</span></span>
<span data-ttu-id="0fa7d-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa7d-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa7d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa7d-168">CommonParameters</span></span>
<span data-ttu-id="0fa7d-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa7d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa7d-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fa7d-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa7d-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fa7d-171">INPUTS</span></span>

### <span data-ttu-id="0fa7d-172">System.String</span><span class="sxs-lookup"><span data-stu-id="0fa7d-172">System.String</span></span>

## <span data-ttu-id="0fa7d-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fa7d-173">OUTPUTS</span></span>

### <span data-ttu-id="0fa7d-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0fa7d-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="0fa7d-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fa7d-175">NOTES</span></span>

## <span data-ttu-id="0fa7d-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fa7d-176">RELATED LINKS</span></span>
