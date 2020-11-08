---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 04778d2aef4bbafe1638e8ab1971f626303c7be5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011306"
---
# <span data-ttu-id="067c7-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="067c7-101">Set-AzAks</span></span>

## <span data-ttu-id="067c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="067c7-102">SYNOPSIS</span></span>
<span data-ttu-id="067c7-103">Felügyelt Kubernetes-fürtöt frissít vagy hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="067c7-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="067c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="067c7-104">SYNTAX</span></span>

### <span data-ttu-id="067c7-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="067c7-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="067c7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="067c7-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="067c7-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="067c7-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="067c7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="067c7-108">DESCRIPTION</span></span>
<span data-ttu-id="067c7-109">Felügyelt Kubernetes-fürtöt frissít vagy hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="067c7-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="067c7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="067c7-110">EXAMPLES</span></span>

### <span data-ttu-id="067c7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="067c7-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="067c7-112">Állítsa be a csomópontok számát az Kubernetes-fürtben az 5 értékre.</span><span class="sxs-lookup"><span data-stu-id="067c7-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="067c7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="067c7-113">PARAMETERS</span></span>

### <span data-ttu-id="067c7-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="067c7-114">-AdminUserName</span></span>
<span data-ttu-id="067c7-115">A Linux virtuális gépek felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="067c7-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="067c7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="067c7-116">-AsJob</span></span>
<span data-ttu-id="067c7-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="067c7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="067c7-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="067c7-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="067c7-119">Az ügyfél azonosítója és az ügyfél titka az AAD-alkalmazással és-szolgáltatóval társítva.</span><span class="sxs-lookup"><span data-stu-id="067c7-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="067c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067c7-120">-DefaultProfile</span></span>
<span data-ttu-id="067c7-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="067c7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="067c7-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="067c7-122">-DnsNamePrefix</span></span>
<span data-ttu-id="067c7-123">A fürt DNS-név előtagja.</span><span class="sxs-lookup"><span data-stu-id="067c7-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="067c7-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="067c7-124">-Id</span></span>
<span data-ttu-id="067c7-125">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="067c7-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="067c7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="067c7-126">-InputObject</span></span>
<span data-ttu-id="067c7-127">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="067c7-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="067c7-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="067c7-128">-KubernetesVersion</span></span>
<span data-ttu-id="067c7-129">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="067c7-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="067c7-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="067c7-130">-Location</span></span>
<span data-ttu-id="067c7-131">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="067c7-131">Azure location for the cluster.</span></span>
<span data-ttu-id="067c7-132">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="067c7-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="067c7-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="067c7-133">-Name</span></span>
<span data-ttu-id="067c7-134">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="067c7-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="067c7-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="067c7-135">-NodeCount</span></span>
<span data-ttu-id="067c7-136">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="067c7-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="067c7-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="067c7-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="067c7-138">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="067c7-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="067c7-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="067c7-139">-NodeVmSize</span></span>
<span data-ttu-id="067c7-140">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="067c7-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="067c7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="067c7-141">-ResourceGroupName</span></span>
<span data-ttu-id="067c7-142">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="067c7-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="067c7-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="067c7-143">-SshKeyValue</span></span>
<span data-ttu-id="067c7-144">Az SSH-kulcs vagy a kulcsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="067c7-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="067c7-145">Az alapértelmezett érték a {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="067c7-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="067c7-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="067c7-146">-Tag</span></span>
<span data-ttu-id="067c7-147">Az erőforrásra alkalmazandó Címkék</span><span class="sxs-lookup"><span data-stu-id="067c7-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="067c7-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="067c7-148">-Confirm</span></span>
<span data-ttu-id="067c7-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="067c7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="067c7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="067c7-150">-WhatIf</span></span>
<span data-ttu-id="067c7-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="067c7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="067c7-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="067c7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="067c7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067c7-153">CommonParameters</span></span>
<span data-ttu-id="067c7-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="067c7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067c7-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="067c7-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067c7-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="067c7-156">INPUTS</span></span>

### <span data-ttu-id="067c7-157">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="067c7-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="067c7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="067c7-158">System.String</span></span>

## <span data-ttu-id="067c7-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="067c7-159">OUTPUTS</span></span>

### <span data-ttu-id="067c7-160">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="067c7-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="067c7-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="067c7-161">NOTES</span></span>

## <span data-ttu-id="067c7-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="067c7-162">RELATED LINKS</span></span>
