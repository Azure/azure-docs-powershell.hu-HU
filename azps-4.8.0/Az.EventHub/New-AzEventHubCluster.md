---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182238"
---
# <span data-ttu-id="70eb4-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="70eb4-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="70eb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="70eb4-103">Új dedikált eventhub-fürtöt hoz létre</span><span class="sxs-lookup"><span data-stu-id="70eb4-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="70eb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70eb4-104">SYNTAX</span></span>

### <span data-ttu-id="70eb4-105">ClusterPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70eb4-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70eb4-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70eb4-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70eb4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70eb4-107">DESCRIPTION</span></span>
<span data-ttu-id="70eb4-108">A New-AzEventHubCluster parancsmag a dedikált eventhub-fürtöt hozza létre a megadott erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="70eb4-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="70eb4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70eb4-109">EXAMPLES</span></span>

### <span data-ttu-id="70eb4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="70eb4-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="70eb4-111">"Eventhub-cluster-5557" dedikált szektorcsoportot hoz létre a resourcegroup "RSG-Cluster27651" a hely southcentralus és kapacitás 1 értékkel</span><span class="sxs-lookup"><span data-stu-id="70eb4-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="70eb4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70eb4-112">PARAMETERS</span></span>

### <span data-ttu-id="70eb4-113">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="70eb4-113">-Capacity</span></span>
<span data-ttu-id="70eb4-114">Cluster Capacity (CU), curerntrly, megengedett érték = 1</span><span class="sxs-lookup"><span data-stu-id="70eb4-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70eb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70eb4-115">-DefaultProfile</span></span>
<span data-ttu-id="70eb4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70eb4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70eb4-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="70eb4-117">-Location</span></span>
<span data-ttu-id="70eb4-118">A fürt helye</span><span class="sxs-lookup"><span data-stu-id="70eb4-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70eb4-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70eb4-119">-Name</span></span>
<span data-ttu-id="70eb4-120">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="70eb4-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70eb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70eb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="70eb4-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="70eb4-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70eb4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70eb4-123">-ResourceId</span></span>
<span data-ttu-id="70eb4-124">A fürt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="70eb4-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70eb4-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="70eb4-125">-Tag</span></span>
<span data-ttu-id="70eb4-126">Hashtables, amely a fürtök erőforrás-címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="70eb4-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70eb4-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70eb4-127">-Confirm</span></span>
<span data-ttu-id="70eb4-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70eb4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70eb4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70eb4-129">-WhatIf</span></span>
<span data-ttu-id="70eb4-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70eb4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70eb4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70eb4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70eb4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70eb4-132">CommonParameters</span></span>
<span data-ttu-id="70eb4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70eb4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70eb4-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70eb4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70eb4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70eb4-135">INPUTS</span></span>

### <span data-ttu-id="70eb4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="70eb4-136">System.String</span></span>

### <span data-ttu-id="70eb4-137">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="70eb4-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="70eb4-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="70eb4-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="70eb4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70eb4-139">OUTPUTS</span></span>

### <span data-ttu-id="70eb4-140">Microsoft. Azure. Command. EventHub. models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="70eb4-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="70eb4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70eb4-141">NOTES</span></span>

## <span data-ttu-id="70eb4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70eb4-142">RELATED LINKS</span></span>
