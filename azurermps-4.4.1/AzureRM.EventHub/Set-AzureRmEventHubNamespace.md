---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493509"
---
# <span data-ttu-id="a2fae-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a2fae-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="a2fae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2fae-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fae-103">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="a2fae-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2fae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2fae-104">SYNTAX</span></span>

### <span data-ttu-id="a2fae-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2fae-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2fae-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2fae-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a2fae-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2fae-107">DESCRIPTION</span></span>
<span data-ttu-id="a2fae-108">A Set-AzureRmEventHubNamespace parancsmag frissíti a megadott esemény-hubok névtér tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a2fae-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a2fae-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2fae-109">EXAMPLES</span></span>

### <span data-ttu-id="a2fae-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2fae-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="a2fae-111">Frissíti a \` létrehozott névtér-MyNamespaceName állapotát \` .</span><span class="sxs-lookup"><span data-stu-id="a2fae-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="a2fae-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2fae-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="a2fae-113">A \` \` AutoInflate = enabled és a MaximumThroughputUnits = 10 névtér MyNamespaceName állapotát frissíti</span><span class="sxs-lookup"><span data-stu-id="a2fae-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="a2fae-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2fae-114">PARAMETERS</span></span>

### <span data-ttu-id="a2fae-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="a2fae-115">-Location</span></span>
<span data-ttu-id="a2fae-116">Az esemény hubok névtér geo-helye.</span><span class="sxs-lookup"><span data-stu-id="a2fae-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2fae-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2fae-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a2fae-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a2fae-119">-SkuCapacity</span></span>
<span data-ttu-id="a2fae-120">Az esemény hub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="a2fae-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a2fae-121">-SkuName</span></span>
<span data-ttu-id="a2fae-122">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="a2fae-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-123">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="a2fae-123">-State</span></span>
<span data-ttu-id="a2fae-124">Megadja a névtér állapotát (letiltott vagy engedélyezett).</span><span class="sxs-lookup"><span data-stu-id="a2fae-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="a2fae-125">-Tag</span></span>
<span data-ttu-id="a2fae-126">Az Hashtables képviselő adatforrások.</span><span class="sxs-lookup"><span data-stu-id="a2fae-126">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2fae-127">-Confirm</span></span>
<span data-ttu-id="a2fae-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2fae-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2fae-129">-WhatIf</span></span>
<span data-ttu-id="a2fae-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2fae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2fae-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2fae-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="a2fae-132">-EnableAutoInflate</span></span>
<span data-ttu-id="a2fae-133">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="a2fae-133">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="a2fae-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="a2fae-135">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, a vaule a 0 – 20 átviteli egység között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a2fae-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fae-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2fae-136">-Name</span></span>
<span data-ttu-id="a2fae-137">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="a2fae-137">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="a2fae-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2fae-138">INPUTS</span></span>

### <span data-ttu-id="a2fae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a2fae-139">System.String</span></span>

### <span data-ttu-id="a2fae-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a2fae-140">System.Int32</span></span>

### <span data-ttu-id="a2fae-141">Microsoft. Azure. Management. EventHub. models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="a2fae-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="a2fae-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2fae-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2fae-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2fae-143">OUTPUTS</span></span>

### <span data-ttu-id="a2fae-144">Microsoft. Azure. Command. EventHub. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a2fae-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="a2fae-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2fae-145">NOTES</span></span>

## <span data-ttu-id="a2fae-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2fae-146">RELATED LINKS</span></span>

