---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158707"
---
# <span data-ttu-id="75cf3-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="75cf3-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="75cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="75cf3-103">fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="75cf3-103">update cluster</span></span>

## <span data-ttu-id="75cf3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75cf3-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75cf3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="75cf3-106">fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="75cf3-106">update cluster</span></span>

## <span data-ttu-id="75cf3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75cf3-107">EXAMPLES</span></span>

### <span data-ttu-id="75cf3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="75cf3-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="75cf3-109">update cluster with key vault properties and sku</span><span class="sxs-lookup"><span data-stu-id="75cf3-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="75cf3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cf3-110">PARAMETERS</span></span>

### <span data-ttu-id="75cf3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75cf3-111">-AsJob</span></span>
<span data-ttu-id="75cf3-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="75cf3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75cf3-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="75cf3-113">-ClusterName</span></span>
<span data-ttu-id="75cf3-114">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="75cf3-114">The cluster name.</span></span>

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

### <span data-ttu-id="75cf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cf3-115">-DefaultProfile</span></span>
<span data-ttu-id="75cf3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75cf3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75cf3-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="75cf3-117">-KeyName</span></span>
<span data-ttu-id="75cf3-118">Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="75cf3-118">Key Name</span></span>

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

### <span data-ttu-id="75cf3-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="75cf3-119">-KeyVaultUri</span></span>
<span data-ttu-id="75cf3-120">Ehhez a kulcshoz engedélyezni kell a kulcstár Uri, a "Végleges törlés elleni védelem" és a "Soft Delete" beállítást.</span><span class="sxs-lookup"><span data-stu-id="75cf3-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="75cf3-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="75cf3-121">-KeyVersion</span></span>
<span data-ttu-id="75cf3-122">Főverzió</span><span class="sxs-lookup"><span data-stu-id="75cf3-122">Key Version</span></span>

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

### <span data-ttu-id="75cf3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75cf3-123">-ResourceGroupName</span></span>
<span data-ttu-id="75cf3-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75cf3-124">The resource group name.</span></span>

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

### <span data-ttu-id="75cf3-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="75cf3-125">-SkuCapacity</span></span>
<span data-ttu-id="75cf3-126">Termékváltozat kapacitása</span><span class="sxs-lookup"><span data-stu-id="75cf3-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf3-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="75cf3-127">-SkuName</span></span>
<span data-ttu-id="75cf3-128">Termékváltozat neve, mostantól csak "CapacityReservation" lehet</span><span class="sxs-lookup"><span data-stu-id="75cf3-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="75cf3-129">-Címkék</span><span class="sxs-lookup"><span data-stu-id="75cf3-129">-Tags</span></span>
<span data-ttu-id="75cf3-130">A fürt címkéi</span><span class="sxs-lookup"><span data-stu-id="75cf3-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="75cf3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75cf3-131">-Confirm</span></span>
<span data-ttu-id="75cf3-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75cf3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cf3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cf3-133">-WhatIf</span></span>
<span data-ttu-id="75cf3-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75cf3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75cf3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75cf3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cf3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cf3-136">CommonParameters</span></span>
<span data-ttu-id="75cf3-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cf3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cf3-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75cf3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cf3-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75cf3-139">INPUTS</span></span>

### <span data-ttu-id="75cf3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="75cf3-140">System.String</span></span>

## <span data-ttu-id="75cf3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75cf3-141">OUTPUTS</span></span>

### <span data-ttu-id="75cf3-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="75cf3-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="75cf3-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75cf3-143">NOTES</span></span>

## <span data-ttu-id="75cf3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75cf3-144">RELATED LINKS</span></span>
