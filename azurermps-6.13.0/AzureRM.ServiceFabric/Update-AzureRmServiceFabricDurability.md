---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 56a6afff6551ae0191ac1f17d3a52c47940e045a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497291"
---
# <span data-ttu-id="12acc-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="12acc-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="12acc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12acc-102">SYNOPSIS</span></span>
<span data-ttu-id="12acc-103">Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.</span><span class="sxs-lookup"><span data-stu-id="12acc-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12acc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12acc-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12acc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12acc-105">DESCRIPTION</span></span>
<span data-ttu-id="12acc-106">A **AzureRmServiceFabricDurability** frissítse a fürt tartósságát vagy SKU-ának frissítését.</span><span class="sxs-lookup"><span data-stu-id="12acc-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="12acc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="12acc-107">EXAMPLES</span></span>

### <span data-ttu-id="12acc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="12acc-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="12acc-109">Ez a parancs a "NT1" NodeType tartóssági rétegét ezüst értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="12acc-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="12acc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12acc-110">PARAMETERS</span></span>

### <span data-ttu-id="12acc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12acc-111">-DefaultProfile</span></span>
<span data-ttu-id="12acc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12acc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12acc-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12acc-113">-DurabilityLevel</span></span>
<span data-ttu-id="12acc-114">Adja meg a tartóssági szintet.</span><span class="sxs-lookup"><span data-stu-id="12acc-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12acc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12acc-115">-Name</span></span>
<span data-ttu-id="12acc-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="12acc-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12acc-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="12acc-117">-NodeType</span></span>
<span data-ttu-id="12acc-118">Adja meg a Service Fabric csomópont típusa nevet.</span><span class="sxs-lookup"><span data-stu-id="12acc-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12acc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12acc-119">-ResourceGroupName</span></span>
<span data-ttu-id="12acc-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12acc-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12acc-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="12acc-121">-Sku</span></span>
<span data-ttu-id="12acc-122">Adja meg a csomópont típusának SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="12acc-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12acc-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12acc-123">-Confirm</span></span>
<span data-ttu-id="12acc-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12acc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12acc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12acc-125">-WhatIf</span></span>
<span data-ttu-id="12acc-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12acc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12acc-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12acc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12acc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12acc-128">CommonParameters</span></span>
<span data-ttu-id="12acc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12acc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12acc-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12acc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12acc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12acc-131">INPUTS</span></span>

### <span data-ttu-id="12acc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="12acc-132">System.String</span></span>
<span data-ttu-id="12acc-133">Paraméterek: NodeType (ByValue), SKU (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12acc-133">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="12acc-134">Microsoft. Azure. Command. ServiceFabric. models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12acc-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="12acc-135">Paraméterek: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12acc-135">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="12acc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12acc-136">OUTPUTS</span></span>

### <span data-ttu-id="12acc-137">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="12acc-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12acc-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12acc-138">NOTES</span></span>

## <span data-ttu-id="12acc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12acc-139">RELATED LINKS</span></span>
