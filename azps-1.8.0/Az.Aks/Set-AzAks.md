---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665745"
---
# <span data-ttu-id="68fe5-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="68fe5-101">Set-AzAks</span></span>

## <span data-ttu-id="68fe5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="68fe5-103">Felügyelt Kubernetes-fürtöt frissít vagy hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="68fe5-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="68fe5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68fe5-104">SYNTAX</span></span>

### <span data-ttu-id="68fe5-105">defaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68fe5-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fe5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68fe5-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fe5-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68fe5-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68fe5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="68fe5-108">DESCRIPTION</span></span>
<span data-ttu-id="68fe5-109">Felügyelt Kubernetes-fürtöt frissít vagy hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="68fe5-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="68fe5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="68fe5-110">EXAMPLES</span></span>

### <span data-ttu-id="68fe5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68fe5-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="68fe5-112">Állítsa be a csomópontok számát az Kubernetes-fürtben az 5 értékre.</span><span class="sxs-lookup"><span data-stu-id="68fe5-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="68fe5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68fe5-113">PARAMETERS</span></span>

### <span data-ttu-id="68fe5-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="68fe5-114">-AdminUserName</span></span>
<span data-ttu-id="68fe5-115">A Linux virtuális gépek felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="68fe5-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="68fe5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68fe5-116">-AsJob</span></span>
<span data-ttu-id="68fe5-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="68fe5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68fe5-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="68fe5-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="68fe5-119">Az ügyfél azonosítója és az ügyfél titka az AAD-alkalmazással és-szolgáltatóval társítva.</span><span class="sxs-lookup"><span data-stu-id="68fe5-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="68fe5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fe5-120">-DefaultProfile</span></span>
<span data-ttu-id="68fe5-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68fe5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68fe5-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="68fe5-122">-DnsNamePrefix</span></span>
<span data-ttu-id="68fe5-123">A fürt DNS-név előtagja.</span><span class="sxs-lookup"><span data-stu-id="68fe5-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="68fe5-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="68fe5-124">-Id</span></span>
<span data-ttu-id="68fe5-125">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="68fe5-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="68fe5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68fe5-126">-InputObject</span></span>
<span data-ttu-id="68fe5-127">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="68fe5-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="68fe5-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="68fe5-128">-KubernetesVersion</span></span>
<span data-ttu-id="68fe5-129">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="68fe5-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="68fe5-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="68fe5-130">-Location</span></span>
<span data-ttu-id="68fe5-131">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="68fe5-131">Azure location for the cluster.</span></span>
<span data-ttu-id="68fe5-132">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="68fe5-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="68fe5-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68fe5-133">-Name</span></span>
<span data-ttu-id="68fe5-134">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="68fe5-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="68fe5-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="68fe5-135">-NodeCount</span></span>
<span data-ttu-id="68fe5-136">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="68fe5-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="68fe5-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="68fe5-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="68fe5-138">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="68fe5-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="68fe5-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="68fe5-139">-NodeVmSize</span></span>
<span data-ttu-id="68fe5-140">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="68fe5-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="68fe5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fe5-141">-ResourceGroupName</span></span>
<span data-ttu-id="68fe5-142">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="68fe5-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="68fe5-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="68fe5-143">-SshKeyValue</span></span>
<span data-ttu-id="68fe5-144">Az SSH-kulcs vagy a kulcsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="68fe5-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="68fe5-145">Az alapértelmezett érték a {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="68fe5-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="68fe5-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="68fe5-146">-Tag</span></span>
<span data-ttu-id="68fe5-147">Az erőforrásra alkalmazandó Címkék</span><span class="sxs-lookup"><span data-stu-id="68fe5-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="68fe5-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68fe5-148">-Confirm</span></span>
<span data-ttu-id="68fe5-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68fe5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68fe5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68fe5-150">-WhatIf</span></span>
<span data-ttu-id="68fe5-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68fe5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68fe5-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68fe5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68fe5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fe5-153">CommonParameters</span></span>
<span data-ttu-id="68fe5-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68fe5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fe5-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fe5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fe5-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68fe5-156">INPUTS</span></span>

### <span data-ttu-id="68fe5-157">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="68fe5-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="68fe5-158">System. String</span><span class="sxs-lookup"><span data-stu-id="68fe5-158">System.String</span></span>

## <span data-ttu-id="68fe5-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68fe5-159">OUTPUTS</span></span>

### <span data-ttu-id="68fe5-160">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="68fe5-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="68fe5-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68fe5-161">NOTES</span></span>

## <span data-ttu-id="68fe5-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68fe5-162">RELATED LINKS</span></span>
