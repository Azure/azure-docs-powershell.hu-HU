---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499512"
---
# <span data-ttu-id="53c15-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="53c15-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="53c15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53c15-102">SYNOPSIS</span></span>
<span data-ttu-id="53c15-103">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="53c15-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53c15-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53c15-104">SYNTAX</span></span>

### <span data-ttu-id="53c15-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53c15-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53c15-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="53c15-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c15-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53c15-107">DESCRIPTION</span></span>
<span data-ttu-id="53c15-108">A Set-AzureRmEventHubNamespace parancsmag frissíti a megadott esemény-hubok névtér tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="53c15-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="53c15-109">Példák</span><span class="sxs-lookup"><span data-stu-id="53c15-109">EXAMPLES</span></span>

### <span data-ttu-id="53c15-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="53c15-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="53c15-111">Frissíti a \` létrehozott névtér-MyNamespaceName állapotát \` .</span><span class="sxs-lookup"><span data-stu-id="53c15-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="53c15-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="53c15-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="53c15-113">A \` \` AutoInflate = enabled és a MaximumThroughputUnits = 10 névtér MyNamespaceName állapotát frissíti</span><span class="sxs-lookup"><span data-stu-id="53c15-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="53c15-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53c15-114">PARAMETERS</span></span>

### <span data-ttu-id="53c15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c15-115">-DefaultProfile</span></span>
<span data-ttu-id="53c15-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53c15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c15-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="53c15-117">-EnableAutoInflate</span></span>
<span data-ttu-id="53c15-118">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="53c15-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="53c15-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="53c15-119">-Location</span></span>
<span data-ttu-id="53c15-120">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="53c15-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="53c15-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="53c15-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="53c15-122">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="53c15-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c15-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53c15-123">-Name</span></span>
<span data-ttu-id="53c15-124">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="53c15-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="53c15-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c15-125">-ResourceGroupName</span></span>
<span data-ttu-id="53c15-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="53c15-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="53c15-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="53c15-127">-SkuCapacity</span></span>
<span data-ttu-id="53c15-128">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="53c15-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="53c15-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="53c15-129">-SkuName</span></span>
<span data-ttu-id="53c15-130">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="53c15-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="53c15-131">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="53c15-131">-State</span></span>
<span data-ttu-id="53c15-132">A névtér letiltása/engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="53c15-132">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c15-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="53c15-133">-Tag</span></span>
<span data-ttu-id="53c15-134">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="53c15-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c15-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53c15-135">-Confirm</span></span>
<span data-ttu-id="53c15-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53c15-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c15-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c15-137">-WhatIf</span></span>
<span data-ttu-id="53c15-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53c15-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c15-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53c15-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c15-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c15-140">CommonParameters</span></span>
<span data-ttu-id="53c15-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53c15-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c15-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c15-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c15-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53c15-143">INPUTS</span></span>

### <span data-ttu-id="53c15-144">System. String</span><span class="sxs-lookup"><span data-stu-id="53c15-144">System.String</span></span>

### <span data-ttu-id="53c15-145">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="53c15-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="53c15-146">System. null ' 1 [[Microsoft. Azure. commands. EventHub. models. NamespaceState, Microsoft. Azure. commands. EventHub, Version = 0.6.7.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="53c15-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="53c15-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="53c15-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53c15-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53c15-148">OUTPUTS</span></span>

### <span data-ttu-id="53c15-149">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="53c15-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="53c15-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53c15-150">NOTES</span></span>

## <span data-ttu-id="53c15-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53c15-151">RELATED LINKS</span></span>
