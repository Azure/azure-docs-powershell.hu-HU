---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187112"
---
# <span data-ttu-id="fa2e8-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="fa2e8-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="fa2e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa2e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2e8-103">Új csomópont-készlet létrehozása a megadott fürtben.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="fa2e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa2e8-104">SYNTAX</span></span>

### <span data-ttu-id="fa2e8-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2e8-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2e8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2e8-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2e8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa2e8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa2e8-108">Új csomópont-készlet létrehozása a megadott fürtben.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="fa2e8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fa2e8-109">EXAMPLES</span></span>

### <span data-ttu-id="fa2e8-110">Node Pool létrehozása alapértelmezett paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="fa2e8-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="fa2e8-111">Windows Server-tároló létrehozása AK-ra</span><span class="sxs-lookup"><span data-stu-id="fa2e8-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="fa2e8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa2e8-112">PARAMETERS</span></span>

### <span data-ttu-id="fa2e8-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="fa2e8-113">-ClusterName</span></span>
<span data-ttu-id="fa2e8-114">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="fa2e8-115">-ClusterObject</span></span>
<span data-ttu-id="fa2e8-116">Adja meg azt a fürtcsomópont-objektumot, amelybe csomópontot szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-117">-Count</span><span class="sxs-lookup"><span data-stu-id="fa2e8-117">-Count</span></span>
<span data-ttu-id="fa2e8-118">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="fa2e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2e8-119">-DefaultProfile</span></span>
<span data-ttu-id="fa2e8-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa2e8-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="fa2e8-121">-EnableAutoScaling</span></span>
<span data-ttu-id="fa2e8-122">Szeretné-e engedélyezni az automatikus méretezést?</span><span class="sxs-lookup"><span data-stu-id="fa2e8-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="fa2e8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fa2e8-123">-Force</span></span>
<span data-ttu-id="fa2e8-124">Node Pool létrehozása akkor is, ha már létezik</span><span class="sxs-lookup"><span data-stu-id="fa2e8-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="fa2e8-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="fa2e8-125">-KubernetesVersion</span></span>
<span data-ttu-id="fa2e8-126">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-126">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fa2e8-127">-MaxCount</span></span>
<span data-ttu-id="fa2e8-128">Csomópontok maximális száma automatikus méretezéshez</span><span class="sxs-lookup"><span data-stu-id="fa2e8-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="fa2e8-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="fa2e8-129">-MaxPodCount</span></span>
<span data-ttu-id="fa2e8-130">A csomópontokon futtatható hüvelyek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="fa2e8-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="fa2e8-131">-MinCount</span></span>
<span data-ttu-id="fa2e8-132">Az automatikus méretezéshez szükséges csomópontok minimális száma</span><span class="sxs-lookup"><span data-stu-id="fa2e8-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="fa2e8-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa2e8-133">-Name</span></span>
<span data-ttu-id="fa2e8-134">A csomópont-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-134">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="fa2e8-135">-OsDiskSize</span></span>
<span data-ttu-id="fa2e8-136">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="fa2e8-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="fa2e8-137">-OsType</span></span>
<span data-ttu-id="fa2e8-138">A OsType az operációs rendszer típusának megadására használható.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="fa2e8-139">Válasszon a Linux és a Windows közül.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="fa2e8-140">A Linux alapértelmezett értéke.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-140">Default to Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2e8-141">-ResourceGroupName</span></span>
<span data-ttu-id="fa2e8-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fa2e8-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="fa2e8-144">A kis prioritású virtuális gép ScaleSetEvictionPolicy a kilakoltatási házirend megadására használható.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="fa2e8-145">Alapértelmezés szerint törölni kell.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-145">Default to Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="fa2e8-146">-ScaleSetPriority</span></span>
<span data-ttu-id="fa2e8-147">A virtuálisgép-készlet prioritásának megadására szolgáló ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="fa2e8-148">Alapértelmezés szerint normál.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-148">Default to regular.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="fa2e8-149">-VmSetType</span></span>
<span data-ttu-id="fa2e8-150">Egy csomópont-gyűjtő típusait jelöli.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-150">Represents types of an node pool.</span></span>
<span data-ttu-id="fa2e8-151">A lehetséges értékek a következők: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="fa2e8-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fa2e8-152">-VmSize</span></span>
<span data-ttu-id="fa2e8-153">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="fa2e8-154">Az alapértelmezett érték Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-154">Default value is Standard_D2_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="fa2e8-155">-VnetSubnetID</span></span>
<span data-ttu-id="fa2e8-156">A VNet a VNet alhálózati azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2e8-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa2e8-157">-Confirm</span></span>
<span data-ttu-id="fa2e8-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2e8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2e8-159">-WhatIf</span></span>
<span data-ttu-id="fa2e8-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2e8-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2e8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2e8-162">CommonParameters</span></span>
<span data-ttu-id="fa2e8-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa2e8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2e8-164">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa2e8-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2e8-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa2e8-165">INPUTS</span></span>

### <span data-ttu-id="fa2e8-166">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fa2e8-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fa2e8-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa2e8-167">OUTPUTS</span></span>

### <span data-ttu-id="fa2e8-168">Microsoft. Azure. Command. AK. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="fa2e8-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="fa2e8-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa2e8-169">NOTES</span></span>

## <span data-ttu-id="fa2e8-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa2e8-170">RELATED LINKS</span></span>
