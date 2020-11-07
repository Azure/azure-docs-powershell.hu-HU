---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678929"
---
# <span data-ttu-id="6e582-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="6e582-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="6e582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e582-102">SYNOPSIS</span></span>
<span data-ttu-id="6e582-103">Új szabály létrehozása a témakör adott előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="6e582-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e582-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e582-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e582-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e582-105">DESCRIPTION</span></span>
<span data-ttu-id="6e582-106">A **New-AzureRmServiceBusRule** parancsmag új szabályt hoz létre az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="6e582-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="6e582-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e582-107">EXAMPLES</span></span>

### <span data-ttu-id="6e582-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6e582-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="6e582-109">A New-AzureRmServiceBusRule parancsmag új szabályt hoz létre a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="6e582-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="6e582-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e582-110">PARAMETERS</span></span>

### <span data-ttu-id="6e582-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e582-111">-DefaultProfile</span></span>
<span data-ttu-id="6e582-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e582-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e582-113">-Name</span></span>
<span data-ttu-id="6e582-114">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="6e582-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e582-115">-Namespace</span></span>
<span data-ttu-id="6e582-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6e582-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e582-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e582-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6e582-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="6e582-119">-SqlExpression</span></span>
<span data-ttu-id="6e582-120">SQL szűrni kifejezés</span><span class="sxs-lookup"><span data-stu-id="6e582-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e582-121">-Subscription</span></span>
<span data-ttu-id="6e582-122">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="6e582-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="6e582-123">-Topic</span></span>
<span data-ttu-id="6e582-124">A téma neve</span><span class="sxs-lookup"><span data-stu-id="6e582-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e582-125">-Confirm</span></span>
<span data-ttu-id="6e582-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e582-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e582-127">-WhatIf</span></span>
<span data-ttu-id="6e582-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e582-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e582-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e582-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e582-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e582-130">CommonParameters</span></span>
<span data-ttu-id="6e582-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e582-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e582-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e582-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e582-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e582-133">INPUTS</span></span>

### <span data-ttu-id="6e582-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6e582-134">System.String</span></span>

## <span data-ttu-id="6e582-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e582-135">OUTPUTS</span></span>

### <span data-ttu-id="6e582-136">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6e582-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="6e582-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e582-137">NOTES</span></span>

## <span data-ttu-id="6e582-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e582-138">RELATED LINKS</span></span>

