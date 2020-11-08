---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182951"
---
# <span data-ttu-id="bb56e-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="bb56e-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="bb56e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb56e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb56e-103">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="bb56e-103">Create cluster</span></span>

## <span data-ttu-id="bb56e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb56e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb56e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb56e-105">DESCRIPTION</span></span>

<span data-ttu-id="bb56e-106">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="bb56e-106">Create cluster</span></span>

## <span data-ttu-id="bb56e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb56e-107">EXAMPLES</span></span>

### <span data-ttu-id="bb56e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb56e-108">Example 1</span></span>
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

<span data-ttu-id="bb56e-109">Fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="bb56e-109">Create cluster</span></span>

## <span data-ttu-id="bb56e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb56e-110">PARAMETERS</span></span>

### <span data-ttu-id="bb56e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb56e-111">-AsJob</span></span>
<span data-ttu-id="bb56e-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bb56e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb56e-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="bb56e-113">-ClusterName</span></span>
<span data-ttu-id="bb56e-114">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="bb56e-114">The cluster name.</span></span>

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

### <span data-ttu-id="bb56e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb56e-115">-DefaultProfile</span></span>
<span data-ttu-id="bb56e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb56e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb56e-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bb56e-117">-IdentityType</span></span>
<span data-ttu-id="bb56e-118">az identitás típusának értéke lehet "SystemAssigned", "nincs".</span><span class="sxs-lookup"><span data-stu-id="bb56e-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

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

### <span data-ttu-id="bb56e-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="bb56e-119">-Location</span></span>
<span data-ttu-id="bb56e-120">A fürt által telepített földrajzi terület.</span><span class="sxs-lookup"><span data-stu-id="bb56e-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="bb56e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb56e-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb56e-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb56e-122">The resource group name.</span></span>

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

### <span data-ttu-id="bb56e-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bb56e-123">-SkuCapacity</span></span>
<span data-ttu-id="bb56e-124">SKU-kapacitás: az értéknek az 100 többszörösének kell lennie, és az 1000-2000-ös tartományába kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bb56e-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

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

### <span data-ttu-id="bb56e-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bb56e-125">-SkuName</span></span>
<span data-ttu-id="bb56e-126">SKU neve, most csak "CapacityReservation" lehet</span><span class="sxs-lookup"><span data-stu-id="bb56e-126">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="bb56e-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="bb56e-127">-Tags</span></span>
<span data-ttu-id="bb56e-128">A fürt címkéi</span><span class="sxs-lookup"><span data-stu-id="bb56e-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="bb56e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb56e-129">-Confirm</span></span>
<span data-ttu-id="bb56e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb56e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb56e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb56e-131">-WhatIf</span></span>
<span data-ttu-id="bb56e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb56e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb56e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb56e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb56e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb56e-134">CommonParameters</span></span>
<span data-ttu-id="bb56e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb56e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb56e-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bb56e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb56e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb56e-137">INPUTS</span></span>

### <span data-ttu-id="bb56e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb56e-138">System.String</span></span>

## <span data-ttu-id="bb56e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb56e-139">OUTPUTS</span></span>

### <span data-ttu-id="bb56e-140">Microsoft. Azure. Command. OperationalInsights. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="bb56e-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="bb56e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb56e-141">NOTES</span></span>

## <span data-ttu-id="bb56e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb56e-142">RELATED LINKS</span></span>
