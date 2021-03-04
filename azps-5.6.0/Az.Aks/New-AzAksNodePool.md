---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 07944177b7c92ff4c515b6d9dcd01d11d3c5a888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923897"
---
# <span data-ttu-id="b7327-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="b7327-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="b7327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7327-102">SYNOPSIS</span></span>
<span data-ttu-id="b7327-103">Hozzon létre egy új csomópontkészletet a megadott fürtben.</span><span class="sxs-lookup"><span data-stu-id="b7327-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="b7327-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7327-104">SYNTAX</span></span>

### <span data-ttu-id="b7327-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7327-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7327-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7327-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7327-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7327-107">DESCRIPTION</span></span>
<span data-ttu-id="b7327-108">Hozzon létre egy új csomópontkészletet a megadott fürtben.</span><span class="sxs-lookup"><span data-stu-id="b7327-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="b7327-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7327-109">EXAMPLES</span></span>

### <span data-ttu-id="b7327-110">Csomópontkészlet létrehozása alapértelmezett paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="b7327-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="b7327-111">Windows Server-tároló létrehozása AKS-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="b7327-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="b7327-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7327-112">PARAMETERS</span></span>

### <span data-ttu-id="b7327-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7327-113">-ClusterName</span></span>
<span data-ttu-id="b7327-114">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b7327-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="b7327-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b7327-115">-ClusterObject</span></span>
<span data-ttu-id="b7327-116">Adja meg a csomópontkészlet létrehozásához használt fürtobjektumot.</span><span class="sxs-lookup"><span data-stu-id="b7327-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="b7327-117">-Count</span><span class="sxs-lookup"><span data-stu-id="b7327-117">-Count</span></span>
<span data-ttu-id="b7327-118">A csomópontkészletek csomópontjainak alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="b7327-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="b7327-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7327-119">-DefaultProfile</span></span>
<span data-ttu-id="b7327-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7327-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7327-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="b7327-121">-EnableAutoScaling</span></span>
<span data-ttu-id="b7327-122">Az automatikus méretarányozó engedélyezése</span><span class="sxs-lookup"><span data-stu-id="b7327-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="b7327-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b7327-123">-Force</span></span>
<span data-ttu-id="b7327-124">Csomópontkészlet létrehozása még akkor is, ha már létezik</span><span class="sxs-lookup"><span data-stu-id="b7327-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="b7327-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="b7327-125">-KubernetesVersion</span></span>
<span data-ttu-id="b7327-126">A fürt létrehozásához használt Kuternetes-verzió.</span><span class="sxs-lookup"><span data-stu-id="b7327-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="b7327-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b7327-127">-MaxCount</span></span>
<span data-ttu-id="b7327-128">Az automatikus méretezés csomópontjainak maximális száma</span><span class="sxs-lookup"><span data-stu-id="b7327-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="b7327-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="b7327-129">-MaxPodCount</span></span>
<span data-ttu-id="b7327-130">A csomóponton futtatható podok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b7327-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="b7327-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="b7327-131">-MinCount</span></span>
<span data-ttu-id="b7327-132">Az automatikus méretezés csomópontjainak minimális száma.</span><span class="sxs-lookup"><span data-stu-id="b7327-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="b7327-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b7327-133">-Name</span></span>
<span data-ttu-id="b7327-134">A csomópontkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="b7327-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="b7327-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="b7327-135">-OsDiskSize</span></span>
<span data-ttu-id="b7327-136">A csomópontkészletek csomópontjainak alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="b7327-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="b7327-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="b7327-137">-OsType</span></span>
<span data-ttu-id="b7327-138">Az operációs rendszer típusának megadásához használt OsType.</span><span class="sxs-lookup"><span data-stu-id="b7327-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="b7327-139">Válasszon a Linux és a Windows rendszer közül.</span><span class="sxs-lookup"><span data-stu-id="b7327-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="b7327-140">Alapértelmezés szerint Linux.</span><span class="sxs-lookup"><span data-stu-id="b7327-140">Default to Linux.</span></span>

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

### <span data-ttu-id="b7327-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7327-141">-ResourceGroupName</span></span>
<span data-ttu-id="b7327-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7327-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7327-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7327-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="b7327-144">ScaleSetEvictionPolicy, amely az alacsony prioritású virtuális gép méretezési beállítása során a kiviction házirend megadására használható.</span><span class="sxs-lookup"><span data-stu-id="b7327-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="b7327-145">Alapértelmezett törlés.</span><span class="sxs-lookup"><span data-stu-id="b7327-145">Default to Delete.</span></span>

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

### <span data-ttu-id="b7327-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="b7327-146">-ScaleSetPriority</span></span>
<span data-ttu-id="b7327-147">ScaleSetPriority, amely a virtuális gépi méretezéskészlet prioritásának megadására használható.</span><span class="sxs-lookup"><span data-stu-id="b7327-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="b7327-148">Alapértelmezés szerint normál.</span><span class="sxs-lookup"><span data-stu-id="b7327-148">Default to regular.</span></span>

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

### <span data-ttu-id="b7327-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="b7327-149">-VmSetType</span></span>
<span data-ttu-id="b7327-150">A csomópontkészletek típusait jelöli.</span><span class="sxs-lookup"><span data-stu-id="b7327-150">Represents types of an node pool.</span></span>
<span data-ttu-id="b7327-151">Lehetséges értékek: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="b7327-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="b7327-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="b7327-152">-VmSize</span></span>
<span data-ttu-id="b7327-153">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="b7327-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="b7327-154">Az alapértelmezett érték Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="b7327-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="b7327-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="b7327-155">-VnetSubnetID</span></span>
<span data-ttu-id="b7327-156">A VNet-alhálózati azonosító megadja a VNet alhálózati azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="b7327-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="b7327-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7327-157">-Confirm</span></span>
<span data-ttu-id="b7327-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7327-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7327-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7327-159">-WhatIf</span></span>
<span data-ttu-id="b7327-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7327-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7327-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7327-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7327-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7327-162">CommonParameters</span></span>
<span data-ttu-id="b7327-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7327-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7327-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7327-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7327-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7327-165">INPUTS</span></span>

### <span data-ttu-id="b7327-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b7327-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b7327-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7327-167">OUTPUTS</span></span>

### <span data-ttu-id="b7327-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="b7327-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="b7327-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7327-169">NOTES</span></span>

## <span data-ttu-id="b7327-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7327-170">RELATED LINKS</span></span>
