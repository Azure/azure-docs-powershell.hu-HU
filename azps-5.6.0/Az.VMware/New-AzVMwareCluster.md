---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: 2433ffa7c1a016af4d3268162587d6b901b30ae9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936394"
---
# <span data-ttu-id="7cf13-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="7cf13-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="7cf13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf13-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf13-103">Fürt létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7cf13-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="7cf13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7cf13-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cf13-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7cf13-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf13-106">Fürt létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7cf13-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="7cf13-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7cf13-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf13-108">1. példa: Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="7cf13-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="7cf13-109">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="7cf13-109">Create cluster</span></span>

## <span data-ttu-id="7cf13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf13-110">PARAMETERS</span></span>

### <span data-ttu-id="7cf13-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf13-111">-AsJob</span></span>
<span data-ttu-id="7cf13-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7cf13-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7cf13-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="7cf13-113">-ClusterSize</span></span>
<span data-ttu-id="7cf13-114">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="7cf13-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf13-115">-DefaultProfile</span></span>
<span data-ttu-id="7cf13-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cf13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf13-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7cf13-117">-Name</span></span>
<span data-ttu-id="7cf13-118">A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="7cf13-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf13-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7cf13-119">-NoWait</span></span>
<span data-ttu-id="7cf13-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7cf13-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7cf13-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="7cf13-121">-PrivateCloudName</span></span>
<span data-ttu-id="7cf13-122">A privát felhő neve.</span><span class="sxs-lookup"><span data-stu-id="7cf13-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="7cf13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf13-123">-ResourceGroupName</span></span>
<span data-ttu-id="7cf13-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7cf13-124">The name of the resource group.</span></span>
<span data-ttu-id="7cf13-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="7cf13-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7cf13-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7cf13-126">-SkuName</span></span>
<span data-ttu-id="7cf13-127">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="7cf13-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="7cf13-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cf13-128">-SubscriptionId</span></span>
<span data-ttu-id="7cf13-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7cf13-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf13-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf13-130">-Confirm</span></span>
<span data-ttu-id="7cf13-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7cf13-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf13-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf13-132">-WhatIf</span></span>
<span data-ttu-id="7cf13-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7cf13-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf13-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cf13-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf13-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf13-135">CommonParameters</span></span>
<span data-ttu-id="7cf13-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf13-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf13-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf13-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf13-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf13-138">INPUTS</span></span>

## <span data-ttu-id="7cf13-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf13-139">OUTPUTS</span></span>

### <span data-ttu-id="7cf13-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="7cf13-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="7cf13-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7cf13-141">NOTES</span></span>

<span data-ttu-id="7cf13-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7cf13-142">ALIASES</span></span>

## <span data-ttu-id="7cf13-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cf13-143">RELATED LINKS</span></span>

