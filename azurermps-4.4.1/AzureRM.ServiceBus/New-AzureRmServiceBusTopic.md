---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494693"
---
# <span data-ttu-id="a60c3-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a60c3-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="a60c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a60c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a60c3-103">Új buszjáratot hoz létre a megadott szolgáltatási busz névtérben.</span><span class="sxs-lookup"><span data-stu-id="a60c3-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a60c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a60c3-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a60c3-105">DESCRIPTION</span></span>
<span data-ttu-id="a60c3-106">A **New-AzureRmServiceBusTopic** parancsmag létrehoz egy új szervizsor-témakört a megadott szolgáltatási busz névtérben.</span><span class="sxs-lookup"><span data-stu-id="a60c3-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a60c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a60c3-107">EXAMPLES</span></span>

### <span data-ttu-id="a60c3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a60c3-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="a60c3-109">Új buszjáratot hoz létre `SB-Topic_exampl1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a60c3-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a60c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a60c3-110">PARAMETERS</span></span>

### <span data-ttu-id="a60c3-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="a60c3-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="a60c3-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a témakört.</span><span class="sxs-lookup"><span data-stu-id="a60c3-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="a60c3-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="a60c3-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="a60c3-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="a60c3-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="a60c3-115">Azt az időtartamot adja meg, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el a rendszer az üzenetet.</span><span class="sxs-lookup"><span data-stu-id="a60c3-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="a60c3-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="a60c3-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="a60c3-117">A duplikált elemek észlelési előzményeinek hosszát meghatározó [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) -szerkezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a60c3-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="a60c3-118">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="a60c3-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="a60c3-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="a60c3-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="a60c3-120">Azt jelzi, hogy engedélyezve vannak-e a kiszolgálóoldali kötegelt műveletek.</span><span class="sxs-lookup"><span data-stu-id="a60c3-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="a60c3-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="a60c3-121">-EnableExpress</span></span>
<span data-ttu-id="a60c3-122">Jelzi, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="a60c3-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="a60c3-123">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="a60c3-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="a60c3-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a60c3-124">-EnablePartitioning</span></span>
<span data-ttu-id="a60c3-125">Itt adhatja meg, hogy engedélyezi-e a téma több bróker közötti particionálását.</span><span class="sxs-lookup"><span data-stu-id="a60c3-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="a60c3-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="a60c3-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="a60c3-127">Itt adhatja meg, hogy engedélyezi-e az előfizetés particionálását.</span><span class="sxs-lookup"><span data-stu-id="a60c3-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="a60c3-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="a60c3-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="a60c3-129">Azt jelzi, hogy engedélyezve van-e a szűrés az üzeneteknek a közzététel előtt.</span><span class="sxs-lookup"><span data-stu-id="a60c3-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="a60c3-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="a60c3-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="a60c3-131">Azt jelzi, hogy az üzenet engedélyezi-e a névtelen hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="a60c3-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="a60c3-132">-IsExpress</span><span class="sxs-lookup"><span data-stu-id="a60c3-132">-IsExpress</span></span>
<span data-ttu-id="a60c3-133">Azt jelzi, hogy a témakör Express engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="a60c3-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="a60c3-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a60c3-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="a60c3-135">A téma maximális mérete megabájtban, ami a témakörhöz lefoglalt memória mérete.</span><span class="sxs-lookup"><span data-stu-id="a60c3-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="a60c3-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="a60c3-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="a60c3-137">Azt jelzi, hogy a témakör ismétlődés-érzékelést követel meg.</span><span class="sxs-lookup"><span data-stu-id="a60c3-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="a60c3-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a60c3-138">-SizeInBytes</span></span>
<span data-ttu-id="a60c3-139">A témakör méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="a60c3-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="a60c3-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="a60c3-140">-SupportOrdering</span></span>
<span data-ttu-id="a60c3-141">Azt jelzi, hogy a témakör támogatja-e a rendelést.</span><span class="sxs-lookup"><span data-stu-id="a60c3-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="a60c3-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a60c3-142">-Confirm</span></span>
<span data-ttu-id="a60c3-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a60c3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60c3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60c3-144">-WhatIf</span></span>
<span data-ttu-id="a60c3-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a60c3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a60c3-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a60c3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60c3-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60c3-147">-DefaultProfile</span></span>
<span data-ttu-id="a60c3-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a60c3-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60c3-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a60c3-149">-Name</span></span>
<span data-ttu-id="a60c3-150">A téma neve</span><span class="sxs-lookup"><span data-stu-id="a60c3-150">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60c3-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a60c3-151">-Namespace</span></span>
<span data-ttu-id="a60c3-152">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a60c3-152">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60c3-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60c3-153">-ResourceGroupName</span></span>
<span data-ttu-id="a60c3-154">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a60c3-154">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60c3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60c3-155">CommonParameters</span></span>
<span data-ttu-id="a60c3-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a60c3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60c3-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60c3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60c3-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a60c3-158">INPUTS</span></span>

### <span data-ttu-id="a60c3-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a60c3-159">System.String</span></span>
<span data-ttu-id="a60c3-160">System. null \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = B77a5c561934e089 \] \] System. null \` 1 System. \[ \[ Int64, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="a60c3-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="a60c3-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a60c3-161">-ResourceGroup</span></span>
 <span data-ttu-id="a60c3-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a60c3-162">System.String</span></span>

### <span data-ttu-id="a60c3-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a60c3-163">-NamespaceName</span></span>
 <span data-ttu-id="a60c3-164">System. String</span><span class="sxs-lookup"><span data-stu-id="a60c3-164">System.String</span></span>

### <span data-ttu-id="a60c3-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a60c3-165">-TopicName</span></span>
 <span data-ttu-id="a60c3-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a60c3-166">System.String</span></span>

### <span data-ttu-id="a60c3-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a60c3-167">-EnablePartitioning</span></span>
 <span data-ttu-id="a60c3-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="a60c3-168">System.Boolean?</span></span>

## <span data-ttu-id="a60c3-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a60c3-169">OUTPUTS</span></span>

### <span data-ttu-id="a60c3-170">Microsoft. Azure. Command. ServiceBus. models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="a60c3-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="a60c3-171">Név: SB-Topic_exampl1 hely: Nyugat-amerikai azonosító:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 típusa: Microsoft. ServiceBus/topic AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 AM CountDetails: DefaultMessageTimeToLive: 10675199.02:: 05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: true FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false IsExpress: false MaxSizeInMegabytes: false RequiresDuplicateDetection: 16384 SizeInBytes: false SubscriptionCount: 0 Status: Active SupportOrdering: UpdatedAt: FALSE: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="a60c3-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="a60c3-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a60c3-172">NOTES</span></span>

## <span data-ttu-id="a60c3-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a60c3-173">RELATED LINKS</span></span>

