---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680564"
---
# <span data-ttu-id="e1e42-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e1e42-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="e1e42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1e42-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e42-103">Esemény-hubok névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e1e42-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1e42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1e42-104">SYNTAX</span></span>

### <span data-ttu-id="e1e42-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1e42-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e1e42-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1e42-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e1e42-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1e42-107">DESCRIPTION</span></span>
<span data-ttu-id="e1e42-108">A New-AzureRmEventHubNamespace parancsmag az esemény típusú hubok új névterét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e1e42-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="e1e42-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1e42-109">EXAMPLES</span></span>

### <span data-ttu-id="e1e42-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1e42-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="e1e42-111">A \` \` megadott földrajzi hely \` MyLocation \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény-hubok névtér-MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="e1e42-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e1e42-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1e42-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="e1e42-113">Létrehozza az esemény-hubok \` névtér \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName \` és a AutoInflate engedélyezve van a MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="e1e42-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="e1e42-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1e42-114">PARAMETERS</span></span>

### <span data-ttu-id="e1e42-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="e1e42-115">-Location</span></span>
<span data-ttu-id="e1e42-116">Az esemény hubok névtér geo-helye.</span><span class="sxs-lookup"><span data-stu-id="e1e42-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="e1e42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e42-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1e42-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e1e42-118">Resource group name.</span></span>

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

### <span data-ttu-id="e1e42-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e1e42-119">-SkuCapacity</span></span>
<span data-ttu-id="e1e42-120">Az esemény hub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="e1e42-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="e1e42-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e1e42-121">-SkuName</span></span>
<span data-ttu-id="e1e42-122">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="e1e42-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e42-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="e1e42-123">-Tag</span></span>
<span data-ttu-id="e1e42-124">Az Hashtables képviselő adatforrások.</span><span class="sxs-lookup"><span data-stu-id="e1e42-124">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="e1e42-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1e42-125">-Confirm</span></span>
<span data-ttu-id="e1e42-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1e42-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1e42-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1e42-127">-WhatIf</span></span>
<span data-ttu-id="e1e42-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1e42-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1e42-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1e42-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1e42-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="e1e42-130">-EnableAutoInflate</span></span>
<span data-ttu-id="e1e42-131">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="e1e42-131">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="e1e42-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e1e42-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e1e42-133">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, a vaule a 0 – 20 átviteli egység között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e1e42-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="e1e42-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1e42-134">-Name</span></span>
<span data-ttu-id="e1e42-135">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="e1e42-135">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="e1e42-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1e42-136">INPUTS</span></span>

### <span data-ttu-id="e1e42-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e1e42-137">System.String</span></span>
<span data-ttu-id="e1e42-138">System. null \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = B77a5c561934e089 \] \] System. null \` 1 System. \[ \[ Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1e42-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1e42-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1e42-139">OUTPUTS</span></span>

### <span data-ttu-id="e1e42-140">Microsoft. Azure. Command. EventHub. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e1e42-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="e1e42-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1e42-141">NOTES</span></span>

## <span data-ttu-id="e1e42-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1e42-142">RELATED LINKS</span></span>

