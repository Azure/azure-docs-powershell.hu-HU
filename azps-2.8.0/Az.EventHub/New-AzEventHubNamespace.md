---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 9217dfa2d5465841cb0ed33c2781849ddebff3b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666475"
---
# <span data-ttu-id="36ace-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="36ace-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="36ace-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36ace-102">SYNOPSIS</span></span>
<span data-ttu-id="36ace-103">Esemény-hubok névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36ace-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="36ace-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36ace-104">SYNTAX</span></span>

### <span data-ttu-id="36ace-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36ace-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ace-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="36ace-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ace-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="36ace-107">DESCRIPTION</span></span>
<span data-ttu-id="36ace-108">A New-AzEventHubNamespace parancsmag az esemény típusú hubok új névterét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="36ace-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="36ace-109">Példák</span><span class="sxs-lookup"><span data-stu-id="36ace-109">EXAMPLES</span></span>

### <span data-ttu-id="36ace-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36ace-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="36ace-111">A \` \` megadott földrajzi hely \` MyLocation \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény-hubok névtér-MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="36ace-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="36ace-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="36ace-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="36ace-113">Létrehozza az esemény-hubok \` névtér \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName \` és a AutoInflate engedélyezve van a MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="36ace-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="36ace-114">Példa: 3 – Kafka engedélyezve névtér</span><span class="sxs-lookup"><span data-stu-id="36ace-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="36ace-115">Az esemény-hubok névtér \` \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName a \` Kafka-és AutoInflate engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="36ace-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="36ace-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36ace-116">PARAMETERS</span></span>

### <span data-ttu-id="36ace-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ace-117">-DefaultProfile</span></span>
<span data-ttu-id="36ace-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36ace-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ace-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="36ace-119">-EnableAutoInflate</span></span>
<span data-ttu-id="36ace-120">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="36ace-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="36ace-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="36ace-121">-EnableKafka</span></span>
<span data-ttu-id="36ace-122">a Kafka engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="36ace-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="36ace-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="36ace-123">-Location</span></span>
<span data-ttu-id="36ace-124">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="36ace-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="36ace-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="36ace-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="36ace-126">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="36ace-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="36ace-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36ace-127">-Name</span></span>
<span data-ttu-id="36ace-128">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="36ace-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="36ace-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ace-129">-ResourceGroupName</span></span>
<span data-ttu-id="36ace-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="36ace-130">Resource Group Name</span></span>

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

### <span data-ttu-id="36ace-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="36ace-131">-SkuCapacity</span></span>
<span data-ttu-id="36ace-132">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="36ace-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="36ace-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36ace-133">-SkuName</span></span>
<span data-ttu-id="36ace-134">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="36ace-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="36ace-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="36ace-135">-Tag</span></span>
<span data-ttu-id="36ace-136">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="36ace-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="36ace-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36ace-137">-Confirm</span></span>
<span data-ttu-id="36ace-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36ace-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ace-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ace-139">-WhatIf</span></span>
<span data-ttu-id="36ace-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36ace-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ace-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36ace-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ace-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ace-142">CommonParameters</span></span>
<span data-ttu-id="36ace-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36ace-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ace-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ace-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ace-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ace-145">INPUTS</span></span>

### <span data-ttu-id="36ace-146">System. String</span><span class="sxs-lookup"><span data-stu-id="36ace-146">System.String</span></span>

### <span data-ttu-id="36ace-147">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36ace-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36ace-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="36ace-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="36ace-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ace-149">OUTPUTS</span></span>

### <span data-ttu-id="36ace-150">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="36ace-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="36ace-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36ace-151">NOTES</span></span>

## <span data-ttu-id="36ace-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36ace-152">RELATED LINKS</span></span>
