---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 739d027d095810ae33f90a7b5cc1ad7caf148081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495373"
---
# <span data-ttu-id="84111-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="84111-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="84111-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84111-102">SYNOPSIS</span></span>
<span data-ttu-id="84111-103">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="84111-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84111-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84111-104">SYNTAX</span></span>

### <span data-ttu-id="84111-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84111-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84111-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="84111-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84111-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="84111-107">DESCRIPTION</span></span>
<span data-ttu-id="84111-108">A Set-AzureRmEventHubNamespace parancsmag frissíti a megadott esemény-hubok névtér tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="84111-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="84111-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84111-109">EXAMPLES</span></span>

### <span data-ttu-id="84111-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="84111-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="84111-111">Frissíti a \` létrehozott névtér-MyNamespaceName állapotát \` .</span><span class="sxs-lookup"><span data-stu-id="84111-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="84111-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="84111-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="84111-113">A \` \` AutoInflate = enabled és a MaximumThroughputUnits = 10 névtér MyNamespaceName állapotát frissíti</span><span class="sxs-lookup"><span data-stu-id="84111-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="84111-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84111-114">PARAMETERS</span></span>

### <span data-ttu-id="84111-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84111-115">-DefaultProfile</span></span>
<span data-ttu-id="84111-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84111-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84111-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="84111-117">-EnableAutoInflate</span></span>
<span data-ttu-id="84111-118">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="84111-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="84111-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="84111-119">-Location</span></span>
<span data-ttu-id="84111-120">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="84111-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="84111-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="84111-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="84111-122">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84111-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84111-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84111-123">-Name</span></span>
<span data-ttu-id="84111-124">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="84111-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="84111-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84111-125">-ResourceGroupName</span></span>
<span data-ttu-id="84111-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="84111-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="84111-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="84111-127">-SkuCapacity</span></span>
<span data-ttu-id="84111-128">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="84111-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="84111-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="84111-129">-SkuName</span></span>
<span data-ttu-id="84111-130">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="84111-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="84111-131">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="84111-131">-State</span></span>
<span data-ttu-id="84111-132">A névtér letiltása/engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="84111-132">Disable/Enable Namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84111-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="84111-133">-Tag</span></span>
<span data-ttu-id="84111-134">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="84111-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84111-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84111-135">-Confirm</span></span>
<span data-ttu-id="84111-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84111-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84111-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84111-137">-WhatIf</span></span>
<span data-ttu-id="84111-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84111-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84111-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84111-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84111-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84111-140">CommonParameters</span></span>
<span data-ttu-id="84111-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84111-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="84111-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84111-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84111-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84111-143">INPUTS</span></span>

### <span data-ttu-id="84111-144">System. String</span><span class="sxs-lookup"><span data-stu-id="84111-144">System.String</span></span>
<span data-ttu-id="84111-145">System. nulla `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. commands. EventHub. models. NamespaceState, Microsoft. Azure. commands. EventHub, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84111-145">System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="84111-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84111-146">OUTPUTS</span></span>

### <span data-ttu-id="84111-147">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="84111-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="84111-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84111-148">NOTES</span></span>

## <span data-ttu-id="84111-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84111-149">RELATED LINKS</span></span>
