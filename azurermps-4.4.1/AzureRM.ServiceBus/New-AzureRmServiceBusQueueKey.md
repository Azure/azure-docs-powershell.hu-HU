---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680482"
---
# <span data-ttu-id="b05a7-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="b05a7-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="b05a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b05a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b05a7-103">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot a Service Bus várólistához.</span><span class="sxs-lookup"><span data-stu-id="b05a7-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b05a7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b05a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b05a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b05a7-106">A **New-AzureRmServiceBusQueueKey** parancsmag újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot a megadott szolgáltatási busz várólistájában és az engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="b05a7-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="b05a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b05a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b05a7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b05a7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="b05a7-109">Újragenerálja a névtér elsődleges kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="b05a7-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="b05a7-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="b05a7-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="b05a7-111">Újragenerálja a névtér másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="b05a7-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="b05a7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b05a7-112">PARAMETERS</span></span>

### <span data-ttu-id="b05a7-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b05a7-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="b05a7-114">Az engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b05a7-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a7-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b05a7-115">-NamespaceName</span></span>
<span data-ttu-id="b05a7-116">A szolgáltatás Buszjának névtér neve.</span><span class="sxs-lookup"><span data-stu-id="b05a7-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05a7-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="b05a7-117">-QueueName</span></span>
<span data-ttu-id="b05a7-118">A szolgáltatás Buszjának várólista neve.</span><span class="sxs-lookup"><span data-stu-id="b05a7-118">The Service Bus queue name.</span></span>

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

### <span data-ttu-id="b05a7-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="b05a7-119">-RegenerateKeys</span></span>
<span data-ttu-id="b05a7-120">Itt adhatja meg, hogy az elsődleges vagy másodlagos kulcsokat szeretné-e újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="b05a7-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05a7-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b05a7-121">-ResourceGroup</span></span>
<span data-ttu-id="b05a7-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b05a7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b05a7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b05a7-123">-Confirm</span></span>
<span data-ttu-id="b05a7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b05a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05a7-125">-WhatIf</span></span>
<span data-ttu-id="b05a7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b05a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b05a7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b05a7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05a7-128">CommonParameters</span></span>
<span data-ttu-id="b05a7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b05a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05a7-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05a7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05a7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b05a7-131">INPUTS</span></span>

### <span data-ttu-id="b05a7-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b05a7-132">-ResourceGroup</span></span>
 <span data-ttu-id="b05a7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a7-133">System.String</span></span>
 

### <span data-ttu-id="b05a7-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b05a7-134">-NamespaceName</span></span>
 <span data-ttu-id="b05a7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a7-135">System.String</span></span>
 

### <span data-ttu-id="b05a7-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b05a7-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b05a7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a7-137">System.String</span></span>
 

### <span data-ttu-id="b05a7-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="b05a7-138">-QueueName</span></span>
 <span data-ttu-id="b05a7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a7-139">System.String</span></span>
 

### <span data-ttu-id="b05a7-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="b05a7-140">-RegenerateKeys</span></span>
 <span data-ttu-id="b05a7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b05a7-141">System.String</span></span>

## <span data-ttu-id="b05a7-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b05a7-142">OUTPUTS</span></span>

### <span data-ttu-id="b05a7-143">Microsoft. Azure. Management. ServiceBus. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="b05a7-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="b05a7-144">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="b05a7-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="b05a7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b05a7-145">NOTES</span></span>

## <span data-ttu-id="b05a7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b05a7-146">RELATED LINKS</span></span>

