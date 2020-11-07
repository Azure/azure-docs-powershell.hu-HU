---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 2ceed94c800a53bae98a3d6ba93dc5cc722cc4e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836213"
---
# <span data-ttu-id="780d5-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="780d5-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="780d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="780d5-102">SYNOPSIS</span></span>
<span data-ttu-id="780d5-103">Esemény-hubok névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="780d5-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="780d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="780d5-104">SYNTAX</span></span>

### <span data-ttu-id="780d5-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="780d5-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780d5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="780d5-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="780d5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="780d5-107">DESCRIPTION</span></span>
<span data-ttu-id="780d5-108">A New-AzEventHubNamespace parancsmag az esemény típusú hubok új névterét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="780d5-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="780d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="780d5-109">EXAMPLES</span></span>

### <span data-ttu-id="780d5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="780d5-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="780d5-111">A \` \` megadott földrajzi hely \` MyLocation \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény-hubok névtér-MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="780d5-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="780d5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="780d5-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="780d5-113">Létrehozza az esemény-hubok \` névtér \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName \` és a AutoInflate engedélyezve van a MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="780d5-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="780d5-114">Példa: 3 – Kafka engedélyezve névtér</span><span class="sxs-lookup"><span data-stu-id="780d5-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="780d5-115">Az esemény-hubok névtér \` \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName a \` Kafka-és AutoInflate engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="780d5-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="780d5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="780d5-116">PARAMETERS</span></span>

### <span data-ttu-id="780d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780d5-117">-DefaultProfile</span></span>
<span data-ttu-id="780d5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="780d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="780d5-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="780d5-119">-EnableAutoInflate</span></span>
<span data-ttu-id="780d5-120">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="780d5-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="780d5-121">-EnableKafka</span></span>
<span data-ttu-id="780d5-122">a Kafka engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="780d5-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="780d5-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="780d5-123">-Location</span></span>
<span data-ttu-id="780d5-124">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="780d5-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="780d5-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="780d5-126">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="780d5-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="780d5-127">-Name</span></span>
<span data-ttu-id="780d5-128">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="780d5-128">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="780d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="780d5-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="780d5-130">Resource Group Name</span></span>

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

### <span data-ttu-id="780d5-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="780d5-131">-SkuCapacity</span></span>
<span data-ttu-id="780d5-132">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="780d5-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="780d5-133">-SkuName</span></span>
<span data-ttu-id="780d5-134">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="780d5-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="780d5-135">-Tag</span></span>
<span data-ttu-id="780d5-136">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="780d5-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d5-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="780d5-137">-Confirm</span></span>
<span data-ttu-id="780d5-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="780d5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="780d5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="780d5-139">-WhatIf</span></span>
<span data-ttu-id="780d5-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="780d5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="780d5-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="780d5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="780d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780d5-142">CommonParameters</span></span>
<span data-ttu-id="780d5-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="780d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780d5-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780d5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780d5-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="780d5-145">INPUTS</span></span>

### <span data-ttu-id="780d5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="780d5-146">System.String</span></span>

### <span data-ttu-id="780d5-147">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="780d5-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="780d5-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="780d5-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="780d5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="780d5-149">OUTPUTS</span></span>

### <span data-ttu-id="780d5-150">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="780d5-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="780d5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="780d5-151">NOTES</span></span>

## <span data-ttu-id="780d5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="780d5-152">RELATED LINKS</span></span>
