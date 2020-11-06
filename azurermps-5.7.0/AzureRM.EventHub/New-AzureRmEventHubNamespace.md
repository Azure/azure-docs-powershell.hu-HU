---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499852"
---
# <span data-ttu-id="7d301-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7d301-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="7d301-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d301-102">SYNOPSIS</span></span>
<span data-ttu-id="7d301-103">Esemény-hubok névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7d301-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d301-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d301-104">SYNTAX</span></span>

### <span data-ttu-id="7d301-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d301-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d301-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d301-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d301-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d301-107">DESCRIPTION</span></span>
<span data-ttu-id="7d301-108">A New-AzureRmEventHubNamespace parancsmag az esemény típusú hubok új névterét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7d301-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="7d301-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d301-109">EXAMPLES</span></span>

### <span data-ttu-id="7d301-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7d301-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="7d301-111">A \` \` megadott földrajzi hely \` MyLocation \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény-hubok névtér-MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="7d301-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7d301-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7d301-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="7d301-113">Létrehozza az esemény-hubok \` névtér \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName \` és a AutoInflate engedélyezve van a MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="7d301-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="7d301-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d301-114">PARAMETERS</span></span>

### <span data-ttu-id="7d301-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d301-115">-DefaultProfile</span></span>
<span data-ttu-id="7d301-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d301-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d301-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7d301-117">-EnableAutoInflate</span></span>
<span data-ttu-id="7d301-118">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="7d301-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d301-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="7d301-119">-Location</span></span>
<span data-ttu-id="7d301-120">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="7d301-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="7d301-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7d301-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7d301-122">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7d301-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d301-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d301-123">-Name</span></span>
<span data-ttu-id="7d301-124">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="7d301-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d301-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d301-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d301-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="7d301-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7d301-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7d301-127">-SkuCapacity</span></span>
<span data-ttu-id="7d301-128">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="7d301-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d301-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7d301-129">-SkuName</span></span>
<span data-ttu-id="7d301-130">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="7d301-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="7d301-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="7d301-131">-Tag</span></span>
<span data-ttu-id="7d301-132">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="7d301-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d301-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d301-133">-Confirm</span></span>
<span data-ttu-id="7d301-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d301-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d301-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d301-135">-WhatIf</span></span>
<span data-ttu-id="7d301-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d301-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d301-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d301-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d301-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d301-138">CommonParameters</span></span>
<span data-ttu-id="7d301-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d301-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7d301-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d301-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d301-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d301-141">INPUTS</span></span>

### <span data-ttu-id="7d301-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7d301-142">System.String</span></span>
<span data-ttu-id="7d301-143">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d301-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="7d301-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d301-144">OUTPUTS</span></span>

### <span data-ttu-id="7d301-145">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7d301-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="7d301-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d301-146">NOTES</span></span>

## <span data-ttu-id="7d301-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d301-147">RELATED LINKS</span></span>
