---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: e09e4f19a63eef1cd4b87760239d4456afee70fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493366"
---
# <span data-ttu-id="4cc10-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4cc10-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4cc10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4cc10-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc10-103">A megadott szabály leírását kapja egy adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="4cc10-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4cc10-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4cc10-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc10-106">A **Get-AzureRmServiceBusRule** parancsmag a megadott szabály leírását az adott előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4cc10-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="4cc10-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4cc10-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc10-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4cc10-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="4cc10-109">Adott előfizetés megadott szabályának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4cc10-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="4cc10-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4cc10-110">PARAMETERS</span></span>

### <span data-ttu-id="4cc10-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4cc10-111">-Name</span></span>
<span data-ttu-id="4cc10-112">Szabály neve.</span><span class="sxs-lookup"><span data-stu-id="4cc10-112">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc10-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4cc10-113">-Namespace</span></span>
<span data-ttu-id="4cc10-114">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4cc10-114">Namespace Name.</span></span>

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

### <span data-ttu-id="4cc10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc10-115">-ResourceGroupName</span></span>
<span data-ttu-id="4cc10-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4cc10-116">The name of the resource group</span></span>

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

### <span data-ttu-id="4cc10-117">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="4cc10-117">-Subscription</span></span>
<span data-ttu-id="4cc10-118">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="4cc10-118">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc10-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="4cc10-119">-Topic</span></span>
<span data-ttu-id="4cc10-120">A téma neve</span><span class="sxs-lookup"><span data-stu-id="4cc10-120">Topic Name.</span></span>

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

### <span data-ttu-id="4cc10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc10-121">-DefaultProfile</span></span>
<span data-ttu-id="4cc10-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4cc10-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc10-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc10-123">CommonParameters</span></span>
<span data-ttu-id="4cc10-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4cc10-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc10-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc10-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc10-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cc10-126">INPUTS</span></span>

### <span data-ttu-id="4cc10-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc10-127">System.String</span></span>

## <span data-ttu-id="4cc10-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cc10-128">OUTPUTS</span></span>

### <span data-ttu-id="4cc10-129">Microsoft. Azure. Command. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4cc10-129">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="4cc10-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4cc10-130">NOTES</span></span>

## <span data-ttu-id="4cc10-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4cc10-131">RELATED LINKS</span></span>

