---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182464"
---
# <span data-ttu-id="dd681-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="dd681-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="dd681-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd681-102">SYNOPSIS</span></span>
<span data-ttu-id="dd681-103">Fürt létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="dd681-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="dd681-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd681-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd681-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd681-105">DESCRIPTION</span></span>
<span data-ttu-id="dd681-106">Fürt létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="dd681-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="dd681-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd681-107">EXAMPLES</span></span>

### <span data-ttu-id="dd681-108">1. példa: fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="dd681-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="dd681-109">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="dd681-109">Create cluster</span></span>

## <span data-ttu-id="dd681-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd681-110">PARAMETERS</span></span>

### <span data-ttu-id="dd681-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd681-111">-AsJob</span></span>
<span data-ttu-id="dd681-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="dd681-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dd681-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="dd681-113">-ClusterSize</span></span>
<span data-ttu-id="dd681-114">A szektorcsoport mérete</span><span class="sxs-lookup"><span data-stu-id="dd681-114">The cluster size</span></span>

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

### <span data-ttu-id="dd681-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd681-115">-DefaultProfile</span></span>
<span data-ttu-id="dd681-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd681-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd681-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd681-117">-Name</span></span>
<span data-ttu-id="dd681-118">A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="dd681-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="dd681-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="dd681-119">-NoWait</span></span>
<span data-ttu-id="dd681-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="dd681-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd681-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="dd681-121">-PrivateCloudName</span></span>
<span data-ttu-id="dd681-122">A privát felhő neve.</span><span class="sxs-lookup"><span data-stu-id="dd681-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="dd681-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd681-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd681-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dd681-124">The name of the resource group.</span></span>
<span data-ttu-id="dd681-125">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="dd681-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dd681-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dd681-126">-SkuName</span></span>
<span data-ttu-id="dd681-127">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="dd681-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="dd681-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd681-128">-SubscriptionId</span></span>
<span data-ttu-id="dd681-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd681-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dd681-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd681-130">-Confirm</span></span>
<span data-ttu-id="dd681-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd681-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd681-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd681-132">-WhatIf</span></span>
<span data-ttu-id="dd681-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd681-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd681-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd681-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd681-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd681-135">CommonParameters</span></span>
<span data-ttu-id="dd681-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd681-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd681-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dd681-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd681-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd681-138">INPUTS</span></span>

## <span data-ttu-id="dd681-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd681-139">OUTPUTS</span></span>

### <span data-ttu-id="dd681-140">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="dd681-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="dd681-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd681-141">NOTES</span></span>

<span data-ttu-id="dd681-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dd681-142">ALIASES</span></span>

## <span data-ttu-id="dd681-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd681-143">RELATED LINKS</span></span>

