---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665746"
---
# <span data-ttu-id="43744-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="43744-101">New-AzAks</span></span>

## <span data-ttu-id="43744-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43744-102">SYNOPSIS</span></span>
<span data-ttu-id="43744-103">Hozzon létre egy új felügyelt Kubernetes-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="43744-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="43744-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43744-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43744-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43744-105">DESCRIPTION</span></span>

<span data-ttu-id="43744-106">Hozzon létre egy új felügyelt Kubernetes-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="43744-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="43744-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43744-107">EXAMPLES</span></span>

### <span data-ttu-id="43744-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43744-108">Example 1</span></span>

<span data-ttu-id="43744-109">Új felügyelt Kubernetes-fürtöt hozhat létre alapértelmezett params.</span><span class="sxs-lookup"><span data-stu-id="43744-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="43744-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43744-110">PARAMETERS</span></span>

### <span data-ttu-id="43744-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="43744-111">-AdminUserName</span></span>
<span data-ttu-id="43744-112">A Linux virtuális gépek felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="43744-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="43744-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43744-113">-AsJob</span></span>
<span data-ttu-id="43744-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43744-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43744-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="43744-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="43744-116">Az ügyfél azonosítója és az ügyfél titka az AAD-alkalmazással és-szolgáltatóval társítva.</span><span class="sxs-lookup"><span data-stu-id="43744-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="43744-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43744-117">-DefaultProfile</span></span>
<span data-ttu-id="43744-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43744-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43744-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="43744-119">-DnsNamePrefix</span></span>
<span data-ttu-id="43744-120">A fürt DNS-név előtagja.</span><span class="sxs-lookup"><span data-stu-id="43744-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="43744-121">-Force</span><span class="sxs-lookup"><span data-stu-id="43744-121">-Force</span></span>
<span data-ttu-id="43744-122">Fürt létrehozása akkor is, ha már létezik</span><span class="sxs-lookup"><span data-stu-id="43744-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="43744-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="43744-123">-KubernetesVersion</span></span>
<span data-ttu-id="43744-124">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="43744-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="43744-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="43744-125">-Location</span></span>
<span data-ttu-id="43744-126">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="43744-126">Azure location for the cluster.</span></span>
<span data-ttu-id="43744-127">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="43744-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="43744-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43744-128">-Name</span></span>
<span data-ttu-id="43744-129">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="43744-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="43744-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="43744-130">-NodeCount</span></span>
<span data-ttu-id="43744-131">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="43744-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="43744-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="43744-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="43744-133">Az operációs rendszer lemezének mérete GB-ban a Node Pool minden csomópontja számára.</span><span class="sxs-lookup"><span data-stu-id="43744-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="43744-134">Minimum 30 GB.</span><span class="sxs-lookup"><span data-stu-id="43744-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="43744-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="43744-135">-NodeVmSize</span></span>
<span data-ttu-id="43744-136">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="43744-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="43744-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43744-137">-ResourceGroupName</span></span>
<span data-ttu-id="43744-138">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="43744-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="43744-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="43744-139">-SshKeyValue</span></span>
<span data-ttu-id="43744-140">Az SSH-kulcs vagy a kulcsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="43744-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="43744-141">Az alapértelmezett érték a {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="43744-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="43744-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="43744-142">-Tag</span></span>
<span data-ttu-id="43744-143">Az erőforrásra alkalmazandó Címkék</span><span class="sxs-lookup"><span data-stu-id="43744-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="43744-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43744-144">-Confirm</span></span>
<span data-ttu-id="43744-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43744-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43744-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43744-146">-WhatIf</span></span>
<span data-ttu-id="43744-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43744-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43744-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43744-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43744-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43744-149">CommonParameters</span></span>
<span data-ttu-id="43744-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43744-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43744-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43744-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43744-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43744-152">INPUTS</span></span>

### <span data-ttu-id="43744-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="43744-153">None</span></span>

## <span data-ttu-id="43744-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43744-154">OUTPUTS</span></span>

### <span data-ttu-id="43744-155">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="43744-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="43744-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43744-156">NOTES</span></span>

## <span data-ttu-id="43744-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43744-157">RELATED LINKS</span></span>
