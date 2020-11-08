---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187571"
---
# <span data-ttu-id="85c67-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="85c67-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="85c67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85c67-102">SYNOPSIS</span></span>
<span data-ttu-id="85c67-103">fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="85c67-103">update cluster</span></span>

## <span data-ttu-id="85c67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85c67-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c67-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85c67-105">DESCRIPTION</span></span>
<span data-ttu-id="85c67-106">fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="85c67-106">update cluster</span></span>

## <span data-ttu-id="85c67-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85c67-107">EXAMPLES</span></span>

### <span data-ttu-id="85c67-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="85c67-108">Example 1</span></span>
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

<span data-ttu-id="85c67-109">fürt frissítése a fő boltozat tulajdonságaival és a SKU-val</span><span class="sxs-lookup"><span data-stu-id="85c67-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="85c67-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85c67-110">PARAMETERS</span></span>

### <span data-ttu-id="85c67-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85c67-111">-AsJob</span></span>
<span data-ttu-id="85c67-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="85c67-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85c67-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="85c67-113">-ClusterName</span></span>
<span data-ttu-id="85c67-114">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="85c67-114">The cluster name.</span></span>

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

### <span data-ttu-id="85c67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c67-115">-DefaultProfile</span></span>
<span data-ttu-id="85c67-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85c67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c67-117">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="85c67-117">-KeyName</span></span>
<span data-ttu-id="85c67-118">Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="85c67-118">Key Name</span></span>

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

### <span data-ttu-id="85c67-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="85c67-119">-KeyVaultUri</span></span>
<span data-ttu-id="85c67-120">A fő pince-URI, a "kiürítési védelem" és a "Soft Delete" funkciónak engedélyezve kell lennie ehhez a rendszerbeállításhoz.</span><span class="sxs-lookup"><span data-stu-id="85c67-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="85c67-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="85c67-121">-KeyVersion</span></span>
<span data-ttu-id="85c67-122">Fő verzió</span><span class="sxs-lookup"><span data-stu-id="85c67-122">Key Version</span></span>

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

### <span data-ttu-id="85c67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c67-123">-ResourceGroupName</span></span>
<span data-ttu-id="85c67-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85c67-124">The resource group name.</span></span>

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

### <span data-ttu-id="85c67-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="85c67-125">-SkuCapacity</span></span>
<span data-ttu-id="85c67-126">SKU-kapacitás</span><span class="sxs-lookup"><span data-stu-id="85c67-126">Sku Capacity</span></span>

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

### <span data-ttu-id="85c67-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="85c67-127">-SkuName</span></span>
<span data-ttu-id="85c67-128">SKU neve, most csak "CapacityReservation" lehet</span><span class="sxs-lookup"><span data-stu-id="85c67-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="85c67-129">-Címkék</span><span class="sxs-lookup"><span data-stu-id="85c67-129">-Tags</span></span>
<span data-ttu-id="85c67-130">A fürt címkéi</span><span class="sxs-lookup"><span data-stu-id="85c67-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="85c67-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="85c67-131">-Confirm</span></span>
<span data-ttu-id="85c67-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85c67-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c67-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c67-133">-WhatIf</span></span>
<span data-ttu-id="85c67-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="85c67-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c67-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85c67-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c67-136">CommonParameters</span></span>
<span data-ttu-id="85c67-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85c67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c67-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="85c67-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c67-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85c67-139">INPUTS</span></span>

### <span data-ttu-id="85c67-140">System. String</span><span class="sxs-lookup"><span data-stu-id="85c67-140">System.String</span></span>

## <span data-ttu-id="85c67-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85c67-141">OUTPUTS</span></span>

### <span data-ttu-id="85c67-142">Microsoft. Azure. Command. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="85c67-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="85c67-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85c67-143">NOTES</span></span>

## <span data-ttu-id="85c67-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85c67-144">RELATED LINKS</span></span>
