---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469826"
---
# <span data-ttu-id="7ee56-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="7ee56-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="7ee56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ee56-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee56-103">Az adott fürt címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="7ee56-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="7ee56-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ee56-104">SYNTAX</span></span>

### <span data-ttu-id="7ee56-105">ClusterPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ee56-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee56-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ee56-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee56-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ee56-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee56-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ee56-108">DESCRIPTION</span></span>
<span data-ttu-id="7ee56-109">A Set-AzEventHubCluster parancsmag frissíti az adott fürt címkéit</span><span class="sxs-lookup"><span data-stu-id="7ee56-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="7ee56-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ee56-110">EXAMPLES</span></span>

### <span data-ttu-id="7ee56-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7ee56-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="7ee56-112">Frissíti a megadott fürt címkéit.</span><span class="sxs-lookup"><span data-stu-id="7ee56-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="7ee56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ee56-113">PARAMETERS</span></span>

### <span data-ttu-id="7ee56-114">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="7ee56-114">-Capacity</span></span>
<span data-ttu-id="7ee56-115">Fürtkapacitás (CU),rntrly, engedélyezett érték = 1</span><span class="sxs-lookup"><span data-stu-id="7ee56-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="7ee56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee56-116">-DefaultProfile</span></span>
<span data-ttu-id="7ee56-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ee56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ee56-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee56-118">-InputObject</span></span>
<span data-ttu-id="7ee56-119">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="7ee56-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee56-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7ee56-120">-Location</span></span>
<span data-ttu-id="7ee56-121">A fürt helye</span><span class="sxs-lookup"><span data-stu-id="7ee56-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee56-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7ee56-122">-Name</span></span>
<span data-ttu-id="7ee56-123">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="7ee56-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee56-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ee56-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7ee56-125">Resource Group Name</span></span>

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

### <span data-ttu-id="7ee56-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee56-126">-ResourceId</span></span>
<span data-ttu-id="7ee56-127">A fürt erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="7ee56-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="7ee56-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ee56-128">-Tag</span></span>
<span data-ttu-id="7ee56-129">Fürtök erőforráscímkéit képviselő hashtables</span><span class="sxs-lookup"><span data-stu-id="7ee56-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee56-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ee56-130">-Confirm</span></span>
<span data-ttu-id="7ee56-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ee56-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee56-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee56-132">-WhatIf</span></span>
<span data-ttu-id="7ee56-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ee56-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee56-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ee56-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee56-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee56-135">CommonParameters</span></span>
<span data-ttu-id="7ee56-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee56-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee56-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ee56-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee56-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ee56-138">INPUTS</span></span>

### <span data-ttu-id="7ee56-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7ee56-139">System.String</span></span>

### <span data-ttu-id="7ee56-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7ee56-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7ee56-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="7ee56-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="7ee56-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ee56-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7ee56-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ee56-143">OUTPUTS</span></span>

### <span data-ttu-id="7ee56-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="7ee56-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="7ee56-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ee56-145">NOTES</span></span>

## <span data-ttu-id="7ee56-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ee56-146">RELATED LINKS</span></span>
