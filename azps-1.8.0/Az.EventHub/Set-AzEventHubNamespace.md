---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670809"
---
# <span data-ttu-id="e4d96-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e4d96-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="e4d96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4d96-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d96-103">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="e4d96-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e4d96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4d96-104">SYNTAX</span></span>

### <span data-ttu-id="e4d96-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4d96-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d96-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d96-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d96-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4d96-107">DESCRIPTION</span></span>
<span data-ttu-id="e4d96-108">A Set-AzEventHubNamespace parancsmag frissíti a megadott esemény-hubok névtér tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e4d96-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e4d96-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e4d96-109">EXAMPLES</span></span>

### <span data-ttu-id="e4d96-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4d96-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="e4d96-111">Frissíti a \` létrehozott névtér-MyNamespaceName állapotát \` .</span><span class="sxs-lookup"><span data-stu-id="e4d96-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="e4d96-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e4d96-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="e4d96-113">A \` \` AutoInflate = enabled és a MaximumThroughputUnits = 10 névtér MyNamespaceName állapotát frissíti</span><span class="sxs-lookup"><span data-stu-id="e4d96-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="e4d96-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4d96-114">PARAMETERS</span></span>

### <span data-ttu-id="e4d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d96-115">-DefaultProfile</span></span>
<span data-ttu-id="e4d96-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4d96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d96-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="e4d96-117">-EnableAutoInflate</span></span>
<span data-ttu-id="e4d96-118">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="e4d96-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="e4d96-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="e4d96-119">-Location</span></span>
<span data-ttu-id="e4d96-120">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="e4d96-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="e4d96-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e4d96-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e4d96-122">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e4d96-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="e4d96-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4d96-123">-Name</span></span>
<span data-ttu-id="e4d96-124">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="e4d96-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="e4d96-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d96-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4d96-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e4d96-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4d96-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e4d96-127">-SkuCapacity</span></span>
<span data-ttu-id="e4d96-128">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="e4d96-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="e4d96-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4d96-129">-SkuName</span></span>
<span data-ttu-id="e4d96-130">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="e4d96-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="e4d96-131">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e4d96-131">-State</span></span>
<span data-ttu-id="e4d96-132">A névtér letiltása/engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="e4d96-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="e4d96-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="e4d96-133">-Tag</span></span>
<span data-ttu-id="e4d96-134">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e4d96-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="e4d96-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4d96-135">-Confirm</span></span>
<span data-ttu-id="e4d96-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4d96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d96-137">-WhatIf</span></span>
<span data-ttu-id="e4d96-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4d96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d96-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4d96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d96-140">CommonParameters</span></span>
<span data-ttu-id="e4d96-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4d96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d96-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d96-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d96-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4d96-143">INPUTS</span></span>

### <span data-ttu-id="e4d96-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e4d96-144">System.String</span></span>

### <span data-ttu-id="e4d96-145">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4d96-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4d96-146">System. null ' 1 [[Microsoft. Azure. commands. EventHub. models. NamespaceState, Microsoft. Azure. PowerShell. parancsmagok. EventHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e4d96-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e4d96-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4d96-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e4d96-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4d96-148">OUTPUTS</span></span>

### <span data-ttu-id="e4d96-149">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4d96-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e4d96-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4d96-150">NOTES</span></span>

## <span data-ttu-id="e4d96-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4d96-151">RELATED LINKS</span></span>
