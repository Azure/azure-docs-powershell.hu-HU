---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680210"
---
# <span data-ttu-id="e9d43-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="e9d43-101">New-AzureRmAks</span></span>

## <span data-ttu-id="e9d43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9d43-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d43-103">Hozzon létre egy új felügyelt Kubernetes-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e9d43-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9d43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9d43-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9d43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9d43-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d43-106">Hozzon létre egy új felügyelt Kubernetes-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e9d43-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e9d43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e9d43-107">EXAMPLES</span></span>

### <span data-ttu-id="e9d43-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e9d43-108">Example 1</span></span>
<span data-ttu-id="e9d43-109">Új felügyelt Kubernetes-fürt létrehozása alapértelmezett params</span><span class="sxs-lookup"><span data-stu-id="e9d43-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e9d43-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9d43-110">PARAMETERS</span></span>

### <span data-ttu-id="e9d43-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="e9d43-111">-AdminUserName</span></span>
<span data-ttu-id="e9d43-112">A Linux virtuális gépek felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="e9d43-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9d43-113">-AsJob</span></span>
<span data-ttu-id="e9d43-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e9d43-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="e9d43-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="e9d43-116">Az ügyfél azonosítója és az ügyfél titka az AAD-alkalmazással és-szolgáltatóval társítva.</span><span class="sxs-lookup"><span data-stu-id="e9d43-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d43-117">-DefaultProfile</span></span>
<span data-ttu-id="e9d43-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9d43-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e9d43-119">-DnsNamePrefix</span></span>
<span data-ttu-id="e9d43-120">A fürt DNS-név előtagja.</span><span class="sxs-lookup"><span data-stu-id="e9d43-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e9d43-121">-Force</span></span>
<span data-ttu-id="e9d43-122">Fürt létrehozása akkor is, ha már létezik</span><span class="sxs-lookup"><span data-stu-id="e9d43-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e9d43-123">-KubernetesVersion</span></span>
<span data-ttu-id="e9d43-124">A Kubernetes a fürt létrehozásához használandó verziója.</span><span class="sxs-lookup"><span data-stu-id="e9d43-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="e9d43-125">-Location</span></span>
<span data-ttu-id="e9d43-126">A fürt Azure-helye.</span><span class="sxs-lookup"><span data-stu-id="e9d43-126">Azure location for the cluster.</span></span>
<span data-ttu-id="e9d43-127">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="e9d43-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9d43-128">-Name</span></span>
<span data-ttu-id="e9d43-129">Kubernetes felügyelt fürt neve</span><span class="sxs-lookup"><span data-stu-id="e9d43-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e9d43-130">-NodeCount</span></span>
<span data-ttu-id="e9d43-131">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="e9d43-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e9d43-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="e9d43-133">A csomópontok alkalmazáskészletének alapértelmezett száma.</span><span class="sxs-lookup"><span data-stu-id="e9d43-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="e9d43-134">-NodeVmSize</span></span>
<span data-ttu-id="e9d43-135">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="e9d43-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d43-136">-ResourceGroupName</span></span>
<span data-ttu-id="e9d43-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e9d43-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e9d43-138">-SshKeyValue</span></span>
<span data-ttu-id="e9d43-139">Az SSH-kulcs vagy a kulcsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e9d43-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="e9d43-140">Az alapértelmezett érték a {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="e9d43-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="e9d43-141">-Tag</span></span>
<span data-ttu-id="e9d43-142">Az erőforrásra alkalmazandó Címkék</span><span class="sxs-lookup"><span data-stu-id="e9d43-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9d43-143">-Confirm</span></span>
<span data-ttu-id="e9d43-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9d43-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d43-145">-WhatIf</span></span>
<span data-ttu-id="e9d43-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9d43-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9d43-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9d43-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d43-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d43-148">CommonParameters</span></span>
<span data-ttu-id="e9d43-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9d43-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d43-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d43-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d43-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9d43-151">INPUTS</span></span>

### <span data-ttu-id="e9d43-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9d43-152">None</span></span>

## <span data-ttu-id="e9d43-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9d43-153">OUTPUTS</span></span>

### <span data-ttu-id="e9d43-154">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e9d43-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e9d43-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9d43-155">NOTES</span></span>

## <span data-ttu-id="e9d43-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9d43-156">RELATED LINKS</span></span>
