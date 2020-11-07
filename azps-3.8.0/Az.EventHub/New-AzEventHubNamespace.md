---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: bbe0f406232086fc0441281ae150f95e2c8eb0a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845618"
---
# <span data-ttu-id="08c01-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="08c01-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="08c01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08c01-102">SYNOPSIS</span></span>
<span data-ttu-id="08c01-103">Esemény-hubok névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="08c01-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="08c01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08c01-104">SYNTAX</span></span>

### <span data-ttu-id="08c01-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08c01-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08c01-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="08c01-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c01-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="08c01-107">DESCRIPTION</span></span>
<span data-ttu-id="08c01-108">A New-AzEventHubNamespace parancsmag az esemény típusú hubok új névterét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="08c01-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="08c01-109">Példák</span><span class="sxs-lookup"><span data-stu-id="08c01-109">EXAMPLES</span></span>

### <span data-ttu-id="08c01-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08c01-110">Example 1</span></span>                                           
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

<span data-ttu-id="08c01-111">A \` \` megadott földrajzi hely \` MyLocation \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény-hubok névtér-MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="08c01-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08c01-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="08c01-112">Example 2</span></span>
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

<span data-ttu-id="08c01-113">Létrehozza az esemény-hubok \` névtér \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName \` és a AutoInflate engedélyezve van a MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="08c01-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="08c01-114">Példa: 3 – Kafka engedélyezve névtér</span><span class="sxs-lookup"><span data-stu-id="08c01-114">Example 3 - Kafka enabled namespace</span></span>
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

<span data-ttu-id="08c01-115">Az esemény-hubok névtér \` \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName a \` Kafka-és AutoInflate engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="08c01-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="08c01-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08c01-116">PARAMETERS</span></span>

### <span data-ttu-id="08c01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c01-117">-DefaultProfile</span></span>
<span data-ttu-id="08c01-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08c01-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08c01-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="08c01-119">-EnableAutoInflate</span></span>
<span data-ttu-id="08c01-120">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="08c01-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="08c01-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="08c01-121">-EnableKafka</span></span>
<span data-ttu-id="08c01-122">a Kafka engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="08c01-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="08c01-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="08c01-123">-Location</span></span>
<span data-ttu-id="08c01-124">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="08c01-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="08c01-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="08c01-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="08c01-126">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="08c01-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="08c01-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08c01-127">-Name</span></span>
<span data-ttu-id="08c01-128">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="08c01-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="08c01-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c01-129">-ResourceGroupName</span></span>
<span data-ttu-id="08c01-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="08c01-130">Resource Group Name</span></span>

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

### <span data-ttu-id="08c01-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="08c01-131">-SkuCapacity</span></span>
<span data-ttu-id="08c01-132">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="08c01-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="08c01-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="08c01-133">-SkuName</span></span>
<span data-ttu-id="08c01-134">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="08c01-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="08c01-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="08c01-135">-Tag</span></span>
<span data-ttu-id="08c01-136">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="08c01-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="08c01-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08c01-137">-Confirm</span></span>
<span data-ttu-id="08c01-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08c01-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c01-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c01-139">-WhatIf</span></span>
<span data-ttu-id="08c01-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08c01-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08c01-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08c01-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c01-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c01-142">CommonParameters</span></span>
<span data-ttu-id="08c01-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08c01-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c01-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c01-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c01-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08c01-145">INPUTS</span></span>

### <span data-ttu-id="08c01-146">System. String</span><span class="sxs-lookup"><span data-stu-id="08c01-146">System.String</span></span>

### <span data-ttu-id="08c01-147">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08c01-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08c01-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="08c01-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08c01-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08c01-149">OUTPUTS</span></span>

### <span data-ttu-id="08c01-150">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="08c01-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="08c01-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08c01-151">NOTES</span></span>

## <span data-ttu-id="08c01-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08c01-152">RELATED LINKS</span></span>
