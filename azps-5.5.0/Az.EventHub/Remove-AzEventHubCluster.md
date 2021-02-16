---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163538"
---
# <span data-ttu-id="3c2e2-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="3c2e2-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="3c2e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2e2-103">A megadott dedikált Eventhub-fürt törlése az Erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="3c2e2-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="3c2e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-104">SYNTAX</span></span>

### <span data-ttu-id="3c2e2-105">ClusterPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c2e2-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c2e2-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c2e2-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c2e2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-108">DESCRIPTION</span></span>
<span data-ttu-id="3c2e2-109">A Remove-AzEventHubCluster parancsmag törli a megadott dedikált eventhub-fürt nevét az adott erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="3c2e2-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="3c2e2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c2e2-110">EXAMPLES</span></span>

### <span data-ttu-id="3c2e2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3c2e2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="3c2e2-112">Az Eventhub-Cluster-5557 fürt törlése RSG-Cluster27651 erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="3c2e2-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="3c2e2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-113">PARAMETERS</span></span>

### <span data-ttu-id="3c2e2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c2e2-114">-AsJob</span></span>
<span data-ttu-id="3c2e2-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c2e2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c2e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2e2-116">-DefaultProfile</span></span>
<span data-ttu-id="3c2e2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c2e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c2e2-118">-InputObject</span></span>
<span data-ttu-id="3c2e2-119">Fürtobjektum</span><span class="sxs-lookup"><span data-stu-id="3c2e2-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3c2e2-120">-Name</span></span>
<span data-ttu-id="3c2e2-121">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="3c2e2-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2e2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c2e2-122">-PassThru</span></span>
<span data-ttu-id="3c2e2-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="3c2e2-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3c2e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c2e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c2e2-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3c2e2-125">Resource Group Name</span></span>

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

### <span data-ttu-id="3c2e2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-126">-ResourceId</span></span>
<span data-ttu-id="3c2e2-127">Fürterőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3c2e2-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2e2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c2e2-128">-Confirm</span></span>
<span data-ttu-id="3c2e2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2e2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2e2-130">-WhatIf</span></span>
<span data-ttu-id="3c2e2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c2e2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c2e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2e2-133">CommonParameters</span></span>
<span data-ttu-id="3c2e2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2e2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c2e2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2e2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-136">INPUTS</span></span>

### <span data-ttu-id="3c2e2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3c2e2-137">System.String</span></span>

### <span data-ttu-id="3c2e2-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3c2e2-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="3c2e2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c2e2-139">OUTPUTS</span></span>

### <span data-ttu-id="3c2e2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c2e2-140">System.Boolean</span></span>

## <span data-ttu-id="3c2e2-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c2e2-141">NOTES</span></span>

## <span data-ttu-id="3c2e2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c2e2-142">RELATED LINKS</span></span>
