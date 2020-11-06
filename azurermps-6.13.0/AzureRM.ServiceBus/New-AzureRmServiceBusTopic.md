---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: e2ca0b6902ecc13c9dfe4f418ea5d321b6e36dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494915"
---
# <span data-ttu-id="b69c0-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b69c0-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="b69c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b69c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b69c0-103">Új buszjáratot hoz létre a megadott szolgáltatási busz névtérben.</span><span class="sxs-lookup"><span data-stu-id="b69c0-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b69c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b69c0-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b69c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b69c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b69c0-106">A **New-AzureRmServiceBusTopic** parancsmag létrehoz egy új szervizsor-témakört a megadott szolgáltatási busz névtérben.</span><span class="sxs-lookup"><span data-stu-id="b69c0-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b69c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b69c0-107">EXAMPLES</span></span>

### <span data-ttu-id="b69c0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b69c0-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

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

<span data-ttu-id="b69c0-109">Új buszjáratot hoz létre `SB-Topic_exampl1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b69c0-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="b69c0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b69c0-110">PARAMETERS</span></span>

### <span data-ttu-id="b69c0-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b69c0-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b69c0-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a témakört.</span><span class="sxs-lookup"><span data-stu-id="b69c0-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="b69c0-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="b69c0-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b69c0-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b69c0-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b69c0-115">Azt az időtartamot adja meg, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el a rendszer az üzenetet.</span><span class="sxs-lookup"><span data-stu-id="b69c0-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="b69c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69c0-116">-DefaultProfile</span></span>
<span data-ttu-id="b69c0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b69c0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b69c0-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b69c0-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="b69c0-119">A duplikált elemek észlelési előzményeinek hosszát meghatározó [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) -szerkezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b69c0-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="b69c0-120">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="b69c0-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="b69c0-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b69c0-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="b69c0-122">Azt jelzi, hogy engedélyezve vannak-e a kiszolgálóoldali kötegelt műveletek.</span><span class="sxs-lookup"><span data-stu-id="b69c0-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="b69c0-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="b69c0-123">-EnableExpress</span></span>
<span data-ttu-id="b69c0-124">Jelzi, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="b69c0-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="b69c0-125">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="b69c0-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="b69c0-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b69c0-126">-EnablePartitioning</span></span>
<span data-ttu-id="b69c0-127">Itt adhatja meg, hogy engedélyezi-e a téma több bróker közötti particionálását.</span><span class="sxs-lookup"><span data-stu-id="b69c0-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="b69c0-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b69c0-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="b69c0-129">A téma maximális mérete megabájtban, ami a témakörhöz lefoglalt memória mérete.</span><span class="sxs-lookup"><span data-stu-id="b69c0-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="b69c0-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b69c0-130">-Name</span></span>
<span data-ttu-id="b69c0-131">A téma neve</span><span class="sxs-lookup"><span data-stu-id="b69c0-131">Topic Name.</span></span>

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

### <span data-ttu-id="b69c0-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b69c0-132">-Namespace</span></span>
<span data-ttu-id="b69c0-133">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b69c0-133">Namespace Name.</span></span>

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

### <span data-ttu-id="b69c0-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="b69c0-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="b69c0-135">Azt jelzi, hogy a témakör ismétlődés-érzékelést követel meg.</span><span class="sxs-lookup"><span data-stu-id="b69c0-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="b69c0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69c0-136">-ResourceGroupName</span></span>
<span data-ttu-id="b69c0-137">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b69c0-137">The name of the resource group</span></span>

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

### <span data-ttu-id="b69c0-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b69c0-138">-SizeInBytes</span></span>
<span data-ttu-id="b69c0-139">A témakör méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="b69c0-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="b69c0-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="b69c0-140">-SupportOrdering</span></span>
<span data-ttu-id="b69c0-141">Azt jelzi, hogy a témakör támogatja-e a rendelést.</span><span class="sxs-lookup"><span data-stu-id="b69c0-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="b69c0-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b69c0-142">-Confirm</span></span>
<span data-ttu-id="b69c0-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b69c0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b69c0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b69c0-144">-WhatIf</span></span>
<span data-ttu-id="b69c0-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b69c0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b69c0-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b69c0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b69c0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69c0-147">CommonParameters</span></span>
<span data-ttu-id="b69c0-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b69c0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69c0-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b69c0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69c0-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b69c0-150">INPUTS</span></span>

### <span data-ttu-id="b69c0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b69c0-151">System.String</span></span>

### <span data-ttu-id="b69c0-152">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b69c0-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b69c0-153">System. null ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b69c0-153">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b69c0-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b69c0-154">OUTPUTS</span></span>

### <span data-ttu-id="b69c0-155">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b69c0-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b69c0-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b69c0-156">NOTES</span></span>

## <span data-ttu-id="b69c0-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b69c0-157">RELATED LINKS</span></span>
