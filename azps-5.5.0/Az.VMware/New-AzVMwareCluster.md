---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: d654b2fa012a793ce48dff2cc5bfb9ade4f99d34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149778"
---
# <span data-ttu-id="743d5-101">New-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="743d5-101">New-AzVMwareCluster</span></span>

## <span data-ttu-id="743d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743d5-102">SYNOPSIS</span></span>
<span data-ttu-id="743d5-103">Fürt létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="743d5-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="743d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="743d5-104">SYNTAX</span></span>

```
New-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -SkuName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="743d5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="743d5-105">DESCRIPTION</span></span>
<span data-ttu-id="743d5-106">Fürt létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="743d5-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="743d5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="743d5-107">EXAMPLES</span></span>

### <span data-ttu-id="743d5-108">1. példa: Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="743d5-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="743d5-109">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="743d5-109">Create cluster</span></span>

## <span data-ttu-id="743d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="743d5-110">PARAMETERS</span></span>

### <span data-ttu-id="743d5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="743d5-111">-AsJob</span></span>
<span data-ttu-id="743d5-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="743d5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="743d5-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="743d5-113">-ClusterSize</span></span>
<span data-ttu-id="743d5-114">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="743d5-114">The cluster size</span></span>

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

### <span data-ttu-id="743d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743d5-115">-DefaultProfile</span></span>
<span data-ttu-id="743d5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="743d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="743d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="743d5-117">-Name</span></span>
<span data-ttu-id="743d5-118">A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="743d5-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="743d5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="743d5-119">-NoWait</span></span>
<span data-ttu-id="743d5-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="743d5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="743d5-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="743d5-121">-PrivateCloudName</span></span>
<span data-ttu-id="743d5-122">A privát felhő neve.</span><span class="sxs-lookup"><span data-stu-id="743d5-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="743d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="743d5-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="743d5-124">The name of the resource group.</span></span>
<span data-ttu-id="743d5-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="743d5-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="743d5-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="743d5-126">-SkuName</span></span>
<span data-ttu-id="743d5-127">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="743d5-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="743d5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="743d5-128">-SubscriptionId</span></span>
<span data-ttu-id="743d5-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="743d5-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="743d5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="743d5-130">-Confirm</span></span>
<span data-ttu-id="743d5-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="743d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743d5-132">-WhatIf</span></span>
<span data-ttu-id="743d5-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="743d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="743d5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="743d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743d5-135">CommonParameters</span></span>
<span data-ttu-id="743d5-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743d5-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="743d5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743d5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="743d5-138">INPUTS</span></span>

## <span data-ttu-id="743d5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="743d5-139">OUTPUTS</span></span>

### <span data-ttu-id="743d5-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="743d5-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="743d5-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="743d5-141">NOTES</span></span>

<span data-ttu-id="743d5-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="743d5-142">ALIASES</span></span>

## <span data-ttu-id="743d5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="743d5-143">RELATED LINKS</span></span>

