---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469134"
---
# <span data-ttu-id="34f1d-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="34f1d-101">New-AzAksCluster</span></span>

## <span data-ttu-id="34f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="34f1d-103">Hozzon létre egy új felügyelt Kuternetes-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="34f1d-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="34f1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="34f1d-104">SYNTAX</span></span>

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

## <span data-ttu-id="34f1d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="34f1d-105">DESCRIPTION</span></span>

<span data-ttu-id="34f1d-106">Hozzon létre egy új Azure Kuternetes Service(AKS) fürtöt.</span><span class="sxs-lookup"><span data-stu-id="34f1d-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="34f1d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="34f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="34f1d-108">Új AKS alapértelmezett paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="34f1d-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="34f1d-109">Windows Server-tároló létrehozása AKS-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="34f1d-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="34f1d-110">Ha Windows Server-tárolót hoz létre egy AKS-kiszolgálón, az AKS létrehozásakor legalább négy paramétert meg kell adnia, és meg kell adnia annak értékét, illetve `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` értékét.</span><span class="sxs-lookup"><span data-stu-id="34f1d-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="34f1d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f1d-111">PARAMETERS</span></span>

### <span data-ttu-id="34f1d-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="34f1d-112">-AcrNameToAttach</span></span>
<span data-ttu-id="34f1d-113">Adja meg a megadott ACR "acrpull" szerepkörét az AKS-szolgáltatásnévnek (pl. myacr)</span><span class="sxs-lookup"><span data-stu-id="34f1d-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="34f1d-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="34f1d-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="34f1d-115">A fürt létrehozásakor engedélyezett bővítménynevek.</span><span class="sxs-lookup"><span data-stu-id="34f1d-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="34f1d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34f1d-116">-AsJob</span></span>
<span data-ttu-id="34f1d-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="34f1d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34f1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f1d-118">-DefaultProfile</span></span>
<span data-ttu-id="34f1d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34f1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f1d-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="34f1d-120">-DnsNamePrefix</span></span>
<span data-ttu-id="34f1d-121">A fürt DNS-névelőtagja.</span><span class="sxs-lookup"><span data-stu-id="34f1d-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="34f1d-122">Ha a felhasználók windowsos tárolót terveznek hozzáadni, <= 9 hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="34f1d-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="34f1d-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="34f1d-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="34f1d-124">Az automatikus méretarányozó engedélyezése</span><span class="sxs-lookup"><span data-stu-id="34f1d-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="34f1d-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="34f1d-125">-EnableRbac</span></span>
<span data-ttu-id="34f1d-126">Engedélyezni kell-e a Role-Based Accessben</span><span class="sxs-lookup"><span data-stu-id="34f1d-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="34f1d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="34f1d-127">-Force</span></span>
<span data-ttu-id="34f1d-128">Fürt létrehozása még akkor is, ha már létezik</span><span class="sxs-lookup"><span data-stu-id="34f1d-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="34f1d-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="34f1d-129">-GenerateSshKey</span></span>
<span data-ttu-id="34f1d-130">Hozza létre az ssh kulcsfájlt a(z) {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="34f1d-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="34f1d-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="34f1d-131">-KubernetesVersion</span></span>
<span data-ttu-id="34f1d-132">A fürt létrehozásához használt Kuternetes-verzió.</span><span class="sxs-lookup"><span data-stu-id="34f1d-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="34f1d-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="34f1d-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="34f1d-134">A Linux virtuális gépek felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="34f1d-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="34f1d-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="34f1d-135">-LoadBalancerSku</span></span>
<span data-ttu-id="34f1d-136">A felügyelt fürt terheléselosztási termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="34f1d-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="34f1d-137">-Location</span><span class="sxs-lookup"><span data-stu-id="34f1d-137">-Location</span></span>
<span data-ttu-id="34f1d-138">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="34f1d-138">Azure location for the cluster.</span></span>
<span data-ttu-id="34f1d-139">Az alapértelmezett érték az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="34f1d-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="34f1d-140">-Name</span><span class="sxs-lookup"><span data-stu-id="34f1d-140">-Name</span></span>
<span data-ttu-id="34f1d-141">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="34f1d-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="34f1d-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="34f1d-142">-NetworkPlugin</span></span>
<span data-ttu-id="34f1d-143">Network plugin used for building Pluginernetes network.</span><span class="sxs-lookup"><span data-stu-id="34f1d-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="34f1d-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="34f1d-144">-NodeCount</span></span>
<span data-ttu-id="34f1d-145">A csomópontkészletek csomópontjainak alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="34f1d-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="34f1d-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="34f1d-146">-NodeMaxCount</span></span>
<span data-ttu-id="34f1d-147">Az automatikus méretezés csomópontjainak maximális száma</span><span class="sxs-lookup"><span data-stu-id="34f1d-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="34f1d-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="34f1d-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="34f1d-149">A csomóponton futtatható podok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="34f1d-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="34f1d-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="34f1d-150">-NodeMinCount</span></span>
<span data-ttu-id="34f1d-151">Az automatikus méretezés csomópontjainak minimális száma.</span><span class="sxs-lookup"><span data-stu-id="34f1d-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="34f1d-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="34f1d-152">-NodeName</span></span>
<span data-ttu-id="34f1d-153">Az ügynökkészlet-profil egyedi neve az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="34f1d-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="34f1d-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="34f1d-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="34f1d-155">A csomópontkészlet egyes csomópontjai esetén az operációs rendszer lemezének mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="34f1d-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="34f1d-156">Legalább 30 GB.</span><span class="sxs-lookup"><span data-stu-id="34f1d-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="34f1d-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="34f1d-157">-NodePoolMode</span></span>
<span data-ttu-id="34f1d-158">A NodePoolMode egy csomópontkészlet módját képviseli.</span><span class="sxs-lookup"><span data-stu-id="34f1d-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="34f1d-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="34f1d-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="34f1d-160">ScaleSetEvictionPolicy, amely az alacsony prioritású virtuális gép méretezési beállítása során a kiviction házirend megadására használható.</span><span class="sxs-lookup"><span data-stu-id="34f1d-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="34f1d-161">Alapértelmezett törlés.</span><span class="sxs-lookup"><span data-stu-id="34f1d-161">Default to Delete.</span></span>

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

### <span data-ttu-id="34f1d-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="34f1d-162">-NodeSetPriority</span></span>
<span data-ttu-id="34f1d-163">ScaleSetPriority, amely a virtuális gépi méretezéskészlet prioritásának megadására használható.</span><span class="sxs-lookup"><span data-stu-id="34f1d-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="34f1d-164">Alapértelmezés szerint normál.</span><span class="sxs-lookup"><span data-stu-id="34f1d-164">Default to regular.</span></span>

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

### <span data-ttu-id="34f1d-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="34f1d-165">-NodeVmSetType</span></span>
<span data-ttu-id="34f1d-166">Az AgentPoolType egy ügynökkészlet típusát képviseli.</span><span class="sxs-lookup"><span data-stu-id="34f1d-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="34f1d-167">Lehetséges értékek: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="34f1d-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="34f1d-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="34f1d-168">-NodeVmSize</span></span>
<span data-ttu-id="34f1d-169">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="34f1d-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="34f1d-170">Az alapértelmezett érték Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="34f1d-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="34f1d-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="34f1d-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="34f1d-172">A VNet-alhálózati azonosító megadja a VNet alhálózati azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="34f1d-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="34f1d-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f1d-173">-ResourceGroupName</span></span>
<span data-ttu-id="34f1d-174">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="34f1d-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="34f1d-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="34f1d-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="34f1d-176">Az AAD-alkalmazáshoz/szolgáltatásnévhez társított ügyfélazonosító és ügyfélnév.</span><span class="sxs-lookup"><span data-stu-id="34f1d-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="34f1d-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="34f1d-177">-SshKeyValue</span></span>
<span data-ttu-id="34f1d-178">SSH-kulcsfájl értéke vagy elérési útja.</span><span class="sxs-lookup"><span data-stu-id="34f1d-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="34f1d-179">Alapértelmezés szerint {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="34f1d-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="34f1d-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="34f1d-180">-SubnetName</span></span>
<span data-ttu-id="34f1d-181">A VirtualNode-bővítmény alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="34f1d-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="34f1d-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="34f1d-182">-Tag</span></span>
<span data-ttu-id="34f1d-183">Az erőforrásra alkalmazandó címkék</span><span class="sxs-lookup"><span data-stu-id="34f1d-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="34f1d-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="34f1d-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="34f1d-185">A Windows-virtuális gépekhez használni kívánt rendszergazdai felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="34f1d-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="34f1d-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="34f1d-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="34f1d-187">A Windows-alapú virtuális gépekhez használható rendszergazdai jelszónak legalább 12 hosszúságúnak kell lennie, és legalább egy kisbetűt ( egy és egy speciális karaktert ) `[a-z]` `[A-Z]` `[!@#$%^&_()]` tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="34f1d-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="34f1d-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="34f1d-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="34f1d-189">A Figyelés bővítmény munkaterületének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="34f1d-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="34f1d-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34f1d-190">-Confirm</span></span>
<span data-ttu-id="34f1d-191">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="34f1d-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f1d-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f1d-192">-WhatIf</span></span>
<span data-ttu-id="34f1d-193">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="34f1d-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f1d-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34f1d-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f1d-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f1d-195">CommonParameters</span></span>
<span data-ttu-id="34f1d-196">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f1d-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f1d-197">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34f1d-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f1d-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34f1d-198">INPUTS</span></span>

### <span data-ttu-id="34f1d-199">Nincs</span><span class="sxs-lookup"><span data-stu-id="34f1d-199">None</span></span>

## <span data-ttu-id="34f1d-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34f1d-200">OUTPUTS</span></span>

### <span data-ttu-id="34f1d-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="34f1d-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="34f1d-202">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="34f1d-202">NOTES</span></span>

## <span data-ttu-id="34f1d-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34f1d-203">RELATED LINKS</span></span>
