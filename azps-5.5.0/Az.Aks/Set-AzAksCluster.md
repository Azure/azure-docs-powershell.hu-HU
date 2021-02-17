---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205911"
---
# <span data-ttu-id="cae8c-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="cae8c-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="cae8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae8c-102">SYNOPSIS</span></span>
<span data-ttu-id="cae8c-103">Felügyelt Kutbernetes-fürt frissítése vagy létrehozása.</span><span class="sxs-lookup"><span data-stu-id="cae8c-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cae8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cae8c-104">SYNTAX</span></span>

### <span data-ttu-id="cae8c-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cae8c-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae8c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cae8c-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae8c-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cae8c-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae8c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cae8c-108">DESCRIPTION</span></span>
<span data-ttu-id="cae8c-109">Felügyelt Kutbernetes-fürt frissítése vagy létrehozása.</span><span class="sxs-lookup"><span data-stu-id="cae8c-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cae8c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cae8c-110">EXAMPLES</span></span>

### <span data-ttu-id="cae8c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cae8c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="cae8c-112">Állítsa be a Kubanetes-fürt csomópontjainak számát 5-re.</span><span class="sxs-lookup"><span data-stu-id="cae8c-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="cae8c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae8c-113">PARAMETERS</span></span>

### <span data-ttu-id="cae8c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cae8c-114">-AsJob</span></span>
<span data-ttu-id="cae8c-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cae8c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cae8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae8c-116">-DefaultProfile</span></span>
<span data-ttu-id="cae8c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cae8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cae8c-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="cae8c-118">-DnsNamePrefix</span></span>
<span data-ttu-id="cae8c-119">A fürt DNS-névelőtagja.</span><span class="sxs-lookup"><span data-stu-id="cae8c-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="cae8c-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="cae8c-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="cae8c-121">Az automatikus méretarányozó engedélyezése</span><span class="sxs-lookup"><span data-stu-id="cae8c-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="cae8c-122">-Id</span><span class="sxs-lookup"><span data-stu-id="cae8c-122">-Id</span></span>
<span data-ttu-id="cae8c-123">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="cae8c-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="cae8c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cae8c-124">-InputObject</span></span>
<span data-ttu-id="cae8c-125">EGY PSKubernetesCluster-objektum, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="cae8c-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="cae8c-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="cae8c-126">-KubernetesVersion</span></span>
<span data-ttu-id="cae8c-127">A fürt létrehozásához használt Kuternetes-verzió.</span><span class="sxs-lookup"><span data-stu-id="cae8c-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="cae8c-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="cae8c-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="cae8c-129">A Linux virtuális gépek felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="cae8c-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="cae8c-130">-Location</span><span class="sxs-lookup"><span data-stu-id="cae8c-130">-Location</span></span>
<span data-ttu-id="cae8c-131">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="cae8c-131">Azure location for the cluster.</span></span>
<span data-ttu-id="cae8c-132">Az alapértelmezett érték az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="cae8c-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="cae8c-133">-Name</span><span class="sxs-lookup"><span data-stu-id="cae8c-133">-Name</span></span>
<span data-ttu-id="cae8c-134">Kutbernetes felügyelt fürt neve.</span><span class="sxs-lookup"><span data-stu-id="cae8c-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="cae8c-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="cae8c-135">-NodeCount</span></span>
<span data-ttu-id="cae8c-136">A csomópontkészletek csomópontjainak alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="cae8c-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="cae8c-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="cae8c-137">-NodeMaxCount</span></span>
<span data-ttu-id="cae8c-138">Az automatikus méretezés csomópontjainak maximális száma</span><span class="sxs-lookup"><span data-stu-id="cae8c-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="cae8c-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="cae8c-139">-NodeMinCount</span></span>
<span data-ttu-id="cae8c-140">Az automatikus méretezés csomópontjainak minimális száma.</span><span class="sxs-lookup"><span data-stu-id="cae8c-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="cae8c-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="cae8c-141">-NodeName</span></span>
<span data-ttu-id="cae8c-142">Az ügynökkészlet-profil egyedi neve az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="cae8c-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="cae8c-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="cae8c-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="cae8c-144">A csomópontkészletek csomópontjainak alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="cae8c-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="cae8c-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="cae8c-145">-NodePoolMode</span></span>
<span data-ttu-id="cae8c-146">A NodePoolMode egy csomópontkészlet módját képviseli.</span><span class="sxs-lookup"><span data-stu-id="cae8c-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="cae8c-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="cae8c-147">-NodeVmSize</span></span>
<span data-ttu-id="cae8c-148">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="cae8c-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="cae8c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae8c-149">-ResourceGroupName</span></span>
<span data-ttu-id="cae8c-150">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cae8c-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="cae8c-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="cae8c-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="cae8c-152">Az AAD-alkalmazáshoz/szolgáltatásnévhez társított ügyfélazonosító és ügyfélnév.</span><span class="sxs-lookup"><span data-stu-id="cae8c-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="cae8c-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="cae8c-153">-SshKeyValue</span></span>
<span data-ttu-id="cae8c-154">SSH-kulcsfájl értéke vagy elérési útja.</span><span class="sxs-lookup"><span data-stu-id="cae8c-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="cae8c-155">Alapértelmezés szerint {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="cae8c-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="cae8c-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="cae8c-156">-Tag</span></span>
<span data-ttu-id="cae8c-157">Az erőforrásra alkalmazandó címkék</span><span class="sxs-lookup"><span data-stu-id="cae8c-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="cae8c-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cae8c-158">-Confirm</span></span>
<span data-ttu-id="cae8c-159">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cae8c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae8c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae8c-160">-WhatIf</span></span>
<span data-ttu-id="cae8c-161">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cae8c-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae8c-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cae8c-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae8c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae8c-163">CommonParameters</span></span>
<span data-ttu-id="cae8c-164">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae8c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae8c-165">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cae8c-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae8c-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cae8c-166">INPUTS</span></span>

### <span data-ttu-id="cae8c-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cae8c-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="cae8c-168">System.String</span><span class="sxs-lookup"><span data-stu-id="cae8c-168">System.String</span></span>

## <span data-ttu-id="cae8c-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cae8c-169">OUTPUTS</span></span>

### <span data-ttu-id="cae8c-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cae8c-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="cae8c-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cae8c-171">NOTES</span></span>

## <span data-ttu-id="cae8c-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cae8c-172">RELATED LINKS</span></span>
