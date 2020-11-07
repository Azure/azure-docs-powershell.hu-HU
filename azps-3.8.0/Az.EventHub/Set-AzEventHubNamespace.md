---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 5717728fa868094a5d1d170af948743d1b9e065b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845561"
---
# <span data-ttu-id="c7731-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c7731-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="c7731-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7731-102">SYNOPSIS</span></span>
<span data-ttu-id="c7731-103">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="c7731-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c7731-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7731-104">SYNTAX</span></span>

### <span data-ttu-id="c7731-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7731-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7731-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7731-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7731-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7731-107">DESCRIPTION</span></span>
<span data-ttu-id="c7731-108">A Set-AzEventHubNamespace parancsmag frissíti a megadott esemény-hubok névtér tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="c7731-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c7731-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7731-109">EXAMPLES</span></span>

### <span data-ttu-id="c7731-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7731-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="c7731-111">Frissíti a \` létrehozott névtér-MyNamespaceName címkéit \` .</span><span class="sxs-lookup"><span data-stu-id="c7731-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="c7731-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c7731-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="c7731-113">A \` \` AutoInflate = enabled és a MaximumThroughputUnits = 10 névtér MyNamespaceName állapotát frissíti</span><span class="sxs-lookup"><span data-stu-id="c7731-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="c7731-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7731-114">PARAMETERS</span></span>

### <span data-ttu-id="c7731-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7731-115">-DefaultProfile</span></span>
<span data-ttu-id="c7731-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7731-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7731-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="c7731-117">-EnableAutoInflate</span></span>
<span data-ttu-id="c7731-118">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="c7731-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="c7731-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="c7731-119">-EnableKafka</span></span>
<span data-ttu-id="c7731-120">a Kafka engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="c7731-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="c7731-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="c7731-121">-Location</span></span>
<span data-ttu-id="c7731-122">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="c7731-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="c7731-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c7731-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c7731-124">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c7731-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="c7731-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7731-125">-Name</span></span>
<span data-ttu-id="c7731-126">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="c7731-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="c7731-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7731-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7731-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c7731-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7731-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c7731-129">-SkuCapacity</span></span>
<span data-ttu-id="c7731-130">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="c7731-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="c7731-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c7731-131">-SkuName</span></span>
<span data-ttu-id="c7731-132">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="c7731-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="c7731-133">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c7731-133">-State</span></span>
<span data-ttu-id="c7731-134">A névtér letiltása/engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="c7731-134">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="c7731-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="c7731-135">-Tag</span></span>
<span data-ttu-id="c7731-136">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c7731-136">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="c7731-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7731-137">-Confirm</span></span>
<span data-ttu-id="c7731-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7731-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7731-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7731-139">-WhatIf</span></span>
<span data-ttu-id="c7731-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7731-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7731-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7731-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7731-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7731-142">CommonParameters</span></span>
<span data-ttu-id="c7731-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7731-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7731-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7731-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7731-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7731-145">INPUTS</span></span>

### <span data-ttu-id="c7731-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c7731-146">System.String</span></span>

### <span data-ttu-id="c7731-147">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c7731-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c7731-148">System. null ' 1 [[Microsoft. Azure. commands. EventHub. models. NamespaceState, Microsoft. Azure. PowerShell. parancsmagok. EventHub, Version = 1.3.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c7731-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c7731-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7731-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c7731-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7731-150">OUTPUTS</span></span>

### <span data-ttu-id="c7731-151">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c7731-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c7731-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7731-152">NOTES</span></span>

## <span data-ttu-id="c7731-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7731-153">RELATED LINKS</span></span>
