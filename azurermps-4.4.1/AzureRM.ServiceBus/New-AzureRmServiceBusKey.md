---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679940"
---
# <span data-ttu-id="76858-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="76858-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="76858-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76858-102">SYNOPSIS</span></span>
<span data-ttu-id="76858-103">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot a szolgáltatási busz névteréhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="76858-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76858-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76858-104">SYNTAX</span></span>

### <span data-ttu-id="76858-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76858-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76858-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="76858-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76858-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="76858-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76858-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="76858-108">DESCRIPTION</span></span>
<span data-ttu-id="76858-109">A **New-AzureRmServiceBusKey** parancsmag új elsődleges vagy másodlagos kapcsolódási karakterláncokat hoz létre a megadott névtérhez, vagy témakörhöz és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="76858-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="76858-110">Példák</span><span class="sxs-lookup"><span data-stu-id="76858-110">EXAMPLES</span></span>

### <span data-ttu-id="76858-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="76858-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="76858-112">Újragenerálja a névtér elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="76858-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="76858-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="76858-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="76858-114">Újragenerálja a várólista elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="76858-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="76858-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="76858-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="76858-116">Újragenerálja a témakör elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="76858-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="76858-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76858-117">PARAMETERS</span></span>

### <span data-ttu-id="76858-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76858-118">-Confirm</span></span>
<span data-ttu-id="76858-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76858-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76858-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76858-120">-Name</span></span>
<span data-ttu-id="76858-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="76858-121">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76858-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="76858-122">-Namespace</span></span>
<span data-ttu-id="76858-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="76858-123">Namespace Name.</span></span>

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

### <span data-ttu-id="76858-124">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="76858-124">-Queue</span></span>
<span data-ttu-id="76858-125">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="76858-125">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76858-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="76858-126">-RegenerateKey</span></span>
<span data-ttu-id="76858-127">Regenerálódni kulcsok-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="76858-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76858-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76858-128">-ResourceGroupName</span></span>
<span data-ttu-id="76858-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="76858-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="76858-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="76858-130">-Topic</span></span>
<span data-ttu-id="76858-131">A téma neve</span><span class="sxs-lookup"><span data-stu-id="76858-131">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76858-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76858-132">-WhatIf</span></span>
<span data-ttu-id="76858-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76858-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76858-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76858-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76858-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76858-135">-DefaultProfile</span></span>
<span data-ttu-id="76858-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76858-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76858-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76858-137">CommonParameters</span></span>
<span data-ttu-id="76858-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76858-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76858-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76858-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76858-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76858-140">INPUTS</span></span>

### <span data-ttu-id="76858-141">System. String</span><span class="sxs-lookup"><span data-stu-id="76858-141">System.String</span></span>

## <span data-ttu-id="76858-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76858-142">OUTPUTS</span></span>

### <span data-ttu-id="76858-143">Microsoft. Azure. Command. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="76858-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="76858-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76858-144">NOTES</span></span>

## <span data-ttu-id="76858-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76858-145">RELATED LINKS</span></span>

