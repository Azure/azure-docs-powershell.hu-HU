---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469858"
---
# <span data-ttu-id="d536b-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="d536b-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="d536b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d536b-102">SYNOPSIS</span></span>
<span data-ttu-id="d536b-103">Létrehoz egy új dedikált eventhub-fürtöt</span><span class="sxs-lookup"><span data-stu-id="d536b-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="d536b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d536b-104">SYNTAX</span></span>

### <span data-ttu-id="d536b-105">ClusterPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d536b-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d536b-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d536b-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d536b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d536b-107">DESCRIPTION</span></span>
<span data-ttu-id="d536b-108">A New-AzEventHubCluster parancsmag létrehozza a dedikált eventhub-fürtöt a megadott erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="d536b-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="d536b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d536b-109">EXAMPLES</span></span>

### <span data-ttu-id="d536b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d536b-110">Example 1</span></span>
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

<span data-ttu-id="d536b-111">Létrehozza az Eventhub-Cluster-5557 dedikált fürtöt az "RSG-Cluster27651" erőforráscsoportban a Location southcentralus és a Capacity as 1 erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="d536b-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="d536b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d536b-112">PARAMETERS</span></span>

### <span data-ttu-id="d536b-113">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="d536b-113">-Capacity</span></span>
<span data-ttu-id="d536b-114">Fürtkapacitás (CU),rntrly, engedélyezett érték = 1</span><span class="sxs-lookup"><span data-stu-id="d536b-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="d536b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d536b-115">-DefaultProfile</span></span>
<span data-ttu-id="d536b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d536b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d536b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d536b-117">-Location</span></span>
<span data-ttu-id="d536b-118">A fürt helye</span><span class="sxs-lookup"><span data-stu-id="d536b-118">Location of Cluster</span></span>

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

### <span data-ttu-id="d536b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d536b-119">-Name</span></span>
<span data-ttu-id="d536b-120">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="d536b-120">Cluster Name</span></span>

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

### <span data-ttu-id="d536b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d536b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d536b-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d536b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="d536b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d536b-123">-ResourceId</span></span>
<span data-ttu-id="d536b-124">A fürt erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="d536b-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="d536b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d536b-125">-Tag</span></span>
<span data-ttu-id="d536b-126">A fürtök erőforráscímkéit képviselő hashtables</span><span class="sxs-lookup"><span data-stu-id="d536b-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="d536b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d536b-127">-Confirm</span></span>
<span data-ttu-id="d536b-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d536b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d536b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d536b-129">-WhatIf</span></span>
<span data-ttu-id="d536b-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d536b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d536b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d536b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d536b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d536b-132">CommonParameters</span></span>
<span data-ttu-id="d536b-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d536b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d536b-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d536b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d536b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d536b-135">INPUTS</span></span>

### <span data-ttu-id="d536b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d536b-136">System.String</span></span>

### <span data-ttu-id="d536b-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d536b-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d536b-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d536b-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d536b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d536b-139">OUTPUTS</span></span>

### <span data-ttu-id="d536b-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="d536b-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="d536b-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d536b-141">NOTES</span></span>

## <span data-ttu-id="d536b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d536b-142">RELATED LINKS</span></span>
