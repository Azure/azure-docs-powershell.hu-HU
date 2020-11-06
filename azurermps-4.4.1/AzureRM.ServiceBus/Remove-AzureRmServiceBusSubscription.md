---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494676"
---
# <span data-ttu-id="0789a-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="0789a-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="0789a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0789a-102">SYNOPSIS</span></span>
<span data-ttu-id="0789a-103">Eltávolítja az előfizetést a megadott szolgáltatási busz névterből származó témára.</span><span class="sxs-lookup"><span data-stu-id="0789a-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0789a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0789a-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0789a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0789a-105">DESCRIPTION</span></span>
<span data-ttu-id="0789a-106">A **Remove-AzureRmServiceBusSubscription** parancsmag eltávolítja az előfizetést a megadott szolgáltatási busz névtérből származó témára.</span><span class="sxs-lookup"><span data-stu-id="0789a-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0789a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0789a-107">EXAMPLES</span></span>

### <span data-ttu-id="0789a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0789a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="0789a-109">Eltávolítja az előfizetést `SB-TopicSubscription-Example1` a `SB-Topic_exampl1` megadott Service Bus névtérben lévő témakörre `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0789a-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="0789a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0789a-110">PARAMETERS</span></span>

### <span data-ttu-id="0789a-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0789a-111">-Confirm</span></span>
<span data-ttu-id="0789a-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0789a-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0789a-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0789a-113">-WhatIf</span></span>
<span data-ttu-id="0789a-114">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0789a-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0789a-115">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0789a-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0789a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0789a-116">-DefaultProfile</span></span>
<span data-ttu-id="0789a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0789a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0789a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0789a-118">-Name</span></span>
<span data-ttu-id="0789a-119">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="0789a-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0789a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0789a-120">-Namespace</span></span>
<span data-ttu-id="0789a-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0789a-121">Namespace Name.</span></span>

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

### <span data-ttu-id="0789a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0789a-122">-ResourceGroupName</span></span>
<span data-ttu-id="0789a-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0789a-123">The name of the resource group</span></span>

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

### <span data-ttu-id="0789a-124">-Topic</span><span class="sxs-lookup"><span data-stu-id="0789a-124">-Topic</span></span>
<span data-ttu-id="0789a-125">A téma neve</span><span class="sxs-lookup"><span data-stu-id="0789a-125">Topic Name.</span></span>

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

### <span data-ttu-id="0789a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0789a-126">CommonParameters</span></span>
<span data-ttu-id="0789a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0789a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0789a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0789a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0789a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0789a-129">INPUTS</span></span>

### <span data-ttu-id="0789a-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0789a-130">-ResourceGroup</span></span>
 <span data-ttu-id="0789a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0789a-131">System.String</span></span>

### <span data-ttu-id="0789a-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0789a-132">-NamespaceName</span></span>
 <span data-ttu-id="0789a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0789a-133">System.String</span></span>

### <span data-ttu-id="0789a-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0789a-134">-TopicName</span></span>
 <span data-ttu-id="0789a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0789a-135">System.String</span></span>

### <span data-ttu-id="0789a-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0789a-136">-SubscriptionName</span></span>
 <span data-ttu-id="0789a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0789a-137">System.String</span></span>

## <span data-ttu-id="0789a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0789a-138">OUTPUTS</span></span>

### <span data-ttu-id="0789a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0789a-139">System.Boolean</span></span>

## <span data-ttu-id="0789a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0789a-140">NOTES</span></span>

## <span data-ttu-id="0789a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0789a-141">RELATED LINKS</span></span>

