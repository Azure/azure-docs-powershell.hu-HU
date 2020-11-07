---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
ms.openlocfilehash: 8fe78fff4d297233ee322b58c426099f160b2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838041"
---
# <span data-ttu-id="2e0be-101">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2e0be-101">New-AzServiceBusTopic</span></span>

## <span data-ttu-id="2e0be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e0be-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0be-103">Új buszjáratot hoz létre a megadott szolgáltatási busz névtérben.</span><span class="sxs-lookup"><span data-stu-id="2e0be-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e0be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e0be-104">SYNTAX</span></span>

```
New-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e0be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e0be-105">DESCRIPTION</span></span>
<span data-ttu-id="2e0be-106">A **New-AzServiceBusTopic** parancsmag létrehoz egy új szervizsor-témakört a megadott szolgáltatási busz névtérben.</span><span class="sxs-lookup"><span data-stu-id="2e0be-106">The **New-AzServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e0be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e0be-107">EXAMPLES</span></span>

### <span data-ttu-id="2e0be-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e0be-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="2e0be-109">Új buszjáratot hoz létre `SB-Topic_exampl1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2e0be-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="2e0be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e0be-110">PARAMETERS</span></span>

### <span data-ttu-id="2e0be-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="2e0be-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="2e0be-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a témakört.</span><span class="sxs-lookup"><span data-stu-id="2e0be-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="2e0be-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="2e0be-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="2e0be-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="2e0be-115">Azt az időtartamot adja meg, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el a rendszer az üzenetet.</span><span class="sxs-lookup"><span data-stu-id="2e0be-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0be-116">-DefaultProfile</span></span>
<span data-ttu-id="2e0be-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e0be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e0be-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="2e0be-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="2e0be-119">A duplikált elemek észlelési előzményeinek hosszát meghatározó [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) -szerkezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e0be-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="2e0be-120">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="2e0be-120">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="2e0be-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="2e0be-122">Azt jelzi, hogy engedélyezve vannak-e a kiszolgálóoldali kötegelt műveletek.</span><span class="sxs-lookup"><span data-stu-id="2e0be-122">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="2e0be-123">-EnableExpress</span></span>
<span data-ttu-id="2e0be-124">Jelzi, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="2e0be-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="2e0be-125">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="2e0be-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="2e0be-126">-EnablePartitioning</span></span>
<span data-ttu-id="2e0be-127">Itt adhatja meg, hogy engedélyezi-e a téma több bróker közötti particionálását.</span><span class="sxs-lookup"><span data-stu-id="2e0be-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2e0be-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="2e0be-129">A téma maximális mérete megabájtban, ami a témakörhöz lefoglalt memória mérete.</span><span class="sxs-lookup"><span data-stu-id="2e0be-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e0be-130">-Name</span></span>
<span data-ttu-id="2e0be-131">A téma neve</span><span class="sxs-lookup"><span data-stu-id="2e0be-131">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e0be-132">-Namespace</span></span>
<span data-ttu-id="2e0be-133">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2e0be-133">Namespace Name.</span></span>

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

### <span data-ttu-id="2e0be-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="2e0be-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="2e0be-135">Azt jelzi, hogy a témakör ismétlődés-érzékelést követel meg.</span><span class="sxs-lookup"><span data-stu-id="2e0be-135">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0be-136">-ResourceGroupName</span></span>
<span data-ttu-id="2e0be-137">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2e0be-137">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="2e0be-138">-SizeInBytes</span></span>
<span data-ttu-id="2e0be-139">A témakör méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="2e0be-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="2e0be-140">-SupportOrdering</span></span>
<span data-ttu-id="2e0be-141">Azt jelzi, hogy a témakör támogatja-e a rendelést.</span><span class="sxs-lookup"><span data-stu-id="2e0be-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0be-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e0be-142">-Confirm</span></span>
<span data-ttu-id="2e0be-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e0be-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e0be-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e0be-144">-WhatIf</span></span>
<span data-ttu-id="2e0be-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e0be-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e0be-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e0be-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e0be-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0be-147">CommonParameters</span></span>
<span data-ttu-id="2e0be-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e0be-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0be-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e0be-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0be-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e0be-150">INPUTS</span></span>

### <span data-ttu-id="2e0be-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0be-151">System.String</span></span>

### <span data-ttu-id="2e0be-152">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e0be-152">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2e0be-153">System. null ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e0be-153">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2e0be-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e0be-154">OUTPUTS</span></span>

### <span data-ttu-id="2e0be-155">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2e0be-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2e0be-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e0be-156">NOTES</span></span>

## <span data-ttu-id="2e0be-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e0be-157">RELATED LINKS</span></span>
