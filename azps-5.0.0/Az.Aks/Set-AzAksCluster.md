---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187103"
---
# <span data-ttu-id="9039f-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="9039f-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="9039f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9039f-102">SYNOPSIS</span></span>
<span data-ttu-id="9039f-103">Felügyelt Kubernetes-fürtöt frissít vagy hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="9039f-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9039f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9039f-104">SYNTAX</span></span>

### <span data-ttu-id="9039f-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9039f-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9039f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9039f-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9039f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9039f-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9039f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9039f-108">DESCRIPTION</span></span>
<span data-ttu-id="9039f-109">Felügyelt Kubernetes-fürtöt frissít vagy hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="9039f-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9039f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9039f-110">EXAMPLES</span></span>

### <span data-ttu-id="9039f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9039f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="9039f-112">Állítsa be a csomópontok számát az Kubernetes-fürtben az 5 értékre.</span><span class="sxs-lookup"><span data-stu-id="9039f-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="9039f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9039f-113">PARAMETERS</span></span>

### <span data-ttu-id="9039f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9039f-114">-AsJob</span></span>
<span data-ttu-id="9039f-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9039f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9039f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9039f-116">-DefaultProfile</span></span>
<span data-ttu-id="9039f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9039f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9039f-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="9039f-118">-DnsNamePrefix</span></span>
<span data-ttu-id="9039f-119">A fürt DNS-név előtagja.</span><span class="sxs-lookup"><span data-stu-id="9039f-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="9039f-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="9039f-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="9039f-121">Szeretné-e engedélyezni az automatikus méretezést?</span><span class="sxs-lookup"><span data-stu-id="9039f-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="9039f-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9039f-122">-Id</span></span>
<span data-ttu-id="9039f-123">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="9039f-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9039f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9039f-124">-InputObject</span></span>
<span data-ttu-id="9039f-125">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9039f-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9039f-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="9039f-126">-KubernetesVersion</span></span>
<span data-ttu-id="9039f-127">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="9039f-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="9039f-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="9039f-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="9039f-129">A Linux virtuális gépek felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="9039f-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="9039f-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="9039f-130">-Location</span></span>
<span data-ttu-id="9039f-131">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="9039f-131">Azure location for the cluster.</span></span>
<span data-ttu-id="9039f-132">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="9039f-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="9039f-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9039f-133">-Name</span></span>
<span data-ttu-id="9039f-134">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="9039f-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9039f-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9039f-135">-NodeCount</span></span>
<span data-ttu-id="9039f-136">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="9039f-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="9039f-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="9039f-137">-NodeMaxCount</span></span>
<span data-ttu-id="9039f-138">Csomópontok maximális száma automatikus méretezéshez</span><span class="sxs-lookup"><span data-stu-id="9039f-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="9039f-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="9039f-139">-NodeMinCount</span></span>
<span data-ttu-id="9039f-140">Az automatikus méretezéshez szükséges csomópontok minimális száma</span><span class="sxs-lookup"><span data-stu-id="9039f-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="9039f-141">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="9039f-141">-NodeName</span></span>
<span data-ttu-id="9039f-142">Az ügynök-készlet profiljának egyedi neve az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="9039f-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="9039f-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="9039f-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="9039f-144">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="9039f-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="9039f-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="9039f-145">-NodePoolMode</span></span>
<span data-ttu-id="9039f-146">A NodePoolMode a csomópontok készletének a módját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9039f-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="9039f-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="9039f-147">-NodeVmSize</span></span>
<span data-ttu-id="9039f-148">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="9039f-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="9039f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9039f-149">-ResourceGroupName</span></span>
<span data-ttu-id="9039f-150">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9039f-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9039f-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="9039f-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="9039f-152">Az ügyfél azonosítója és az ügyfél titka az AAD-alkalmazással és-szolgáltatóval társítva.</span><span class="sxs-lookup"><span data-stu-id="9039f-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9039f-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="9039f-153">-SshKeyValue</span></span>
<span data-ttu-id="9039f-154">Az SSH-kulcs vagy a kulcsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9039f-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="9039f-155">Az alapértelmezett érték a {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="9039f-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="9039f-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="9039f-156">-Tag</span></span>
<span data-ttu-id="9039f-157">Az erőforrásra alkalmazandó Címkék</span><span class="sxs-lookup"><span data-stu-id="9039f-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="9039f-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9039f-158">-Confirm</span></span>
<span data-ttu-id="9039f-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9039f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9039f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9039f-160">-WhatIf</span></span>
<span data-ttu-id="9039f-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9039f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9039f-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9039f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9039f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9039f-163">CommonParameters</span></span>
<span data-ttu-id="9039f-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9039f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9039f-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9039f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9039f-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9039f-166">INPUTS</span></span>

### <span data-ttu-id="9039f-167">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9039f-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="9039f-168">System. String</span><span class="sxs-lookup"><span data-stu-id="9039f-168">System.String</span></span>

## <span data-ttu-id="9039f-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9039f-169">OUTPUTS</span></span>

### <span data-ttu-id="9039f-170">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9039f-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="9039f-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9039f-171">NOTES</span></span>

## <span data-ttu-id="9039f-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9039f-172">RELATED LINKS</span></span>
