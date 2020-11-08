---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185458"
---
# <span data-ttu-id="8df33-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="8df33-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="8df33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8df33-102">SYNOPSIS</span></span>
<span data-ttu-id="8df33-103">A megadott dedikált Eventhub-fürt törlése a ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8df33-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="8df33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8df33-104">SYNTAX</span></span>

### <span data-ttu-id="8df33-105">ClusterPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8df33-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df33-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8df33-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df33-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df33-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df33-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8df33-108">DESCRIPTION</span></span>
<span data-ttu-id="8df33-109">A Remove-AzEventHubCluster parancsmag törli az adott dedikált eventhub-fürtöt az adott resourcegroup</span><span class="sxs-lookup"><span data-stu-id="8df33-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="8df33-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8df33-110">EXAMPLES</span></span>

### <span data-ttu-id="8df33-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8df33-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="8df33-112">Törli a Eventhub-cluster-5557-fürtöt RSG-Cluster27651 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="8df33-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="8df33-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8df33-113">PARAMETERS</span></span>

### <span data-ttu-id="8df33-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8df33-114">-AsJob</span></span>
<span data-ttu-id="8df33-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8df33-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8df33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df33-116">-DefaultProfile</span></span>
<span data-ttu-id="8df33-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8df33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8df33-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8df33-118">-InputObject</span></span>
<span data-ttu-id="8df33-119">Cluster objektum</span><span class="sxs-lookup"><span data-stu-id="8df33-119">Cluster Object</span></span>

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

### <span data-ttu-id="8df33-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8df33-120">-Name</span></span>
<span data-ttu-id="8df33-121">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="8df33-121">Cluster Name</span></span>

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

### <span data-ttu-id="8df33-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8df33-122">-PassThru</span></span>
<span data-ttu-id="8df33-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8df33-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8df33-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df33-124">-ResourceGroupName</span></span>
<span data-ttu-id="8df33-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8df33-125">Resource Group Name</span></span>

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

### <span data-ttu-id="8df33-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8df33-126">-ResourceId</span></span>
<span data-ttu-id="8df33-127">Fürterőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8df33-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="8df33-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8df33-128">-Confirm</span></span>
<span data-ttu-id="8df33-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8df33-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df33-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df33-130">-WhatIf</span></span>
<span data-ttu-id="8df33-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8df33-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df33-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8df33-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df33-133">CommonParameters</span></span>
<span data-ttu-id="8df33-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8df33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df33-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8df33-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df33-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8df33-136">INPUTS</span></span>

### <span data-ttu-id="8df33-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8df33-137">System.String</span></span>

### <span data-ttu-id="8df33-138">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8df33-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="8df33-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8df33-139">OUTPUTS</span></span>

### <span data-ttu-id="8df33-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8df33-140">System.Boolean</span></span>

## <span data-ttu-id="8df33-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8df33-141">NOTES</span></span>

## <span data-ttu-id="8df33-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8df33-142">RELATED LINKS</span></span>
