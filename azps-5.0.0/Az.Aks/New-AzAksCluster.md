---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187111"
---
# <span data-ttu-id="dea0a-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="dea0a-101">New-AzAksCluster</span></span>

## <span data-ttu-id="dea0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dea0a-102">SYNOPSIS</span></span>
<span data-ttu-id="dea0a-103">Hozzon létre egy új felügyelt Kubernetes-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="dea0a-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="dea0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dea0a-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dea0a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dea0a-105">DESCRIPTION</span></span>

<span data-ttu-id="dea0a-106">Hozzon létre egy új Azure Kubernetes-szolgáltatási (ak-os) fürtöt.</span><span class="sxs-lookup"><span data-stu-id="dea0a-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="dea0a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dea0a-107">EXAMPLES</span></span>

### <span data-ttu-id="dea0a-108">Az új ak az alapértelmezett params.</span><span class="sxs-lookup"><span data-stu-id="dea0a-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="dea0a-109">Windows Server-tároló létrehozása AK-ra</span><span class="sxs-lookup"><span data-stu-id="dea0a-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="dea0a-110">Ha a Windows Server-tárolót AK-ra szeretné létrehozni, legalább négy következő paramétert kell megadnia az AK-hoz való létrehozásakor, valamint a és a `NetworkPlugin` `NodeVmSetType` és a és a be és a be `azure` és `VirtualMachineScaleSets` az érték</span><span class="sxs-lookup"><span data-stu-id="dea0a-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="dea0a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dea0a-111">PARAMETERS</span></span>

### <span data-ttu-id="dea0a-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="dea0a-112">-AcrNameToAttach</span></span>
<span data-ttu-id="dea0a-113">Adja meg a megadott ACR – AK-os acrpull "" szerepét (például myacr).</span><span class="sxs-lookup"><span data-stu-id="dea0a-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="dea0a-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="dea0a-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="dea0a-115">A fürtök létrehozásakor engedélyezni kívánt bővítmények nevei.</span><span class="sxs-lookup"><span data-stu-id="dea0a-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dea0a-116">-AsJob</span></span>
<span data-ttu-id="dea0a-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dea0a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dea0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea0a-118">-DefaultProfile</span></span>
<span data-ttu-id="dea0a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dea0a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea0a-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="dea0a-120">-DnsNamePrefix</span></span>
<span data-ttu-id="dea0a-121">A fürt DNS-név előtagja.</span><span class="sxs-lookup"><span data-stu-id="dea0a-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="dea0a-122">A hossznak <= 9, ha a felhasználók Windows-tároló hozzáadását tervezik meg.</span><span class="sxs-lookup"><span data-stu-id="dea0a-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="dea0a-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="dea0a-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="dea0a-124">Szeretné-e engedélyezni az automatikus méretezést?</span><span class="sxs-lookup"><span data-stu-id="dea0a-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="dea0a-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="dea0a-125">-EnableRbac</span></span>
<span data-ttu-id="dea0a-126">Szeretné-e engedélyezni a Kubernetes Role-Based az Accessben</span><span class="sxs-lookup"><span data-stu-id="dea0a-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="dea0a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="dea0a-127">-Force</span></span>
<span data-ttu-id="dea0a-128">Fürt létrehozása akkor is, ha már létezik</span><span class="sxs-lookup"><span data-stu-id="dea0a-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="dea0a-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="dea0a-129">-GenerateSshKey</span></span>
<span data-ttu-id="dea0a-130">Az SSH-kulcs létrehozása a {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="dea0a-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="dea0a-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="dea0a-131">-KubernetesVersion</span></span>
<span data-ttu-id="dea0a-132">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="dea0a-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="dea0a-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="dea0a-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="dea0a-134">A Linux virtuális gépek felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="dea0a-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="dea0a-135">-LoadBalancerSku</span></span>
<span data-ttu-id="dea0a-136">A felügyelt fürthöz tartozó terheléselosztó SKU.</span><span class="sxs-lookup"><span data-stu-id="dea0a-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="dea0a-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="dea0a-137">-Location</span></span>
<span data-ttu-id="dea0a-138">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="dea0a-138">Azure location for the cluster.</span></span>
<span data-ttu-id="dea0a-139">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="dea0a-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="dea0a-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dea0a-140">-Name</span></span>
<span data-ttu-id="dea0a-141">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="dea0a-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="dea0a-142">-NetworkPlugin</span></span>
<span data-ttu-id="dea0a-143">A Kubernetes-hálózat építésére szolgáló hálózati bővítmény.</span><span class="sxs-lookup"><span data-stu-id="dea0a-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="dea0a-144">-NodeCount</span></span>
<span data-ttu-id="dea0a-145">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="dea0a-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="dea0a-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="dea0a-146">-NodeMaxCount</span></span>
<span data-ttu-id="dea0a-147">Csomópontok maximális száma automatikus méretezéshez</span><span class="sxs-lookup"><span data-stu-id="dea0a-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="dea0a-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="dea0a-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="dea0a-149">A csomópontokon futtatható hüvelyek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="dea0a-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="dea0a-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="dea0a-150">-NodeMinCount</span></span>
<span data-ttu-id="dea0a-151">Az automatikus méretezéshez szükséges csomópontok minimális száma</span><span class="sxs-lookup"><span data-stu-id="dea0a-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="dea0a-152">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="dea0a-152">-NodeName</span></span>
<span data-ttu-id="dea0a-153">Az ügynök-készlet profiljának egyedi neve az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="dea0a-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="dea0a-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="dea0a-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="dea0a-155">Az operációs rendszer lemezének mérete GB-ban a Node Pool minden csomópontja számára.</span><span class="sxs-lookup"><span data-stu-id="dea0a-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="dea0a-156">Minimum 30 GB.</span><span class="sxs-lookup"><span data-stu-id="dea0a-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="dea0a-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="dea0a-157">-NodePoolMode</span></span>
<span data-ttu-id="dea0a-158">A NodePoolMode a csomópontok készletének a módját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="dea0a-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="dea0a-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="dea0a-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="dea0a-160">A kis prioritású virtuális gép ScaleSetEvictionPolicy a kilakoltatási házirend megadására használható.</span><span class="sxs-lookup"><span data-stu-id="dea0a-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="dea0a-161">Alapértelmezés szerint törölni kell.</span><span class="sxs-lookup"><span data-stu-id="dea0a-161">Default to Delete.</span></span>

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

### <span data-ttu-id="dea0a-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="dea0a-162">-NodeSetPriority</span></span>
<span data-ttu-id="dea0a-163">A virtuálisgép-készlet prioritásának megadására szolgáló ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="dea0a-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="dea0a-164">Alapértelmezés szerint normál.</span><span class="sxs-lookup"><span data-stu-id="dea0a-164">Default to regular.</span></span>

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

### <span data-ttu-id="dea0a-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="dea0a-165">-NodeVmSetType</span></span>
<span data-ttu-id="dea0a-166">A AgentPoolType az ügynök-készlet típusait jelöli.</span><span class="sxs-lookup"><span data-stu-id="dea0a-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="dea0a-167">A lehetséges értékek a következők: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="dea0a-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="dea0a-168">-NodeVmSize</span></span>
<span data-ttu-id="dea0a-169">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="dea0a-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="dea0a-170">Az alapértelmezett érték Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="dea0a-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="dea0a-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="dea0a-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="dea0a-172">A VNet a VNet alhálózati azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dea0a-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="dea0a-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dea0a-173">-ResourceGroupName</span></span>
<span data-ttu-id="dea0a-174">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="dea0a-174">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="dea0a-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="dea0a-176">Az ügyfél azonosítója és az ügyfél titka az AAD-alkalmazással és-szolgáltatóval társítva.</span><span class="sxs-lookup"><span data-stu-id="dea0a-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="dea0a-177">-SshKeyValue</span></span>
<span data-ttu-id="dea0a-178">Az SSH-kulcs vagy a kulcsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="dea0a-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="dea0a-179">Az alapértelmezett érték a {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="dea0a-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="dea0a-180">-SubnetName</span></span>
<span data-ttu-id="dea0a-181">A VirtualNode addon alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="dea0a-181">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-182">-Címke</span><span class="sxs-lookup"><span data-stu-id="dea0a-182">-Tag</span></span>
<span data-ttu-id="dea0a-183">Az erőforrásra alkalmazandó Címkék</span><span class="sxs-lookup"><span data-stu-id="dea0a-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="dea0a-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="dea0a-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="dea0a-185">A Windows VM-hez használható rendszergazdai Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="dea0a-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="dea0a-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="dea0a-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="dea0a-187">A Windows VMs-szolgáltatáshoz használt rendszergazdai jelszónak legalább 12-nek kell lennie, amely legalább egy kisbetűs karaktert tartalmaz, azaz `[a-z]` egy `[A-Z]` és egy speciális karaktert `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="dea0a-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="dea0a-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="dea0a-189">Az addon figyelési munkaterületének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dea0a-189">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea0a-190">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dea0a-190">-Confirm</span></span>
<span data-ttu-id="dea0a-191">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dea0a-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dea0a-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea0a-192">-WhatIf</span></span>
<span data-ttu-id="dea0a-193">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dea0a-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dea0a-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dea0a-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dea0a-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea0a-195">CommonParameters</span></span>
<span data-ttu-id="dea0a-196">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dea0a-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea0a-197">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dea0a-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea0a-198">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea0a-198">INPUTS</span></span>

### <span data-ttu-id="dea0a-199">Nincs</span><span class="sxs-lookup"><span data-stu-id="dea0a-199">None</span></span>

## <span data-ttu-id="dea0a-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea0a-200">OUTPUTS</span></span>

### <span data-ttu-id="dea0a-201">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="dea0a-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="dea0a-202">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dea0a-202">NOTES</span></span>

## <span data-ttu-id="dea0a-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dea0a-203">RELATED LINKS</span></span>
