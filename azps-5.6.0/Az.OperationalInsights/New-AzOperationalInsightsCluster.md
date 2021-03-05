---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: c34bb862d3928e6dbbaa55a9660c4868e38941b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011797"
---
# <span data-ttu-id="79333-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="79333-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="79333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79333-102">SYNOPSIS</span></span>
<span data-ttu-id="79333-103">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="79333-103">Create cluster</span></span>

## <span data-ttu-id="79333-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79333-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79333-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79333-105">DESCRIPTION</span></span>

<span data-ttu-id="79333-106">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="79333-106">Create cluster</span></span>

## <span data-ttu-id="79333-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79333-107">EXAMPLES</span></span>

### <span data-ttu-id="79333-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="79333-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="79333-109">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="79333-109">Create cluster</span></span>

## <span data-ttu-id="79333-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79333-110">PARAMETERS</span></span>

### <span data-ttu-id="79333-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79333-111">-AsJob</span></span>
<span data-ttu-id="79333-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="79333-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79333-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79333-113">-ClusterName</span></span>
<span data-ttu-id="79333-114">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="79333-114">The cluster name.</span></span>

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

### <span data-ttu-id="79333-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79333-115">-DefaultProfile</span></span>
<span data-ttu-id="79333-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79333-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79333-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="79333-117">-IdentityType</span></span>
<span data-ttu-id="79333-118">az identitás típusa, az érték lehet "SystemAssigned", "Nincs".</span><span class="sxs-lookup"><span data-stu-id="79333-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79333-119">-Location</span><span class="sxs-lookup"><span data-stu-id="79333-119">-Location</span></span>
<span data-ttu-id="79333-120">A fürt központi telepítésének földrajzi régiója.</span><span class="sxs-lookup"><span data-stu-id="79333-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79333-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79333-121">-ResourceGroupName</span></span>
<span data-ttu-id="79333-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79333-122">The resource group name.</span></span>

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

### <span data-ttu-id="79333-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="79333-123">-SkuCapacity</span></span>
<span data-ttu-id="79333-124">Termékváltozat kapacitásának, az értéknek a 100 többszörösének kell lennie, és a tartomány értéke 1000–2000 között lehet.</span><span class="sxs-lookup"><span data-stu-id="79333-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79333-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="79333-125">-SkuName</span></span>
<span data-ttu-id="79333-126">Termékváltozat neve, mostantól csak "CapacityReservation" lehet</span><span class="sxs-lookup"><span data-stu-id="79333-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79333-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="79333-127">-Tags</span></span>
<span data-ttu-id="79333-128">A fürt címkéi</span><span class="sxs-lookup"><span data-stu-id="79333-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="79333-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79333-129">-Confirm</span></span>
<span data-ttu-id="79333-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79333-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79333-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79333-131">-WhatIf</span></span>
<span data-ttu-id="79333-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79333-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79333-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79333-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79333-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79333-134">CommonParameters</span></span>
<span data-ttu-id="79333-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79333-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79333-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79333-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79333-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79333-137">INPUTS</span></span>

### <span data-ttu-id="79333-138">System.String</span><span class="sxs-lookup"><span data-stu-id="79333-138">System.String</span></span>

## <span data-ttu-id="79333-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79333-139">OUTPUTS</span></span>

### <span data-ttu-id="79333-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="79333-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="79333-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79333-141">NOTES</span></span>

## <span data-ttu-id="79333-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79333-142">RELATED LINKS</span></span>
